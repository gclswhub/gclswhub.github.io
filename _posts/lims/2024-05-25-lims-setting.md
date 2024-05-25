---
title: LIMS System Setting Data Model
date: 2024-05-25 15:42:00 +0900
categories: [LIMS, Setting]
tags: [lims]     # TAG names should always be lowercase
author: eric
---

### Setting Data Model

#### User Model

| Field          | Description                                         |
|----------------|-----------------------------------------------------|
| User ID        | Unique identifier for the user                      |
| Username       | Username for logging into the system                |
| Password       | Encrypted password for user authentication          |
| Email          | Email address of the user                           |
| Role           | Role or permission level of the user                |
| Last Login     | Date and time of the user's last login              |
| Created At     | Date and time when the user account was created     |
| Updated At     | Date and time when the user account was last updated|

#### SystemConfiguration Model

| Field            | Description                                         |
|------------------|-----------------------------------------------------|
| Config ID        | Unique identifier for the system configuration      |
| Config Key       | Key or name of the configuration setting            |
| Config Value     | Value of the configuration setting                  |
| Description      | Description or purpose of the configuration setting |

#### Standard Model

| Field          | Description                                         |
|----------------|-----------------------------------------------------|
| Standard ID    | Unique identifier for the standard                  |
| Standard Name  | Name or title of the standard                       |
| Description    | Description of the standard                         |
| Applicable Areas | Areas to which the standard is applicable         |
| Created At     | Date and time when the standard was created        |
| Updated At     | Date and time when the standard was last updated   |

#### Equipment Model

| Field            | Description                                         |
|------------------|-----------------------------------------------------|
| Equipment ID     | Unique identifier for the equipment                 |
| Equipment Name   | Name or description of the equipment                |
| Equipment Type   | Type or category of the equipment                   |
| Manufacturer     | Manufacturer of the equipment                       |
| Model Number     | Model number or identifier of the equipment         |
| Calibration Status | Status indicating whether the equipment is calibrated |
| Calibration Date   | Date when the equipment was last calibrated        |
| Maintenance Status | Status indicating whether the equipment is under maintenance |
| Maintenance Date   | Date of the last maintenance activity               |
| Created At       | Date and time when the equipment was added to the system |
| Updated At       | Date and time when the equipment information was last updated |

#### BackupModel

| Field             | Description                                         |
|-------------------|-----------------------------------------------------|
| Backup ID         | Unique identifier for the backup                    |
| Backup Type       | Type or method of backup (e.g., Manual, Automated)  |
| Backup Timestamp  | Date and time when the backup was performed         |
| Backup Location   | Location where the backup is stored                 |
| Backup Status     | Status of the backup process (e.g., Successful, Failed) |

#### Integration Model

| Field             | Description                                         |
|-------------------|-----------------------------------------------------|
| Integration ID    | Unique identifier for the integration               |
| Integration Name  | Name or description of the integration              |
| Integration Type  | Type or method of integration (e.g., API, Webhook)  |
| Integration Status| Status of the integration process (e.g., Active, Inactive) |

#### AuditLog Model

| Field             | Description                                         |
|-------------------|-----------------------------------------------------|
| Log ID            | Unique identifier for the audit log                 |
| Action            | Action performed (e.g., Login, Data Access)         |
| User ID           | Identifier of the user performing the action        |
| Timestamp         | Date and time when the action occurred              |
| IP Address        | IP address of the user's device                     |
| Details           | Additional details or information about the action |
