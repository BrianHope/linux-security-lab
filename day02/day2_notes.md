The goal of day 2 was to understand how Linux enforces access control through permissions and ownership, and how misconfigurations in these mechanisms directly lead to security failures sich as privilege escalltion, data exposure, and service breakage. This day builds on filesystem knowldege from day 1 and establishes the foundation for understanding why systems fila silently and how attackers gain elevated access without exploiting vulnerabilities.


The Linux Permission Model - 

Owner - the account that owns the file
Group - a set of users with shared access
Other - all remaining users on the system

Each entity can have - 
r (read)
w (write)
x (execute)

Reading ls -l Output - 

-rw-r--r-- 1 user group 4096 file.txt

- regular file
- rw- owner can read and write
- r-- group can read
- r-- others can read
- user - file owner
- group - file group
- 4096 file size
- file.txt - file name and type

Understanding this output is crucial for diagnosing permission errors


Symbolic and Numeric mode can both be used to modify permissions

Read -4
Write - 2 
Execute - 1

chmod 640 secrets.txt

Owner - rw-
Group - r--
Other ---


Ownership vs Permissions:

Ownership determines who permissions apply to

Attackers prefer misconfigs because they are reliable, repeatable and rarely monitored

Most real world breaches succeed due to misconfiuration rather than missing patches.






