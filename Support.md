# Support

Contents

Strategy
Motto: Don't screw up. Back up.
We keep at least on months' worth of daily backups of the following systems:
Databases
Applications and relates assets
Code Repositories
Issue Management Database
Backup file location
Currently, all files are backed up into the directory /data/backups on server mapp01.
Backup file naming convention
[BACKUPDATE]_[ENVIRONMENT]_[DATATYPE]_[SERVER]_[ITEMNAME].[FILETYPE].bz2
Where:
[BACKUPDATETIME]
   The ISO date‐time in the format YYYYMMDDHHMMSS 
[ENVIRONMENT]
   The environment name that was backed up, e.g. PROD, TEST, etc... 
   If it is used for all environments, theni it is SYSTEM 
[DATATYPE]
   database, application, subversion/git repository 

[SERVER]

   The friendly server name that this was backed up from 
[ITEMNAME]
   database name, application domain, repository name 
[FILETYPE]
   Depending on the output of the backup file creator: sql, bak, tar, diff, log, dump 
bz2
   We save on diskspace and bandwidth by BZIP2‐compressing the backup file 
By default, backups are FULL backups. Difference­based or log­based backups are indicated in the
[FILETYPE] term.
Housekeeping of older Backup files
TODO
Vaulting of older Backup files
TODO

Performance Monitoring ­ 
Performance Monitoring
Contents

Basic tools for spot­checking system behaviour
This describes tools for observing and monitoring basic performance metrics. Correcting and fine­tuning are described
elsewhere.
HTOP Performance Monitoring Tool
HTOP does not come with the standard Red Hat distribution so it needs to be installed if not there already (described here:
Command: htop
Purpose: This utility displays the following useful metrics:
Server uptime
CPU usage
Memory usage
Details of currently­running processes
Usage: It is possible to arrange the order of display using the function key shortcuts. Hit F10 or ‘Q’ to quit.

Performance Monitoring ­ 
24­hour Historical Plots
The following performance plots are available and can be run directly from the command line on each of the servers. If you
have correctly connected with your X11 session open, the plots are visible on your desktop and you can scale then at will.
The data in the plots is based on samples taken in 5 minute intervals through a cron job and logged to the /var/log directory.
The cron job that creates the samples is set up on each server in the /etc/crontabfile:
SHELL=/bin/bash 
PATH=/sbin:/bin:/usr/sbin:/usr/bin 
MAILTO=sysadmin@matchi.biz 
HOME=/ 
# For details see man 4 crontabs 
# Example of job definition: 
# .‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐ minute (0 ‐ 59) 
# |  .‐‐‐‐‐‐‐‐‐‐‐‐‐ hour (0 ‐ 23) 
# |  |  .‐‐‐‐‐‐‐‐‐‐ day of month (1 ‐ 31) 
# |  |  |  .‐‐‐‐‐‐‐ month (1 ‐ 12) OR jan,feb,mar,apr ... 
# |  |  |  |  .‐‐‐‐ day of week (0 ‐ 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat 
# |  |  |  |  | 
# *  *  *  *  * user‐name command to be executed 
* * * * * /root/t.sh 
# Record processor loading every 5 minutes 
*/5 * * * * root /usr/bin/uptime | /bin/awk '{if($6=="min,"){print $11 $12 $13}else{print $10 $11 $12}}' | sed ‐e 's/,/ /g' | /usr/bin/xargs ‐I {} /bin/date +"\%m \%d \%H \%M {}" >> /var/log/uptime
# Record TCP Connections every 5 minutes 
*/5 * * * * root  /bin/netstat ‐nt | /bin/grep ESTABLISHED | /usr/bin/tail ‐n +3 | /usr/bin/wc ‐l | /usr/bin/xargs ‐I {} /bin/date +"\%m \%d \%H \%M {}" >> /var/log/connections
# Record memory consumption every 5 minutes 
*/5 * * * * root /usr/bin/free | /usr/bin/head ‐2 | /usr/bin/tail ‐1 | /bin/awk '{print $3/$2*100}' | /usr/bin/xargs ‐I {} /bin/date +"\%m \%d \%H \%M {}" >> /var/log/memory
# Record number of page faults 
*/5 * * * * root /usr/bin/vmstat | /usr/bin/head ‐3 | /usr/bin/tail  ‐n +3  | /bin/awk '{print strftime("\%m \%d \%H \%M", systime()) " " $7 " " $8}'  >> /var/log/pagefaults
There is also a corresponding log­rotate configuration in the /etc/logrotate.d/matchi, that creates a weekly archive, keeps
5 weeks of archives, and deletes anything older:
/var/log/pagefaults { 
  missingok 

Performance Monitoring ­ 
  notifempty 
  create 0640 madman adm 
  copytruncate 
  rotate 5 
  weekly 
} 
/var/log/connections { 
  missingok 
  notifempty 
  create 0640 madman adm 
  copytruncate 
  rotate 5 
  weekly 
} 
/var/log/memory { 
  missingok 
  notifempty 
  create 0640 madman adm 
  copytruncate 
  rotate 5 
  weekly 
} 
/var/log/uptime { 
  missingok 
  notifempty 
  create 0640 madman adm 
  copytruncate 
  rotate 5 
  weekly 
}
TCP connections
Command: showconnections.sh
Purpose: This shows the number of active TCP connections on the server. The sample data is held in
/var/log/connections.
Interpretation: This number of connections are not only Web connections, but can also include SSH connections. An
usual number or a spike in connections means that the server may be under a web­session attack or an SSH attack.
Relative CPU­loading
Command: showcpuloading.sh
Purpose: This shows the relative CPU­loading on the server. The sample data is held in /var/log/uptime.
Interpretation: Load averages are not normalized for the number of CPUs in a system, so a load average of 1 means
a single CPU system is loaded all the time while on a 4 CPU system it means it was idle 75% of the time. On a 6 CPU
server, when the load average is 1, it means that the CPU's are idle 83% of the time. The relative loads are averaged
over a sampling windows of 1 minute, 5 minutes and 15 minutes.
Memory Usage
Command: showmemory.sh
Purpose: This shows the relative memory consumption on the server. The sample data is held in /var/log/memory.
Interpretation: When memory usage is high, it may mean that there could be some run­away processes. This
processed can be identified using the htop command, if that is the case. Constanthigh­memory usage may lead to
page­faults. High memory usage tends to show up other system short­comings too. In principle, there is nothing
wrong with high memory usage ­ you paid for it, you should be able to use it after all.
Page­Faults

Command: showpagefaults.sh
Performance Monitoring ­ 
Purpose: This shows the number of page­faults being experienced at the time of the data sample. The sample data is
held in /var/log/pagefaults.
Interpretation: Page­faults happen when there is insufficient memory, or when the memory is too fragmented, to
allocate a contiguous block of memory when a process requests it. Some existing memory content is written to the
swap partition (on physical servers it is often an actual partition on a hard disk) and the freed up space is then used to
service the original memory request. This is a Swap­Out page­fault. Likewise, when the swapped­out memory is
written back into physical memory because it's owner process required, a Swap­In page­fault happens.

Technical FAQs & FIXES ­ 
Technical FAQs & FIXES
Contents

Database FAQs & FIXES
Overrun of group_concat string length
Symptom: Broken JSON expressions that the website can't process, or unclosed HTML tags on pages
that contain dynamic SQL­generated reports
Explanation: This may happen in views that do a group_concat to create comma­delimited strings or a
JSON string of row­data. By default, group_concat results are truncated to 1024 characters.
Affected areas: Database views called vwString_...
Remedy:
Edit the file /etc/my.cnf (as a sudo­er)
Add group_concat_max_len = 10K
Restart the mysql daemon: sudo /etc/init.d/mysqld restart
Extended Latin Characters are not correctly saved in the database
Symptom: Interesting artefacts are stored and displayed in string­type columns instead of the intended
characters
Explanation:
This may happen because the string­type columns is not set to a character set that can display such
characters. By default, we the use UTF­8 character set for all string data.
If the database is not set to UTF­8, then any new columns created in tables will assume the default
character set of the database.
Affected areas: String­type columns
Remedy:
Change the database to UTF­8 encoding:
ALTER DATABASE [database] CHARACTER SET utf8 COLLATE utf8_unicode_ci;
This operation can be performed on an active database without affecting its performance.
Edit the file /etc/my.cnf (as a sudo­er) to ensure that any future databases created are of the correct
character set and collation:

Technical FAQs & FIXES ­ 
[client] 
default‐character‐set=utf8 
[mysql] 
default‐character‐set=utf8 
[mysqld] 
init_connect='SET collation_connection = utf8_unicode_ci' 
character‐set‐server = utf8 
collation‐server = utf8_unicode_ci
Restart the mysql daemon: sudo /etc/init.d/mysqld restart
Change the offending string­type fields in each table to UTF­8:
alter table [tablename] modify column [columnname] [stringtype] character set utf8 collate utf8_unicode_ci;
Server FAQ & FIXES
BASH: Cannot allocate memory
Symptoms: You may encounter this error either on the console, a CRON report that has been emailed to
you, or in the system log files:
When running a command:
‐bash: fork: Cannot allocate memory
or in a CRON notification email:
/etc/cron.hourly/01restart_fsm_daemon_PROD.sh: fork: Cannot allocate memory 
Explanation: The Linux Kernel was not able to allocate memory to run a process. This is often the case
when a process repeatedly spawns itself and consumes a chunk of memory.
Affected Areas: Only the immediate server is affected. The impact of failed processes should be well
understood in order to recover any lost data.
Remedy: Check the memory consumption. Use the free ‐m command. There appears to be sufficient
memory:
$ free ‐m 
             total       used       free     shared    buffers     cached 
Mem:          8192       5001       3190          4          0       3656 
‐/+ buffers/cache:       1344       6847 
Swap:            0          0          0
Also look at the actual memory usage. This shows that there is still some memory left to go around:
$ sudo cat /proc/meminfo 
MemTotal:        8388608 kB                                                                                                
MemFree:         3264852 kB                                                                                                
Cached:          3744196 kB                                                                                                
Buffers:               0 kB                                                                                                
Active:          2724464 kB                                                                                                
Inactive:        2351060 kB                                                                                                

Technical FAQs & FIXES ­ 
Active(anon):     641136 kB                                                                                                                                                                     
Inactive(anon):   690192 kB                                                                                                                                                                     
Active(file):    2083328 kB                                                                                                                                                                     
Inactive(file):  1660868 kB                                                                                                                                                                     
Unevictable:           0 kB                                                                                                                                                                     
Mlocked:               0 kB 
SwapTotal:             0 kB 
SwapFree:              0 kB 
Dirty:               288 kB 
Writeback:             0 kB 
AnonPages:       1331328 kB 
Shmem:              4868 kB 
Slab:              48200 kB 
SReclaimable:       2588 kB 
SUnreclaim:        45612 kB
To see which process are consuming memory, run htop and order on the "MEM%" column.
In this case, it shows that the Java Virtual Machine may be to blame. The process that we know of that uses the
JVM on this particular server is the JIRA applicaiton, so restart the process:

Technical FAQs & FIXES ­ 
$ sudo /etc/init.d/jira stop 
executing using dedicated user 
                ..... 
          .... .NMMMD.  ... 
        .8MMM.  $MMN,..~MMMO. 
        .?MMM.         .MMM?. 
     OMMMMZ.           .,NMMMN~ 
     .IMMMMMM. .NMMMN. .MMMMMN, 
       ,MMMMMM$..3MD..ZMMMMMM. 
        =NMMMMMM,. .,MMMMMMD. 
         .MMMMMMMM8MMMMMMM, 
           .ONMMMMMMMMMMZ. 
             ,NMMMMMMM8. 
            .:,.$MMMMMMM 
          .IMMMM..NMMMMMD. 
         .8MMMMM:  :NMMMMN. 
         .MMMMMM.   .MMMMM~. 
         .MMMMMN    .MMMMM?. 
      Atlassian JIRA 
                   
Detecting JVM PermGen support... 
PermGen switch is supported. Setting to 384m 
If you encounter issues starting or stopping JIRA, please see the Troubleshooting guide at http://confluence.atlassian.com/display/JIRA/Installation+Troubleshooting+Guide
Server startup logs are located in /opt/atlassian/jira/logs/catalina.out 
Using CATALINA_BASE:   /opt/atlassian/jira 
Using CATALINA_HOME:   /opt/atlassian/jira 
Using CATALINA_TMPDIR: /opt/atlassian/jira/temp 
Using JRE_HOME:        /opt/atlassian/jira/jre/ 
Using CLASSPATH:       /opt/atlassian/jira/bin/bootstrap.jar:/opt/atlassian/jira/bin/tomcat‐juli.jar 
Using CATALINA_PID:    /opt/atlassian/jira/work/catalina.pid
Start the process again:
$ sudo /etc/init.d/jira start 
...
The process should now be running OK again without unduly consuming memory. Until it looses the plot
again.
Consider a further scenario:
Running htop again shows that another process may also be causing memory allocation failures. In this case it
is the Dropbox daemon:
Kill the offending process off using the kill ‐9 [process Id]­command. You can get the process Id by listing
all the processes with the ps ‐ef and piping it through a filter of the name of the process that you are looking
for, | grep dropbox. In this case, the process Id is 19031. When the process is killed, it is a good idea to confirm
that the process is actually terminated with a final ps ‐ef | grep dropbox, which should only return the process
of the grep­command itself:
$ ps ‐ef | grep dropbox 
madman   32569 15248  0 14:31 pts/1    00:00:00 grep dropbox 
$ kill ‐9 19031 
$ ps ‐ef | grep dropbox 
madman     317 15248  0 14:31 pts/1    00:00:00 grep dropbox
Finally checking with htop again, there are not processes left that consume memory.

Note
You can also kill processes off on HTOP itself by selecting the process from the list and hitting the  F9 ­key.
This works for when there is only one process to kill, but not when there is a run­away spawning of multiple
processes.
Technical FAQs & FIXES ­ 
Retry running the process
First record the current number of memory allocation failures / page faults:
madman@s16972617 mapp01 ~ $ sudo cat /proc/user_beancounters | head ‐3 
Version: 2.5 
       uid  resource                     held              maxheld              barrier                limit              failcnt
 73354475:  kmemsize                 42066418             43372544             50331648             58720256                  242
In this example, it is 242.
Restart the offending process and see if the number of page faults grows. If it does, another process may be at
fault.
Reboot a Server
You can reboot the server from the command line like this:
$ sudo shutdown ‐r now 
Broadcast message from madman@s16972617.onlinehome‐server.info 
        (/dev/pts/1) at 14:41 ... 
The system is going down for reboot NOW!
Since it is a virtual server, it should come up in about 30 seconds. Real ('tin') servers may take a little longer to
come backup.
Note
Remember to use the ‐r option, which will cause the server to come up again. If you inadvertently stopped the
server completely by using the ‐h option, then you can restart the server from the data centre's PLESK website.
Contents

HTPASSWD Password Protection
Requirement
Do this when a site needs an additional layer of access control before it can be accessed. It is done for all non­
production sites, so that not even search engines can access these. It is also done for the Administrator interface
on the production environment.
Set up
It is easiest to do this when logged in as user root.
$ sudo su ‐ 
[sudo] password for madman:
You are now logged in as root. Be carefull! Create a password file for the particular user or user group. In this
case, we create a password for user liberty and use matchi for the password. The name of file that holds this
user's credentials is htpasswd.liberty. In this example, we keep this as a separate file with simple login criteria,
since it is only for a temporary demo site for later tear­down.
$ cd /etc/httpd/conf 
$ sudo htpasswd ‐c htpasswd.liberty liberty 
New password: XXXXXX 
Re‐type new password: XXXXXXX 
Adding password for user liberty 
$ cat htpasswd.liberty 
liberty:YYYYYYYYYYYYY
Assign password to website
We also assign the sysadmin's password file to the ../administrator directory of the website, so that this part
remains reserved for internal systems use.

# nano httpd.conf
 ­ 
# DEMO SITE 
# demo.matchi.biz 
<Directory /var/www/vhosts/s16972616.onlinehome‐server.info/demo.matchi.biz> 
 Allow from all 
 AuthType Basic 
 AuthName "IP address logged." 
 AuthUserFile "/etc/httpd/conf/htpasswd.barclays" 
 Require valid‐user 
</Directory> 
# DEMO SITE ADMIN 
# demo.matchi.biz administrator 
<Directory /var/www/vhosts/s16972616.onlinehome‐server.info/demo.matchi.biz/administrator> 
 Allow from all 
 AuthType Basic 
 AuthName "IP address logged." 
 AuthUserFile "/etc/httpd/conf/htpasswd" 
 Require valid‐user 
</Directory>
Restart the Apache Server:
# /etc/init.d/httpd restart 
Stopping httpd:                                            [  OK  ] 
Starting httpd:                                            [  OK  ]
Remember to log out again:
# exit 
logout 
$
Enabling detailed Logging
Requirement
Do this to track errors on the website down.
{{Warning||Only do this on non­production environments since lots of logging can impact the server's
performance.}
Set up
In the Apache configuration file, /etc/httpd/conf/httpd.conf (for Red Hat), set the log level as follows:
LogLevel debug
Apply Changes
Restart the Apache server to actualize this change:
# /etc/init.d/httpd restart

View the Apache Error Log
 ­ 
# cd /var/log/httpd 
# tail ‐f error_log

Operational HOWTOs ­ 
Operational HOWTOs
Contents

Onboarding of New Staff
How to set up your new email account on your email client
Overview
We use GMAIL for our email hosting and many of our collaboration tools. New user accounts need to be
provisioned (at a cost) through the administrator interface in Google Apps.
Notes for Administrator
Create the user in the Google Apps Administrator console under "Üsers"
Auto­create the password

Operational HOWTOs ­ 
Send the email containing the login details to the new user's private email address
Summary of Email Configuration Settings
Email Address
Your email address is in the form: [firstname].[lastname]@matchi.biz
Your password will have been emailed to you to an existing email address.
IMAP Server
imap.gmail.com
Port 993
Connection Security: SSL/TLS
Authentication Method: Normal Password
User Name: [your full new email address]
Password: [your email password]
SMTP Server
You may already be using another SMTP server for sending emails from your other email accounts, but set this
one up too in The name of fields may differ slightly on your particular email client:
SMTP Server: smtp.gmail.com
Port: 465
Security: SSL/TLS
Authentication Method: Normal Password
User Name: [your nice and shiny new email address]
Password: [your email password]
Webmail: gmail.com
User Name: [your full new email address]
Password: [your email password]
What is my email address?
The convention we follow for email addresses is [firstname].[lastname]@matchi.biz, all lower­case, and no
middle name or initial unless required for disambiguation.
You should have received an email in your personal email account detailing your Matchi email address and the
default password.
Change your email password
You should have your initial password emailed to you to in your private email account. You can change your
password by logging in with your email address and password to gmail.com.
Setting up a Desk­top and Smart­phone email client
Most desktop email clients are supported. You may need to set your email account up to allow a lesser security
setting:
Log in to the web email at gmail.com
Click on this link: https://www.google.com/settings/security/lesssecureapps

Operational HOWTOs ­ 
Select the 'Turn on access for less secure apps' option.
You also need to enable IMAP access on your email account:
Log in to the web email at gmail.com (if not already done)
Click on thie link https://mail.google.com/mail/u/0/#settings/fwdandpop
Select the 'Enable IMAP' option
Hit the 'Save Changes' button
Create a WIKI account for the user
Log in as administrator on http://wiki.matchi.biz
Go to "Special Pages" and under "Login/Create Account" select the link "Create Account".
Select the option "Use a temporary random password and send it to the specified email address", and you
should be presented with a screen like this:

Fill in the fields and let the intended user set their own password: We use the simple convention of the login
being the user's first name in lower case.
Operational HOWTOs ­ 
Create a JIRA account for the user
Log in as administrator on http://jira.matchi.biz
Under the Admininstrator Menu, go to User Management (you may be prompted to confirm your login), and
select the "Invite Users" option.
Enter the user's email address and let the user complete their own registration.
You can assign the user to projects once the user has confirmed their invite.
Create a ZOHO account for the user
Not all new staff users require this. Note that each new account on ZOHO incurs the cost of approximately $10
per month.
Create a Matchi Website Operations account for the user
Not all new staff users require this.
Access to servers and databases is via Public/Private key­pairs.
Create and deploy a key­pair for Windows users
Creating the key­pair
Install the PuTTY suite of applications from
http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html
Run the PuTTYgen application

Operational HOWTOs ­ 
Generate a 2048­bit RSA keypair.
Save the private key in the Window user's home directory, subdirectory .ssh, as id‐rsa
Save the public key in the Window user's home directory, subdirectory .ssh, as id‐rsa.pub
Deploying the public key
Append the content of the public key to the file /home/madman/.ssh/authorized_hosts on the server to
which the user should have access to.
Offboarding of Staff
Equipment Return
Return all borrowed equipment. This may include:
Laptop & charger
Mobile Phone & charger
USB Storage devices
3G USB
Monitor, keyboard, mouse
Access card, keys and keyfob
Security Checklist for Leavers
For all Leavers
Email
Change the access password.
Set the email to reply with a _I don't work here anymore_ message
Set a forward to a nominated person
Do not delete the account for at least 6 months.
Calendar
Remove from all team calendars
Slack
ZoHo
Remove person from the Slack team list
Remove person from the Zoho users
EverNote
Remove person from the EverNote users
Intellectual Company Property
Leaver to demonstrate to a technical person that personal BYO laptop, mobile phone, portable USB storage

Operational HOWTOs ­ 
Contains no source code or documentation
Email account and all content is deleted on BYO laptop's email program
All working directories relating to Matchin projects are deleted
Leaver to acknowledge that no intellectual property is held anywhere else, such as at personal premises, other
devices or in the cloud
For Developer Leavers
Server Access
There should be one administration account to all servers (madman). Login should only be possible to via
public/private key pair and no via password. It is sufficient to remove the leaver's public key from the server's
key ring
Remove user's public key from all servers. Look for the leaver's key in the file
/home/madman/.ssh/authorized_keys and remove that line from the file. The file authorized_keys is in
this format:
ssh‐rsa [very long key string]== [user name]@[remote computername] 
...
Check all other accounts that may exist on the server, even though there should only be one user account.
Also check the root account for the existence of the file /root/.ssh/authorized_keys ­ it should not exist.
If it does, find out how it got there (was the /etc/ssh/sshd_config file altered?), preserve the evidence
and remove the file.
Source Repository Access
Remove the leaver's authentication criteria from /etc/svn‐auth‐users on the server that hosts the repository (at
the time of writing, it is mapp01). The file /etc/svn‐auth‐users is in this format:
[user]:[authentication key]. 
...

Sysadmin HOWTOs ­ 
Sysadmin HOWTOs
Contents

environment

Sysadmin HOWTOs ­ 

HOWTO Reboot a Server
When do we need to do this?
You would only ever need to reboot a server in the following situations:
When a server has run out of memory due to memory leakage which is caused by poor code
Too many open database sessions (attributable to poor code ­ you know who you are!)
Upgrading the kernel due to security issues.
Overview
There are a number of ways to reboot a server. Depending on the state that the servers is in, e.g. it may suffer
from a massive memory haemorrhage, not all methods to initiate a server reboot are possible:
SSH session: Issue the sudo reboot command
Virtuozzo Power Panel. This is only availalbe on virtual servers.
Plesk Control Panel. This is available on all types of servers that have Plesk is installed
Serial Console. This option is only available for physical servers
Hosting Administration Panel. This option is only available for physical servers
The duration of a server reboot and resumption of full service
For a virtual server is about 60 seconds
For a physical server is about 150 seconds
Note
If a server reboot takes much longer, you should inspect the server logs and determine why the reboot has taken
so long. And obviously remedy the issue.
Reboot via a SSH console session
$
Reboot via the Virtuozzo Power Panel
Go to the Virtuozzo Power Panel appliance through this URL: https://[server's IPv4 addres]/vz/cp. Log in as
user root and the Server Initial Password (see Infrastructure section for details).
Reboot via the Plesk Control Panel
Log into the Server's Plesk Control Panel and select the "Tools and Settings" option:

Sysadmin HOWTOs ­ 
In the "Server Management" box, select the "Restart Server" link:
Confirm the operation by clicking on Yes:
The browser window should immediately clear with an error message (depending on your browser). Be
sure to check that server has come up again by trying to reestablish the Plesk Constrol Panel session.

Reboot via the Serial Console
Sysadmin HOWTOs ­ 
$
Reboot via the Hosting Administration Panel
This method has some flaws, as it can not tell you whether the server was even running at all, or if the reboot
was successful.
Go to https://admin.1and1.co.uk and log in using the server's hosting account details.
Select the contract that relates to the server in question. Find the "Server Administration" block and
select "Recovery Tool":
Make the selections as below:

Sysadmin HOWTOs ­ 
Confirm your action:
Wait for a confirmation:

Sysadmin HOWTOs ­ 
HOWTO Upgrade a server's kernel
When do we need to do this?
As a guide, security improvements are main reason for upgrading a kernel. It is unlikely that you would need to
upgrade the kernel due to new features in the kernel or promises of performance improvements.
You can only upgrade the kernel of a physical server. You can not upgrade the kernel of a virtual server
yourself. If the kernel version of the virtual server is not satisfactory, then move to a physical server or wait for
the hosting provider to eventually upgrade the virtualizer's operating system.
Overview
In some cases after a kernel upgrade, it may be necessary to upgrade packages that are affected by a kernel
upgrade.
HOWTO Refresh a technical environment
When do we need to do this?
This is only necessary when a non­production environment needs to be aligned with the production
environment in order to to creates a baseline for a new tranche of development or testing.
You should not ever need to refresh the production environment from a non­production environment, as you
will loose recent data changes and potentially cause a production outage while doing this.
Overview
The following environments are accessible from the public internet ­ albeit that all but the PRODuction
environment are password protected:
PROD ­ Production. Visible to the public. https://matchi.biz
DEV ­ Development. Password protected. http://dev.matchi.biz
TEST ­ Test environment. Password protected. http://test.matchi.biz
MERGE ­ Code merge environment. Password protected. http://merge.matchi.biz
STARTUP ­ Code merge environment. Password protected. http://startup.matchi.biz
REPORT ­ Report Development environment. Password protected. http://report.matchi.biz
PERF ­ Performance Testing environment. Password protected and on a dedicated server.
http://perf.matchifranchizing.biz
Things you should know before proceeding:
Most of these environments are completely backed up every night.

Sysadmin HOWTOs ­ 
The subdomains have previously been created on the hosting provider's administrative interface
The non­production environments are hardly used.
Most environments are on the same server instance (for the time being), excepts for the performance
testing environment, which necessarily needs to be on a dedicated server.
The environments are based off the directory /var/www/vhosts/s16972616.onlinehome‐server.info on
server mweb01, and
/var/www/vhosts/s17502230.onlinehome‐server.info on server mfran01.
The performance environment is on a dedicated server and on a separate domain, so that it can benefit
from Cloudflare's Content Delivery Network (CDN) features.
The refresh date of the environment is always obvious from the name as it appears on a browser, and is in
the form [ENVIRONMENT [YYYYMMDD], e.g. TEST 20151114.
Refresh an environment
It is unlikely that you would ever need to refresh the production environment from another environment. It you
ever feel that this is required, think again!
The steps to refresh a target environment from a source environment are done on the web server (mweb01),
followed by a number of operations that are performed on the database server (mdb01).
In this example the source environment is the PRODUCTION environment, and the target environment is one
called TEST.
Backup the existing target environment's application
On the web server (mwebXX):
Take a current snapshot of the target environment's application in case you need to revert back to it it. In the
example here, the backup file is held in the HOME directory of the currently logged­in user and is a BZip­
version­2 compressed tape archive, i.e. a .tar.bz2 file. It is useful to include a datestamp in the name of the
backup file, in the form YYYYMMDD.
There are the available application directories:
$ cd /var/www/vhosts/s16972616.onlinehome‐server.info 
$ ls 
demo.matchi.biz 
dev.matchi.biz 
launch.matchi.biz   
matchi.org         
merge.matchi.biz 
report.matchi.biz 
startup.matchi.biz 
test.matchi.biz 
...
Create a snapshot of the TEST­environment's application:
$ tar ‐cjf  ~/test.matchi.biz.YYYYMMDD.tar.bz2  test.matchi.biz
Backup the existing target environment's database
On the database server (called mdbXX):

Take a current snapshot of the target environment's database in case you need to revert back to it it. In the
example here, the backup file is held in the HOME directory of the currently logged­in user and is a BZip­
version­2 compressed SQL dump, i.e. a .sql.bz2 file. A date stamp is included in the name of the backup file in
the ISO date format of YYYYMMDD.
Sysadmin HOWTOs ­ 
List all the databases:
$ mysql ‐e 'show databases' 
‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐+ 
| Database                | 
+‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐‐+ 
| information_schema      | 
| build_20140119          |                                                                                                                                                                                        
| build_20140325          |                                                                                                                                                                                        
| build_20140507          |                                                                                                                                                                                        
| build_20140725          |                                                                                                                                                                                        
| build_20150129          |                                                                                                                                                                                        
| build_20150731          |                                                                                                                                                                                        
| build_20151105          |                                                                                                                                                                                        
| demo_20150929           | 
| dev_20150129            | 
| dev_20150227            | 
| dev_20150316            | 
| dev_20150414            | 
| dev_20150623            | 
| dev_20150804            | 
| launch_20130906         | 
| merge_20140702          | 
| merge_20151029          | 
| multi_20141012          | 
| mysql                   | 
| perf_20150216           | 
| perf_20151110           | 
| startup_20140512        | 
| startup_20150129        | 
| startup_20150825        | 
| test_20150312           | 
| test_20150316           | 
| test_20150320           | 
| etc ....
Create a backup of the existing target environment's database, say, test_20150316, to
test_20150320_YYYYMMDD.sql.bz2, where YYYYMMDD is today's date:
$ mysqldump ‐‐routines  test_20150320 | bzip2 > test_20150320_YYYYMMDD.sql.bz2
Copy the Source environment's application to the Target environment
Remember that it is safer to first go to the target directory and to pull the content of the source directory into it.
First, clear all but the configuration files out of the target directory:
$ cd /var/www/vhosts/s16972616.onlinehome‐server.info/test.matchi.biz
Confirm that you are indeed in the target directory before proceeding:
$ pwd 
/var/www/vhosts/s16972616.onlinehome‐server.info/test.matchi.biz
So you are sure that you are in the correct directory? If so, remove all the directories from
/var/www/vhosts/s16972616.onlinehome‐server.info/test.matchi.biz

Sysadmin HOWTOs ­ 
$ find . ‐type d ‐exec sudo rm ‐fr {} 2>/dev/null \;
Copy the source content from the PRODuction environment to 'here'. You should remain in the
var/www/vhosts/s16972616.onlinehome‐server.info/test.matchi.biz directory and pull the content from the
source directory into the current target directory:
$ sudo cp ‐r ../matchi.biz/* . 
[sudo] password for madman:
Configure the new environment
There should be a pre­built configuration file for this environment ready, what needs to be altered slightly and
copied to the proper name. This file is called configuration.php.ENVIRONMENT, where ENVIRONMENT is the
environment name, e.g. test, dev, etc... In the case, we have the file configuration.php.test and edit the
following changes in it:
Change the name of the database ­ by convention, this holds today's date
Change the site name ­ by convention, this holds today's date in ISO form YYYYMMDD
$ sudo nano configuration.php.test 
  ... 
  public $sitename = 'TEST 20151129'; 
  ... 
  public $db = 'test_20151129'; 
  ...
Set the originator of emails sent from the website as follows:
  public $mailfrom = 'test.support@matchi.biz'; 
  public $fromname = 'Test Matchi.Biz Support'; 
  public $sendmail = '/usr/sbin/sendmail'; 
  public $smtpauth = '1'; 
  public $smtpuser = 'support@matchi.biz';
A non­production environment is likely to not have SSL (The exception to this may be for a pre­production
environment). Set the SSL flag to 0:
  ... 
  public $force_ssl = 0; 
  ...
Also confirm that you have the correct tmp and logs directories set up:
  ... 
  public $log_path = '/var/www/vhosts/[SERVERNAME].onlinehome‐server.info/[ENVIRONMENT]/logs'; 
  public $tmp_path = '/var/www/vhosts/[SERVERNAME].onlinehome‐server.info/[ENVIRONMENT]/tmp';   
  ...
To recap:
[SERVERNAME] is the server Id that allocated by the hosting provider
[ENVIRONMENT] is the name of the environment that you are busy creating
Some file manipulations are required to complete the system­level configuration:
Advise search engines to not search in this environment. robots.txt should just contain the following:

User‐agent: * 
Disallow: /
Sysadmin HOWTOs ­ 
Set the access control for all the files
$ sudo chown ‐R plesk:psaserv *
Save the changes to configuration.php:  Ctrl O ,  Ctrl X
Set up the database for the new environment
This is performed on the database server (mdb01).
Dump the production database to a file
The production database is named build_YYYYMMDD, where YYYYMMDD is the date the database was
instantiated for the first time, build_20151105. Do a complete database dump, including all stored procedures,
to a dump file, build_20151105_20151109.sql, where the second date is today's date.
$ mysqldump ‐‐routines  build_20151105 > build_20151105_20151129.sql
Create a new database instance
The target database is named ENVIRONMENT_YYYYMMDD, where YYYYMMDD is today's date.
mysql ‐e 'create database test_20151109'
Load the database dump into the new instance
Note the ­c option when importing the data as this prevents the comments in the stored procedures from getting
stripped out.
$ mysql ‐c test_20151109 < build_20151105_20151109.sql
Database Changes for non­production environments
The following changes need to be made to prevent both operations staff and external user from receiving
unwanted notifications, and for the end­to­end system behaviour to be consistent with the environment that it is
in.
Anonymize all external users' email addresses
This prevents accidental emails getting sent to real users. System users mostly have a user_id < 900. Members
who belong to the testing group (Group Id 22) should not have their email addresses mangled.
set @ENVIRONMENT='test'; 
update mtchi_users  
   set email = concat(substr(md5(id),1,10),'@[ENVIRONMENT].matchi.biz')  
 where id >= 900 
   and id not in (select user_id 
                    from mtchi_user_usergroup_map 

                   where group_id = 22 
                 )
Sysadmin HOWTOs ­ 
Replace '[ENVIRONMENT]' with the environment name so that non­production emails can be traced to their
origin.
The result is that you should have email addresses like this:
mysql> select email from mtchi_users where id > 900 limit 10; 
d045c59a90@matchi.biz 
043c3d7e48@matchi.biz 
4daa3db355@matchi.biz 
e820a45f1d@matchi.biz 
90794e3b05@matchi.biz 
b7892fb3c2@matchi.biz 
74bba22728@matchi.biz 
5c936263f3@matchi.biz 
1ce927f875@matchi.biz 
8065d07da4@matchi.biz
Add [ENVIRONMENT] prefix to all notification email subjects
To prevent any confusion when emails arrive from a non­production environment in a developer's and tester's
mail client (and the emails should not arrive on anyone else's mail client, BTW), the email's subject line should
be prefixed with the environment's name.
For example, when preparing a test environment, do this:
set @ENVIRONMENT='test'; 
update mtchi_inno_system_picklist_event_types 
   set subject = concat('[',upper(left(@ENVIRONMENT,1)),lower(substring(@ENVIRONMENT,2)),'] ',subject);
All system­emitted emails will now be prefixed with "[Test] ".
Warning
Remember that these records can't be worked back into the production environment again, now that they
permanently are tainted.
Un­Hide hidden Innovations and Organizations
Some test innovations and test organization exist on the production system but are marked as 'hidden' so that
they do not appear in any real searches to actual external users. These 'hidden' innovations and organizations
are useful for a test environment as it can save a tester from creating a Test Innovation or Test Organizations, so
can be 'un­hidden'. The 'is_hidden' flag needs to be reset on all innovations and organisations in the test
environment:
mysql> update mtchi_inno set is_hidden = 0 where is_hidden = 1; 
mysql> update mtchi_inno_organizations set is_hidden = 0 where is_hidden = 1;
Change System URL for the non­production environment
Set the URLs that are contained in system­generated notifications so that they point to the non­production
environments and exhibit the correct behaviour when tested:

Sysadmin HOWTOs ­ 
mysql> update mtchi_inno_config set value = 'http://test.matchi.biz' where param = 'SystemURL';
Change Email Notifications for the non­production environment
In any of the non­production environments, copies of system­generated notifications need to be sent to the test
email account instead of Zoho.
mysql> update mtchi_inno_config set value = 'test@matchi.biz' where param = 'NotificationDispatchOpsRecipients';
Set all Email Notifications Groups to the Test Group on the non­production environment
In any of the non­production environments, system­generated notifications that are sent to user groups need to
be sent to only members of the Test user group, Id=22.
mysql> update mtchi_inno_system_picklist_event_types set notificant_groups = 22 where notificant_groups is not null;
Set the Apache configuration for the environment
You should not need to make any changes, but if you have to, such as setting different password criteria, make
the changes here:
$ sudo nano /etc/httpd/conf/httpd.conf
Get Apache to re­read the configuration without having to restart the service:
$ sudo /etc/init.d/httpd graceful
Set the Environment Logo in the Template
To avoid any further ambiguity, it helps to also indicate in the site what environment it is. This is done:
The site name is set in the configuration.php file ­ see previous steps.
A modified Matchi logo is selected from the template configuration, as follows:
In the administrator panel in http://[ENVIRONMENT].matchi.biz/administrator, go to Extensions ­> Templates
­> Matchi Template ­> Features, and select the logo image images/MatchiBizLogo_TEST.png in the case of the
TEST environment.
HOWTO Server Maintenance
Keeping the server's patch level up to date
Update application packages
You can update all the packages on a server to the latest release:
$ sudo yum update

This lists all the packages that are upgraded or to be installed as a result of new dependencies.
Sysadmin HOWTOs ­ 
================================================================================================ 
 Package                          Arch     Version                            Repository   Size 
================================================================================================ 
Updating: 
 ...  
Transaction Summary 
================================================================================================ 
Install       3 Package(s) 
Upgrade     220 Package(s) 
Total download size: 285 M 
Is this ok [y/N]:  
Warning
An impact analysis should be performed before confirming the execution of the update.
Not all updates are good ­ even though they have been verified and tested by the trusted repositories such
as REDHAT, REMI, EPEL and others.
Some updates include new features or behaviours that may impact the stability of your existing
application.
The update can be processor intensive, and may even knock some existing processes out. Keep a watch on log
files for process that have been knocked out and be ready to restart them. It is best to perform any kind of
update during low server usage.
Updating the RKHUNTER file hashes
Update the file hashes of the new files on RKHUNTER, or you will get false alert emails that the server may
been compromised, similar to the following:
Subject: [rkhunter] Warnings found for s16972617 
Please inspect this machine, because it may be infected. 
Run this command to update the file hashes:
$ sudo rkhunter ‐‐propupd 
File updated: searched for 167 files, found 138
Update the Linux Kernel
This is currently managed by the providers of the server virtual hosting environment. In this type of
environment, it is not possible to update a Linux kernel. It is however possible to update the kernel on
dedicated servers (a.k.a. 'tin').
What kernel am I running?
Use this command to check the kernel version:
$ uname ‐r 

You can also see all the details of the operating system in one go:
Sysadmin HOWTOs ­ 
$ uname ‐a 
What Linux Distribution am I runing?
This is the vendor of the Linux distrubution:
 $ cat /etc/issue | head ‐1 
CentOS release 6.6 (Final)
HOWTO Joomla Framework and Component
Maintanance
Installation of New Third­Party Joomla Components
Pre­Production Testing
The installation of all third­party component should first be regression tested in a non­production environment.
Apart from a successful regression test outcome, the new component should also comply to the following
crtieria:
Flawless installation, with no error messages or warnings
Flawless un­installation, with no error messages or warnings
No impact on performance
The components is fit for purpose and performs the expected function adequately
Upgrading Third­Party Joomla Components
Pre­Production Testing
The upgrade of existing third­party components should be regression­tested on a pre­production environment
before it is deployed on the Production environment. Since many of the components in use are from third
parties, there is no guarantee that the behaviour and integration between one to the next version will be
consistent.
Upgrading Third­Party Joomla Components when upgrading the
Joomla Core Framework
Decision Criteria
It is useful to cross­reference component­provider's latest release notes (on their respective websites usually) to
verify if a component needs to be upgraded in line with a new Joomla Core Framework release. Some
components also announce on the Joomla Administrartor panel if they are due for an upgrade.
Pre­Production Testing

If so, the third­party component should also be upgraded at the same time and included in the regression test.
Upgrading Components and the Joomla Core Framework
Sysadmin HOWTOs ­ 
Decision Criteria
The same is true when the Joomla core needs to be updated, since this can cause third­party components to fail.
This is a frequently documented phenomenon where third­party components fail to stay in lock­step with the
Joomla core. If the third­party components fail to work with after an upgrade of the Joomla Core Framework
and no component upgrades are available, then the upgrade of the Joomla Core Framework should be
abandoned.
Pre­Production Testing
It is possible to reduce some of the regression testing effort by doing a code comparison between the AS­IS and
TO­BE versions. In some cases, a security patch for the Joomla Core consist of a few lines of code only. A
useful tool for comparing code between directories on a wholesale basis is the open­source Meld tool from
http://meldmerge.org and works on all OSs.
Special Security Step for all Upgrades and new Installations
All script files in the Joomla directory tree are set to read­only and owned by the Apache daemon for security
purposes. There is an hourly process, on the hour, that sets all script files in the Joomla directory tree to read­
only again if they were accidentally left writable by an installation procedure.
Therefore, before you can install a new component or upgrade an existing one, the directory needs to
momentarily be set to writable:
$ cd /var/www/vhosts/[servername]/matchi.biz 
$ sudo find  administrator bin cli components includes language layouts libraries media modules plugins templates \
 ‐not ‐path "*/cache*" ‐not ‐path "*.svn/*" ‐type f \( ‐name "*.php" ‐or ‐name "*.ini"  \) ‐exec chmod u+w {} \;  ‐print | wc ‐l
When the upgrade/installation is complete, remove the write­privileges again:
$ sudo find  administrator bin cli components includes language layouts libraries media modules plugins templates \
‐not ‐path "*/cache*" ‐not ‐path "*.svn/*" ‐type f \( ‐name "*.php" ‐or ‐name "*.ini"  \) ‐exec chmod u‐w {} \;  ‐print | wc ‐l
Since there are no process semaphores to mark that an installation is in progress, upgrades and installations
need to be done in the period between the hours, in case you are faced with an inexplicable upgrade/installation
failure.

