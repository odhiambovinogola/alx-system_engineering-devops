# describing what each script is doing
0. pwd - prints the absolute path name of the current working directory
1. ls - Display the contents list of your current directory
2. cd - changes the working directory to the user’s home directory
3. ls -l - Display current directory contents in a long format
4. ls -al - Display current directory contents, including hidden files in long format
5. ls -lna - Display current directory contents in:
	* Long format
	* with user
	* group IDs displayed numerically, And hidden files (starting with .)
6. mkdir /tmp/my_first_directory - creates a directory named my_first_directory in the /tmp/ directory
7. mv /tmp/betty /tmp/my_first_directory - Move the file betty from /tmp/ to /tmp/my_first_directory
8. rm /tmp/my_first_directory/betty - Delete the file betty.
	* The file betty is in /tmp/my_first_directory
9. rm -r /tmp/my_first_directory - Delete the directory my_first_directory that is in the /tmp directory
10. cd - = changes the working directory to the previous one
11. ls -al . .. /boot - lists all files (even ones with names beginning with a period character, which are normally hidden) in the current directory and the parent of the working directory and the /boot directory (in this order), in long format
12. file /tmp/iamafile -  prints the type of the file named iamafile. The file iamafile will be in the /tmp directory when we will run your script
13. ln -s /bin/ls __ls___ - a symbolic link to /bin/ls, named __ls__. The symbolic link should be created in the current working directory
14.  cp -u *.html .. - script that copies all the HTML files from the current working directory to the parent of the working directory, but only copy files that did not exist in the parent of the working directory or were newer than the versions in the parent of the working directory. consider that all HTML files have the extension .html
15. mv [[:upper:]]* /tmp/u - Create a script that moves all files beginning with an uppercase letter to the directory /tmp/u
16. rm *~ - script that deletes all files in the current working directory that end with the character ~
17. mkdir -p welcome/to/school - script that creates the directories welcome/, welcome/to/ and welcome/to/school in the current directory
18. ls -xamp - command that lists all the files and directories of the current directory, separated by commas (,).
	* Directory names should end with a slash (/)
	* Files and directories starting with a dot (.) should be listed
	* listing should be alpha ordered, except for the directories . and .. which should be listed at the very beginning
	* Only digits and letters are used to sort; Digits should come first
	* You can assume that all the files we will test with will have at least one letter or one digit
	* The listing should end with a new line
19.* 0 string SCHOOL School data
   * !:mime School
 - Create a magic file school.mgc that can be used with the command file to detect School data files. School data files always contain the string SCHOOL at offset0
