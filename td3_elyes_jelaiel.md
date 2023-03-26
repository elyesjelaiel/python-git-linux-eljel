# Exercice 1

1. Display the list of files and folders at the root using ls -l
``` ls -l ```

2. In a pipeline (using |), append a grep instruction to only display informations of bin
``` ls -l grep bin ```

3. Append an awk instruction to only display the size of bin
``` ls -l / | grep bin | awk '{print $5}' ```

4. Now rather extract the month, day and year of creation of the folder bin
``` ls -l / | grep bin | awk '{print $5}' ```

5. Now rearrange the instruction to get the following output format : 2020-
Oct-26 (from original data : Oct 26 2020



# Exercice 2

``` curl https ://en.wikipedia.org/wiki/List_of_cyberattacks > cyberattacks.txt 
cat cyberattacks.txt | grep meta
cat cyberattacks.txt | grep -oP "meta\s\w+"  #-o : output ; -P : Perl regex syntax)
cat cyberattacks.txt | grep -oP "(?<=meta\s)\w+" #ce qui est après meta
cat cyberattacks.txt | grep -P 'A cyberattack is' #ne va pas marcher (voir ligne suivante)
cat cyberattacks.txt | grep -P 'A <a href="/wiki/Cyberattack" title="Cyberattack">cyberattack</a> is any type'
cat cyberattacks.txt | grep -A1 'mw-content-text' | grep -v 'mw-content-text' 
cat cyberattacks.txt | grep -P "(?<=<title>)"
cat cyberattacks.txt | grep -P "(?<=<title>).*(?=</title>)" 
cat cyberattacks.txt | grep -oP "(?<=<title>).*(?=</title>)"  ```
