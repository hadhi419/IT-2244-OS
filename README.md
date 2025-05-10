Description
On the 24th of March 2025, during Day 04 of the Operating Systems IT-2244 course, I worked with Linux date commands and shell script creation. The practical involved using various date commands to display the current date and time in different formats, including the day, year, weekday, month, hour, and minute. I also learned how to create and execute shell scripts to automate tasks and perform arithmetic operations. These exercises helped me understand how to interact with time-related data in Linux and how to use shell scripts for automation and performing basic operations.

Practical Steps

To begin, I viewed the calendar for the current month (March 2025) using the cal command. This displayed the calendar for the month, showing all the days and weeks of March 2025. I typed cal in the terminal and the output was:

March 2025
Su Mo Tu We Th Fr Sa
1 2 3 4 5 6 7
8 9 10 11 12 13 14
15 16 17 18 19 20 21
22 23 24 25 26 27 28
29 30 31

To display the current day of the month, I used the command date +%d. This command showed the current day, which was 24, as seen below:

24

To display the last two digits of the year, I used date +%y, which returned "25," the last two digits of the current year:

25

To display the full name of the current weekday, I used the command date +%A. This returned "Tuesday," as shown below:

Tuesday

Next, I displayed the abbreviated name of the weekday by using date +%a, which returned "Tue":

Tue

To display the abbreviated name of the current month, I used date +%b, which returned "Mar":

Mar

To display the full name of the current month, I used date +%B, which returned "March":

March

I then displayed the current month as a two-digit number using date +%m. This showed "03," as seen below:

03

To display the current minute as a two-digit number, I used date +%M. This returned "06":

06

I used date +%H to display the current hour in 24-hour format, which showed "11":

11

To display the abbreviated month name, which is the same as %b, I used date +%h, and it also returned "Mar":

Mar

Creating a Shell Script File (.sh)

A .sh file is a shell script used in Unix and Linux systems. It contains a series of commands written in shell languages like Bash, Zsh, or others. These scripts automate tasks, execute multiple commands sequentially, and can include loops, conditions, and functions.

Here’s how I created and executed a shell script:

I created a new file using the vi editor with the command vi prgrm1.sh.

I entered INSERT mode by pressing i and typed the following script to ask for the user's name and three numbers, calculate the sum and average, and then print the results:

echo "Who are you?"
read name
echo "Enter Number 1"
read x
echo "Enter Number 2"
read y
echo "Enter Number 3"
read z

sum=$(($x + $y + $z))
avg=$(($sum / 3))

echo "Hi" $name
echo "Summation " $sum
echo "Average " $avg

After typing the script, I saved and exited by pressing Esc, typing :wq, and hitting Enter.

To verify the file creation, I listed its details with ls -l prgrm1.sh.

I granted execution permissions using chmod 777 prgrm1.sh.

To confirm the updated permissions, I used ls -l prgrm1.sh and it displayed rwxrwxrwx, indicating that execution rights were granted.

Finally, I ran the script with ./prgrm1.sh. The output was as follows:

Who are you?
Adam
Enter Number 1
20
Enter Number 2
10
Enter Number 3
20
Hi Adam
Summation 50
Average 16

Reading Two Inputs from the User and Performing Arithmetic Operations Using Shell Script

I created another shell script named arithmetic.sh by typing vi arithmetic.sh.

I entered the following script:

echo "Enter Number 1"
read num1
echo "Enter Number 2"
read num2

add=$(($num1 + $num2))
sub=$(($num1 - $num2))
mul=$(($num1 * $num2))
div=$(($num1 / $num2))

echo "Addition $add"
echo "Subtraction $sub"
echo "Multiplication $mul"
echo "Division $div"

After saving the file, I granted execution permissions using chmod 777 arithmetic.sh.

I executed the script with ./arithmetic.sh, and the output was:

Enter Number 1
20
Enter Number 2
2
Addition 22
Subtraction 18
Multiplication 40
Division 10

Summary
This practical helped me gain a solid understanding of working with date commands and shell scripting in a Linux environment. I learned how to use the date command to display various date and time formats and how to create and execute shell scripts to automate tasks. By writing shell scripts that perform arithmetic operations and handle user inputs, I developed better scripting and automation skills. These tasks improved my ability to interact with the Linux command line and automate simple processes effectively.
