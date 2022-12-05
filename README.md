Write a script that prints “Hello, World”, followed by a new line to the standard output.



#!/bin/bash

echo "Hello, World"



Write a script that displays a confused smiley "(Ôo)'.

#!/bin/bash

echo "\"(Ôo)'"



Display the content of the /etc/passwd file.

#!/bin/bash

cat /etc/passwd



Display the content of /etc/passwd and /etc/hosts



#!/bin/bash

cat /etc/passwd /etc/hosts





Display the last 10 lines of /etc/passwd

#!/bin/bash

tail -n 10 /etc/passwd 



Display the first 10 lines of /etc/passwd

#!/bin/bash

head -n 10 /etc/passwd



Write a script that displays the third line of the file iacta.



The file iacta will be in the working directory



#!/bin/bash

head -n 3 iacta | tail -n 1



Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line.

#!/bin/bash

echo "Holberton School" > \\\*\\\\"'\"Holberton School\"\\'"\\\\\*\$\\\?\\\*\\\*\\\*\\\*\\\*\:\)



Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it



#!/bin/bash

ls -la > ls_cwd_content



Write a script that duplicates the last line of the file iacta



The file iacta will be in the working directory



#!/bin/bash

tail -n 1 iacta >> iacta



Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.

#!/bin/bash

find . -type f -name "*.js" -delete



Write a script that counts the number of directories and sub-directories in the current directory.



The current and parent directories should not be taken into account

Hidden directories should be counted



#!/bin/bash

find . -type d -not -name '.' | wc -l



Create a script that displays the 10 newest files in the current directory.



Requirements:



One file per line

Sorted from the newest to the oldest



#!/bin/bash

ls -t1 | head -n 10





Create a script that takes a list of words as input and prints only words that appear exactly once.



Input format: One line, one word

Output format: One line, one word

Words should be sorted

#!/bin/bash

sort | uniq -u



Display lines containing the pattern “root” from the file /etc/passwd

#!/bin/bash

grep -i "root" /etc/passwd



Display the number of lines that contain the pattern “bin” in the file /etc/passwd

#!/bin/bash

grep -c -i "bin" /etc/passwd



Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.



#!/bin/bash

grep -i "root" -A 3 /etc/passwd



Display all the lines in the file /etc/passwd that do not contain the pattern “bin”

#!/bin/bash

grep -i -v "bin" /etc/passwd



Display all lines of the file /etc/ssh/sshd_config starting with a letter.



#!/bin/bash

grep -i "^[a-z]" /etc/ssh/sshd_config



Replace all characters A and c from input to Z and e respectively.

#!/bin/bash

tr "A" "Z" | tr "c" "e"



Create a script that removes all letters c and C from input.

#!/bin/bash

tr -d "cC"



Write a script that reverse its input.



#!/bin/bash

rev



Write a script that displays all users and their home directories, sorted by users.



Based on the the /etc/passwd file

#!/bin/bash

cut -d ':' -f 1,6 /etc/passwd | sort
