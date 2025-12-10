## Linux Concepts

###### 1. grep command
###### 2. sed command
###### 3. awk command
###### 4. cut command

#### 1. grep (Global Regular Expression Print)

A command-line tool used to search for lines that match a given pattern in files or input. It supports regular expressions and is commonly used for filtering.

| **Command / Option**       | **Description**                                                  | **Example**                                     |
| -------------------------- | ---------------------------------------------------------------- | ----------------------------------------------- |
| grep "Keyword" Filename   | Searches the keyword/pattern in a given file.                    | grep "Keyword" Filename                        |
| grep -i                   | Searches the keyword and ignores case sensitivity.               |  grep -i "neha" Filename                        |
| grep -v                   | Shows all lines except the searched keyword.                     | grep -v "Neha" Filename                       |
| grep -c                  | Shows how many times a word appears in the file.                 | grep -c "Neha" Filename                        |
| grep -w                   | Searches for the exact word.                                     | grep -w "Nehanya" Filename                     |
|  grep -n                  | Shows matching lines with line numbers.                          | grep -n "Neha" Filename                        |
| grep "Keyword"            | Searches for a keyword in single or multiple files.              | grep "Brother" Filename1 Filename2             |
| grep -h                  | Searches keyword but hides the filename in output.               | grep -h "Brother" Filename1 Filename2          |
| grep -e                  | Searches multiple keywords in a single file.                     | grep -e "Neha" -e "Pooja" Filename            |
| grep -e (multiple files) | Searches multiple keywords in multiple files.                    | grep -e "Neha" -e "Pooja" Filename1 Filename2  |
| grep -l                   | Shows only filenames that contain the keyword.                   |  grep -l "Jack" Filename1 Filename2 Filename3   |
|  grep -lr                 | Searches recursively in files/directories.                       |  grep -lr "Brother"                            |
| grep -f                  | Searches many keywords stored in another file.                   | grep -f Names Filename                        |
| grep "^Keyword"          | Prints lines starting with the keyword.                          |  grep "^My" Filename                           |
| grep "Keyword$"           | Prints lines ending with the keyword.                            | grep "India$" Filename                         |
| grep -R                  | Searches a keyword recursively in all files of a directory.      |  grep -R "Jerry"                               |
| grep -q                   | Quiet mode—does not print output; use `echo $?` to check status. | grep -qR "Rachel" Friends/                    |

#### 2. sed 
A stream editor used to modify text using patterns—commonly for search/replace, deleting or inserting lines, and batch editing text without opening the file manually.

| **Description**                                                                     | **Command / Text**                                                                                                                                               | **Example**                                    |
| ----------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------- |
| How to change one name to another name?                                             | sed ‘s/Suraj/Surendra/g’ data                                                                                                                                    | sed ‘s/Suraj/Surendra/g’ data                  |
| How to show only a given line or range of lines?                                    | sed -n '1p' file_name <br> sed -n '1,5p' file_name <br> sed -n '$p' file_name → last line                                                                        | sed -n '1,5p' file_name                        |
| How to see all the users from India Country?                                        | sed -n '/India/p' file_name <br> Sed -n ‘/50000/p’ data —--> For salary                                                                                          | sed -n '/India/p' file_name                    |
| How to use multiple expression in sed command?                                      | Example: If you wanna only see 2 and 5th line <br> sed -n -e '2p' -e '5p' file_name                                                                              | sed -n -e '2p' -e '5p' file_name               |
| How to see all the users from India and Germany?                                    | sed -n -e '/India/p' -e '/Germany/p' file_name                                                                                                                   | sed -n -e '/India/p' -e '/Germany/p' file_name |
| How to see next 4 lines from 2nd line?                                              | sed -n ‘2,+4p’ file_name                                                                                                                                         | sed -n ‘2,+4p’ file_name                       |
| How to see every 2nd line from first line?                                          | sed -n ‘1~2p’ file_name —->Even line number                                                                                                                      | sed -n ‘1~2p’ file_name                        |
| How to read expression from external file?                                          | sed -f ex_file file_name                                                                                                                                         | sed -f ex_file file_name                       |
| How to replace a word in a file and show?                                           | sed 's/<string_to_change>/<new_string>/g' file_name                                                                                                              | sed 's/old/new/g' file_name                    |
| How to replace a word in a file and show except a given line or only in given line? | sed '5 s/<string_to_change>/<new_string>/g' file_name —> Change Name <br> sed '5! s/<string_to_change>/<new_string>/g' file_name —> doesn’t change have (!) sign | sed '5 s/old/new/g' file_name                  |
| How to replace a word and and edit in your file?                                    | sed -i's/<string_to_change>/<new_string>/g' file_name                                                                                                            | sed -i 's/old/new/g' file                      |
| How to change salary or country of a user (Paul)?                                   | sed '/Paul/ s/25000/35000/g' file_name <br> sed '/Paul/ s/India/US/g' file_name <br> sed ‘s/56000/70000/g’ data —> All change                                    | sed '/Paul/ s/25000/35000/g' file_name         |
| How to delete a line?                                                               | sed '1d' file_name (to delete first line) <br> sed '1,2d' file_name <br> sed '$d' file_name                                                                      | sed '1d' file_name                             |
| How to delete user from India country?                                              | sed ‘/India/d’ file_name                                                                                                                                         | sed ‘/India/d’ file_name                       |
| How to delete empty line?                                                           | sed '/^$/d' file_name                                                                                                                                            | sed '/^$/d' file_name                          |
| How to replace tab with space?                                                      | sed 's/\t/ /g' file_name                                                                                                                                         | sed 's/\t/ /g' file_name                       |
| How to copy output of sed command in separate file?                                 | sed -n ‘/India/ w new_file_name’ file_name                                                                                                                       | sed -n ‘/India/ w new.txt’ file_name           |
| How to add new line after a given line no.?                                         | sed '5 a new_text' file_name                                                                                                                                     | sed '5 a new_text' file_name                   |
| How to add new line after a given string, so it will add text after Paul?           | sed '/Paul/ a new_text' file_name                                                                                                                                | sed '/Paul/ a new_text' file_name              |
| How to edit existing line instead of adding new line?                               | sed '5 c new_text' file_name                                                                                                                                     | sed '5 c new_text' file_name                   |
| How to add new line before a given string, so it will add text before Paul?         | sed '/Paul/ i new_text' file_name                                                                                                                                | sed '/Paul/ i new_text' file_name              |
| How to see the hidden characters?                                                   | sed -n 'l' file_name                                                                                                                                             | sed -n 'l' file_name                           |
| How to wrap your file content with given no. of characters?                         | sed -n 'l 50' file_name                                                                                                                                          | sed -n 'l 50' file_name                        |
| How to read content from a file and use in our command?                             | sed '3 r externalfile' file_name                                                                                                                                 | sed '3 r externalfile' file_name               |
| How to stop execution of sed command as soon as first occurance found?              | sed ‘/India/ q’ file_name <br> sed ‘5 q’ file_name (stop execution at line 5)                                                                                    | sed ‘/India/ q’ file_name                      |
| How to provide exit status for your sed command?                                    | sed ‘/India/ q 100’ file_name                                                                                                                                    | sed ‘/India/ q 100’ file_name                  |
| How to execute external command line date in your expression?                       | sed '2 e date' file_name                                                                                                                                         | sed '2 e date' file_name                       |
|
| How to see the line number in file?                                                 | sed '=' file_name                                                                                                                                                | sed '=' file_name                              |
|                                                                                     | sed -n -e '/TEST/=' app.txt                                                                                                                                      | sed -n -e '/TEST/=' app.txt                    |

#### 3. awk
A powerful text-processing and pattern-scanning language used to filter data, extract fields, and perform calculations or complex transformations on text (especially columnar data).

| **Description**                                              | **Command**                                          | 
| ------------------------------------------------------------ | ---------------------------------------------------- | 
| How to see column 2 or 3?                                    | awk '{print $2}' file_name                           | 
| How to see multiple coulumns?                                | awk '{print $2,$3}' file_name                        | 
| How to see last column?                                      | awk '{print $NF}' file_name                          | 
| How to see line no.?                                         | awk '{print NR}' file_name                           | 
| How to see line no. with - ?                                 | awk '{print NR "- " $2}' file_name                   |
| How to get a column from CSV?                                | awk -F, '{print $7}' country.txt                     | 
| How to change the salary of Pol?                             | awk '{if($2=="Pol"){$3="90000"} print $0}' file_name | 
| How to see data of users whose salary is more than 40000?    | awk '{if($3>40000) print $0}' file_name              |
| How to see a line whose length of character is more than 15? | awk 'length($0)>15' file_name                        |
| How to see data of Indian users?                             | awk '/India/ {print}' file_name                      | 
| How to see a specific line example 3rd line?                 | awk 'NR==3 {print}' file_name                        |
| How to see range of lines, 3 to 5th line?                    | awk 'NR==3,NR==5 {print}'                            |
| How to see which lines are empty?                            | awk 'NF==0 {print NR}' file_name                     |
| How to check no. of lines in the file?                       | awk 'END {print NR}' file_name                       | 
| How to use for loop in AWK command?                          | awk 'BEGIN {for(i=0;i<=10;i++) print i;}'            |                                          
| How to use while loop in AWK command?                        | awk 'BEGIN {while(i<10){ i++; print "Num is " i;}}'  |  

#### 4. cut 
A command used to extract specific sections of each line of input—usually extracting columns or character ranges based on delimiters.

| **Description**                                      | **Command**                                    | 
| ---------------------------------------------------- | ---------------------------------------------- | 
| How to see only 2nd char?                            | cut -c2 file_name                              | 
| How to see 1 to 4 char?                              | cut -c1-4 file_name                            |
| How to see only 2 and 4th char?                      | cut -c2,3 file_name                            | 
| How to see data from CSV?                            | cut -d: -f 3 file_name                         |
| How to change the delimeter of output?               | cut -d, -f 1- country.txt --output-delimiter=" | 
| How to use cut command with other commands like cat? | Using pipe |                                   | 
