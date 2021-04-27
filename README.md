
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

* Toggle registration form.


-----


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
