# 0x02. Shell, I/O Redirections and filters

0. echo "Hello, World"

 Prints "Hello, World", followed by a new line to the standard output

1. echo "\"(Ôo)'"
	* Displays a confused smiley "(Ôo)'

2. cat /etc/passwd
	* Displays the content of the /etc/passwdfile

3. cat /etc/passwd /etc/hosts
	* Displays the content of /etc/passwd and /etc/hosts

4. tail -n 10 /etc/passwd
	* Displays the last 10 lines of /etc/passwd

5. head -n 10 /etc/passwd
	* Displays the first 10 lines of /etc/passwd

6. head -n 3 iacta | tail -n 1
	* Displays the third line of the file iacta

7. echo "Best School" > \\\*\\\\"'\"Best School\"\\'"\\\\\*\$\\\?\\\*\\\*\\\*\\\*\\\*\:\)
	* Creates a file named exactly \\\*\\\\"'\"Best School\"\\'"\\\\\*\$\\\?\\\*\\\*\\\*\\\*\\\*\:\) containing the test Best School ending by a new line

8. ls -la >> ls_cwd_content
	* Writes into the file ls_cwd_content the result of the command ls -la

9. tail -n 1 iacta >> iacta
	* Duplicates the last line of the file iacta

10. find . -type f -name "*.js" -delete
	* 	Deletes all the regular files with a .js extension that are present in the current directory and all its subfolders

11. find . -type d -not -name '.' | wc -l
	* Counts the number of directories and sub-directories in the current directory

12. ls -t1 | head -n 10
	* Displays the 10 newest files in the current directory

13. sort | uniq -u
	* Takes a list of words as input and prints only words that appear exactly once

14. grep -i "root" /etc/passwd
	* Displayes lines containing the pattern "root" from the file /etc/passwd

15. grep -c -i "bin" /etc/passwd
	* Displays the number of lines that contain the pattern "bin" in the file /etc/passwd

16. grep -i "root" -A 3 /etc/passwd
	* Displays lines containing the patter "root" and 3 lines after them in the file /etc/passwd

17. grep -i -v "bin" /etc/passwd
	* Displays all the lines in the file /etc/passwd that do not contain the pattern "bin"

18. grep -i "^[a-z]" /etc/ssh/sshd_config
	* Displays all lines of the file /etc/ssh/sshd_config starting with a letter

19. tr "A" "Z" | tr "c" "e"
	* Replaces all characters A and c from input to Z and e respectively

20. tr -d "cC"
	* Removes all letters c and C from input

21. rev
	* Reverses its input

22. cut -d ':' -f 1,6 /etc/passwd | sort
	* Displays all users and their home directories, sorted by users


100. find . -empty | rev | cut -d '/' -f 1 | rev

	* Finds all empty files and directories in the current directory and all sub-directories

101. find -type f -name "*.gif" | rev | cut -d "/" -f 1 | cut -d '.' -f 2- | rev | LC_ALL=C sort -f

	* Lists all the files with a .gif extension in the current directory and all its sub-directories

102. cut -c 1 | paste -s -d ''

	* Decodes acrostics that use the first letter of each line

103. tail -n +2 | cut -f -1 | sort -k 1 | uniq -c | sort -rnk 1 | head -n 11 | rev | cut -d ' ' -f -1 | rev

	* Parses web servers in TSV format as input and displays the 11 hosts or IP addresses which did the most requests 
