## Moving partial flow between environments.
## Preface
single consistent approach to deploy/promote workflows.  
allowing customers that require to deploy/promote at the job level and sub folder.  
customer will be able to deploy/promote a folder while changing only one or few jobs through Automation-api 

## Prerequisite
To follow the tutorial, deploy the Folder_1+job and Folder_2 form the JSON file [deploy folder1 and folder2](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/Folder1%2Bjob_Folder2.json)<br/> 

1. In this example we will work with two folders: Folder_1 and Folder_2, we will copy a job named Dummy_Job_2 from Folder_1 to Folder_2

   * Get the job definition with the cli:  
    ctm deploy jobs::get -s "ctm=*&folder=Folder_1"

    * from the response copy the job and add the PathElement object to the job as in -  [copy job to Folder_2](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/copy_job_between_folders.json)<br/>  

    *  Deploy the json:  
    ctm deploy [copy job to Folder_2](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/copy_job_between_folders.json)<br/> 

    * You should have a result: [copy job to Folder_2 result](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/add_job_result.json)
      ctm deploy jobs::get -s "ctm=*&folder=Folder_2"
      
      
2. In this example we will work with two folders: Folder_1 and Folder_2, we will moved a job named Dummy_Job_2 from Folder_1 to Folder_2 (Folder_2)


## delete specific jobs/sub-folders Cli command example:
Tutorial on the [delete job](https://docs.bmc.com/docs/automation-api/monthly/deploy-service-1116950327.html#Deployservice-deploy_jobs_deletedeployjob::delete)
that explains how to delete job/subfolder automate code deployment.  
ctm deploy job::delete [Path] [server] [library]
  
## Adding/updateing specific jobs/sub-folders Cli command example:

Tutorial on the [product web page](https://docs.bmc.com/docs/display/workloadautomation/Tutorial+-+Automating+code+deployment)
that explains how DevOps engineer can automate code deployment.

JSON example:<br/>
[deploy folder1 and folder2](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/Folder1%2Bjob_Folder2.json)<br/>
[add specific sub-folder](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/addSubFolderAsRoot.json)
