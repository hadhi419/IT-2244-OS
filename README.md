#!/bin/bash

echo "------------------------------------"
echo "1. Get the Calendar and Date"
echo "------------------------------------"
# Expected Output:
# → Full calendar of the current month
# → Current day number
cal
date +%d

echo ""
echo "------------------------------------"
echo "2. Get the Student Name and Marks for 3 Subjects"
echo "------------------------------------"
# Example:
# Enter the name: John
# Enter the mark for subject1: 65
# Enter the mark for subject2: 75
# Enter the mark for subject3: 85
# Total: 225
# Average: 75
echo "Enter the name:"
read name
echo "Enter the mark for subject1:"
read mark1
echo "Enter the mark for subject2:"
read mark2
echo "Enter the mark for subject3:"
read mark3
total=$(($mark1 + $mark2 + $mark3))
average=$(($total / 3))
echo "Total: $total"
echo "Average: $average"

echo ""
echo "------------------------------------"
echo "3. Simple Calculator with Arithmetic Operations"
echo "------------------------------------"
# Example:
# Enter 2 numbers: 5 and 2
# Summation: 7
# Subtraction: 3
# Division: 2
# Multiplication: 10
echo "Enter the first number:"
read num1
echo "Enter the second number:"
read num2
sum=$(($num1 + $num2))
sub=$(($num1 - $num2))
div=$(($num1 / $num2))
mul=$(($num1 * $num2))
echo "Summation: $sum"
echo "Subtraction: $sub"
echo "Division: $div"
echo "Multiplication: $mul"

echo ""
echo "------------------------------------"
echo "4. Get the Day Based on User Input (1–7)"
echo "------------------------------------"
# Example:
# Enter the number: 3
# Output: Wednesday
echo "Enter the number:"
read num
if [ "$num" -lt 8 ]; then
  if [ "$num" -eq 1 ]; then
    echo "Monday"
  elif [ "$num" -eq 2 ]; then
    echo "Tuesday"
  elif [ "$num" -eq 3 ]; then
    echo "Wednesday"
  elif [ "$num" -eq 4 ]; then
    echo "Thursday"
  elif [ "$num" -eq 5 ]; then
    echo "Friday"
  elif [ "$num" -eq 6 ]; then
    echo "Saturday"
  elif [ "$num" -eq 7 ]; then
    echo "Sunday"
  fi
else
  echo "Invalid Number"
fi

echo ""
echo "------------------------------------"
echo "5. Verify Username"
echo "------------------------------------"
# Example:
# Enter username: kalaf
# Output: Username is correct/incorrect
echo "Enter username:"
read name
username=$(whoami)
if [ "$name" = "$username" ]; then
  echo "Username is correct"
else
  echo "Username is incorrect"
fi

echo ""
echo "------------------------------------"
echo "6. Compare Two Numbers"
echo "------------------------------------"
# Example:
# Enter two numbers: 6 and 9
# Output: 6 is less than 9
echo "Enter two numbers:"
read n1 n2
if [ "$n1" -gt "$n2" ]; then
  echo "$n1 is greater than $n2"
elif [ "$n1" -eq "$n2" ]; then
  echo "$n1 is equal to $n2"
else
  echo "$n1 is less than $n2"
fi

echo ""
echo "------------------------------------"
echo "7. Simple Calculator Using 'expr'"
echo "------------------------------------"
# Example:
# Enter the first number: 4
# Enter the second number: 2
# Output:
# Summation: 6
# Subtraction: 2
# Division: 2
# Multiplication: 8
echo "Enter the first number:"
read a
echo "Enter the second number:"
read b
sum=$(expr $a + $b)
sub=$(expr $a - $b)
div=$(expr $a / $b)
mul=$(expr $a \* $b)
echo "Summation: $sum"
echo "Subtraction: $sub"
echo "Division: $div"
echo "Multiplication: $mul"
