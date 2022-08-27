## Moving partial flow between environments.
## Preface
single consistent approach to deploy/promote workflows.
allowing customers that require to deploy/promote at the job level and sub folder
customer will be able to deploy/promote a folder while changing only one or few jobs through Automation-api 

## Prerequisite
in order to add/update jobs/sub-folders foler/sub-folder muse be exist
jobs/sub-folders will be added/updated only under existing folder/sub-folder


Tutorial on the [delete job](https://docs.bmc.com/docs/automation-api/monthly/deploy-service-1116950327.html#Deployservice-deploy_jobs_deletedeployjob::delete)
that explains how to delte job/subfolder automate code deployment.

ctm deploy job::delete [Path] [server] [library]
  
  | Syntax | Description |
| ----------- | ----------- |
| Path | specify the folder path location in the JSON <br/> * a mandatory field <br/> * valid Folder-  mandatory not empty, contains the path for the job to be deleted, separated by Colons |
| server | specifies a Control-M Scheduling Server from where to delete the job  <br/>  * a mandatory field |
| library  | The library is mandatory/needed only in z/os |
  

## Adding/updateing specific jobs/sub-folders Cli command example:

Tutorial on the [product web page](https://docs.bmc.com/docs/display/workloadautomation/Tutorial+-+Automating+code+deployment)
that explains how DevOps engineer can automate code deployment.

in order to add jobs or sub folder to spacific folder new path element need to be added:

| Syntax | Description |
| ----------- | ----------- |
| Path  | specify the folder path location in the JSON where to add/update the job/subFolder <br/> a mandatory field in case job/subFolder is in the root level <br/> mandatory not empty, contains the path for the job/subfolder to be inserted, separated by Colons |
| server  | specifies a Control-M Scheduling Server where to add/update the job/subFolder <br/> a mandatory field  - in case job/subFolder is in the root level <br/> if there is only one server in the system field is not mandatory (like in folder)  |
| library  | The library is mandatory/needed only in z/os |

JSON example:<br/>
[add specific job](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/addJobAsRoot.json)<br/>
[add specific sub-folder](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/addSubFolderAsRoot.json)
