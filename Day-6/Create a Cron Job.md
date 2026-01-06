Question

The Nautilus system admins team has prepared scripts to automate several day-to-day tasks. They want them to be deployed on all app servers in Stratos DC on a set schedule. Before that, they need to test similar functionality with a sample cron job. Perform the steps below:

a. Install cronie package on all Nautilus app servers and start the crond service.
b. Add a cron job */5 * * * * echo hello > /tmp/cron_text for the root user.

Answer with Explanation
Step 1 — Install cronie Package

cronie is the cron implementation used in RHEL/CentOS-based systems.
It provides the cron daemon (crond) that runs scheduled jobs.

Run the following commands on each app server:
sudo yum install -y cronie

Step 2 — Enable & Start crond Service
sudo systemctl enable crond
sudo systemctl start crond
sudo systemctl status crond


Step 3 — Add Cron Job for Root User

Edit the root user’s crontab:

sudo crontab -e

*/5 * * * * echo hello > /tmp/cron_text





*/5	Every 5 minutes
*	Every hour
*	Every day of month
*	Every month
*	Every day of week