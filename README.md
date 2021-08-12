
# CHANGELOG


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

-----

## Abril 20, 2021

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

## Jul 13, 2021

### components versiones

* supervisor. 2.5.1-1-gc505924

* web. 2.5.0-2-g9331f371

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

