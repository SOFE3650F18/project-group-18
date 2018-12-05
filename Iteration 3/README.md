Iteration 3: Addressing Quality Attribute Scenario Driver 
(QA-2)
================================================================

Step 2: Establish Iteration Goal by Selecting Drivers
-----------------------------------------------------

>   For this iteration, the architect focuses on the QA-2 quality attribute
>   scenario: During failure or error state, backups can be used to restore
>   data.

Step 3: Choose 1+ Elements of System to Refine
----------------------------------------------

The elements to be refined are the application and database servers.

Step 4: Choose 1+ Design Concepts that Satisfy the Selected Driver

| **Design Decision & Location**                                                                      | **Rationale and Assumptions**                                                                                                                         |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Using the active redundancy tactic by replicating application and database servers                  | By replicating these servers, the system can withstand the failure of one of the application or database servers without affecting functionality.     |
| Creating backup servers of the application server, the database server and other important elements | By backing up the entire system, the system can react to failure or error states of one or more elements by restoring via the backups that were made. |

Step 5: Instantiate Architectural Elements, Allocate Responsibilities and Define Interfaces
-------------------------------------------------------------------------------------------

| **Design Decision & Location**                              | **Rationale**                                                                                                            |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Implement active redundancy in application/database servers | Since each server has a backup, in the event of error/failure, system will use backup server to withstand functionality. |
| Implement backup restore using technology support           | In the event of an error or failure, system or elements of system will be restored using backups.                        |

Step 6: Sketch Views & Record Design Decisions
----------------------------------------------

![Iteration3_Step6](https://github.com/SOFE3650F18/project-group-18/blob/master/Iteration%203/Iteration%203_%20Step%206.png)
----------------------------------------

Step 7: Perform Analysis of Current Design & Review Iteration Goal and Design Objectives
----------------------------------------------------------------------------------------

| **Not Addressed**               | **Partially Addressed** | **Completely Addressed** | **Design Decisions Made in Iteration 3**                                                |
|---------------------------------|-------------------------|--------------------------|-----------------------------------------------------------------------------------------|
|                                 | CON-1                   | QA-2, UC-15              | Making the application/database servers redundant, system is able to withstand failure. |
|                                 |                         | QA-2, UC-15              | Periodic backup of servers will allow system to restore when failure occurs.            |
| QA-1, QA-5, CON-5, CON-7, UC-21 |                         |                          | No relevant decision made.                                                              |
