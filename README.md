<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>


# Implement Group Policy in Active Directory


## Platform and Tools Used

## Objective

In this project, I demonstrate how to implement a Group Policy Object (GPO) in Active Directory to enforce specific security settings. Group Policy is one of the most efficient methods to centrally manage and enforce policies across user groups within an organization.

-----

## Scenario

For this project, I created a GPO that disables access to the **Task Manager** for members of the **HR** group. This group consists of three users: **Nathan, Pipa, and Tsehay**. By enabling the **Remove Task Manager** policy setting and linking it to the HR group, these users are prevented from opening or using **Task Manager**:

<img width="300" alt="Capture 0" src="https://github.com/user-attachments/assets/473e6045-9e7e-4de9-8ed1-126be02e40f8" />

-----

### Create New GPO

1. I created a new Group Policy Object (GPO) under the **Group Policy Objects** container and named it **Task Manager** by navigating through:  
**Group Policy Management** > right-click **Group Policy Objects** > **New** > name it **Task Manager**:

<img width="400" alt="Capture" src="https://github.com/user-attachments/assets/43c975ef-9868-48b0-b7c3-47fd20bfcd49" />

## Enable Remove Task Manager

1. To access the **Remove Task Manager** option, I navigated through the following path:  
Right-click **Task Manager GPO** > **Edit** > **User Configuration** > **Policies** > **Administrative Templates** > **System** > **Ctrl+Alt+Del Options** > **Remove Task Manager**.  

<img width="400" alt="Capture 2" src="https://github.com/user-attachments/assets/f7625834-9fbd-4967-b50a-01cca9075383" />

2. I then selected **Remove Task Manager**, checked the **Enabled** option, and clicked **Apply** followed by **OK**:  

<img width="300" alt="Capture 3" src="https://github.com/user-attachments/assets/b18beafe-4d05-4fca-8827-2ddc34b55bb8" />


## Link and enforce Task Manager GPO to HR 

1. To link the **Task Manager** GPO to the **HR** group, I dragged the **Task Manager** GPO onto **HR** and clicked **OK**.  

<img width="300" alt="Capture 4" src="https://github.com/user-attachments/assets/5da26eaa-631e-45e6-ba67-29689223c06c" />
