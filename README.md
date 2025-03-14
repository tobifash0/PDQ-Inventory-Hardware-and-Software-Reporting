# Overview : Lab 11 PDQ Inventory: Hardware and Software Reporting
This repository documents my home lab focused on PDQ Inventory: Hardware and Software Reporting using VirtualBox. The lab aims to explore PDQ Inventory's capabilities for gathering detailed reports on hardware and software configurations across a network of virtual machines. The project will include setting up PDQ Inventory, creating custom reports, and automating hardware/software data collection for system management and network monitoring.

## Objectives
- Learn PDQ Inventory: Explore how to set up PDQ Inventory and configure it for comprehensive hardware and software reporting.
- Create Custom Reports: Learn how to build and customize reports to track hardware specifications, software installations, and system configurations.

## Documentation
In this home lab, I will showcase the installation and uses of PDQ Inventory. To start, open File Explorer and navigate to the SimoTech folder. Inside, you should find the PDQ Inventory application.

<br>

![Screenshot 2025-03-14 at 3 40 14 AM](https://github.com/user-attachments/assets/33a406a7-f628-4178-bc1c-7c77e597893c)

<br>

1. We can double click on the application to start the installation then continue it to install to finish. Launch the application once finish.

<br> 

![Screenshot 2025-03-14 at 4 57 25 AM](https://github.com/user-attachments/assets/1bfb1980-feb1-4f36-b421-52e4480d711d)

<br>

2. Lets add Desktop2 to PDQ Inventory, to do that select “Computers” on top → “Add computers” then “Active Directory - Browse by Name” then select “Desktop2.tobifash.com” as the target to add then select “OK”.

<br>

![Screenshot 2025-03-14 at 5 01 21 AM](https://github.com/user-attachments/assets/41a74017-fef7-4994-991f-de24539e6b6c)

<br>

3. PDQ Inventory is a powerful IT asset management tool that helps track and manage hardware and software across a network. It provides real-time insights, automates reporting, and integrates seamlessly with tools like PDQ Deploy for efficient software updates and policy compliance.

Here are some of the features we can use in PDQ Inventory: Right-click on Desktop2, then select Run Report → Share Folders to generate a report on the shared folders available on that machine.

<>br> 

![image](https://github.com/user-attachments/assets/5c5e2138-9a69-4874-80f0-3721a7d411ce)

<br>

4. This show us all the folders that are mapped on it. Lets double click on “ADMIN$”

<br> 

![image](https://github.com/user-attachments/assets/7cbc28f4-987c-44b7-9467-4f75fee7374e)

<br>

5. It will give us all the details and specifications that are on that computer, such as who is logged in currently, what the domain controller is, the host name, what operating system it is, and what version of Windows it is using.

<br> 

![Screenshot 2025-03-14 at 5 03 20 AM](https://github.com/user-attachments/assets/914ebe49-84ad-40e1-8749-4b85f46d1f65)

<br> 

6. On the left-hand side, we can see all the items we can explore on Desktop2. Let's take a look at the Applications by clicking on it. This is a great way to check what applications are installed on the computer. If something is missing, we can use this feature to identify the missing software and download it accordingly.

<br> 

![image](https://github.com/user-attachments/assets/80313bb8-5437-469e-9bb9-2ab832943ba0)

<br> 

7. To verify if we have these applications downloaded, let's go to our Desktop2 VM and open Control Panel → Uninstall a Program. This will display the list of applications installed on Desktop2 under Bob's account.

<br> 

![image](https://github.com/user-attachments/assets/dab4b384-6bc6-4957-8d41-116f34bc445a)

<br> 

8. We can also navigate to the CPU section on the left to see how many CPU cores are available on Desktop2. It will also provide information about the processors being used on the system.

<brr> 

![Screenshot 2025-03-14 at 5 06 14 AM](https://github.com/user-attachments/assets/5ab31344-a5a8-4668-81c9-44a5c3bd977e)

<br> 

9. The Environment tab on the left shows us the path directories configured on Desktop2 as well.

<br> 

![Screenshot 2025-03-14 at 5 07 33 AM](https://github.com/user-attachments/assets/f7691aef-4f28-4cf9-b6bf-12b6d1fc83be)

<br> 

10. We can look into Printers and see which printer machines are installed on Desktop2 as well.

<br> 

![image](https://github.com/user-attachments/assets/c47577a0-bae4-430d-b807-d1c0872e5ba5)

<br> 

11. On the Shares tab, we can see our shared drives.

<br> 

![image](https://github.com/user-attachments/assets/3e45f20c-37e9-413d-a620-46176d77c74d)

<br> 

12. If we wanted to remote admin into Desktop2 then double click on “ADMIIN$”, here we can see things on a system level.

<br> 

![Screenshot 2025-03-14 at 5 07 33 AM](https://github.com/user-attachments/assets/d3fd4713-9169-40ae-a9bb-f3d84f0c00ad)

<br> 

13. If we wanted to add a specific file to Desktop2, we can double click on “C$” then add anything in there.

<br>

![image](https://github.com/user-attachments/assets/275534a6-8190-47ec-9f8d-070b98342aa2)

<br>

14. Lets copy the text document “results” then go into “Users” → into “Bob” → then “Desktop”.

<br> 

<img width="683" alt="Screenshot 2025-03-14 at 5 30 56 AM" src="https://github.com/user-attachments/assets/9860fb0e-82d2-465b-9859-8faadaa2d489" />

<br> 

15. Paste the copied "results" file onto the Desktop, and we can see that the file was successfully transferred to our Desktop2 VM from our Windows Server 2022 VM using PDQ Inventory.

<br> 

![image](https://github.com/user-attachments/assets/264033e1-1bf0-40e7-a26d-4b970917002c)

<br> 


16. Some additional features in PDQ Inventory include Manage with MMC, which allows us to manage Computer Management on the Desktop2 VM directly from PDQ Inventory. To use this, select Tools at the top, then choose Manage with MMC.


<br> 

![image](https://github.com/user-attachments/assets/d017842c-dfe3-447e-bf92-327f1e0cb5cd)

<br> 

17. We can create a new user on Desktop2 if we wanted to by using this feature.

<br> 

![image](https://github.com/user-attachments/assets/c8ce85ed-9458-4fb3-8ff1-25e9b9205d2a)

<br> 

18. Another tool we can use is “Remote Desktop” if we want to remote into Desktop2 from PDQ Inventory.

<br>

![image](https://github.com/user-attachments/assets/206be133-0c3b-43d5-8afe-b97dfd4c0065)

<br> 

19. Another powerful feature we can use is remotely rebooting Desktop2. To do this, select Tools, then choose Reboot/Shutdown.

<br> 

![image](https://github.com/user-attachments/assets/46d67489-e0f8-4709-a817-2358d8f9a844)

<br> 

20. Now, let's print a report on Desktop2. Return to the home page in All Computers, right-click on Desktop2, and select Print Preview. This feature is useful if, for example, a manager requests a report on a specific user's computer.

<br> 

![Screenshot 2025-03-14 at 5 15 12 AM](https://github.com/user-attachments/assets/cd7a9a3d-9ccf-4532-8a04-5ef9c0fa38af)

<br> 

21. Now, let's print a report on the hardware devices on Desktop2. Right-click on Desktop2, then select Run Report → Hardware Devices. This will generate a report of all the hardware devices installed on Desktop2.

<br> 

![image](https://github.com/user-attachments/assets/9a3f1f8d-843a-465f-af5d-d2e87afab855)

<br> 

22. Select the printer icon on the top left to preview the report. This will display a list of all the hardware devices associated with Desktop2.

<br> 

![image](https://github.com/user-attachments/assets/cf853d77-ac77-4490-b2be-05be07bc76b7)

<br>

23. Lastly, we can launch PDQ Deploy for Desktop2 through PDQ Inventory. In All Computers, right-click on Desktop2, select Tools, and then choose Run PDQ Deploy.

<br> 

![image](https://github.com/user-attachments/assets/cdeb7fd2-df17-4198-b6bd-f8248a538a72)

<br> 

24. From here, we can deploy applications or software packages onto Desktop2 using this feature. Let's select the Mozilla Firefox package that we previously installed on our Windows Server 2022 VM, then click OK to deploy it onto the Desktop2 VM.

<br> 

![Screenshot 2025-03-14 at 5 17 42 AM](https://github.com/user-attachments/assets/b92ebd0e-fa09-43dc-8ea5-25dbe6798b6d)

<br> 

25. Notice on the left that Desktop2.tobifash.com is the target for the Firefox application deployment. Now, select Deploy Now to begin the deployment process.

<br> 

![Screenshot 2025-03-14 at 5 18 26 AM](https://github.com/user-attachments/assets/80421786-143c-4a5e-a489-2f041acd11b7)

<br> 

26. Now, we can see that Firefox has been successfully installed on our Desktop2 VM through the PDQ Deploy deployment process.

<br> 

![image](https://github.com/user-attachments/assets/9ad5a539-bd53-4979-95f7-42a20dfac32b)

<br> 

27. Congratulations! We have successfully completed Home Lab 10 on PDQ Deploy and Inventory!

This project focused on using PDQ Inventory within a VirtualBox environment to track and manage hardware and software across virtual machines. We explored creating and analyzing reports, gaining insights into user resources, and generating reports for managers or supervisors.

👉 [Next Lab 12 : Printer Setup on Server 2022, NTFS Permissions0](https://github.com/tobifash0/Printer-Setup-on-Server-2022-NTFS-Permissions)
