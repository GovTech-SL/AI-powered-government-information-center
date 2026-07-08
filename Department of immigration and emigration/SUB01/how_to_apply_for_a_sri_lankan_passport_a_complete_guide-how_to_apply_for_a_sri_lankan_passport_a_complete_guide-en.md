# ISVA-INT-EPT 0.0.2.pdf

## Page 1

Identity and Access Management (IAM) 
EPT 
Release Note Version 0.0.2 
Date : 2nd Of December 2025

## Page 2
ddd
DOCUMENT INFORMATION 
Product Name: Identity and Access 
Management (IAM) 
Module Name: EPT 
 
Client: Commercial Bank PLC 
Release Date: 02 /12/2025 
Document Version: 0.0.2 
Main Release No.: 0.0.1 
Patch No.: N/A 
CR Release No: N/A 
Build No: N/A 
SRN Type: N/A​ ​ 
PREPARED BY: ​
 
Name: Dewmini Abeywardhana 
Designation: Engineer – Quality Assurance 
Signature:N/A 
Date: 02/12/2025 
REVIEW & APPROVAL 
 
 
Name 
Designation 
Signature 
Date 
Reviewed By: 
Kemali 
Munasinghe 
Lead-Quality 
Assurance 
N/A 
02/12/2025 
Approved By: 
Chathura 
Ekanayake 
Senior Project Manager 
 N/A 
02/12/2025

## Page 3

DOCUMENT REVISION HISTORY 
Issue Version No. 
Date 
Description 
Author (name) 
ISVA-INT-EPT 0.0.1 
06/11/2025 
Feature Release Note 
Dewmini Abeywardhana 
 
 
Table Of Content 
 
1.0 Overview of the Document​
4 
2.0 Deliverables​
4 
3.0 Bug Fixes​
5 
4.0 Known Issues​
6 
5.0 Known Limitations​
7 
6.0 Features not tested in this release​
8 
7.0 Supporting Documents​
8

## Page 4

1.0 Overview of the Document 
 
This document provides a summary of the bug fixes, known issues, and known limitations 
identified in the EPT system. All fixes listed have been verified and validated by the QA team. 
Additionally, any features currently on hold, environment-specific limitations, or deviations 
from the approved Business Requirement Document (BRD) and System Requirement 
Specification (SRS) are documented here. 
2.0 Deliverables 
Testing was carried out in the EPT UAT environment integrated with ISVA UAT. 
1.​
EPT UAT Environment (Service Provider Sessions)​
 
EPT UAT URL: 
https://uateptdabsrv.ept.com:8083/web/login 
●​
Username: dewmini1 Password: combank@1234 
●​
Username: dewmini2 Password: combank@1234 
 
2.​ ISVA UAT Environment (Identity Provider Sessions)​
 
 ISVA UAT URL: 
 https://172.16.148.15 
●​
Username: admin@local Password: authAdmin@987 
 
3.​ Reports and Monitoring​
 
○​
Kibana Dashboard Link: 
https://aee-admin.combank.net/kibana

## Page 5

●​
Username: readOnlyUser Password: readOnlyUser 
3.0 Bug Fixes 
The following bug fixes are included in this release. Each bug has been tested and verified in 
the EPT UAT environment integrated with ISVA UAT. 
 
Defect ID 
Defect Description 
Status 
EPT-02 
EPT user redirected to DEV environment successfully logout 
page after logging out from UAT environment 
Close 
EPT-04 
"In the User Activity Report, for EPT login action , the SP URL 
shows only the SP name instead of the full URL. 
The SP URL should display the full URL consistently for all 
actions in the User Activity Report." 
Close 
EPT-06 
When the same user logs in from Device 2 while already 
logged in on Device 1, the user correctly receives the 
“Terminated” screen on Device 2. 
However, the active session on Device 1 is not terminated as 
expected ,the user can still continue accessing the application 
on Device 1. 
Close 
EPT-08 
When the same user logs in from Browser 2 while already 
logged in on Browser 1, the user correctly receives the 
“Terminated” screen on Browser 2. 
However, the active session on Browser 1 is not terminated as 
expected ,the user can still continue accessing the application 
on Browser 1. 
Close

## Page 6

EPT-09 
When the same user logs (BB system) from Device 2 while 
already logged in on Device 1(EPT system), the user correctly 
receives the “Terminated” screen on Device 2(BB system). 
However, the active session on Device 1 (EPT system) is not 
terminated as expected ,the user can still continue accessing 
the application on Device 1 (EPT system). 
[This scenario is happened to all other systems] 
Close 
EPT-10 
When the same user logs in from Browser 2(BB) while already 
logged in on Browser 1(EPT), the user correctly receives the 
“Terminated” screen on Browser 2(BB). 
However, the active session on Browser 1(EPT) is not 
terminated as expected ,the user can still continue accessing 
the application on Browser 1 (EPT). 
[This scenario is happened to all other systems] 
Close 
4.0 Known Issues 
The known issues identified in the previous ISVA-EPT-0.0.1 release are listed below. 
 
Defect ID 
Defect Description 
Status 
Dev Comment 
EPT-07 
Incorrect 
error 
message 
displayed 
randomly after 1 invalid OTP request 
Open 
Developer : Sahan Thilina 
“WIP” 
EPT-05 
When a user logs out from the EPT system, 
the logout action is not recorded in the 
"User Activity Report, only recorded login 
action. 
Open 
Developer : Sahan Thilina 
“WIP”

## Page 7

5.0 Known Limitations 
The known limitations identified in the previous ISVA-EPT-0.0.1 release are listed below. 
 
Defect ID 
Defect Description 
Status 
Dev Comment 
EPT-01 
MFA lockout countdown starts at 15:04 
instead of the expected 15:00 
Limitation 
Supun : [23/10] This depends on 
the clock of the client machine. 
Eg, the Citrix environment is a 
few seconds behind the ISVA 
server. so the calculation will 
show some additional seconds, 
RDP machine clock shows a bit 
less. The only option is to have 
NTP configured within the bank 
and have a synchronized time 
over servers and clients. 
(Common issue) 
EPT-03 
User navigated to "Something Went Wrong" 
page after ISVA session removal and 
re-login with valid 1FA credentials 
Limitation 
Sahan : 2025/11/06 - This is 
expected behavior as ISVA 
would not know where the user 
initially tried to go to once the 
session is terminated 
EPT-11 
When 1 factor is blocked in the chrome 
screen when the same user tries to login to 
the system using another browser. User 
navigates to the 1 factor page and enters 
valid 
1 
factor 
credentials. 
Then 
user 
navigate to 1 factor lock out countdown 
page.Again countdown starts at 30:00 
instead of remaining time 
Limitation 
Sahan : 2025/11/06 - Known 
limitation. Highlighted in gap 
analysis

## Page 8

EPT-12 
When 1 factor is blocked in the device1, the 
same user tries to login to the system using 
device 2. User navigate to 1 factor page and 
enter valid 1 factor credentials.Then user 
navigate to 1 factor lockout countdown 
page.Again countdown started in 30:00 
instead of remaining time 
Limitation 
Sahan : 2025/11/06 - Known 
limitation. Highlighted in gap 
analysis 
6.0 Features not tested in this release 
●​
The EPT Session Termination API was not tested as the required Active Directory (AD) 
access needed to execute and validate the flow was not available. 
7.0 Supporting Documents 
●​
Test Case Execution Sheet for this release is attached below. 
https://docs.google.com/spreadsheets/d/1NBdeXH7MKToYX3dyRUd_eFv8be88zSFdb9
HS7dqjyqg/edit?usp=sharing
