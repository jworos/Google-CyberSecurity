PROJECT DESCRIPTION

I work as a security professional at an organization, i work closely with to the research team.
The research team needs to update the permissions for some files and directories inside the "Projects" directory.
The current permissions, do not show the level of authorization that should be guven to the files.

My task is to update the permissions so as to keep the system secure.
I will perform the following tasks to complete this task:

CHECK FILE AND DIRECTORY DETAILS

The code below shows how I used Linux commands to navigate and check the file permissions.

<img width="745" alt="Screenshot 2023-11-27 at 09 49 10" src="https://github.com/jworos/Google-CyberSecurity/assets/85462184/bce358e8-97a1-435d-8716-f9bb74a31a04">

Firstly, I used the ls command to display the directories/files in the current directory I am in.
In the second line, I used the CD command to navigate in the "Projects" folder, in the third line, I used the ls command to display the directories and files in the "projects" directory.

Lastly, in the forth line, I used the ls -la command to display the permissions given to the files and directories in the project directory, it also shows that there is a hidden file with the name .project_x.txt.


DESCRIBE THE PERMISSIONS STRING

The 10-character string can be broken down to know what authorization each files have. 
This is the 10-character string: drwxrwxrwx

The first character 'd' means directory, if the first character is an hyphen '-', that means it is a file. The other 9 characters represent user, group, and other, where the 2nd - 4th character represents permissions for the user where r = read, w = write, x = execute. If the permission has an hyphen '-', it means the user does not have that specific permission.

The 5nd - 7th character represents permissions for group, while the 8nd - 10th character represents permissions for other.

Permission for each user needs to be set as required for everyone involved.

CHANGE THE FILE PERMISSIONS 

The organization has stated that they do not want other to have acces to write access to any of the files, so we have to check to confirm the file/directory that gave write access to other.

From the screen shot above, we can observe that project_k.txt has write access for other, so we have to change that permission.

<img width="698" alt="Screenshot 2023-11-27 at 18 26 50" src="https://github.com/jworos/Google-CyberSecurity/assets/85462184/935bfb33-3f82-4874-80ae-c71b153fa74a">

In the new screen shot above, after identifying the file (project_k.txt) with write permmission access given to other, I changed the permission of the file using the chmod o-w project_k.txt command, after running the command, I ran the ls -la command to show the files and their current permission, file permission change was done after the chmod command was given.

CHANGE FILE PERMISSIONS ON HIDDEN FILE
The team wants to locate a hidden file, and change the permissions so that no one can have write authority to the file, but user and group can have read authority.

I ran the chmod U-w.g-w.g+r .project x.txt, which removes write permission from user and group, then adds read permission to group. after running that command, I ran the ls -la command to confirm that the command was carried out correctly.

<img width="698" alt="Screenshot 2023-11-27 at 18 39 08" src="https://github.com/jworos/Google-CyberSecurity/assets/85462184/896a874c-2977-4584-a83b-8e8a6b48b6b5">


CHANGE DIRECTORY PERMISSIONS

The organizations wants only researcher2 to have access to the drafts directory, from the screenshot below, I ran the ls -la command to show all the files/directories in the directory, after locating the draft directory and its permission, I carried out the following command:

I ran the chmod g-× drafts, which removes execute permission for group to that directory, after running that command, I ran the ls -la command to confirm that the command was carried out correctly.

<img width="698" alt="Screenshot 2023-11-27 at 18 43 19" src="https://github.com/jworos/Google-CyberSecurity/assets/85462184/4dc72e1e-49a5-47f8-aec3-ddbfe0d07953">

SUMMARY

Using the ls -la command to identity the permissions of files/directories in the project folder of my organization, both hidden and not hidden, I was able to change the permissions given to different users who access multiple documents in this folder using the chmod command.
