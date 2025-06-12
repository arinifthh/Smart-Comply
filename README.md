# Smart-Comply

1. SmartComply will be used by a single tenant (e.g., Econsave):
   - Each company (like Econsave) would typically be treated as one tenant in a multi-tenant SaaS system.
   - This tenant can have multiple branches (e.g., different store locations).

2. Internal auditors from Econsave will use SmartComply to audit each branch:
   - Internal auditors are part of the tenant's (Econsave’s) organization and are responsible for performing audits at each branch.
   - Admins (from Econsave) are responsible for building audit forms:

3. Different forms for different compliance standards:
   Each compliance standard (e.g., HALAL vs HACCP) may have different requirements, so it’s common to have different audit forms for each.

4. Auditors can see a list of audits, categorized by branch and compliance type:


## Audit

- Percentage score no decimal
- Tambah bole edit/delete form
- Tanya dorang, perlu ke buat datatable ?
- Add branch value
- Corrective Action diff page
- Follow up audit diff page
- add draft other than submit
- try form with diff section (kena split each section) 
- dekat follow audit takyah ada corrective action as note tu kan ? (bole add dekat atas)

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
