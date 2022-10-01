# 10 LINUX COMMANDS
## SSH
Login into a remote Linux machine.

        ### SSH
        SSH username@ip-address of hostname

## whois
Shows whois information about the given domain such as registrar info, registrant info, admin info if available.

        ## To display available information of apple.com
        whois apple.com

## host
Performs IP lookup for the domain name or vice-versa.

        ## Displays IP address of apple.com
        host apple.com

        ## Displays domain name of 17.253.144.10
        host 17.253.144.10

## date
Displays date and time of the system.

        ## Displays date and time of the system
        date

        ## Displays date and time of 5 days ago
        date --date="5 days ago"

        ## Similarly, displays date and time of 10 seconds ago 
        date --date="10 seconds ago"

## cal
Displays calender.

        ## Displays the current month with day highlighted
        cal

        ## Displays the third month of 1997
        cal 03 1997

## grep
Search for pattern in given file.

        ## Searches and displays lines containing string "linux" in file.txt
        grep "linux" file.txt

        ## Searches and displays lines containing string "linux" in files in directory dir
        grep -r "linux" dir

        ## Searches for the exact word "linux" in file.txt
        grep -w "linux" file.txt

        ## Ignores the case while searching
        grep -i "linux" file.txt

## useradd
Add new users. 

        ## Add new user named friends
        sudo useradd friends

        ## Set password for friends
        sudo passwd friends

        ## Specify userid 3001, group as users while adding user
        sudo useradd -u 3001 -g users osakue

        ## Create user with expiry date as 2021-02-30
        sudo useradd -e 2021-02-30 osakue

        ## Check Account/Password expiry dates for osakue
        sudo chage -l osakue

## userdel
Delete users.

        ## Delete user named friends
        sudo userdel friends

        ## Delete user friends and it's home directory
        sudo userdel -r friends

## top
Displays in real time all the running process along with CPU usage, Memory usage, Priority, CPU time.

        ## You can press q to exit from the display
        top

## free
Returns the memory status (RAM)

        ## Outputs the memory status in kilobytes
        free

        ## Outputs the memory status in gigabytes or you can use -m for megabyte, -b for byte
        free -g