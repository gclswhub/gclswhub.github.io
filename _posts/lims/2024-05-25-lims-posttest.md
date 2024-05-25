---
title: LIMS System Post-Testing Data Model
date: 2024-05-25 15:42:00 +0900
categories: [LIMS, Post-Testing]
tags: [lims]     # TAG names should always be lowercase
author: eric
---

### Post-Testing Data Model

#### DataAnalysis Model

| Field              | Description                                           |
|--------------------|-------------------------------------------------------|
| Analysis ID        | Unique identifier for the data analysis               |
| Execution ID       | Identifier of the test execution associated with the analysis (Foreign Key to TestExecution Model) |
| Analysis Type      | Type or method of analysis (e.g., Statistical Analysis, Visual Inspection) |
| Analysis Results   | Results obtained from the data analysis               |
| Analyst ID         | Identifier of the analyst conducting the analysis (Foreign Key to User Model) |
| Analysis Timestamp | Timestamp indicating when the analysis was performed |

#### TestResult Model

| Field              | Description                                           |
|--------------------|-------------------------------------------------------|
| Result ID          | Unique identifier for the test result                 |
| Execution ID       | Identifier of the test execution associated with the result (Foreign Key to TestExecution Model) |
| Test Parameters    | Parameters or conditions under which the test was conducted |
| Actual Results     | Actual results obtained from the test                 |
| Pass/Fail Status   | Pass/Fail status indicating the outcome of the test   |
| Comments           | Additional comments or notes related to the test result|
| Reviewer ID        | Identifier of the reviewer who reviewed the test result (Foreign Key to User Model) |
| Review Date        | Date and time when the test result was reviewed       |

#### SampleStorage Model

| Field              | Description                                           |
|--------------------|-------------------------------------------------------|
| Storage ID         | Unique identifier for the sample storage              |
| Sample ID          | Identifier of the sample being stored (Foreign Key to Sample Model) |
| Storage Location   | Location where the sample is stored                   |
| Storage Conditions | Conditions under which the sample is stored           |
| Storage Date       | Date when the sample was stored                       |
| Expiry Date        | Date when the sample is set to expire                 |

#### ProjectHistory Model

| Field         | Description                                            |
|---------------|--------------------------------------------------------|
| History ID    | Unique identifier for the project history entry        |
| Project ID    | Identifier of the project associated with the history  |
| Action        | Type of action or event (e.g., Data Analysis, Report Generation) |
| Description   | Detailed description of the action or event            |
| Timestamp     | Date and time when the action or event occurred        |

#### ProjectTimeline Model

| Field              | Description                                           |
|--------------------|-------------------------------------------------------|
| Timeline ID        | Unique identifier for the timeline entry              |
| Project ID         | Identifier of the project associated with the timeline |
| Milestone Description | Description of the milestone or event                |
| Milestone Date    | Date when the milestone or event is scheduled to occur|
