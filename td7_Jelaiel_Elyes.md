## Exercice 1

1. Create an empty working directory called “td4”.
``` mkdir td4 ```

2. Initialize a Git repository in it.
``` cd td4 ```
``` git init ```

3. Install the Linux python3-pip package using your Linux package manager.
``` sudo apt update ```
``` sudo apt-get install python3-pip ```

4. Install the VirtualEnv Python package using pip3.
``` pip3 install virtualenv ```

5. Create a Python virtual environment called “.env”. Do you see the change in your working directory ?
``` virtualenv .env ```

6. Activate your virtual environment. Do you see the change in your prompt ?
``` source .env/bin/activate ```

7. List the Python packages installed in your virtual environment.
``` pip list ```

8. Does Git want you to commit something ? Do you think it is a good thing ?
hint : You can find templates at https://github.com/github/gitignore


9. Create a .gitignore file to tell Git which files should be untracked.


10. Does Git want you to commit something ?
Do you think it is a good thing this time ?


11. Do your first commit and check that Git is happy    now


## Exercice 2

1. Install the Python package Requests using pip.
info : Requests is a simple, yet elegant HTTP library and the de facto
standard for querying RESTful web API.
``` pip install requests ```
``` import requests ```


2. Create a Python script that returns the list of all place ids in Derbyshire.
hint : Look at the county structure inside the web API documentation
hint : As the web API returns JSON, no need to use regular expressions


3. Commit your changes in Git
