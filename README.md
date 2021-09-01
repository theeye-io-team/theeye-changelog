
# CHANGELOG

-----


## Components

| Name | Description |
|-----|-----|
| supervisor | Core API |
| web | SPA UI |
| gateway | Micro Services API |
| auth | Authentication Micro Service (saas) |
| sync | Core Task execution sync response |
| docs | Online documentation |

-----

# RELEASES


* [Sep 1, 2021](#sep-1-2021)

* [Aug 13, 2021](#aug-13-2021)

* [Aug 2, 2021](#aug-2-2021)

* [Jul 22, 2021](#jul-22-2021)

* [Jul 13, 2021](#jul-13-2021)

* [Jun 10, 2021](#jun-10-2021)

* [May 12, 2021](#may-12-2021)

* [Apr 20, 2021](#Apr-20-2021)


-----

## Sep 1, 2021

### Components Versiones

* supervisor. 2.8.0    

* web. 2.8.0     

* gateway. 1.6.0     

* auth. 0.0.1     

* sync. 0.0.3      


### Main features.

#### Supervisor Api


* SECFIX - [fad908f](https://github.com/theeye-io/supervisor/commit/fad908f) dynamic settings control fix [(#169)](https://github.com/theeye-io/supervisor/pull/169)


* FEATURE/BUGFIX - [bd09617](https://github.com/theeye-io/supervisor/commit/bd09617) Task job assignee [(#185)](https://github.com/theeye-io/supervisor/pull/185)

Launch tasks using assignee.
Extend members translation.
Unify workflows and tasks checks.


* FEATURE - [a1575d1](https://github.com/theeye-io/supervisor/commit/a1575d1) add scheduler additional parameters [(#183)](https://github.com/theeye-io/supervisor/pull/183)


* BUGFIX - [d90e8e6](https://github.com/theeye-io/supervisor/commit/d90e8e6) user is not preset. should not fail [(#182)](https://github.com/theeye-io/supervisor/pull/182)

trigger onhold was not working.



#### Gateway Api

* MAINTENANCE - [0a5d508](https://github.com/theeye-io/api_gateway/commit/0a5d508) remove popup component custom event [(#83)](https://github.com/theeye-io/api_gateway/pull/83)

this event is no longer emitted. was removed


* FEATURE - [01648be](https://github.com/theeye-io/api_gateway/commit/01648be) Swagger [(#82)](https://github.com/theeye-io/api_gateway/pull/82)

this is in progress. structure was added.

Listening on /api/docs



#### Web UI

* FEATURE/BUGFIX - [73be66e2](https://github.com/theeye-io/web/commit/73be66e2) merge cron features [(#277)](https://github.com/theeye-io/web/pull/277)

The scheduler was improved.
Human format was removed.
Added cron with example and Timezone auto-discover.
UI Improved.


* FEATURE/BUGFIX - [eafe00c4](https://github.com/theeye-io/web/commit/eafe00c4) move code. improve verification. add isassignee [(#298)](https://github.com/theeye-io/web/pull/298)

Show Popup is now tied to the job-completed event.
The custom pop-event was removed.


* FEATURE - [f7868ae5](https://github.com/theeye-io/web/commit/f7868ae5) Download button component [(#295)](https://github.com/theeye-io/web/pull/295)

A download button component was added in table view.

* FEATURE - [abeaf926](https://github.com/theeye-io/web/commit/abeaf926) Import arguments from a task json backup [(#273)](https://github.com/theeye-io/web/pull/273)

New buttons added to work with task arguments:

Export to File (Args can be exported to recipe)
Import from File (From task recipe supported)
Copy (from existent tasks)


* BUGFIX - [6b31457d](https://github.com/theeye-io/web/commit/6b31457d) mixed value detected [(#294)](https://github.com/theeye-io/web/pull/294)

* FEATURE - [0905ee28](https://github.com/theeye-io/web/commit/0905ee28) Environment variables GUI [(#266)](https://github.com/theeye-io/web/pull/266)

* BUGFIX - [aa6320f7](https://github.com/theeye-io/web/commit/aa6320f7) scheduler-permissions [(#288)](https://github.com/theeye-io/web/pull/288)

* FEATURE/BUGIX - [273accbb](https://github.com/theeye-io/web/commit/273accbb) Opcionales text [(#271)](https://github.com/theeye-io/web/pull/271)

Improve optional arguments parsing.
Keep legacy behoviour.


* BUGIFX - [3817a9ef](https://github.com/theeye-io/web/commit/3817a9ef) Fixed scheduler button showing up for users [(#291)](https://github.com/theeye-io/web/pull/291)

Acls added to buttons. Hide buttons to non-admin users.

* FEATURE - [0bf1a96a](https://github.com/theeye-io/web/commit/0bf1a96a) Render on click collapse [(#292)](https://github.com/theeye-io/web/pull/292)

Job rows are no longer rendered onload.

-----


## Aug 13, 2021


### components versiones

* supervisor. 2.7.2    

* web. 2.7.2   

* gateway. 1.5.0

* auth. 0.0.1     

* sync. 0.0.3      



### Main features.


#### Supervisor

(tag: 2.7.2) Fix jobs query. add more info. UI need improves

Remove jobs filteringg (#181)

(origin/reschedule-fix) validate payload (#180)

(tag: 2.7.1)

add more data to response (#179)

missing validation (#178)

(tag: 2.7.0)

restart schedule using new next run (#177)

running jobs counter api (#176)

Scheduler pause (#175)


#### Web UI

(tag: 2.7.2) capture close button (#290)

2.7.1 Release Fixes. Jobs fetch and onHold checks

Jobs fetch fixes (#289)

Optional arguments types validation (#286)

"Unknown" notifications for schedules fixed (#281)

Emprolijar isPendingCheck y arreglar el chequeo de pending jobs (#270)

(tag: 2.7.1)

resync and repopulate improves (#284)

fetch jobs on check pending (#283)

webhook refactoring (#282)

use collection to count. reduce jobs payload. (#280)

(tag: 2.7.0)

file page (#272)

add more control to jobs operations counter (#276)

boton para cambiar el assignee de una job pending (#269)

Filter members in orgation menu (#267)

Tying current running jobs to the API (#255)

Implemented functional buttons (#254)

Scheduler pause button (#256)

-----


## Aug 2, 2021


### components versiones

* supervisor. 2.6.1    

* web. 2.6.1   

* gateway. 1.5.0

* auth. 0.0.1     

* sync. 0.0.3      



### Main features.


#### Supervisor

Admin users can cancel jobs again (#173)

Fix for dynamic settings validation.


#### Web UI

Text argument does not stringify by default

Legacy is the default argument type behavior

in-progress job also optionals enabled. (#268)

Admin users is able to cancel jobs (again) (#265)

Restore workflow jobs fetch on-loading


-----

## Jul 22, 2021

### components versiones

* supervisor. 2.6.0   

* web. 2.6.0

* gateway. 1.5.0

* auth. 0.0.1     

* sync. 0.0.3      

### Main features.

#### Supervisor

* Evaluate arguments as mime text/plain (#170)

* Fix dynamic settings verification (#172)

* Add control to non-cancellable jobs (#171)


#### Web UI


* Task arguments improved to work with optionals (#258)

  Text arguments type added.

* Scripts Linked models. Fix verification order (#263)

* Argument type options/remote options admit multiples selections (#252)

* Member page search input (#262)

* Ask confirmation to modify scripts attached to multiple models (#253)

* Ordered monitor check interval list (#259)

* Verify my-pending tasks (#241)

* Jobs control. can be canceled. (#249)

* Combo arguments admit 0 as input value (#251)


-----

## Jul 13, 2021

### components versiones

* supervisor. 2.5.2

* web. 2.5.1

* gateway. 1.5.0

* auth. 0.0.1     

* sync. 0.0.3      

### Main features.


#### Supervisor API


* Workflow user inputs (#152)

  > Users assignee and observers can be controled.   

  > Added security.    

  > The approvers in approval tasks has new variants.   

  > Workflows dynamic settings can now be forbidden.   

* change exceded jobs clean order - create then clean (#161)

* Task/Workflow can be cancellable (#164)

* add limit/removal jobs exec policy by task/workflow (#168)


#### Gateway API

* Escape regexp case insensitive in all db query (#76)

* Encrypted configs (#77)

* lower case email on user invitation (#79)

* create AD/LDAP users with default/domain group. (#80)

* A lot of fixes with users, members, authorization and authentication of users (#76 #79 #81)


#### Web UI

* Build webserver support for on premise installations (#237)

* remove customer from request payload and url (#231)

>    remove customer from request payload and url. no longer needed

>    searchbox fix: not found new created task

>    rename property (acl_dynamic => empty_viewers)

>    fix grecaptcha verification

>    added participants information to jobs

>    assigned_user default value

* named integration tokens (#234)

* workflow table view fix (#238)

* client socket connection improved (#244)

* dynamic settings security improved (#247)

-----

## Jun 10, 2021

### components versiones

* supervisor. 2.4.2

* web. 2.4.2

* gateway. 1.4.2

* auth. 0.0.1     

* sync. 0.0.3      

### Main features.

* (supervisor) re-enable job.lifecycle (user can cancel) (#155). users with limited access can cancel jobs again

* (supervisor) HOTFIX: workflow path rename.

* (web) build version and scripts (#236)

* (gateway) Enterprise Auth. verify username & email (#75)

-----

## May 12, 2021

### components versiones

* supervisor. 2.4.1   

* web. 2.4.1

* gateway. 1.4.1

* auth. 0.0.1     

* sync. 0.0.3      

### Main features.

* (Gw|Web) FEATURE: Optional. organizations display name setting (display_name property added)

* (Gw) FIX: Requests compression support restored. Prevents sending static files uncompressed

* (Web) FIX: Jobs list limit (paginator). Hide jobs elements from the UI. Memory leaks and browser freeze

* (Web) FIX: Check jobs ownership and interactions, using users email and id

* (Web) HOTFIX: Searchbox fixes, Workflows and Groups now can be searched.

* (Web) HOTFIX: Workflow current, last and first job determined correctly

* (supervisor) Task & Workflows ACL controller (#154)

* (supervisor) organization display name

-----

## Apr 20, 2021

### components versiones

* supervisor. 2.4.0   

* web. 2.4.0    

* gateway. 1.4.0    

* auth. 0.0.1     

* sync. 0.0.3      

### Main features.

#### on-premises

* LDAP/AD Login. Users profile creation and verification can now be performed in case-insensitive manner.

Default group (configuration req.)
User match/create by email, username (case insensitive)

* Toggle email notifications for activation, customerInvitation, invitation, passwordRecover, registration.

* Toggle registration form, google login options, password reset form.

* Can customize login form inputs placeholders 


#### cross env (saas, on-premises)

* Cloud Domain Enterprise login (Azure AD integration)

* Notifications can now be sent using email and username.

* Dynamic approvers for Approval tasks. Approvers are set during task Triggering and should be defined in the previous task of a workflow or from the triggering task.

* ACL's and dynamic ACL's for Task and Workflows. This allows assignment of the workflow/task (job) execution to particular users. The ACL's must be set during task triggering.

* Task Arguments can now be set as Optional

* Core Arguments as JSON encoded (optional). The core will JSON.encode all task arguments and JSON.decode for each argument will be required within the scripts. Future releases will perform this process automatically.

* Added Task input type JSON. Validation only applicable for user input.

* Approval Task parametrization: success_enabled, failure_enabled, cancel_enabled, ignore_enabled 

* Task properties can now be set dynamically. (working on the documentation)

* Username was added to env THEEYE_JOB_USER

* Can now dynamically set user_inputs, user_inputs_member

* Optional during triggers can be set via API and task output. (working on the documentation)

* Workflow Job table view. The jobs list is displayed aligned in columns, each filled in with the arguments received in the first step (task) of the workflow.

* New endpoints added in the Core API.

| method | path | description |
| ----- | ----- | ----- |
| GET | /workflow/:workflow_id/job |  Fetch all workflow jobs (fetch api ready) |
| GET | /workflow/:workflow_id/job/:job | Fetch a workflow job | 
| GET | /workflow/:workflow_id/job/:job/jobs | Fetch all task jobs withing a workflow job execution |
| PUT | /job/:job/assignee | Set user_inputs, user_inputs_members. also set job acl. body filter username, email. determine organization using session |
| PUT | /job/:job/acl | Set job acl |
| PUT | /workflows/:workflow/job/:job/acl | Set job acl by workflow |
| PUT | /workflows/:workflow/job/:job/cancel | Cancel workflow job execution |
  
-----
