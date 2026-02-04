Linux Permissions:

1. File type (-, d, l)
2. Permissions (rw-, r--, r--)
3. Owner
4. Group
5. Size
6. Date
7. File/Dir name

Permission Triad:
1. Owner
2. Group
3. Other

Each file and directory gets r - read, w - write, x - execute


Why should logs be readable but not writeable?

Logs should be readable so that users can see what is happening on the system and they should not be writeable because they should not change or be tampered with.

Why should scripts be executable but not writable by everyone?

Scripts should be executable so that the user can physcially use the script to complete tasks and they should not be writable so the code is not altered.

Configurations files should be readable in order for users to be able to see how things are setup on the system but should be tightly controlled to prevent tampering.

Permission Visualization Drill:

ls -l /etc/passwd:

root is the owner of this file and everyone can read but only the owner can write to it

ls -l /etc/shadow:

root is the owner of this file and only the owner and group can read and only the owner can write 

ls -l /var/log:

most of these files are owned by root and syslog and mostly only the owner and group can read and the owner can write 
