## Moving partial flow between environments.
## Preface
single consistent approach to deploy/promote workflows.  
allowing customers that require to deploy/promote at the job level and sub folder.  
customer will be able to deploy/promote a folder while changing only one or few jobs through Automation-api 

## Prerequisite

1. In this example we will add single job to folder:

   * deploy Folder_1:  
      ctm deploy [deploy Folder_1](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/simpleFolder.json)<br/> 

    * add job to Folder_1 (add the PathElement object to the job) -    
        ctm deploy [add job to Folder_1](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/add_job_to_Folder_1.json)<br/>

    * You should get the result: [add job to Folder_1 result](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/add_job_to_folder_result%20.json)<br/> 
      ctm deploy jobs::get -s "ctm=*&folder=Folder_1"

2. In this example we will work with two folders: Folder_1 and Folder_2, we will copy a job named Dummy_Job_2 from Folder_1 to Folder_2

   * deploy the Folder_1+job and Folder_2:  
      ctm deploy [deploy folder1 and folder2](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/Folder1%2Bjob_Folder2.json)<br/> 

   * Get the job definition with the cli:  
      ctm deploy jobs::get -s "ctm=*&folder=Folder_1"

    * from the response copy the job and add the PathElement object to the job as in -  [copy job to Folder_2](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/copy_job_between_folders.json)<br/>  

    *  Deploy the json:  
    ctm deploy [copy job to Folder_2](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/copy_job_between_folders.json)<br/> 

    * You should get the result: [copy job to Folder_2 result](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/add_job_result.json)<br/>
      ctm deploy jobs::get -s "ctm=*&folder=Folder_2"
      
      
3. In this example we will work with two folders: Folder_1 and Folder_2 (Folder_2 is sub_folder of Folder_1)  
     we will move the job that exist under Folder_1 (parent folder) to Folder_2 (sub folder)  
    * deploy the Folder_1 + job and Folder_2 as sub folder of Folder_1: 
        ctm deploy [deploy Folder_1 and Folder_2 as sub folder + job](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/folder1%2Bfolder2_as_subfolder%2Bjob.json)<br/>
       
    * Get the job definition with the cli:  
        ctm deploy jobs::get -s "ctm=*&folder=Folder_1"
        
    * From the response copy the job and add the PathElement object to the job as in [move job to subFolder](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/copy_job_between_folders.json)<br/>

    *  Deploy the json:  
      ctm deploy [move job to subFolder](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/copy_job_between_folders.json)<br/>
      
    * You should get the result: [move job to subfolder_result](https://github.com/eitan2810/automation-api-quickstart/blob/302--Job-and-sub-folder-level-deploy/control-m/302-%20Job%20and%20sub%20folder%20level%20deploy/move_job_to_subFolder_result%20.json)<br/>
      ctm deploy jobs::get -s "ctm=*&folder=Folder_1"
      


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
