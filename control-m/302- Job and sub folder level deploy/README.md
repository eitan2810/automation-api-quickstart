## Moving partial flow between environments.
## Preface
single consistent approach to deploy/promote workflows.  
allowing customers that require to deploy/promote at the job level and sub folder.  
customer will be able to deploy/promote a folder while changing only one or few jobs through Automation-api 

## Prerequisite
in order to add/update jobs/sub-folders  
foler/sub-folder muse be exist
jobs/sub-folders will be added/updated only under existing folder/sub-folder


## delete specific jobs/sub-folders Cli command example:
Tutorial on the [delete job](https://docs.bmc.com/docs/automation-api/monthly/deploy-service-1116950327.html#Deployservice-deploy_jobs_deletedeployjob::delete)
that explains how to delete job/subfolder automate code deployment.  
ctm deploy job::delete [Path] [server] [library]
  
## Adding/updateing specific jobs/sub-folders Cli command example:

Tutorial on the [product web page](https://docs.bmc.com/docs/display/workloadautomation/Tutorial+-+Automating+code+deployment)
that explains how DevOps engineer can automate code deployment.

JSON example:<br/>
[add specific job](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/addJobAsRoot.json)<br/>
[add specific sub-folder](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/addSubFolderAsRoot.json)
