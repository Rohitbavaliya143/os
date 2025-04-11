# os
prtc
# write a shell script that uses a switch-case (case statement) to  
#let the user: 
#1️ Check if a file exists 
#2️ Check if a directory exists 
#3️ Check if a file is empty 
# Function to check if a file exists 
 
CODE 
check_file() { 
    echo "Enter the file name:" 
    read filename 
    if [ -f "$filename" ]; then 
        echo "File '$filename' exists." 
    else 
        echo "File '$filename' does not exist." 
    fi 
} 
 
# Function to check if a directory exists 
check_directory() { 
    echo "Enter the directory name:" 
    read dirname 
    if [ -d "$dirname" ]; then 
        echo "Directory '$dirname' exists." 
    else 
        echo "Directory '$dirname' does not exist." 
    fi 
} 
 
# Function to check if a file is empty 
check_empty_file() { 
    echo "Enter the file name:" 
    read filename 
    if [ -f "$filename" ]; then 
        if [ ! -s "$filename" ]; then 
            echo "File '$filename' is empty." 
        else 
            echo "File '$filename' is not empty." 
        fi 
    else 
        echo "File '$filename' does not exist." 
    fi 
} 
 
# Main menu using case statement 
echo "Choose an option:" 
echo "1. Check if a file exists" 
echo "2. Check if a directory exists" 
echo "3. Check if a file is empty" 
echo "4. Exit" 
read choice 
 
case $choice in 
    1) check_file;; 
    2) check_directory ;; 
    3) check_empty_file ;; 
    4) echo "Exiting..."; exit ;; 
    *) echo "Invalid option. Please enter a valid choice." ;; 
esac 
 
 
# Function to display digital clock and calendar 
show_clock_calendar() { 
    while true; do 
        clear  
        echo "======================================" 
        echo " DIGITAL CLOCK & CALENDAR " 
        echo "======================================" 
        echo ""     
        echo " Time: $(date +"%H:%M:%S")"         
echo " Date: $(date +"%d %B %Y")" 
#%d The two-digit day of the month padded with leading zeroes 
if applicable. Example: 09. 
#%B The full month name. Example: September. 
#%Y The four-digit year. Example: 2001. 
echo ""         
cal 
echo "" 
echo "======================================" 
sleep 1 # Wait for 1 second before updating 
done 
} 
# Call the function 
show_clock_calendar 
