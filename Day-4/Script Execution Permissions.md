In a bid to automate backup processes, the xFusionCorp Industries sysadmin team has developed a new bash script named xfusioncorp.sh. While the script has been distributed to all necessary servers, it lacks executable permissions on App Server 3 within the Stratos Datacenter. Your task is to grant executable permissions to the /tmp/xfusioncorp.sh script on App Server 3. Additionally, ensure that all users have the capability to execute it.

SOlution

SSH into Server-3
ssh user@IP

chmod 755 /tmp/xfusioncorp.sh

chmod = change mode
we have owner group other permissions

4	read (r)
2	write (w)
1	execute (x)


So 7 = 4+2+1 → rwx
and 5 = 4+1 → r-x