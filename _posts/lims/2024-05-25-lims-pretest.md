---
title: LIMS System Pre-Testing Data Model
date: 2024-05-25 14:35:00 +0900
categories: [LIMS, Pre-Testing]
tags: [lims]     # TAG names should always be lowercase
author: eric
---

### 1.1 Sample Reception and Registration

#### Sample Model

| Field              | Description                                        |
|--------------------|----------------------------------------------------|
| Sample ID          | Unique identifier for the sample                   |
| Sample Type        | Type or category of the sample                     |
| Sample Quantity    | Quantity or amount of the sample                   |
| Sample Source      | Source or origin of the sample                     |
| Sample Condition   | Condition or state of the sample                   |
| Client ID          | Identifier of the client associated with the sample (Foreign Key to Client Model) |
| Registration Date  | Date and time when the sample was registered      |

#### Client Model

| Field              | Description                                       |
|--------------------|---------------------------------------------------|
| Client ID          | Unique identifier for the client                  |
| Client Name        | Name of the client                                |
| Contact Information| Contact details of the client (phone, email, etc.)|
| Billing Information| Billing details of the client (address, account number, etc.)|

### 1.2 Test Request and Planning

#### TestRequest Model

| Field               | Description                                         |
|---------------------|-----------------------------------------------------|
| Request ID          | Unique identifier for the test request              |
| Client ID           | Identifier of the client making the test request (Foreign Key to Client Model) |
| Test Items          | Description of the test items included in the request|
| Requested Test Date | Date when the test is requested                     |
| Priority            | Priority level of the test request                  |
| Status              | Current status of the test request (e.g., Pending, Approved, Rejected) |

#### TestItem Model

| Field              | Description                                      |
|--------------------|--------------------------------------------------|
| Item ID            | Unique identifier for the test item              |
| Test Name          | Name or title of the test                        |
| Test Description   | Detailed description of the test                 |
| Required Materials | Materials or resources required for the test     |
| Test Standard      | Standard to which the test must adhere (Foreign Key to Standard Model) |

#### Standard Model

| Field              | Description                                           |
|--------------------|-------------------------------------------------------|
| Standard ID        | Unique identifier for the standard                     |
| Standard Name      | Name or title of the standard                         |
| Description        | Description of the standard                           |
| Applicable Areas   | Areas to which the standard is applicable (e.g., EMC, Safety, Energy Efficiency, Software) |

### 1.3 Sample Preparation

#### SampleProcessing Model

| Field             | Description                                            |
|-------------------|--------------------------------------------------------|
| Processing ID     | Unique identifier for the sample processing activity   |
| Sample ID         | Identifier of the sample being processed (Foreign Key to Sample Model) |
| Processing Date   | Date and time when the processing activity occurred    |
| Processing Type   | Type or nature of the sample processing activity       |
| Processing Details| Additional details or notes about the processing activity |

### 1.4 Test Standard Management

#### Standard Model (already defined in section 1.2)

### 1.5 Project History and Timeline Management

#### ProjectHistory Model

| Field         | Description                                            |
|---------------|--------------------------------------------------------|
| History ID    | Unique identifier for the project history entry        |
| Project ID    | Identifier of the project associated with the history  |
| Action        | Type of action or event (e.g., Sample Reception, Test Planning, Sample Preparation) |
| Description   | Detailed description of the action or event            |
| Timestamp     | Date and time when the action or event occurred        |

#### ProjectTimeline Model

| Field              | Description                                           |
|--------------------|-------------------------------------------------------|
| Timeline ID        | Unique identifier for the timeline entry              |
| Project ID         | Identifier of the project associated with the timeline |
| Milestone Description | Description of the milestone or event                |
| Milestone Date    | Date when the milestone or event is scheduled to occur|

