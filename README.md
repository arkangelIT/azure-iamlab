# azure-iamlab

## Purpose

Welcome to my documentation page for a hybrid IAM lab hosted in MSFT Azure cloud! The purpose of this lab is to setup a testing environment and show proof of concept for IAM principles and cloud management operations. Another use of the lab is to trial different technologies and services available in the Azure cloud to continously improve operations. The following sections will document the lab architecture, lessons learned, and other key information. 


## Architecture

![Architecture Diagram](/assets/iamlab-diagram.png)

## Lessons Learned

- Need to edit the Link order for the Default Domain Policy so seperate GPOs ex. Password Policy can be applied as primary instead of the default policy.
-https://specopssoft.com/blog/check-password-requirements-active-directory/
-Good detail on default domain GPO management
- Using Free Trial, configured alternate domain to sync with local AD domain.
-https://learn.microsoft.com/en-us/answers/questions/2141057/how-to-setup-active-drirectory-sync-with-mismatche
-Azure billing can be confusing, the top level is the Billing Profile and any credits or funds come from this profile. They are then applied to Subscriptions underneath the profile. Received a message that I had no credits, but this was for the Subscription being used, not the billing profile.  


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
![AD Users](/assets/iamlab-users.png)


### GROUPS:

![AD Users](/assets/iamlab-groups.png)



# MICROSOFT ENTRA INFO:

## CONDITIONAL ACCESS POLICIES:

### **Require MFA - All Users**

STATE: Enabled

SCOPE: All Users excluding Admin account

### Block Legacy Auth

STATE: Enabled

SCOPE: All Users


## SSPR POLICY:

STATE: ENABLED

SCOPE: ALL USERS

![SSPR](/assets/iamlab-sspr.png)
