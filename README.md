# Data-Warehouse-Cloud
Data Warehouse Cloud Technical Content

Based on Olaf Fischer's excellent content which can be found here:  https://blogs.sap.com/2021/10/12/sap-data-warehouse-cloud-data-integration-monitoring-sample-content-for-reporting/

# Relevant DWC  tables with statistics: (when monitoring is activated)

TASK_LOCKS_V_EXT
Table with unfinished tasks

TASK_LOG_MESSAGES_V_EXT
Table with messages for each task

TASK_LOGS_V_EXT
Table with each task

TASK_SCHEDULES_V_EXT
Table with schedule for each application/space/object

https://help.sap.com/doc/653e215be007410e80e64dfc537ef2d0/cloud/en-US/SAP_Data_Warehouse_Cloud_Administrator_Guide.pdf (as of page 255)


# Prerequisites for consuming SQL view in SAC build in DWC:

Semantic Usage >> “Analytical Dataset”
Expose for Consumption >> On (default setting)
Status >> Deployed

# We have extended the content in the following areas:

1. View “MON_LOCK_FAILED_TASK_DETAILS” as a replacement of LOCK_DETAILS (extended with application (in key) & last failed task is retrieved. View looks at the tasks that are running in the system and collects the corresponding messages.

2. View “MON_LOCK_TASK_DETAILS” is a new view with a list of all locked Jobs and the underlying details. It checks jobs which are still running and therefore are reponsible for locking other jobs. View looks at the tasks that are causing locks in the system and collects the messages of the latest failed task related to the same application/space/object combination in DWC

3. View ..... 


