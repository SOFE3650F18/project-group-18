Iteration 1: Structure the System
=================================

Step 1: Review Inputs
---------------------

| Design Purpose | This is a greenfield system in the mature domain. The purpose is to produce a sufficiently detailed design to support the construction of the system. |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|


Based on the use-cases derived from the collected requirements the primary
functional requirements are determined to be:

| Use Case | Description                                                                                                                                                              | Rationale                                                                 |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| UC-15    | Maintainers create back-ups of the system and use it later on to restore partial or complete back-ups.                                                                   | Directly supports the core function of system availability and usability. |
| UC-21    | The system is developed using java framework where information on the system is self-contained. Integrated APIs allow for other systems to use the information provided. | Directly supports system performance and availability.                    |

The quality attribute scenarios have been prioritized as follows:

| **Quality Attribute ID** | **Importance to Customer** | **Difficulty of Implementation** | **Driver** |
|--------------------------|----------------------------|----------------------------------|------------|
| **QA-1**                 | High                       | High                             | ✔          |
| **QA-2**                 | High                       | High                             | ✔          |
| **QA-3**                 | Medium                     | Medium                           |            |
| **QA-4**                 | Medium                     | Low                              |            |
| **QA-5**                 | High                       | Medium                           | ✔          |

**Constraints:** Constraints 1, 5, 7, and 8 have been considered as drivers.

Step 2: Establish Iteration Goal by Selecting Drivers
-----------------------------------------------------

The primary goal of iteration 1 is to establish an overall system structure to
serve the needs of the customer. The primary decisions considered to influence
the system are the following drivers:

UC-15 System Redundancy and Availability

UC-21 System Development and Maintenance

QA-1 Interoperability, Security, Modifiability

QA-2 Performance, Usability, Availability

QA-5 Security

CON-1 System Performance: System Demand

CON-5 System Performance & Usability: Browser Support

CON-7 System Modifiability: Interoperability

CON-8 System Performance: Java

Step 3: Chose 1+ Elements of the System to Refine
-------------------------------------------------

The element to be refined is the entire course management system, primarily
consisting the main framework of the system.

Step 4: Chose 1+ Design Concepts That Satisfy The Selected Drivers
------------------------------------------------------------------

| **Design Decision** | **Rationale**                                                                                                                                                                                                          |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Web Application     | To meet the needs of all users, the reference architecture of a web application will be implemented.                                                                                                                   |
| Object-Oriented     | Supports use of a Java framework will assist with separation of classes and permissions. It also adheres to constraints provided.                                                                                      |
| N-Tier Architecture | Top-Tier: Client program handles the display of info on the web client Middle-Tier: Application program implements the logic of business software application to access database servers Bottom-Tier: Database Servers |

Step 5: Instantiate Architectural Elements, Allocate Responsibilities & Define Interfaces
-----------------------------------------------------------------------------------------

No functionalities and interfaces are defined in this first iteration.

Step 6: Sketch Views & Record Design Decisions
----------------------------------------------

Step 7: Analysis of Current Design & Review Iteration Goal & Achievement of Design Purpose
------------------------------------------------------------------------------------------

| **Not Addressed** | **Partially Addressed**      | **Completely Addressed** | **Design Decisions Made in Iteration 1**                                                                                 |
|-------------------|------------------------------|--------------------------|--------------------------------------------------------------------------------------------------------------------------|
|                   | CON-7, CON-5, CON-1, QA - 1, |                          | To meet the needs of all users, the reference architecture of a web application will be implemented.                     |
|                   | QA - 2, CON - 1              |                          |                                                                                                                          |
|                   | UC-21                        | CON-8                    | Use of a Java framework will assist with separation of classes and permissions. It also adheres to constraints provided. |
|                   | QA-5, UC-15                  |                          | Layered architecture creates stages of abstraction that can be used to grant and restrict permissions.                   |
