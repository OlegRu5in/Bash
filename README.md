# 📌 Bash

Bash is a versatile tool for performing various tasks, which in some cases allows you to avoid installing specialized software.
It allows you to read and run commands, execute scripts, work with files. 

I am happy to share some bash commands that I used to do tasks during my Quality Assurance studies. 

## Navigation

- [Working with files and directories](#task-1)
- [Editing files, checking and killing proccesses, working with websites](#task-2)

## Task 1

##### Working with files and directories
```bash
pwd                                   # Show current directory path
mkdir test1                           # Create a directory named test1
cd test1                              # Go to directory test1 
touch {1..3}                          # Create file 1,2 and 3 inside directory test1
ls                                    # Check directory test1 content 
cd                                    # Go home directory 
mkdir test2                           # Create directory test2 inside home directory
rmdir test2                           # Delete directory test2 
cd test1                              # Go back to directory test1
rm 2                                  # Delete file 2 
mkdir test3                           # Create directory test3
touch file{1..2}                      # Add two files to directory test3
cd ..                                 # Go back to parent directory
rmdir -rf test3                       # Delete directory test3  
mkdir test4                           # Create directory test4
mv ~/test1/{1,3} ~/test4              # Move files 1 and 3 from directory test1 to directory test4
echo line > 1                         # Add to file 1 three lines with the words line
echo line >> 1            
echo line >> 1
cat 1                                 # Check content of file 1
echo line > 3                         # Add three lines to file 3 with the words line
echo line >> 3
echo line >> 3
cat 1 3                               # Check contents of file 1 and file 3 at once
nano 1                                # Using one of the editors, replace all lines in file 1
press: ^\
enter (what we want to replace): line
enter (what we change to): 123
Choose to replace all: A
exit editor:^X
save changes: Y
```
## Task 2
##### Editing files, checking and killing proccesses, pinging websites
```bash
mkdir test3                                   # Create directory test3 
cd test3                                      # Open directory test3 
touch {4..6}                                  # Add three files 4, 5 and 6 to the test 3 folder
echo -e "row1\nrow2\nrow3\nrow4" > 4          # Add 4 lines row1, row2, row3, row4 to each file
echo -e "row1\nrow2\nrow3\nrow4" > 5          
echo -e "row1\nrow2\nrow3\nrow4" > 6 
grep -i"row2" 5                               # Find the line "row2" in file 5 
grep -R "row" .                               # Find the line "row" in the test3 directory
grep "row" -c 6                               # Count number of lines containing word "row" in file 6
find . -name 5                                # Find file 5 in test3 directory
find . -type f -name 5 -delete                # Using find command delete file 5
echo test > 4                                 # Using the echo command, add the word "test" to file 4
sed 's/test/fail/g' 4                         # Change the word "test" in file 4 to "fail"
echo test >> 4                                # Add the word "test" to file 4 so that the content is preserved
ps aux                                        # View all processes in the system
kill 666                                      # Kill process 666 in console
ping artsiomrusau.com                         # Check the availability of the website artsiomrusau.com using ping
ping -c 5 artsiomrusau.com                    # Send 5 packages to artsiomrusau.com  
curl https://petstore.swagger.io/v2/pet/      # Using GET and cURL command, get info about registered pets 
findByStatus/?status=available,sold,pending              
curl -H 'Content-Type: application/json'      # Using POST and cURL command, create a new user at petstore
--data '{"id":6568,"username":"Ivan",
"firstName":"Ivan","lastName":"Ivanov",
"email":"ivanovii@gmail.com","password":"12345",
"phone":"+123456789","userStatus":"0"}' 
https://petstore.swagger.io/v2/user
```

