# System Architecture Document

## Overview
This document describes the architecture of a system designed to provide a set of services to users of different partners. Each partner has a distinct set of users, and their functionalities and permissions are configured individually.

## User Types and Transitions

The system supports several types of end users:
-	Guest
-	Basic
-	Advanced
-	Company
  
Each partner can create unique combinations of these user types. The following transitions are possible:
-	Guest → Basic → Advanced → Company
- Company → Advanced → Basic → Guest

## User Session and Operation Limits

| User Type | Session Duration (min) | Max number of operations daily/weekly |
|---|---|---|
| Guest User | 20 | 5/20 |
| Basic User (KYC successfully completed) | - | 20/50 |
|  User | - | - |
| Advanced User | - | - |
| Company User | - | - |

> **Note:**
> After reaching any of the limits (session duration or max number of operations), Guest users are transitioned to the `idle` state.



> **Note for the SME**: need to add conditions for becoming Company/Advanced users. Like the KYC-completed condition for the Basic User.


