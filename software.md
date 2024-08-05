# Software and Computer Resources

## Software Access
UIUC provides many free softwares. We even get free Microsoft Windows(10 and 11) and Microsoft 365 licences. Visit https://webstore.illinois.edu/shop/ and login using your Illnois ID. Add any software to the cart and checkout. You don’t have to put any card details. After checkout you will get a screen with the installation instruction and licence keys.

# Matlab and Virtual Machines
Matlab is not available for download at the university. We can only use it through another service called Illinois Anywhere (https://techservices.illinois.edu/illinois-anyware/). It is a virtual server that we can use as an alternate to our local machines. But the data is lost after we logout and hence ensure that you save the data on your local disk

# VPN access
Follow the instructions at https://answers.uillinois.edu/illinois/98773

# Collection of more resources
You can visit https://techservices.illinois.edu/student-resource-guide/ to get an overview of all the software-based services available for a student at UIUC.

# Remote connection to lab workstations and computation nodes

## Accessing research group computers
Currently, we have many workstations with various computational capabilities. Most of the workstations are physically located in our lab at MEL 1214.

To access workstations, you need to first reserve a time slot using [this google form](https://docs.google.com/forms/d/e/1FAIpQLSdlS5YfXGFcA1PmO1cRzOvmQpiYS5Gd-IQXK2Z6SlDuIxqSPw/viewform). The form provides a list of all the machines with their intended use and specs. Before reserving a time slot, please make sure the time slot for that specific machine is empty through [this calendar](https://calendar.google.com/calendar/u/1?cid=Y19lOTk3MjI5OGQ3YjUxYmZmMzkwNjE3OGZjNDg4YmUxYjgwZWZlYzJkMWQ1MDQxMGRlNTJkMjcyNmU3MzZhNDBmQGdyb3VwLmNhbGVuZGFyLmdvb2dsZS5jb20). You don't have to add your time slot to the calendar as it will automatically be populated after submitting the form. If you made any mistake in the form or you would like to edit/delete your time slot, you can do so directly in the calendar. Please keep time slot reservation specific to your needs, and try to be considerate for other that might need the workstation too.

After reserving the time slot, you can access the machine using **Windows Remote Desktop Connection**, which should be natively implemented in your personal computer's Windows. To access the machine:
1. Open **Windows Remote Desktop Connection**
2. Enter the computer address: *mechse-wpk-XX.ad.uillinois.edu*, where XX is the machine number
3. Click **Connect**
4. A credentials prompt will appear. Enter the User name as **UOFI\YourNetID** (replace YourNetID with your NetID, make sure you are using **\** and not **/**). For Password, use your NetID password. Check **Remember me** for easier connection later
5. You might get a message stating that *The certificate is not from a trusted certifying authority*, just ignore the message and click **Yes**
6. You are connected now to the workstation

Notes:
1. You have to be connected to the campus network to access the lab computers. If you are outside campus network, you can use [Campus VPN](https://github.com/wpklab/KingLabWiki/blob/main/software.md#vpn-access)
2. Only connect to a machine within your time slot. If you would like to access the machine within someone else's time slot, ask for permission first.
3. Don't use the machine without reserving a time slot
4. Don't run background resource-consuming tasks without reserving a time slot

## Accessing campus cluster nodes
Clusters are high-performance computers with many GPUs and CPU cores that work as a single entity. Our lab has 2 cluster nodes each with 8xL40S GPUs, dual AMD 7763, 1TB of RAM, and HDR100. It is under the project group "wpk". It is highly recommended to complete the following courses before moving into using clusters:
1. [Basics of HPC](https://www.hpc-training.org/moodle/course/view.php?id=39)
2. [Introduction to HPC workflow](https://www.hpc-training.org/moodle/course/view.php?id=71)
3. Basics of Linux CLI - [Lesson 1](https://www.linfo.org/command_line_lesson_1.html), [Lesson 2](https://www.linfo.org/command_line_lesson_2.html)
To access the courses you would have to create an account on Globus. Globus is also a useful entity to help us transfer file to and fro from the HPCs. The second course will also help you get acquainted with Globus and its needs.
After you have gained access to the campus clusters, you can access them using SSH. You can use a GUI tool like PUTTY, or MobaXTerm in Windows or use CLI directly. To use CLI:
1. Open up the terminal in Linux and MacOS or Powershell in Windows.
2. Type ssh <netid>@cc-login.campuscluster.illinois.edu
3. When prompted enter your password
4. Close the terminal
5. GoTo your email and accept the terms and conditions in the mail you would receive
6. Now you can access the cluster using step 2

# Guidelines for using remote machines
## Research group computers
1. If you are installing software (Especially Python), make sure to check **Install for this user only** option if possible. This way there would be no conflicts of installed software between different users.
2. Use the *C drive* for any computations as it is an SSD and the computation would be faster. Make sure to keep your files inside your user directory (C:/Users/YourNetID). For any data storage, either use the other drive or use storage nodes
3. Clean your files (especially on C drive) regularly, as it is a shared storage with other users in the lab.

