Lab Task – Create a Non-Interactive User on App Server 2
Problem Statement

To accommodate the backup agent tool’s specifications, the system admin team at xFusionCorp Industries requires the creation of a user with a non-interactive shell.

Task:
Create a user named mariyam with a non-interactive shell on App Server 2.





Solution:

Step-1: Connect to App Server 2 from Jump Host   -   Using SSH
Step-2: Create user with Non-Interactive Shell
sudo useradd -s /sbin/nologin mariyam
useradd → creates a new user

-s → specifies shell path

/sbin/nologin → prevents interactive login
