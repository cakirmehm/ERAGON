# ERAGON
ERAGON is a CI/CD and reporting tool with the capabilities of using DOORS, JIRA and GIT at the same time.


It runs on a server computer and checks the code, requirements and test procedures for a period of time. It uses capabilities from 
	Test Management Tool, 
	Code Checker Tool, 
	Requirement Checker Tool,
	DOORS Filter Tool,
	Folder Checker Tool.

 ** Earnings
 1. It reduced the License Cost at least fifty percent. 
 2. It provided immediate cure for the pain in the test, code or requirements.
 3. The audits got easier and it is really liked by the audit team. Because we could show all the things in a linked hieararchy with reason and result.
 4. It also reduced the workload on teams.
 

 ----- CODE ----
* For code; it reads the code from the GIT repository and performs these checks:
    1. Coding Standard Check; (The coding standard of the company. It can be defined and changed at run time)
    2. Code - Requirement Traceability Check (In DO-178C, codes are tied to Low Level Requirements. We store LLRs and class definitions on DOORS as linked to each other. Thus we can query the tracability state of a class definition)
    3. Aged Code Files; ERAGON lists the files that are not commited or changed for a long time (user defined).
    4. TBD: Build and Logs; In the future, it will build the current code in main branch, and send e-mail to the person who did the related commit/merge.

----- TEST ----
* For test; it reads all the test procedures and sources from GIT repository and perform some checks like in TMT:
   1. Test Standard Check; (Used macros, sources and syntax are checked)
   2. Test - Requirement Check; (We store the requirements on DOORS and TMT can automatically fetch the related requirements of a test procedure. It logs the test procedures without requirements or requirements that are open)
  3. Open JIRA Issues on Tests; (Each fail on a test result are tied to a JIRA issue. TMT makes it compulsory to close these issues for the test author. ERAGON shows the open issues on test documents.)
  4. Open Review Items on Tests; (TMT can operate a review action for a test procedure document and stores it in a DB. ERAGON reads this DB and logs the open review items.)
  5. Aged Test Documents; ERAGON lists the test documents that are not commited or changed for a long time (user defined).
  6. NotRun Test Documents; It also lists the test documents that are not run and created test run results for a long time (user defined).
  7. Auto-Publish; It creates TMT Publish Catalog automatically on a web server.
  8. TBD: Auto-run and report (Some tests can run automatically without user prompt. These kind of tests can be run automatically on a certain time of the day)

----- REQUIREMENTS ----
* For requirements, ERAGON creates dxl scripts at run time and uses DOORS as a requirement DB.
   1. Requirement Standard Check; (Legal/illegal keywords, attributes, attribute values etc.)
   2. Requirement Change Log ; (ERAGON stores the last requirement document and whenever a change occurs, it finds the related code/test documents and creates notification)
   3. Traceability Check; (All requirements should be traced to code/tests and there must not be any open requirement. ERAGON lists the open requirements).
   4. Custom Filters/Checks; User can define any filter and target module set to be applied. ERAGON creates notification when any object occurs in the filter)
   5. JIRA Changes; Each baseline in a module is tracked with a JIRA Issue. ERAGON finds the change in related JIRA Issue and notifies the DOORS module to be reviewed.


----- FILE SYSTEM ----
* For disk drives and network drives, ERAGON can perform some checks in file system :
   1. File Duplication; (it creates a CRC-32 code for each files in the drive and finds the duplications using this code)
   2. Changes in a Directory; (it immediately notifies the user when a file is added/deleted/updated/renamed)
   3. File Storage; (it notifies the user when the capacity is about to reach to the maximum)



## Setting Parameters
https://github.com/cakirmehm/ERAGON/blob/main/ERAGON-1.mov

## Checking GIT Repo and Creating Notifications
https://user-images.githubusercontent.com/17138051/163271748-b5bdb986-6b71-4a7c-b231-267e00850673.mov





# ERAGON
