Following security audits, the xFusionCorp Industries security team has rolled out new protocols, including the restriction of direct root SSH login.
Your task is to disable direct SSH root login on all app servers within the Stratos Datacenter.


Solution:
Login to the server -ssh tony@stapp01.stratos.xfusioncorp.com
Enter Password
Next Go to
Cd /etc
cd ssh
vi sshd_config and add
PermitRootLogin no
Save :wq!

Next restart sshd -> sudo systemctl restart sshd