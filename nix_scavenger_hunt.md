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

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:* 

/home/cabox/workspace/

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?* 
challenge_files   LICENSE  nix_scavenger_hunt.md  nix_scavenger_hunt_stretch.md  README.md  super_scavengers.md                                               

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?*
total 40K
drwxrwxr-x 4 cabox cabox 4.0K Jan 16 21:14 .
drwxrwxr-x 3 cabox cabox 4.0K Jan 16 21:14 ..
drwxrwxr-x 7 cabox cabox 4.0K Jan 16 21:14 challenge_files
drwxrwxr-x 8 cabox cabox 4.0K Jan 16 21:14 .git
-rw-rw-r-- 1 cabox cabox 1.1K Jan 16 21:14 LICENSE
-rw-rw-r-- 1 cabox cabox 5.4K Jan 16 21:14 nix_scavenger_hunt.md
-rw-rw-r-- 1 cabox cabox  319 Jan 16 21:14 nix_scavenger_hunt_stretch.md
-rw-rw-r-- 1 cabox cabox 2.7K Jan 16 21:14 README.md
-rw-rw-r-- 1 cabox cabox  255 Jan 16 21:14 super_scavengers.md


* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://man.he.net/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*

        -a, 
              do not ignore entries starting with .
        -h, 
              with -l, print sizes in human readable format (e.g., 1K 234M 2G)

        -l    use a long listing format

* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*

bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*

            /

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*

/home/cabox

* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*

3

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
/home/cabox/workspace/wats1030-intro-to-unix

* Press the up arrow on your keyboard. *What just happened?*
It listed "cd .."
* Press the up arrow a few more times. *What do you see?*
It listed recent commands 
* Run the `history` command. *What do you see?*
It listed all of the commands I had typed, including 'history'

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*

cabox

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*

cabox    pts/0        2019-01-16 21:09 (52.161.27.120)

* How long has your system been running? Use `uptime` to see, and *paste the result here:*
 
 21:27:04 up 20 min,  1 user,  load average: 0.00, 0.00, 0.00

* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*

It appears to list information about processes that are running 

* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*

It displayed information about proccesses that are running and updated the information


### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*

2

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*

01-15-2015

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*

./tmp/modi_laboriosam.txt

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*

2

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*

/home/cabox/workspace/wats1030-intro-to-unix/challenge_files/serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incidunt. Explicabo vel esse blanditiis dolorem culpa non quia.

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*

list of all files including files.txt

* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*

It stopped when it couldn't show any more on the screen and had the word More at the bottom to let you know there is more

* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*

root       479  0.0  1.6  93060  4248 ?        Ss   21:08   0:00 sshd: cabox [priv]
cabox      490  0.0  0.7  93060  1924 ?        S    21:08   0:00 sshd: cabox@notty
cabox      491  0.0  0.3  12824   956 ?        Ss   21:08   0:00 /usr/lib/openssh/sftp-server
cabox      492  0.0  0.5  11180  1388 ?        Ss   21:08   0:00 bash -c cd ./workspace/ && inotifywait . --monitor -e move,create,delete --exclude '.*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)'
cabox      493  0.0  0.2   6476   768 ?        S    21:08   0:00 inotifywait . --monitor -e move,create,delete --exclude .*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)
root       494  0.0  1.6  93060  4264 ?        Ss   21:09   0:00 sshd: cabox [priv]
cabox      505  0.0  0.7  93060  1896 ?        S    21:09   0:00 sshd: cabox@pts/0
cabox      506  0.0  2.3  23716  6092 pts/0    Ss   21:09   0:00 -bash
cabox      746  0.0  0.5  11180  1396 ?        Ss   21:11   0:00 bash -c cd ./workspace/ && inotifywait wats1030-into-to-unix --monitor -e move,create,delete --exclude '.*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)'
cabox      747  0.0  0.2   6476   772 ?        S    21:11   0:00 inotifywait wats1030-into-to-unix --monitor -e move,create,delete --exclude .*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)
cabox      759  0.0  0.5  11180  1392 ?        Ss   21:14   0:00 bash -c cd ./workspace/ && inotifywait wats1030-intro-to-unix --monitor -e move,create,delete --exclude '.*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)'
cabox      760  0.0  0.2   6476   708 ?        S    21:14   0:00 inotifywait wats1030-intro-to-unix --monitor -e move,create,delete --exclude .*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)
cabox      761  0.0  0.5  11180  1392 ?        Ss   21:15   0:00 bash -c cd ./workspace/ && inotifywait wats1030-intro-to-unix/.git --monitor -e move,create,delete --exclude '.*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)'
cabox      762  0.0  0.2   6476   708 ?        S    21:15   0:00 inotifywait wats1030-intro-to-unix/.git --monitor -e move,create,delete --exclude .*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)
cabox      790  0.0  0.5  11180  1396 ?        Ss   21:48   0:00 bash -c cd ./workspace/ && inotifywait wats1030-intro-to-unix/challenge_files --monitor -e move,create,delete --exclude '.*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)'
cabox      791  0.0  0.2   6476   772 ?        S    21:48   0:00 inotifywait wats1030-intro-to-unix/challenge_files --monitor -e move,create,delete --exclude .*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)
cabox      792  0.0  0.5  11180  1396 ?        Ss   21:48   0:00 bash -c cd ./workspace/ && inotifywait wats1030-intro-to-unix/challenge_files/tmp --monitor -e move,create,delete --exclude '.*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)'
cabox      793  0.0  0.2   6476   708 ?        S    21:48   0:00 inotifywait wats1030-intro-to-unix/challenge_files/tmp --monitor -e move,create,delete --exclude .*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)
cabox      794  0.0  0.5  11180  1392 ?        Ss   21:48   0:00 bash -c cd ./workspace/ && inotifywait wats1030-intro-to-unix/challenge_files/serial-numbers --monitor -e move,create,delete --exclude '.*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)'
cabox      795  0.0  0.2   6476   712 ?        S    21:48   0:00 inotifywait wats1030-intro-to-unix/challenge_files/serial-numbers --monitor -e move,create,delete --exclude .*(.*.swpc.*|.*node_modules/.*|.git/objects/.*|.git/subtree-cache/.*)
cabox      806  0.0  0.6  36028  1672 pts/0    R+   22:01   0:00 ps aux
cabox      807  0.0  0.4  12888  1140 pts/0    S+   22:01   0:00 grep --color=auto cabox


------OR------

cabox      809  0.0  0.4  12888  1072 pts/0    S+   22:01   0:00 grep --color=auto angeline-n

*I didn't know if you meant username as in what gets printed when I do the whoami command or my username for github*
