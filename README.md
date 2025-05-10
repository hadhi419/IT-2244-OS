Description
On the 21st of March 2025, during Day 03 of the Operating Systems IT-2244 course, I worked with Tab-Separated Values (TSV) files in Linux. The practical involved creating TSV files, extracting specific columns using cut and awk, displaying rows, counting fields and lines, and searching for content. I also used grep to filter specific data within the file. These exercises helped me improve my data manipulation skills and my understanding of working with files in a Linux environment.

Practical Steps
To begin, I created a TSV file named abc.tsv by using the vi text editor. I typed vi abc.tsv to open the editor, pressed i to enter insert mode, and entered the sample data:

11 22 44 55
88 99 77 55
22 66 00 33
11 22 77 88

After typing the data, I pressed Esc, typed :wq, and hit Enter to save and exit the editor, thus creating the file abc.tsv.

Extracting Columns from the TSV File
To extract the first column from the TSV file, I used the cut command with the following syntax: cut -d $'\t' -f1 abc.tsv. This command extracts the first column, resulting in the following output:

11
88
22
11

To extract the third column using awk, I ran the command awk '{print $3}' abc.tsv, which returned:

44
77
00
77

Displaying Rows from the TSV File
To display the first two rows, I used the head command with the argument -n 2 (i.e., head -n 2 abc.tsv). This displayed the first two rows:

11 22 44 55
88 99 77 55

For the last two rows, I used the tail command with the argument -n 2 (i.e., tail -n 2 abc.tsv). This command displayed the last two rows:

22 66 00 33
11 22 77 88

To display the fourth row, I combined head -n 4 abc.tsv and tail -n 1 to show the fourth line:

11 22 77 88

Displaying Entire File Contents
To display all lines of the TSV file, I used awk '{print}' abc.tsv. This command printed every line of the file:

11 22 44 55
88 99 77 55
22 66 00 33
11 22 77 88

Counting Fields and Lines
To determine how many fields (columns) were in the first line, I used the awk command with {print NF; exit} to count the fields, which returned 4 since there are 4 columns:

4

To count the total number of lines in the file, I used the command wc -l abc.tsv, which gave the output:

4 abc.tsv

Searching for Specific Content
To display lines containing '88' from the first five lines, I used the head and grep combination: head -n 5 abc.tsv | grep '88'. The command filtered and returned the lines containing '88':

88 99 77 55
11 22 77 88

Counting Fields Using Tab Separator in awk
To count the number of fields using tab as the separator, I used awk -F '\t' '{print NF; exit}' abc.tsv. This returned the number of fields (columns) in the file:

4

Summary
This practical gave me a solid understanding of working with Tab-Separated Values (TSV) files in a Linux environment. I learned how to create TSV files, extract and display specific columns and rows, count fields and lines, and search for content using various Linux commands like cut, awk, head, tail, wc, and grep. These tasks helped me improve my ability to handle structured data and process files efficiently from the command line.
