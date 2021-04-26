
# CHANGELOG

-----

## Components

### supervisor. Core API

### web. SPA UI

### gateway. Micro Services API

### auth. Authentication Micro Service (saas)

### sync. Core Task execution sync response.

### docs. Online documentation


-----


# RELEASES

* supervisor. 2.4.0   

* web. 2.4.0    

* gateway. 1.4.0    

* auth. 0.0.1     

* sync. 0.0.3      


## Abril 20, 2021

Main features.


-----


### on-premises

* LDAP/AD Login. Users profile creation and verification is now case insensitive.

Default group (configuration req.)
User match/create by email, username (case insensitive)

* Enable/disable email notifications: activation, customerInvitation, invitation, passwordRecover, registration

* Enable/disable registration form


-----


### cross env (saas, on-premises)

* Cloud Domain Enterprise login (Azure AD integration)

* Can send notification using email and username

* Approval task with dynamic approvers. Can set the approver during task Triggering. Specify the approvers in the previous task of a workflow or from the triggering task.

* Task and Workflows with ACL's and dynamic ACL's. This allowes to assign the workflow/task (job) execution to particular users. The ACL's must be set during task triggering.

* Task Arguments can now be Optional

* Core Arguments JSON encoded (optional). The core will JSON.encode all task arguments and within the scripts will be required to JSON.decode each argument. This will be made automatically in next releases.

* Added Task input type JSON. Validate user input only.

* Approval Task parametrization: success_enabled, failure_enabled, cancel_enabled, ignore_enabled 

* It is posible to set properties dynamically in some tasks. (working on the documentation)

* Username was added to env THEEYE_JOB_USER

* Can now dynamically set user_inputs , user_inputs_member

* Optional during triggers can be set via API and via task output (working on the documentation)

* Workflow Job table view. The jobs list is displayed aligned in columns. The columns are filled in with the arguments received in the first step (task) of the workflow.

* Core API new endpoints added.

> Fetch all workflow jobs (fetch api ready):
  GET /workflow/:workflow_id/job

> Fetch a workflow job:
  GET /workflow/:workflow_id/job/:job

> Fetch all task jobs withing a workflow job execution:
  GET /workflow/:workflow_id/job/:job/jobs

> Set user_inputs, user_inputs_members. also set job acl. body filter username, email. determine organization using session
  PUT /job/:job/assignee

> Set job acl
  PUT /job/:job/acl

> Set job acl by workflow
  PUT /workflows/:workflow/job/:job/acl

> Cancel workflow job execution
  PUT /workflows/:workflow/job/:job/cancel
