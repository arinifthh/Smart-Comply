# Smart-Comply

## Where to edit ?
1. in 'Shared/Sections/Navbar/_NavBarPartial.cshtml <br>
![image](https://github.com/user-attachments/assets/1ece39e3-6537-4156-9cd4-5a67dbaccf81)

2. in 'Shared/Sections/Menu <br>
![image](https://github.com/user-attachments/assets/cfd837a1-c3d7-4a4a-a75a-ac1f58743d1d)


## My Part 
1. Tugar Logo ✅
2. Understand Database
3. Can Choose User Role
   - dynamic form builder at admin side
   - fill form at audit side
   - view form at manager side 
5. Find where to edit sidebar ✅
6. Change Icon

## Audit Module

1. Before integration create mock form
2. Edit the form part so it gave error if :
   - Name, place = 'none'
   - Score = 'none'
   - Verification uncomplete
   - Add Comment section (opt)
   - Add file (opt)
   - Designation letak "e.g. : Operations Manager " (official title) - ni bukan from dynamic form builder ?
   - Yg ni tak user friendly, should be '>' then '^' but ke bawah <br>
     ![image](https://github.com/user-attachments/assets/c554d517-da08-444c-8905-c33e43a0c5c3)
   - Can add pic for verification (Strong Proof) ?
   - Report show section to not 1.1 1.2..
   - Dekat report signature tak keluar
     
3. Add filter to audit history datatable :
   - Based on status (Completed, Need Follow Up Audit)
   - Based on compliance (Halal, HACCP..)
   - Based on places
     
4. On corrective Action
   - Only display yg tak full mark
   - Display by section macam original form
   - Add date for follow up audit
   - Refer doc for further
     
6. Auditor can :
   - add new 
   - delete
   - Add follow up audit
   - Add corrective action
     
7. Manager can view :
   - Datatable
   - Report
     
8. Verification
   ![image](https://github.com/user-attachments/assets/58b32726-0d41-4e60-a2fe-6538bbce36ef)
    Checked by (Auditor/s): The person(s) who performed the audit and documented the findings. <br>
    Acknowledged by (Outlet): The person in charge of the audited location who received and understood the findings. <br>
    Verified by: A higher authority or oversight person who reviews and formally approves the audit report for its validity and implications. <br>

## Common Error 
1. YourProjectName -> AspnetCoreMvcFull
2. 

## Hold

1. Create Other Compliance Forms: Create HACCP_AuditForm.cshtml, OSH_AuditForm.cshtml, and ISO22000_AuditForm.cshtml in Views/Auditor/. For these, copy the entire content of the new HalalAuditForm.cshtml and just change: (just do HALAL for example kot, sebab type of compliance form ni admin yg buat)

ViewData["Title"] = "HACCP Audit Form"; (and similarly for OSH, ISO22000).
Crucially, modify the example audit items (<tbody> content) to be relevant to HACCP, OSH, or ISO 22000. I provided HACCP examples in the previous response, so you can adapt those.

## How to Integrate Later:

When your friend's admin part is ready, the integration will involve:

Admin-Generated Form Data: Your friend's dynamic form builder will likely generate a "form definition" (e.g., a JSON schema, an XML file, or a specific database structure) that describes the fields, types, and validation rules for a particular audit form.
Auditor Form Rendering: Your auditor application will then need to:
Fetch this form definition from the server (which was saved by the admin part).
Use JavaScript (e.g., a client-side library like React, Vue, or even plain JavaScript) to dynamically render the form fields based on this definition. This replaces your static .cshtml forms.
Data Submission to Dynamic Structure: When the auditor submits, your application will send the data back to the server, and the server will need to save this data according to the structure specified by the form definition. This is where a more flexible database design (e.g., using JSON columns, or an EAV model) might come into play on the server side.

## Curious
1. Kita ke yg set minimum score tu or admin yg set masa form builder ?
2. Siapa yg set max score untuk dia kena buat follow up audit, admin or kita ?
3. Remark tu nak ke, tpi dia takde mention 
4. Corrective action before or after submit ?
