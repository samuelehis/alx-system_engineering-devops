#!/bin/bash
Navigate into:
cd alx-system_engineering-devops/
mkdir 0x02-shell_redirections
cd 0x02-shell_redirections/

create a readme file 
-------------------------------
Now Let Start

------------------------------

Tasks

0. Hello World
mandatory
Write a script that prints “Hello, World”, followed by a new line to the standard output.

Answer:

#!/bin/bash' 

echo "Hello, World"

chmod u+x 0-hello_world
----------------------------------------------------------------

1. Confused smiley
mandatory
Write a script that displays a confused smiley "(Ôo)'.

Answer:
use a text editor for this
#!/bin/bash
echo "\"(Ôo)'"

chmod u+x 1-confused_smiley

----------------------------------------------------------

2. Let's display a file
mandatory
Display the content of the /etc/passwd file.

Answer:

#!/bin/bash
cat /etc/passwd

chmod u+x 2-hellofile

--------------------------------------------------------------------


3. What about 2?
mandatory
Display the content of /etc/passwd and /etc/hosts

Answer:

echo '#!/bin/bash' > 3-twofiles
echo 'cat /etc/passwd /etc/hosts' >> 3-twofiles

chmod u+x 3-twofiles

-----------------------------------------------------------------------

4. Last lines of a file
mandatory
Display the last 10 lines of /etc/passwd

Answer:

echo '#!/bin/bash' > 4-lastlines
echo 'tail -10 /etc/passwd' >> 4-lastlines
chmod u+x 4-lastlines

--------------------------------------------------------------------


5. I'd prefer the first ones actually
mandatory
Display the first 10 lines of /etc/passwd

Answer:

echo '#!/bin/bash' > 5-firstlines
echo 'head /etc/passwd' >> 5-firstlines
chmod u+x 5-firstlines

------------------------------------------------------------------------------

6. Line #2
mandatory
Write a script that displays the third line of the file iacta.

The file iacta will be in the working directory

You’re not allowed to use sed

Answer:

echo '#!/bin/bash' > 6-third_line
echo 'head -n 3 iacta | tail -n 1' >> 6-third_line
chmod u+x 6-third_line

-------------------------------------------------------------------------------------

7. It is a good file that cuts iron without making a noise
mandatory
Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line.


Answer:

echo '#!/bin/bash' > 7-file
echo 'echo "Best School" > '\*\\'\''"Best School"\'\''\\*$\?\*\*\*\*\*:)'' >> 7-file
echo chmod u+x 7-file

------------------------------------------------------------------------------------------------

8. Save current state of directory
mandatory
Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.

Answer:

echo '#!/bin/bash' > 8-cwd_state
echo 'ls -la > ls_cwd_content' >> 8-cwd_state
chmod u+x 8-cwd_state

-------------------------------------------------------------------------------------------------------

9. Duplicate last line
mandatory
Write a script that duplicates the last line of the file iacta

The file iacta will be in the working directory

Answer:

echo '#!/bin/bash' 9-duplicate_last_line
echo 'tail -1 iacta >> iacta' >> 9-duplicate_last_line
chmod u+x 9-duplicate_last_line

--------------------------------------------------------------------------------------------------

10. No more javascript
mandatory
Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders

Answer:

echo '#!/bin/bash' > 10-no_more_js
echo 'find -name "*.js" -type f -delete' >> 10-no_more_js
chmod u+x 10-no_more_js

-----------------------------------------------------------------------------------------------


11. Don't just count your directories, make your directories count
mandatory
Write a script that counts the number of directories and sub-directories in the current directory.

The current and parent directories should not be taken into account
Hidden directories should be counted

Answer:

echo '#!/bin/bash' > 11-directories
echo 'find -mindepth 1 -type d | wc -l' >> 11-directories
chmod u+x 11-directories

------------------------------------------------------------------------------------------------------------


12. What’s new
mandatory
Create a script that displays the 10 newest files in the current directory.

Requirements:

One file per line
Sorted from the newest to the oldest

Answer:

echo '#!/bin/bash' > 12-newest_files
echo 'ls -t | head -10' >> 12-newest_files
chmod u+x 12-newest_files

------------------------------------------------------------------------------------------------

13. Being unique is better than being perfect
mandatory
Create a script that takes a list of words as input and prints only words that appear exactly once.

Input format: One line, one word
Output format: One line, one word
Words should be sorted

Answer:

echo '#!/bin/bash' > 13-unique
echo 'sort | uniq -u' >> 13-unique
chmod u+x 13-unique

-------------------------------------------------------------------------------------------------------


14. It must be in that file
mandatory
Display lines containing the pattern “root” from the file /etc/passwd

Answer:

echo '#!/bin/bash' > 14-findthatword
echo 'grep root /etc/passwd' >> 14-findthatword
chmod u+x 14-findthatword

-------------------------------------------------------------------------------------------

15. Count that word
mandatory
Display the number of lines that contain the pattern “bin” in the file /etc/passwd

Answer:

echo '#!/bin/bash' > 15-countthatword
echo 'grep -c bin /etc/passwd' >> 15-countthatword

chmod u+x 15-countthatword

---------------------------------------------------------------------------------------------------

16. What's next?
mandatory
Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.

Answer:

echo '#!/bin/bash' > 16-whatsnext
echo 'grep -A 3 root /etc/passwd' >> 16-whatsnext
chmod u+x 16-whatsnext

------------------------------------------------------------------------------------------------------

17. I hate bins
mandatory
Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.

Answer:

echo '#!/bin/bash' > 17-hidethisword
echo 'grep -v bin /etc/passwd' >> 17-hidethisword
chmod u+x 17-hidethisword

------------------------------------------------------------------------------------------------------------------------------


18. Letters only please
mandatory
Display all lines of the file /etc/ssh/sshd_config starting with a letter.

include capital letters as well

Answer:

echo '#!/bin/bash' > 18-letteronly
echo 'grep '^[[:alpha:]]' /etc/ssh/sshd_config' >> 18-letteronly
chmod u+x 18-letteronly

-------------------------------------------------------------------------------------------

19. A to Z
mandatory
Replace all characters A and c from input to Z and e respectively.

Answer:

echo '#!/bin/bash' > 19-AZ
echo 'tr A Z | tr c e' >> 19-AZ
chmod u+x 19-AZ

--------------------------------------------------------------------------------------------------

20. Without C, you would live in hiago
mandatory
Create a script that removes all letters c and C from input.

Answer:

echo '#!/bin/bash' > 20-hiago
echo 'tr -d C | tr -d c' >> 20-hiago
chmod u+x 20-hiago

------------------------------------------------------------------------------------------------------------------------

21. esreveR
mandatory
Write a script that reverse its input.

Answer:

echo '#!/bin/bash' > 21-reverse
echo 'rev' >> 21-reverse
chmod u+x 21-reverse

---------------------------------------------------------------------------------------------------------------------------------------------------

22. DJ Cut Killer
mandatory
Write a script that displays all users and their home directories, sorted by users.

Based on the the /etc/passwd file

Answer:

echo '#!/bin/bash' > 22-users_and_homes
echo 'cut -d : -f 1,6 /etc/passwd | sort' >> 22-users_and_homes
chmod u+x 22-users_and_homes

--------------------------------------------------------------------------------------------------------------------------------------------


23. Write a command that finds all empty files and directories in the current directory and all sub-directories.

Only the names of the files and directories should be displayed (not the entire path)
Hidden files should be listed
One file name per line
The listing should end with a new line
You are not allowed to use basename, grep, egrep, fgrep or rgrep

Answer:

echo '#!/bin/bash' > 100-empty_casks
echo 'find . -empty -printf "%f\n"' >> 100-empty_casks
chmod u+x 100-empty_casks

--------------------------------------------------------------------------------------------------------------------

24. A gif is worth ten thousand words
#advanced
Write a script that lists all the files with a .gif extension in the current directory and all its sub-directories.

Hidden files should be listed
Only regular files (not directories) should be listed
The names of the files should be displayed without their extensions
The files should be sorted by byte values, but case-insensitive (file aaa should be listed before file bbb, file .b should be listed before file a, and file Rona should be listed after file jay)
One file name per line
The listing should end with a new line
You are not allowed to use basename, grep, egrep, fgrep or rgrep

Answer:

echo '#!/bin/bash' > 101-gifs
echo 'find . -name "*.gif" -type f -printf "%f\n" | rev |cut -d. -f2- | rev | LC_ALL=C sort -f' >> 101-gifs
chmod u+x 101-gifs

--------------------------------------------------------------------------------------------------------------------------

25. Acrostic
#advanced
An acrostic is a poem (or other form of writing) in which the first letter (or syllable, or word) of each line (or paragraph, or other recurring feature in the text) spells out a word, message or the alphabet. The word comes from the French acrostiche from post-classical Latin acrostichis). As a form of constrained writing, an acrostic can be used as a mnemonic device to aid memory retrieval. Read more.

Create a script that decodes acrostics that use the first letter of each line.

The ‘decoded’ message has to end with a new line
You are not allowed to use grep, egrep, fgrep or rgrep

Answer:

echo '#!/bin/bash' > 102-acrostic
echo 'echo $(cut -c1 | tr -d " \n")' >> 102-acrostic
chmod u+x 102-acrostic

----------------------------------------------------------------------------------------------------------------------------------------------------


26. The biggest fan
#advanced
Write a script that parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests.

Order by number of requests, most active host or IP at the top
You are not allowed to use grep, egrep, fgrep or rgrep

Answer:

echo '#!/bin/bash' > 103-the_biggest_fan
echo 'tail -n +2 | sort | cut -f1 | uniq -c | sort -g -r | head -11 | tr -s " " | cut -d" " -f3' >> 103-the_biggest_fan
chmod u+x 103-the_biggest_fan

---------------------------------------------------------------------------------------------------

			-=-=-=-=-=-  Success is Sure! -=-=-=-=-=-
		
	Name: Samuel Ehis
