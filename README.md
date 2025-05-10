Description
This practical session was conducted on the 16th of March 2025 as part of Day 02 of the Operating Systems IT-2244 course. The primary focus was on connecting to a Linux server using PuTTY, exploring fundamental Linux file and text manipulation commands, and managing file permissions. Additionally, we learned how to work with file attributes in the Windows Command Prompt. This hands-on experience deepened my understanding of both Linux terminal and Windows command-line environments.

Features:
Connecting to a Server with PuTTY
I launched PuTTY on a Windows system and entered the server’s IP address, 172.16.140.150, in the Host Name field. After clicking “Open,” a terminal session started. I logged in using a username and the password 789*asd (not visible during typing). Once authenticated, I successfully connected to the remote server and accessed the Linux command-line interface.

Navigating the Linux File System
I used the pwd command to confirm the current working directory, which was shown as /home/username.
The ls command listed the contents of the current directory.
Using ls -l, I viewed a detailed list of files and directories with metadata such as permissions, owner, size, and modification date.
With ls -a, hidden files (those beginning with a dot) were also displayed.
The command ls -ltr listed all files in long format, sorted by modification time from oldest to newest.
An example output showed:

A symbolic link to the bin directory: bin -> /home/kalaf/.local/bin

Two files: file.txt and abc.txt, with respective sizes and timestamps.

Creating and Editing Files
To create an empty file, I used the touch command with a filename such as abc.txt.
To open and edit files, I used the vi command followed by the filename. Inside the editor, I pressed i to enter insert mode and added content. For example, in a file named xyz.txt, I typed:
John 32 Engineer
Jane 22 Student
Bob 33 Doctor
Mary 25 Teacher
Alice 32 Nurse
To save and exit, I pressed the Escape key, typed :wq, and hit Enter.

Viewing File Contents
To view files, I used the more command with a filename like abc.txt, which displayed the content one page at a time.
To scroll through files both forward and backward, I used the less command, offering more navigation flexibility.

Creating and Searching CSV Files
I created a CSV file named pqr.csv using the vi editor.
To find this file later, I used the find command with the following pattern: find . -name "*.csv".
The output confirmed the file location as ./pqr.csv.

Counting Lines in a File
I used the wc -l command with the filename xyz.txt. The output returned:
6 xyz.txt
This indicated that the file had six lines.

Extracting Columns and Rows from a CSV File
To extract the second column from pqr.csv, I used the cut command with the delimiter set to a comma. The command returned the following values:
34
78
34
78

To extract the first and third columns from the same file, the command output was:
23,56
56,90
12,14
09,58

Using the awk command, I printed only the first column of pqr.csv. The result was:
23
56
12
09

Using Head and Tail to View Specific File Lines
The head -n 5 pqr.csv command displayed the first five lines of the CSV file:
23,34,56,78
56,78,90,34
12,34,14,67
09,78,58,32

Similarly, the tail -n 2 pqr.csv command showed the last two lines:
12,34,14,67
09,78,58,32

Extracting and Appending Data Between Files
To extract the second column from pqr.csv and append it to a new file called pqrNew.csv, I used a cut command with redirection. After executing the command, viewing pqrNew.csv returned:
34
78
34
78

In another task, I extracted the first three rows from pqr.csv using the head command and appended them to a file named rows.csv. Viewing rows.csv showed the contents as:
23,34,56,78
56,78,90,34
12,34,14,67

Understanding File Permissions
We explored Linux file permissions, which are categorized into read, write, and execute for three user groups: owner, group, and others.
Permissions are displayed as a 9-character string, for example: -rwxr-xr--
This means:

The owner has read, write, and execute permissions.

The group has read and execute permissions.

Others have only read permission.

Using octal (numeric) representation, permissions can be assigned more efficiently:

777: Full permissions for everyone

755: Full permissions for the owner; read and execute for others

644: Read and write for the owner; read-only for others

700: Full permissions for the owner; no access for anyone else

Windows Command Prompt Practical
Managing File Attributes with ATTRIB
In the Windows CMD environment, I practiced using the ATTRIB command to modify file attributes.
First, I created two files named abc.txt and xyz.txt.
To hide abc.txt, I set its hidden attribute.
To make the file visible again, I ran the command: ATTRIB -H xyz.txt
This action removed the hidden attribute from xyz.txt, making it visible again.

To protect a file from modification, I set it as read-only using the command: ATTRIB +R abc.txt
After applying this attribute, abc.txt could no longer be edited until the read-only status was removed.

Summary
This session was highly beneficial in developing my command-line skills across both Linux and Windows systems. I learned how to connect to a server using PuTTY, manipulate files and directories, retrieve and process data, and apply file permissions in Linux. Additionally, I gained insight into managing file visibility and edit protection using Windows Command Prompt. These exercises helped reinforce theoretical knowledge with practical experience, making me more confident in navigating and automating tasks in real-world operating system environments.
