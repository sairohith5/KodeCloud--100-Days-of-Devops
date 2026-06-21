Question

The production support team of xFusionCorp Industries needs a Bash script to automate website backup tasks.

A static website is hosted on App Server 1 (stapp01), and a script must be created with the following requirements:

Tasks to perform:

Create a zip archive named:

xfusioncorp_beta.zip

from:

/var/www/html/beta

Store the archive locally in:

/archives/

Copy the archive to the Nautilus Storage Server (ststor01) in:

/archives/
Ensure the script does NOT ask for password during file transfer.

The script must be placed in:

/scripts/beta_archive.sh
Do NOT use sudo inside the script.
✅ Answer
📄 Script: /scripts/beta_archive.sh
#!/bin/bash

# Create zip archive of beta website
zip -r /archives/xfusioncorp_beta.zip /var/www/html/beta

# Copy archive to Storage Server
scp /archives/xfusioncorp_beta.zip natasha@ststor01:/archives/
🔐 SSH Passwordless Setup (One-time requirement)

To avoid password prompts during SCP:

Step 1: Generate SSH key
ssh-keygen
Step 2: Copy key to Storage Server
ssh-copy-id natasha@ststor01

Password:

Bl@kW
Step 3: Verify connection
ssh natasha@ststor01

Exit after successful login:

exit
🚀 Execution Steps
1. Give execute permission
chmod +x /scripts/beta_archive.sh
2. Run script
/scripts/beta_archive.sh
🔍 Verification
On App Server:
ls -l /archives/
On Storage Server:
ssh natasha@ststor01
ls -l /archives/

Expected output:

xfusioncorp_beta.zip
🧠 Key Learning
Bash scripting for automation
File compression using zip
Secure file transfer using scp
SSH key-based authentication
Basic DevOps backup workflow