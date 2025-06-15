# Smart-Comply

1. SmartComply will be used by a single tenant (e.g., Econsave Pulai):
   - Each company (like Econsave) would typically be treated as one tenant in a multi-tenant SaaS system.

2. Internal auditors from Econsave will use SmartComply to audit each branch:
   - Internal auditors are part of the tenant's (Econsave’s) organization and are responsible for performing audits.
   - Admins (from Econsave) are responsible for building audit forms:

3. Different forms for different compliance standards:
   Each compliance standard (e.g., HALAL vs HACCP) may have different requirements, so it’s common to have different audit forms for each.

4. Auditors can see a list of audits, categorized by branch and compliance type:


## Audit
### Important part 
- Corrective Action diff page ✅
- Follow up audit diff page ✅
- details in diff section
- corrective action in diff section 
- generate report on submitted form and follow up
- in views detail ada drop down bole pilih, first audit, second audit, third audit
- every audit ni kat bawah ada corrective action and follow up audit, so corrective action & fua takyah letak kat dropdown history
- warning if submit empty record
- Tambah bole edit/archive form
- kalau generate report kena letak corrective action follow up audit semua ke ?
- view details to patut ada generate first audit form then follow up audit,
- follow up audit bole buat berapa kali, kalau lebih sekali kena letak first audit, second audit like that ?
- tambah status ke untuk score tu macam excellent, fair semua tu
- fix if tambah follow up audit jangan ubah score initial audit
- Index.cshtml
  - Tambah column followupaudit date
  - tambah filter
  - score no decimal
  - remove time from audit date
  - tambah option macam all, draft, completed
  - only keluar CA and FUA for record yg required
- Details
  - Add generate report ✅
  - scale (tk penting)
  - remove theme by ap tu, kacau report 

### KIV
- tak perlu buat macam item then standard ke ?
- radio button checkbox dropdown mmg takde score eh
- kalau guna number input je bole dpt score, mmg cemtu ke eh ?
- perlu ke compliance level ? (kalau sempat add nanti)

### After complete Important
- make datatable bigger  
- tambah scale kat auditform (1-very poor, 2-poor,..)
- fix why text tak dpt score details 
- Percentage score no decimal 
- add corrective action on follow up audit
- fix real time score on follow up audit
- buang corrective action and follow up audit if dah 100% and complete
- Buat datatable ✅
- Remove branch value from database 
- add draft other than submit
- fix why if tak log in jadi error (authorize problem maybe)
- Manager can view audit history
- Fix signature part
- Tukar symbol untuk menu audit ✅ 
- org boleh pilih kena follow up untuk yg tak fullscore or kita set ?
- modify status, (draft, need corrective action, need follow up, completed,archived (hidden or lowest record)
- add day if report 
- Add warning
  - warning if put value more than max 

## Where to edit ?
1. in 'Shared/Sections/Navbar/_NavBarPartial.cshtml <br>
![image](https://github.com/user-attachments/assets/1ece39e3-6537-4156-9cd4-5a67dbaccf81)

2. in 'Shared/Sections/Menu <br>
![image](https://github.com/user-attachments/assets/cfd837a1-c3d7-4a4a-a75a-ac1f58743d1d)

## Curious
1. Kita ke yg set minimum score tu or admin yg set masa form builder ?
2. Siapa yg set max score untuk dia kena buat follow up audit, admin or kita ?
3. Remark tu nak ke, tpi dia takde mention 
4. Corrective action before or after submit ?
