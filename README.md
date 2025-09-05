<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>


# Implement Group Policy in Active Directory


## Platform and Tools Used

- Windows Server 2022 VM
- Active Directory
- Web Browser

## Objective

In this project, I will demonstrate how I implemented a Group Policy in Active Directory to enforce specific security settings. Group Policy is one of the most efficient methods to centrally manage and enforce policies across user groups within an organization.

For this project, I created a GPO that disables access to the **Task Manager** for members of the **HR** group. This group consists of three users: **Nathan, Pipa, and Tsehay**. By enabling the **Remove Task Manager** policy setting and linking it to the HR group, these users are prevented from opening or using **Task Manager**:

<img width="300" alt="Capture 0" src="https://github.com/user-attachments/assets/473e6045-9e7e-4de9-8ed1-126be02e40f8" />

-----

### Create New GPO

1. I created a new Group Policy Object (GPO) under the **Group Policy Objects** container and named it **Task Manager** by navigating through:  
**Group Policy Management** > right-click **Group Policy Objects** > **New** > name it **Task Manager**:

<img width="400" alt="Capture" src="https://github.com/user-attachments/assets/43c975ef-9868-48b0-b7c3-47fd20bfcd49" />

### Enable Remove Task Manager

1. To access the **Remove Task Manager** option, I navigated through the following path:  
Right-click **Task Manager GPO** > **Edit** > **User Configuration** > **Policies** > **Administrative Templates** > **System** > **Ctrl+Alt+Del Options** > **Remove Task Manager**.  

<img width="400" alt="Capture 2" src="https://github.com/user-attachments/assets/f7625834-9fbd-4967-b50a-01cca9075383" />

2. I then selected **Remove Task Manager**, checked the **Enabled** option, and clicked **Apply** followed by **OK**:  

<img width="300" alt="Capture 3" src="https://github.com/user-attachments/assets/b18beafe-4d05-4fca-8827-2ddc34b55bb8" />



### Link and enforce Task Manager GPO to HR 

1. To link the **Task Manager** GPO to the **HR** group, I dragged the **Task Manager** GPO onto **HR** and clicked **OK**.  

<img width="300" alt="Capture 4" src="https://github.com/user-attachments/assets/5da26eaa-631e-45e6-ba67-29689223c06c" />

2. Next, I enabled the **Enforced** setting on the **Task Manager** GPO for the **HR** group by navigating:  
Right-click **Task Manager** > check **Enforced**. By doing this, the policy will be offically at work. 

<img width="300" alt="IMG_5010" src="https://github.com/user-attachments/assets/5c46c5ec-826b-4f6c-af9b-1e6e5d00612b" />

3. After enabling and enforcing **Remove Task Manager**, I updated the Group Policy settings by running the command `gpupdate /force`:  

<img width="400" alt="Capture 6" src="https://github.com/user-attachments/assets/8ddc2196-a1ce-4ecf-b118-2c969ed5c5e8" />


### Test Policy on HR user

1.To verify that the **Remove Task Manager** policy was applied correctly, I logged in as one of the users in the **HR** group, **Tsehay**.  

<img width="400" alt="Capture 7" src="https://github.com/user-attachments/assets/15733726-0675-4031-ae43-5bc67a312b28" />

2. As intended, the policy was successfully enforced, and user **Tsehay** is unable to access the **Task Manager**:  

  <img width="350" alt="capture 8" src="https://github.com/user-attachments/assets/5da10576-4741-4f4c-b0ec-9d1067338496" />
  <img width="150" alt="capture 9" src="https://github.com/user-attachments/assets/bbb904a9-d16f-463f-b323-42517490c6cd" />
</p>

----

## Conclusion

This project demonstrated how Group Policy in Active Directory can be used to enforce security settings across specific user groups. By creating, linking, and enforcing a GPO, I successfully restricted members of the **HR** group from accessing the **Task Manager**. This exercise highlights the effectiveness of Group Policy as a centralized management tool, ensuring consistent policy enforcement while reducing the need for manual configuration on individual machines.







