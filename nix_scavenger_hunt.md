# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:** Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:
  */home/cabox/workspace 
   
* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?
  *LICENSE  README.md  challenge_files  nix_scavenger_hunt.md  nix_scavenger_hunt_stretch.md  super_scavengers.md 
  
* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*
  *drwxrwxr-x 4 cabox cabox 4.0K Apr  1 00:47 .                                                                                                               
  drwxr-xr-x 7 cabox cabox 4.0K Apr  1 00:47 ..                                                                                                              
  drwxrwxr-x 8 cabox cabox 4.0K Apr  1 00:47 .git                                                                                                            
  -rw-rw-r-- 1 cabox cabox 1.1K Apr  1 00:47 LICENSE                                                                                                         
  -rw-rw-r-- 1 cabox cabox 2.7K Apr  1 00:47 README.md                                                                                                       
  drwxrwxr-x 7 cabox cabox 4.0K Apr  1 00:47 challenge_files                                                                                                 
  -rw-rw-r-- 1 cabox cabox 5.8K Apr  1 00:53 nix_scavenger_hunt.md                                                                                           
  -rw-rw-r-- 1 cabox cabox  317 Apr  1 00:47 nix_scavenger_hunt_stretch.md                                                                                   
  -rw-rw-r-- 1 cabox cabox  191 Apr  1 00:47 super_scavengers.md     
  
* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://linux.die.net/man/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*   
-A  List all entries except for . and ...  Always set for the super-user  -H  Symbolic links on the command line are followed.  This option is assumed if none of the -F, -d, or -l options are specified.   -l      (The lowercase letter ell  List in long format.  See below.  If the output is to a terminal, a total sum for all the file sizes is output on a line before the long listing.

* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*
bin  boot  dev  etc  fastboot  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var                                           

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*
/home/cabox

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*
-bash: /home/cabox: Is a directory   

* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*
2

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?* 
workspace

* Press the up arrow on your keyboard. *What just happened?* 
It enter the cd command  

* Press the up arrow a few more times. *What do you see?*
It cycled through the commands

* Run the `history` command. *What do you see?*
History of all the commands I've ran 

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*
cabox

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*
No there is no one else. 

* How long has your system been running? Use `uptime` to see, and *paste the result here:*
 20:46:04 up 18 min,  1 user,  load average: 0.00, 0.00, 0.00
 
* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*
It looks like what has happened or been processed on this terminal while it has been logged into. 

* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*
This is the current real time of what is actually happening in the terminal as it processes.

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?* 
2

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*
A serious of numbers, possibly credit card numbers. 

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*
tmp file 

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*
./Lissie-Strosin.user:4:Jewessfurt, WA 00816-7241                                                                                                          
./Britt-Erdman.user:4:O'Harachester, WA 37261  

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*
./serial-numbers/eaque_molestiae.txt:4:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incidunt. Explicabo vel esse blanditiis dolorem culpa non quia. 

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*
The input of this session. 

* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
total 464K                                                                                                                                                 
drwxrwxr-x 7 cabox cabox 4.0K Apr  6 21:48 .                                                                                                               
drwxrwxr-x 4 cabox cabox 4.0K Apr  1 00:47 ..                                                                                                              
drwxrwxr-x 2 cabox cabox 4.0K Apr  1 00:47 01                                                                                                              
-rw-rw-r-- 1 cabox cabox    0 Apr  1 00:47 2015_special_stuff.demo                                                                                         
-rw-rw-r-- 1 cabox cabox   93 Apr  1 00:47 Afton-Jast.user                                                                                                 
-rw-rw-r-- 1 cabox cabox   85 Apr  1 00:47 Aimee-Maggio.user                                                                                               
-rw-rw-r-- 1 cabox cabox   79 Apr  1 00:47 Alfonso-Gottlieb.user                                                                                           
-rw-rw-r-- 1 cabox cabox  100 Apr  1 00:47 Allen-Kemmer.user                                                                                               
-rw-rw-r-- 1 cabox cabox   86 Apr  1 00:47 Almina-Cormier.user                                                                                             
-rw-rw-r-- 1 cabox cabox   87 Apr  1 00:47 Alta-Lemke.user                                                                                                 
-rw-rw-r-- 1 cabox cabox   79 Apr  1 00:47 Amina-McGlynn.user                                                                                              
-rw-rw-r-- 1 cabox cabox   78 Apr  1 00:47 Anabel-Hammes.user                                                                                              
-rw-rw-r-- 1 cabox cabox   61 Apr  1 00:47 Ancel-Conn.user                                                                                                 
-rw-rw-r-- 1 cabox cabox   87 Apr  1 00:47 Anjali-Halvorson.user                                                                                           
-rw-rw-r-- 1 cabox cabox   64 Apr  1 00:47 Ardath-Kuvalis.user                                                                                             
-rw-rw-r-- 1 cabox cabox   90 Apr  1 00:47 Avah-Dickinson.user                                                                                             
-rw-rw-r-- 1 cabox cabox   79 Apr  1 00:47 Ayaan-Stiedemann.user                                                                                           
-rw-rw-r-- 1 cabox cabox   79 Apr  1 00:47 Aylin-Grant.user                                                                                                
-rw-rw-r-- 1 cabox cabox   70 Apr  1 00:47 Bedford-Sipes.user                                                                                              
-rw-rw-r-- 1 cabox cabox   82 Apr  1 00:47 Benita-King.user                                                                                                
-rw-rw-r-- 1 cabox cabox   92 Apr  1 00:47 Benito-Stoltenberg.user                                                                                         
-rw-rw-r-- 1 cabox cabox   83 Apr  1 00:47 Beverlee-Moen.user                                                                                              
-rw-rw-r-- 1 cabox cabox   76 Apr  1 00:47 Brad-Thiel.user                                                                                                 
-rw-rw-r-- 1 cabox cabox   68 Apr  1 00:47 Brayan-Douglas.user                                                                                             
-rw-rw-r-- 1 cabox cabox   80 Apr  1 00:47 Bria-Satterfield.user                                                                                           
-rw-rw-r-- 1 cabox cabox   70 Apr  1 00:47 Bridgette-Reichel.user                                                                                          
-rw-rw-r-- 1 cabox cabox   78 Apr  1 00:47 Britt-Erdman.user                                                                                               
-rw-rw-r-- 1 cabox cabox   66 Apr  1 00:47 Britta-Hammes.user                                                                                              
-rw-rw-r-- 1 cabox cabox   68 Apr  1 00:47 Bryant-Kuhic.user                                                                                               
-rw-rw-r-- 1 cabox cabox   86 Apr  1 00:47 Bryton-Aufderhar.user                                                                                           
-rw-rw-r-- 1 cabox cabox   82 Apr  1 00:47 Caitlin-Grady.user                                                                                              
-rw-rw-r-- 1 cabox cabox   99 Apr  1 00:47 Carroll-Hartmann.user                                                                                           
-rw-rw-r-- 1 cabox cabox   80 Apr  1 00:47 Claudie-McClure.user                                                                                            
-rw-rw-r-- 1 cabox cabox   72 Apr  1 00:47 Clemente-Haley.user                                                                                             
-rw-rw-r-- 1 cabox cabox   84 Apr  1 00:47 Cleo-VonRueden.user                                                                                             
-rw-rw-r-- 1 cabox cabox   89 Apr  1 00:47 Codie-Romaguera.user                                                                                            
-rw-rw-r-- 1 cabox cabox   73 Apr  1 00:47 Cooper-Reynolds.user                                                                                            
-rw-rw-r-- 1 cabox cabox   80 Apr  1 00:47 Corrie-Bogisich.user                                                                                            
-rw-rw-r-- 1 cabox cabox   57 Apr  1 00:47 Dannielle-Green.user                                                                                            
-rw-rw-r-- 1 cabox cabox   86 Apr  1 00:47 Deedee-Jacobson.user                                                                                            
--More--   

* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*
root       528  0.0  0.6  63876  3308 ?        Ss   21:42   0:00 sshd: cabox [priv]                                                                        
cabox      530  0.0  0.2  64008  1512 ?        S    21:42   0:00 sshd: cabox@notty                                                                         
cabox      531  0.0  0.1  12776   940 ?        Ss   21:42   0:00 /usr/lib/openssh/sftp-server                                                              
root       546  0.0  0.6  63876  3456 ?        Ss   21:51   0:00 sshd: cabox [priv]                                                                        
cabox      548  0.0  0.2  63876  1468 ?        S    21:51   0:00 sshd: cabox@pts/0                                                                         
cabox      549  0.0  0.3  18140  2028 pts/0    Ss   21:51   0:00 -bash                                                                                     
cabox      559  0.0  0.2  15520  1144 pts/0    R+   21:52   0:00 ps aux                                                                                    
cabox      560  0.0  0.1   8816   748 pts/0    S+   21:52   0:00 grep --color=auto cabox     

