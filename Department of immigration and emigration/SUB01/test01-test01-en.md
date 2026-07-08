# NCINGA_GovTech GIC_ReleaseNote v1.0.pdf

## Page 1
test01
GovTech_GIC: 
AI-driven Government Information Platform 
Release Note v 1.0 
Date: 06th of July 2026

## Page 2

DOCUMENT INFORMATION 
Product Name: GovTech_GIC_AI-driven 
Government Information Platform 
Module Name: Phase 01 
Client: GovTech 
Release Date: 06/07/2026 
Document Version: 1.0 
Main Release No.: 1.0 
Patch No.: N/A 
CR Release No: N/A 
Build No: N/A 
SRN Type: N/A​ ​ 
PREPARED BY: ​
 
Name: Dewmini Abeywardhana 
Designation: Engineer – Quality Assurance 
Signature : N/A 
Date: 06/07/2026 
REVIEW & APPROVAL 
 
 
Name 
Designation 
Signature 
Date 
Tested By: 
Dewmini 
Abeywardhana 
Hirunisha Nirmani 
Pirashanthy 
Balakrishnan 
Dojitha Gamage 
Engineer — Quality 
Assurance 
Intern – Quality Assurance 
Engineer — Quality 
Assurance 
Intern — Quality Assurance 
N/A 
06/07/2026 
Reviewed By: 
Kemali 
Munasinghe 
Wasantha 
Karunadasa 
Lead-Quality Assurance 
 
Senior Lead - Business 
Analyst 
N/A 
06/07/2026 
1

## Page 3

Jasintha 
Dassanayake 
Architect - Software 
Engineering 
Approved By: 
Nikil Jayasuriya 
Associate Project Manager 
 N/A 
06/07/2026 
 
 
DOCUMENT REVISION HISTORY 
Issue Version No. 
Date 
Description 
Author (name) 
- 
- 
- 
- 
 
 
 
Table Of Contents 
Table Of Contents​
2 
1.0 Overview of the Document​
3 
2.0 Deliverables​
4 
3.0 Features included in this release​
4 
3.1 GIC – Content Management System (CMS)​
4 
3.2 GIC – Citizen Portal with AI Chat Assistant​
8 
4.0 Bug Fixes​
10 
5.0 Known Issues​
11 
6.0 Known Limitations​
12 
7.0 Supporting Documents​
12 
7.1 User Roles and Access​
12 
7.2 Test Case Sheet​
13 
 
 
 
 
2

## Page 4

1.0 Overview of the Document 
This Release Note documents Phase 01 of the GovTech – Government Information Platform 
(GIC) testing release. It provides a summary of the features delivered for testing, the scope 
covered during Quality Assurance (QA), identified defects, known issues, known limitations, 
bug fixes , recommendations, and the deliverables associated with this testing cycle. 
The testing activities were performed by the QA Team of the NCINGA (Pvt) Ltd based on the 
agreed Scope of Work (SOW) and the supporting project documentation. The QA team 
validated and verified the implemented functionalities against business requirements, 
functional specifications and other supporting project artifacts to ensure that the delivered 
features meet the expected system behavior. 
The GovTech – Government Information Platform (GIC) is designed to enable the centralized 
collection, management, review, approval, storage, and delivery of verified government 
information. The platform supports government institutions in managing information 
efficiently while providing the public with accurate and approved information through a 
multilingual conversational interface. 
This release note serves as a record of the Phase 01 QA activities and provides stakeholders 
with a consolidated view of the testing outcomes. It establishes the baseline for release 
readiness by documenting the functionality validated, testing observations, outstanding risks, 
and recommendations, while ensuring alignment with the agreed project scope and 
supporting informed decisions for subsequent project phases. 
This Phase 01 release covers the testing of English-language only. 
 
 
 
 
 
3

## Page 5

2.0 Deliverables 
 
Testing was carried out in the CMS and the Citizen Portal QA environment. 
1. CMS QA Environment 
●​
 URL: https://qa.ai-gicp.com/ 
●​
 initial credentials : CTA Admin (GA) - GovTech Admin 
Email: test-ga@ncinga.net Password: Test1234 
GovTech Admin is authorized to create new users in the system. 
2. Citizen Portal QA Environment 
●​
 URL: https://qa.citizens.ai-gicp.com/ 
 
 
 
3.0 Features included in this release 
3.1 GIC – Content Management System (CMS) 
The GIC – Content Management System (CMS) is the administrative portal of the 
Government Information Platform, designed for authorized government users to create, 
manage, review, approve, and publish government information. The CMS provides a 
structured workflow that ensures information is validated before being made available to 
citizens through the Citizen Portal. It also enables efficient content governance, user 
management, and publication control, supporting the delivery of accurate, consistent, and 
up-to-date government information. 
The table below summarizes the CMS features that were tested and validated as part of the 
Phase 01 release. 
4

## Page 6

Module 
Feature 
Functionality 
CMS 
User Role Management 
Implemented role-based access for three 
user roles: 
01.Content Manager 
02.Department Admin 
03.GovTech Admin 
 
Each role is assigned specific permissions 
and responsibilities to support content 
creation, 
review, 
approval, 
publication, 
platform administration, and access to 
approved government information, ensuring 
a 
secure 
and 
structured 
content 
governance workflow. 
 
Remark: For detailed role-based access and 
user responsibilities, please refer to the 
corresponding 
table 
in 
the Supporting 
Documents section. 
CMS 
User Authentication and 
First-Time Login 
Implemented secure user authentication for 
authorized CMS users through email and 
password-based login. The system supports 
first-time user onboarding by enforcing a 
temporary password change, completion of 
mandatory 
account 
information, 
and 
password creation before granting access 
to the CMS Dashboard. Subsequent logins 
require the newly created password and 
provide 
access 
based 
on 
the 
user's 
assigned role. 
5

## Page 7

CMS 
User Logout 
Implemented a secure logout mechanism 
that allows authenticated users to safely 
end 
their 
CMS 
session. 
Upon 
logout 
confirmation, the system terminates the 
active session and redirects the user to the 
GIC CMS Login page. Users must re-enter 
valid credentials to access the system 
again. 
CMS 
Role-Based Dashboards 
Implemented dedicated dashboards for 
Content Manager, Department Admin, and 
GovTech 
Admin, 
providing 
role-specific 
summaries, 
content 
status 
indicators, 
approval queues, overdue items, and quick 
access to frequently used functions. The 
dashboards 
enable 
users to efficiently 
monitor content lifecycle activities, including 
content creation, drafts, pending approvals, 
rejected 
items, published content, and 
overdue tasks based on their assigned 
responsibilities. 
 
CMS 
Content Management 
Implemented 
comprehensive 
content 
management capabilities, enabling Content 
Managers 
to 
create, edit, review, and 
manage Articles, FAQs, and Schedulers. The 
system supports document uploads with 
multiple processing modes (Auto, Text, 
Scanned, and AI OCR), a rich text editor, 
AI-assisted compliance checks, content 
lifecycle 
management, 
revision 
control, 
approval workflows, publication, retirement, 
and AI embedding status monitoring to 
6

## Page 8

ensure 
government 
information 
is 
accurately 
reviewed, 
approved, 
and 
published to the Citizen Portal. 
CMS 
Scheduler Management 
Implemented 
an 
automated 
scheduler 
management module that enables Content 
Managers 
to 
configure, 
execute, 
and 
manage web scraping tasks for collecting 
government information from predefined 
websites. The feature supports scheduler 
creation, 
configurable 
execution 
frequencies, 
page 
discovery, 
URL 
management, 
execution 
history, 
status 
monitoring, 
manual 
execution, 
pause/resume functionality, editing, and 
deletion. Successfully scraped content is 
automatically converted into draft articles 
for 
review, 
approval, 
and 
publication 
through the standard CMS content lifecycle. 
CMS 
Content Approval 
Workflow 
Implemented a multi-level content approval 
workflow that enables Department Admins 
and GovTech Admins to review, approve, 
reject, and revoke submitted content before 
publication. 
The 
workflow 
includes 
publishing pipeline visibility, review remarks 
for rejected content, final publication to the 
Citizen 
Portal 
upon 
GovTech 
Admin 
approval, 
and 
controlled 
content 
progression 
to 
ensure 
governance, 
accuracy, and compliance throughout the 
content lifecycle. 
7

## Page 9

CMS 
 
 
 
User 
Management 
 
Implemented 
role-based 
user 
management, enabling GovTech Admins 
and Department Admins to manage users 
according to the defined organizational 
hierarchy. The feature supports user listing 
based 
on 
access 
permissions, 
profile 
management, 
department 
assignment 
management, and user deletion, ensuring 
secure 
administration 
and 
controlled 
access to the CMS. 
CMS 
System Settings 
Implemented a system settings module for 
GovTech Admins to monitor the operational 
health of the GIC CMS. The feature provides 
visibility into GitHub API usage, including 
rate limits, remaining requests, and reset 
time, as well as the connectivity status and 
response time of core system services, 
enabling administrators to monitor platform 
availability and identify service connectivity 
issues. 
Remark: The Settings page was verified for 
basic accessibility and display only. Detailed 
functional validation of the Settings page is 
planned for a future release. 
 
 
 
 
 
 
 
 
 
8

## Page 10

3.2 GIC – Citizen Portal with AI Chat Assistant 
The GIC – Citizen Portal with AI Chat Assistant is the public-facing component of the 
Government Information Platform, providing citizens with a centralized and user-friendly 
interface to access verified government information, services, announcements, and other 
public resources. The portal is designed to improve information accessibility by enabling 
users to easily search, browse, and discover government content published through the GIC 
Content Management System (CMS). 
A key capability of the Citizen Portal is the AI Chat Assistant, which leverages approved 
government content to provide intelligent, multilingual responses to citizen queries. The AI 
assistant enables users to obtain accurate information, discover relevant government 
services, and navigate available resources through a conversational interface. 
The table below summarizes the Citizen Portal features that were tested and validated as 
part of the Phase 01 release. 
Module 
Feature 
Functionality 
Citizen Portal 
Home Page 
Implemented the Citizen Portal Home Page, 
providing citizens with a centralized entry 
point 
to 
access 
verified 
government 
information and services. The home page 
includes 
an 
AI-powered 
conversational 
interface, government information search, 
department 
browsing, 
multilingual 
language selection, and quick access to 
frequently requested government services, 
delivering an intuitive and user-friendly 
experience. 
9

## Page 11

Citizen Portal 
AI Search & Chat 
Assistant 
Implemented an AI-powered conversational 
assistant that enables citizens to search 
and 
retrieve 
verified 
government 
information using natural language queries. 
The 
assistant 
generates 
contextually 
relevant responses based on approved CMS 
content, 
including 
Articles, 
FAQs, 
and 
website-scraped 
content, 
and 
provides 
direct hyperlinks to referenced resources for 
quick access to supporting information, 
improving information discovery and user 
experience. 
Citizen Portal 
Department Navigation 
Implemented 
a 
department-based 
navigation feature that enables citizens to 
browse published government information 
by Department and Sub-Department. Users 
can 
expand department categories to 
access 
related 
content, 
view 
detailed 
information, 
and 
launch 
the 
AI 
Chat 
Assistant directly from the Departments 
page for conversational assistance and 
information retrieval. 
Citizen Portal 
About Page 
Implemented an About page that provides 
citizens with key information about the 
Government Information Platform, including 
its mission, vision, service values, and 
organizational overview. The page also 
includes 
contact 
information, 
quick 
navigation links, privacy and accessibility 
information, 
and 
official 
government 
branding and copyright details to improve 
transparency and user awareness. 
10

## Page 12

4.0 Bug Fixes 
As this is the initial Phase 01 release of the GovTech – Government Information Platform, no 
bug fixes are included in this release. 
5.0 Known Issues 
Known issues of this release are listed below. These will be fixed in the subsequent releases. 
 
Defect ID 
Defect Description 
Status 
CMS_051 
When a user pastes certain valid URLs into the input 
field and clicks the Discover button, the system 
returns a 502 Bad Gateway error instead of 
processing the URL. This issue does not occur for all 
URLs—some URLs are processed successfully, and 
some valid URLs consistently result in the 502 error. 
​
 
 
Open 
CMS_065 
When the user selects the "My Content" filter on the 
Articles page, the system should display only the 
content created or owned by the logged-in user. 
However, the filter is not working correctly, as it 
displays content that does not belong to the 
current user. 
Open 
CMS_089 
After the session times out, the application displays 
an "Authorization Expired" message with a "Back to 
Login" button. However, when the user clicks the 
button, 
they 
are 
redirected 
directly 
to 
the 
dashboard without being prompted to log in again. 
Open 
CMS_090 
When a draft is submitted, it goes to the 
Department 
Admin 
for 
approval. 
After 
the 
Department Admin approves it, the workflow 
proceeds to the GovTech Admin stage. If the 
Department Admin revokes the article, FAQ, or 
scraped embedding at this stage, the status should 
Open 
11

## Page 13

pending not Done 
CMS_091 
Article name is displayed as a hyperlink 
Open 
CHAT_019 
After selecting a rating, the user is unable to modify 
or update the selected rating. The application does 
not provide an option to edit the submitted rating, 
which prevents users from correcting an accidental 
selection or changing their feedback. 
Open 
 
6.0 Known Limitations 
N/A 
 
7.0 Supporting Documents 
7.1 User Roles and Access 
 
Function 
Sub Module 
Content 
Manager 
Department 
Admin 
GovTech 
Admin 
Content upload 
Scheduler Setup 
TRUE 
FALSE 
FALSE 
 
Article Setup 
TRUE 
FALSE 
FALSE 
FAQ Setup 
TRUE 
FALSE 
FALSE 
Approvals 
View approval status 
TRUE 
TRUE 
FALSE 
12

## Page 14

First approval 
acceptance 
FALSE 
TRUE 
FALSE 
Second approval 
acceptance 
FALSE 
FALSE 
TRUE 
User Management 
Manage content 
managers 
FALSE 
TRUE 
FALSE 
Manage department 
admin 
FALSE 
FALSE 
TRUE 
Settings 
N/A 
TRUE 
TRUE 
TRUE 
7.2 Test Case Sheet 
 
Location: 
https://docs.google.com/spreadsheets/d/1UVsLvYktMgCn_GnSfY8pSoGv2_ub5zvVxddiUykNn
fY/edit?usp=sharing 
 
13
