# BACKUP-AUTOMATION
Backups are an essential part of database administration as they provide a way to recover data in case of data loss or a disaster, like a power outage or a cyber-attack.  Automating the backup process ensures that backups are taken at regular intervals and reduces the risk of human error. 

**BACKUP AUTOMATION**

One of the major responsibilities of a DBA is ensuring that, regular backups of the database are running.

**CASE STUDY**

A Company is a medium-sized organization that heavily relies on its SQL Server database for critical business operations. They have experienced data loss in the past due to manual backup processes and are looking for a robust backup automation solution to ensure data availability and minimize downtime.

**Solution:**
To address the client's challenges and meet their backup requirements, a comprehensive backup automation system was implemented. Their backup process are listed below 

**1. Full backup every SUNDAY 11PM**

**2. Differential backup Every DAY except sundays at 10pm**

**3. Transaction Log backup to run every 15 minutes**

The key tools used is SQL SERVER MAINTENANCE PLAN in SSMS

**PROCESS OF BACKUP AUTOMATION USING SQL SERVER MAINTENANCE PLAN**  

**STEP 1**
In your SQL Server Management Studion 
--> GO to management on you obeject explorer 
--> Right click on maintenance plan
![image](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/BACKUP-AUTOMATION/assets/100750844/e52a9ec3-5e84-44e1-93e7-cc0e9b62147c)



--> Click on Maintenance Plan Wizared (A dialog box will appear)

![image](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/BACKUP-AUTOMATION/assets/100750844/f69f97c4-4036-4d0d-a659-4f651cbe16d1)

--> Click on _Next, this will display where to set up your backup plan properties_
--> Rename your maintenance plan 
--> Give it a description
--> Select seperate schedule for each task 
![image](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/BACKUP-AUTOMATION/assets/100750844/f342cddc-8253-409c-acef-771b3dfa401c)

--> Click on _Next_
--> Select the type of task that the plan will perform 

**Backup Database (FULL)**

**Backup Database (DIFFERENTIAL)**

**Backup Database (TRANSACTION LOG)**
  
 ![image](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/BACKUP-AUTOMATION/assets/100750844/b4ddc1f0-8fe9-4dcd-a59e-6848df01cefa)

--> Click on --Next (This will display the order in which the task will be performed  )
![image](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/BACKUP-AUTOMATION/assets/100750844/ba4215f4-dbda-43c1-a3f8-c8658c8336f8)

A dialog box will appear to define each backup process 

--> FOR FULL BACKUP 
--> On the general pane Select all database 
--> Tick the 'Ignore databases where the state is not online'
![image](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/BACKUP-AUTOMATION/assets/100750844/b849092c-f009-4e0f-8daf-9f43f63970bd)

--> ANd click Ok 
--> Click on the DESTINATION pane 
--> Tick the 'Create a subdirectory for each database'
--> Choose a location to save you bakup 

![image](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/BACKUP-AUTOMATION/assets/100750844/937c7db9-d0ba-493c-9743-9a5db3c1f3dd)

--> Click on the OPTION pane 
--> Check the 'verify backup integrity box'
![image](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/BACKUP-AUTOMATION/assets/100750844/2f93e5e4-46cd-4c33-91a7-f03aeff5baf0)

--> Go to schedule below the pane 
--> Click on CHANGE to edit the schedule properties 
--> Change the name of the schedule 
--> Adjust the schedule timing base on daily or weekly or monthly as required by the organization 
![image](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/BACKUP-AUTOMATION/assets/100750844/f6a95ba4-17fc-4197-b819-cf3777ddc834)

--Click on Ok 
--> Then _Next_


Perform the same process for the DIFFERENTIAL BACKUP
--> After Completion , Click on _NEXT

Perform the same process for the TRANSACTION LOG BACKUP

CLICK ON NEXT 

THEN FINISH TO COMPLETE THE BACKUP AUTOMATION PLAN 

![image](https://github.com/DATABASE-ADMINISTRATOR-PROJECTS/BACKUP-AUTOMATION/assets/100750844/c34c47cb-f52f-4086-adc0-8c4690c77b1d)
