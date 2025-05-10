Description

On the 28th of March 2025, during Day 05 of the Operating Systems IT-2244 course, I worked with Linux commands to manipulate CSV files, focusing on searching, extracting, sorting, and processing data. This practical session introduced me to using commands like grep, awk, and sort to perform various operations on CSV data. The exercise helped me understand how to work with structured data in Linux, automate data extraction, and apply sorting techniques for practical data analysis.

Practical Steps

To begin, I used the grep command to find all rows in the CSV file that contained the word "Engineering." This allowed me to locate the relevant rows where employees from the Engineering department were listed. The command returned the following rows:

102,Bob,25,50000,Engineering
105,Eve,28,60000,Engineering
108,Hank,32,68000,Engineering

The grep command searches for the word "Engineering" and returns any row containing that word.

Next, I determined the number of columns in the first row of the CSV file by using the awk command. By specifying the comma as a field separator, the command returned the number of columns, which was 5.

I then used awk again to count the number of columns in every row of the CSV file. This command processed each row and displayed the number 5 for all rows, confirming that each row in the CSV file has 5 columns.

To sort the rows by salary in descending order, I used the sort command. This command took the CSV file, sorted it based on the salary column (the 4th column), and returned the rows in reverse order (highest salary first). The output was as follows:

104,David,40,90000,HR
103,Charlie,5,80000,Data Science
106,Frank,38,75000,HR
107,Grace,27,72000,Data Science
110,Jack,31,71000,HR
101,Alice,30,70000,Data Science
108,Hank,32,68000,Engineering
109,Ivy,29,62000,Data Science
105,Eve,28,60000,Engineering
102,Bob,25,50000,Engineering

This sorting allowed me to organize the rows based on salary, with the highest salaries listed first.

I then sorted the rows by salary in ascending order (lowest salary first). Using the sort command with a numerical sort flag, the rows were arranged from the lowest salary to the highest:

102,Bob,25,50000,Engineering
105,Eve,28,60000,Engineering
109,Ivy,29,62000,Data Science
108,Hank,32,68000,Engineering
101,Alice,30,70000,Data Science
110,Jack,31,71000,HR
107,Grace,27,72000,Data Science
106,Frank,38,75000,HR
103,Charlie,5,80000,Data Science
104,David,40,90000,HR

In the final step, I performed a multi-level sort by sorting first by department and then by the name of the employees. The sorting was done in reverse order, which resulted in the following:

110,Jack,31,71000,HR
106,Frank,38,75000,HR
104,David,40,90000,HR
108,Hank,32,68000,Engineering
105,Eve,28,60000,Engineering
102,Bob,25,50000,Engineering
109,Ivy,29,62000,Data Science
107,Grace,27,72000,Data Science
103,Charlie,5,80000,Data Science
101,Alice,30,70000,Data Science

This command first sorted by the 5th column (Department) in reverse order, and when departments were the same, it sorted by the 2nd column (Name), also in reverse order.

Summary

This practical session helped me gain hands-on experience with Linux text-processing commands, particularly grep, awk, and sort, for manipulating structured data. I learned how to efficiently search for specific patterns within a file, calculate the number of columns in a row, and apply sorting based on different criteria like salary and department. Multi-level sorting showed me how to combine multiple sorting criteria to organize data more effectively. These skills are essential for analyzing and processing CSV data in a Linux environment, improving my ability to handle real-world data manipulation tasks.
