# Td2 Fundamental Linux functionalities

## Exercice 1

1. Put system up to date
``` sudo apt update + sudo apt upgrate ```

2. Display
- Linux version
``` uname -r ```

- Current processes and memory usage associated
``` top ```

- Display it in a more pleasant way ("more readable for humans")
``` ps ```

- Number of processors
``` nproc ```

- L1, L2 and L3 cache size
``` lscpu ```

- Disk space
``` df -h ```

- Monted devices
``` mount ```

- Connected usb devices
``` lsusb ```

- Hostname
``` hostname ```

## Exercice 2

1. Create a variable x and assign it the short text piri pimpin
``` "x = piri pimpin" ```

2. Display the value of this variable
``` echo $x ```

3. Add to this value the following text piri pimpon
It should contain the following : piri pimpim piri pimpon
``` x+= "piri pimpon" ```

4. Create a folder named my_programs, then enter into that folder
``` mkdir my_programs ```
``` cd my_programs ```

5. Create a script named pilou that displays pilou pilou
``` vim pilou ```
``` I ; echo "pilou pilou" ; Esc ; :w :q ```

6. Run this script
``` source pilou ```

7. Make this script executable
chmod u+x pilou

8. Run the script by writting its name only
./pilou

9. Programs called from the terminal are usually found thanks to a variable
named PATH
Display the content of the variable PATH
```echo $PATH ```

10. Add the path of your current location to the global variable PATH
```PATH=$PATH:$(pwd)```

11. When you are sure of the result, export it
``` export PATH ```

12. Go to your home directory
``` cd ~ ```

13. Run your script by writting its name only
``` pilou ```

14. Change the value of the PATH in the .profile file in order to make it
permanent
 

15. Create a new shell and run your script using its name only


## Exercice 3

1. Create a script say_hello.sh
``` vim say_hello.sh ```
— Make it write the current date and time followed by ’Hello’
— It should write it in a file named ’hellos.txt’
``` echo "$(date) Hello" >> hellos.txt ```
— Each new output should be appened to the file (it shouldn’t remove
previous hellos)

2. Make the script executable
``` chmod +x say_hello.sh ```

3. Use crontab to schedule the running of the script every minute
``` crontab -e ***** /sayhello.sh ```

## Exercice 4

1. Create a folder named hash_checksum. Go into this folder
``` mkdir hash_checksum ```
``` cd hash_checksum ```

2. Inside this folder, create two files named .sensible_addresses and .sensible_passwords
``` touch .sensible_addresses ```
``` touch .sensible_passwords ```

3. Display the list of files of the folder
``` ls -a ```

4. Still inside the folder hash_checksum, create a script named gentle_script.sh.
This script should display the following text "Have a good day"
``` echo "Have a good day" > gentle_script.sh ```

5. Run the script
``` bash gentle_script.sh ```

6. Compute the sha256sum of gentle_script. Store it into a file named
log_sha
``` sha256sum gentle_script.sh > log_sha ```

7. Now corrupt the file by adding a line of code that deletes any file starting
with : ".sensible"
``` echo "rm -rf .sensible*" >> gentle_script.sh ```

8. Compute again the sha256sum of gentle_script. Store it into the log_sha
file
``` sha256sum gentle_script.sh >> log_sha ```

9. Run the script
``` bash gentle_script.sh ```

10. Display again the list of files of the folder
``` ls -a ```

11. Display the log_sha content : are the hashes any different ?
``` cat log_sha ```



# Exercice 5
1. Install the QPDF free command-line program.
Part of this program is the zlib-flate command that compress and uncompress files using the deflate algorithm.
``` sudo apt-get install qpdf ```

2. Create a directory "compress", go into this directory
``` mkdir compress ```
``` cd compress ```

3. Create a first file "hello" whose content is "Hello"
``` echo "Hello" > hello ```

4. Compute the deflate compression (level 1) of this file. Store the compressed file size into a file log_compress


5. Create a second file "hello_multiple" whose content is 1000 lines of "Hello"
2
6. Compute the deflate compression (level 1) of this file. Store the compressed file size into a file log_compress
7. Create a third file "hello_mulitple_i" whose content is 1000 lines of "Hello
i" (i varying from 1 to 100)
8. Compute the deflate compression (level 1) of this third file. Store the
compressed file size into log_compress
9. Display the content of log_compress
10. Compute the compression ratio of each file, also display it as a simple
fraction (e.g. 12.6 => 10 :1)
11. Analyse the results

