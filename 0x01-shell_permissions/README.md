chmod:

Description: chmod is used to change file permissions on Unix-based systems.
Options:
chmod +x <filename>: Adds execute permission to the file.
chmod -x <filename>: Removes execute permission from the file.
chmod u=rw,g=r,o=r <filename>: Sets read and write permissions for the owner, read permission for the group, and read permission for others.
Example: chmod +x script.sh will make the script.sh file executable.
sudo:

Description: sudo stands for "Super User Do" and allows authorized users to execute commands with elevated privileges.
Options:
sudo <command>: Runs the specified command with administrative privileges.
sudo -u <username> <command>: Runs the command as the specified user.
Example: sudo apt-get update will update the package repository with administrative privileges.
su:

Description: su stands for "Switch User" and allows you to switch to another user account.
Options:
su <username>: Switches to the specified user account.
Example: su john will switch to the user account named "john".
chown:

Description: chown is used to change the owner of a file or directory on Unix-based systems.
Options:
chown <new_owner> <filename>: Changes the owner of the file to the specified user.
Example: chown john file.txt will change the owner of file.txt to the user "john".
chgrp:

Description: chgrp is used to change the group ownership of a file or directory on Unix-based systems.
Options:
chgrp <new_group> <filename>: Changes the group owner of the file to the specified group.
Example: chgrp staff file.txt will change the group owner of file.txt to the group "staff".
id:

Description: id is used to display the user and group IDs of the current user.
Options: (No common options)
Example: id will display information about the current user's ID and group memberships.
groups:

Description: groups is used to display the groups a user belongs to.
Options: (No common options)
Example: groups john will show the groups that the user "john" is a member of.
whoami:

Description: whoami is used to display the username of the current user.
Options: (No common options)
Example: whoami will display the current user's username.
adduser and useradd:

Description: Both commands are used to add new user accounts on Unix-based systems. However, adduser is more user-friendly and interactive, while useradd is used in scripts or for advanced administration.
Options: (Several options available for both commands to specify user details, groups, home directory, etc.)
Example (adduser): adduser jennifer will interactively prompt to create a new user named "jennifer."
addgroup:

Description: addgroup is used to add a new group on Unix-based systems.
Options: (Several options available to specify group details)
Example: addgroup developers will create a new group named "developers."



chown options

Change the owner and/or group of each FILE to OWNER and/or  GROUP.
       With --reference, change the owner and group of each FILE to those
       of RFILE.

       -c, --changes
              like verbose but report only when a change is made

       -f, --silent, --quiet
              suppress most error messages

       -v, --verbose
              output a diagnostic for every file processed

       --dereference
              affect the referent of each  symbolic  link  (this  is  the
              default), rather than the symbolic link itself

       -h, --no-dereference
              affect  symbolic links instead of any referenced file (use‐
              ful only on systems that can change the ownership of a sym‐
              link)

       --from=CURRENT_OWNER:CURRENT_GROUP
              change the owner and/or group of each file only if its cur‐
              rent owner and/or group match those specified here.  Either
              may  be  omitted, in which case a match is not required for
              the omitted attribute

       --no-preserve-root
              do not treat '/' specially (the default)

       --preserve-root
              fail to operate recursively on '/'

       --reference=RFILE
              use  RFILE's  owner  and  group  rather   than   specifying
              OWNER:GROUP values

       -R, --recursive
              operate on files and directories recursively

       The following options modify how a hierarchy is traversed when the
       -R option is also specified.  If more than one is specified,  only
       the final one takes effect.

       -H     if  a  command line argument is a symbolic link to a direc‐
              tory, traverse it

       -L     traverse every symbolic link to a directory encountered

       -P     do not traverse any symbolic links (default)

       --help display this help and exit

       --version
              output version information and exit

       Owner is unchanged if missing.  Group is unchanged if missing, but
       changed  to  login  group if implied by a ':' following a symbolic
       OWNER.  OWNER and GROUP may be numeric as well as symbolic.
