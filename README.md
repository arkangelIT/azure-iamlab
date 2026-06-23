# azure-iamlab

## Purpose

Welcome to my documentation page for a hybrid IAM lab hosted in MSFT Azure cloud! The purpose of this lab is to setup a testing environment and show proof of concept for IAM principles and cloud management operations. Another use of the lab is to trial different technologies and services available in the Azure cloud to continously improve operations. The following sections will document the lab architecture, lessons learned, and other key information. 


## Architecture

INSERT IMAGE OF ARCHITECTURE
![Architecture Diagram](/assets/entraconnect.png)


## Components 

![Entra Connect](/assets/entraconnect.png)


# ACTIVE DIRECTORY INFO:

## HOST DETAILS:

NAME: DC01

TYPE: Windows Server 2022

## DIRECTORY STRUCTURE:

### FOREST: IAMLAB.LOCAL

**DOMAIN**: iamlab.local / iamlab297.onmicrosoft.com

├── OU=Corporate

│ ├── OU=Users

│ ├── OU=Groups

│ ├── OU=Computers

│ └── OU=Service Accounts

├── OU=IT

│ ├── OU=IT-Users

│ └── OU=IT-Groups

└── OU=Disabled Accounts

### USERS:



### GROUPS:





# MICROSOFT ENTRA INFO:

## CONDITIONAL ACCESS POLICIES:

### **Require MFA - All Users**

STATE: Enabled

SCOPE: All Users excluding Admin account(Jo Ey)

### Block Legacy Auth

STATE: Enabled

SCOPE: All Users

!image.png

## SSPR POLICY:

STATE: ENABLED

SCOPE: ALL USERS

!image.png
