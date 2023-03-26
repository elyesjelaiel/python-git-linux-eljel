# Exercice 1

1. Go to the root directory
``` cd / ```

2. Display the content of the current (root) directory
``` ls / ```

3. Check your current location
``` pwd ```

4. Try to create a directory named test
``` sudo mkdir test ```

5. Go to the general home directory (should contain folders named after each user)
``` cd .. ```

6. Go to your home directory
``` cd ```

7. Go back to the general home directory (located "just above")
``` cd .. ```

8. Go again "just above", you should be back to the root directory
``` cd .. ```

9. Go directly to your home directory (named after you). It should be a
very simple command, which take no name as parameter of the path
``` cd ```

10. Try to create a directory named test
``` mkdir test ```

11. Go into this new directory
``` cd test ```

12. Check your current location
``` pwd ```


# Exercice 2

1. Go to your home directory (should be named after you, you might be
there by default)
``` cd ```

2. Check your current location
``` pwd ```

3. Create a folder linux_ex_1
``` mkdir linux_ex_1 ```

4. Go into this folder
``` cd linux_ex_1 ```

5. Create an empty text file named [first_name]_[last_name].txt (e.g. alexis_bogroff.txt)
``` vim elyes_jelaiel.txt ```

6. Create a folder notes
```mkdir notes ```

7. Move your text file into this folder
``` mv elyes_jelaiel.txt notes ```

8. Rename the text file by appending the current year [first_name]_[last_name]_[current_year].txt
``` mv elyes_jelaiel.txt elyes_jelaiel_2023 ```

9. Make a copy of this folder, name it notes_2022
cp -r notes notes_2022

10. Delete the first folder (notes) using the verbose option
``` rm -r notes ```

# Exercice 3

1. Create a script script_1.sh in the folder linux_ex_1
``` vim script_1.sh ```

2. In the script, write the commands that would output the following :
Script running please wait ...
Done.

``` echo "Script running please wait ..." ```
``` echo "Done. "```

3. Quit editing and save the script
``` :wq ```

4. Display the content of the script (using a command, not from an editor)
``` cat script_1.sh ```

5. Run the script
``` source script_1.sh```

# Exercice 4

1. Create a file credentials in the folder linux_ex_1
``` vim credentials ```

(a) Write any kind of (fake) personal information within the file
``` hej ```
(b) Display the file content
``` cat credentials ```
(c) Display the current permissions
``` ls -l credentials ```


2. Change the current permissions to : read only for all users
``` chmod a=r credentials ```
(a) Display the new permissions
``` ls -l credentials ```
(b) Modify and save the file
``` vim credentials ```
(c) Display the file content
``` cat credentials ```

3. Change the permissions back to read and write for all users
```chmod back credentials ```
(a) Display the new permissions
``` ls -l credentials ```
(b) Modify and save the file
nano credentials
#Crtl+X+Y+ENT
(c) Display the file content
``` cat credentials ```


## on the same file
1. Add the execute permission to the owner
``` chmod o=a+r credentials ```
(a) Display the new permissions
``` ls -l credentials ```

2. Remove the read permission to other users
(a) Display the new permissions
``` ls -l credentials ```

3. Change the permissions to read, write and execute for all users
``` chmod a=rxw credentials ```
(a) Display the new permissions
```ls -l credentials```

## 4.2

1. Go to the root folder
``` sudo su - ```

2. Create a file in root user mode named .private_file
``` touch .private_file ```
a. Write some information in the file
``` sudo vim .private_file ```
b. Display the file content
``` sudo cat .private_file```
c. Display all the files in the folder including hidden files
``` ls -a ```

3. Modify the file in normal user mode
``` vim .private_file ```
a. Write some new information in the file
``` I + text + Esc + :w + :q ```
b. Display the file content
``` cat .private_file ```

4. Modify the file in root user mode
``` sudo vim .private_file ```
a. Write some new information in the file
 ```sudo -i```
 ```vim .private_file```
 ```i```
 ```Modified```
b. Display the file content
``` sudo cat .private_file ```

5. Change permissions to read, write and execute for all users
``` sudo chmod 777 .private_file ```
a. Modify the file content in normal user mode
``` vim .private_file ```

b. Display the file content
``` cat .private_file ```

## 4.3

1. Change permissions of .private_file to read and write for all users, in
normal user mode
``` chmod 666 .private_file ```

2. Set the new file owner as the current user
``` sudo chown $user .private_file ```

3. Change permissions of .private_file to read and write for all users, in
normal user mode
```chmod 666 .private_file ```

## 4.5

1. Display the cmatrix help function
``` cmatrix -help ```

2. Launch cmatrix and make it display white characters (in place of the
green)
``` cmatrix -C white ```

3. Re-launch cmatrix and slow down the speed of characters actualization


4. Stop cmatrix
``` Ctrl + c ```
5. Launch cmatrix with both :
