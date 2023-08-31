# describing what each script is doing
0. su betty - switches the current user to the user betty
1. whoami - prints the effective username of the current user
2. groups - prints all the groups the current user is part of
3. sudo chown betty hello - changes the owner of the file hello to the user betty
4. touch hello - creates an empty file called hello
5. chmod u+x hello - adds execute permission to the owner of the file hello
6. chmod +114 hello - adds execute permission to the owner and the group owner, and read permission to other users, to the file hello 
