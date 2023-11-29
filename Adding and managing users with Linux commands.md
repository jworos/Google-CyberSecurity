DESCRIPTION

A new employee with the username researcher9 joins the organization where work. I have been tasked to add them to the system and continue to manage their access during their time with the organization.

ADDING A NEW USER

￼<img width="694" alt="Screenshot 2023-11-29 at 08 01 06" src="https://github.com/jworos/Google-CyberSecurity/assets/85462184/2365882f-3f57-4e8c-8bfd-41223d8f9878">


Since we have been tasked to add the new employee with username researcher9, I used the command show in the screenshot above:

In the first line, I used the pwd command to show my current working directory, in the second line, I used the “sudo useradd researcher9” to add the new user to the organisation’s system.

Lastly, I used the “sudo usermod -g research team researcher9” command to add the user to a primary group.

ASSIGNING FILE OWNERSHIP

I was also tasked to assign file ownership to the new user, I used the command in the screenshot below to carry out that task:
￼
<img width="694" alt="Screenshot 2023-11-29 at 08 10 48" src="https://github.com/jworos/Google-CyberSecurity/assets/85462184/32bda004-0e87-4e79-8aa2-cd8fff80c41f">

From the screenshot, I used the command “sudo chown researcher9 /home/researcher2/projects /project_r.t×t” assign ownership of the project_r.txt file to the user which was located in /home/researcher2/projects/project_r.txt

ADDING A USER TO A SECONDARY GROUP

A couple of months later, this employee's role at the organization has changed, and they are working in both the Research and the Sales departments, so I have been tasked to add the employee to a secondary group which was done in the screenshot below:

<img width="694" alt="Screenshot 2023-11-29 at 08 14 44" src="https://github.com/jworos/Google-CyberSecurity/assets/85462184/05d427e0-d69c-44a6-8361-fc5c1261ed8f">


In the first line of command, there was a typographical error on my part which prompted the command to give an error output, in the second line of code the error was corrected with the right one.

Using sudo “usermod -a -G sales team researcher9” I was able to add the user to an existing group without removing the employee from his primary group.

DELETING A USER

A year later, the user researcher9 decided to leave the company, I have been tasked to delete the user from the system.

<img width="694" alt="Screenshot 2023-11-29 at 08 28 11" src="https://github.com/jworos/Google-CyberSecurity/assets/85462184/2877b7db-d7be-40cd-9f66-9b96fe8f1851">


In the first line of code, I used the sudo “userdel researcher9” which returned an error. This error occurred because when you create a new user in Linux, a group with the same name as the user is automatically created and the user is the only member of that group. 

So I used the “sudo groupdel researcher9” which gave us the correct output.

SUMMARY

After a new employee was assigned a new username, I was tasked to adding the new user to the system, and to also add the user to a primary group called "research_team", after adding the user to the group, I was tasked to change the user's permission on files, this was done using the chown command.

A year later, the employee, decided to leave the company. I was tasked to remove his details from the system.
