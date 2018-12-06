Iteration 2: Support Primary Functionality
==========================================

Step 2: Establish Iteration Goal by Selecting Drivers
-----------------------------------------------------

The primary goal in Iteration 2 is to address the architectural concern of
identifying structures to support primary functionality. The primary use cases
to be considered here are:

| **Usecase** | **Title**      | **Concerns**                       | **Description**                                                                                                                                                          |
|-------------|----------------|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| UC-15       | Back-Up        | System Redundancy and Availability | Maintainers create back-ups of the system. Backups can be used later to restore partial or complete back-ups or prevent system performance loss.                         |
| UC-21       | Java Framework | System Development and Maintenance | The system is developed using java framework where information on the system is self-contained. Integrated APIs allow for other systems to use the information provided. |

Step 3: Choose 1+ Elements of System to Refine
----------------------------------------------

As the n-tier layered architecture is composed of the three layers that make up
the core functionality of the system, they will be decomposed further.

Step 4: Chose 1+ Design Concepts That Satisfy The Selected Drivers
------------------------------------------------------------------

| **Design Decision & Location** | **Rationale & Assumptions**                                                                                                                                                                                                                     |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Google App Engine              | Web framework that allows for the implementation of a Java-based development. Applications are run from multiple servers and are sandboxed to allow for efficiency. Scaling for applications is also supported for cope under increased demand. |
| Cloud SQL (PostgreSQL & MySQL) | Supported under the App Engine, both are powerful database management systems that are focused around stability, security, and expandability.                                                                                                   |
| Event Driven Programming       | Allows for a dynamic user interface the event-driven architecture caters to both client and server sides to allow for high performance under load.                                                                                              |

Step 5: Instantiate Architectural Elements, Allocate Responsibilities & Define Interfaces
-----------------------------------------------------------------------------------------

| **Design Decision & Location** | **Rationale**                                                                        |
|--------------------------------|--------------------------------------------------------------------------------------|
| Google App Engine              | The main point of the connector to communicate with the database, client and server. |
| Cloud SQL (PostgreSQL & MySQL) | Data storage and retrieval                                                           |
| Event Driven Programming       | Processes events to generate responses from the back-ups and restoration processes   |

Step 6: Sketch Views & Record Design Decisions
----------------------------------------------

![Iteration2_deployment]( https://github.com/SOFE3650F18/project-group-18/blob/master/Iteration%202/Deployment.png)
![Iteration2_sequence](https://github.com/SOFE3650F18/project-group-18/blob/master/Iteration%202/Sequence%20Diagram.png)

Step 7: Perform Analysis of Current Design & Review Iteration Goal & Achievement of Design Purpose
--------------------------------------------------------------------------------------------------

| **Not Addressed** | **Partially Addressed** | **Completely Addressed** | **Design Decisions Made in Iteration 1**                                                                   |
|-------------------|-------------------------|--------------------------|------------------------------------------------------------------------------------------------------------|
|                   | CON-1                   | CON-7, CON-5, UC-21      | App engine provides flexible versatile client-server to communicate with the database and various systems. |
|                   | QA-02, UC-15            | QA-01                    | Using CloudSQL ensures self-contained data set that is secure and accessible.                              |
| QA-05             |                         |                          | No relevant decision was made.                                                                             |
