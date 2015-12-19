How To: Add people to an MIT Moira list
=======================================

Through this tutorial, you'll learn some basic skills in the terminal, vm, and ssh-ing into servers. This tutorial is catered people with access to the Terminal application. :)


1. Open Terminal and connect to MIT Athena Servers.
-------------------------------------------------------
* You can search for the terminal in your Applications. When Terminal opens, connect to the MIT Athena servers (on which you can do all the fun mailing list changes) by typing:
`ssh your_username@athena.dialup.mit.edu`
* Type in the password associated with your Kerberos as prompted.


2. Create a textfile for the Kerberos addresses.
------------------------------------------------
* Try typing `ls` to see the current directory, or folder that you are in. This will show other "directories" (which you often visualize as folders in the Finder app) and files. 
* Create a textfile using vim (although you could use any text editor, but I've gotten used to vim), by typing `vi YourFileName.txt`. It doesn't matter what the name is really, because we'll get rid of this file later (unless you feel really attached to it).
* In your Excel sheet, or Google sheet, copy and paste the list of email addresses on your sheet into the text file. Every email address should be on its own line. 
* Save your textfile by pressing the ESC button, and then typing `:wq`, which you'll see at the bottom of your Terminal. This should bring you back to the home directory (Try typing `ls` to see where you are). 

3. (Opt.) If your addresses include "@mit.edu"
----------------------------------------------
The later command that we will use (`blanche`) doesn't accept email addresses with the "@mit.edu" string. We want just the Kerberos usernames, so we need to get rid of "@mit.edu" if your textfile includes them. 

You can filter out this string from every line in your textfile by using the `sed` command. If you like the Excel or Google sheets interface better, I recommend just doing find/replace to remove the "@mit.edu". 

If you've decided to try out `sed` (woo trying new things!), make sure you're in the directory with your textfile, and type `sed 's/@mit.edu//' YourFileName.txt` 

