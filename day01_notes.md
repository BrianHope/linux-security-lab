What was day 1 for?

Day 1 was to set up a clean Linux lab, learn the filesystem structure, and understand why each directory matters for security.

Why does filesystem knowldege matter for security?

Knowing the filesystem helps to identify where evidnece, configuration, and sensitive data live. It allows me to investigate efficiently and prevent attackers from exploiting key directories.


Linux Filesystem Overview:

Root - 

Purpose: Root of everything. Compromises here give full control over the system.

/bin - Essential system binaries (ls, cp, rm). Access allows attackers to change the state of the machine and disrupt operations.

/sbin - Administrative Binaries (ip, mount). Access allows attackers to change the state of the machine and distrupt operations.

/etc - Configuration Files (user accounts). Misconfigurations or tampering can grant attackers unauthorized access.

/var - Variable files like logs and caches. Logs provide evidence of activity. First place to check in an incident response.

/home - User directories and personal files. Sensitive information can be stolen by attackers.

/tmp - Temporary files (installers files, runtime data, downloads). World writable and attackers can hide malicious file and run exploits.

/usr - Install software, libraries and supporting files. Compromised software can run malicious code.


Commands Used:

ls - List files/directories. Helps locate where things are in the file system.

cd - Moves between directories and is essential for navigating the file system.

tree - Shows file structure, helps understans hierarchy

pwd - Prints the working directory 


Reflection -

One thing that felt unfarmilar was all of the different directories and what kind of files live and operate inside of them. I think attackers would most likely try to hide files in /tmp because it's world writable and noisy.
