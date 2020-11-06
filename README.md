# .scripts
Custom Linux scripts to help with setup and common operations.

## Installation
It is recommended that the .scripts/ directory is installed in the user's home directory

- cd
- git clone http://github.com/areif-dev/.scripts.git

To quickly reference scripts from anywhere in the system add .scripts/ to PATH
- nano ~/.bashrc
- Add this line to the bottom:
  - export PATH=~/.scripts:$PATH
- Press <ctrl+x>
- Press <Y>
- Press <Enter>
- Enter "source ~/.bashrc"
  
All the scripts should be executable immediatly after installation, but in case they are not
  
 ## Usage
 To execute a script from anywhere in the terminal, simply type the name of the script and press <Enter>
  
 ### Update Script
 The update script is used to combine the apt update, upgrade, and autoremove commands 
 - Enter "update"
 - Enter sudo password when prompted
 - A list of upgradable packages will be printed to the screen along with a prompt to continue
 - Enter "y" or "n" to continue installing or quit, respectively
 - All upgradable packages will then be upgraded and autoremoved
 
 ### Git Commit Script
 The git_commit script is used to automatically stage, commit, and push all changes in a git repo
 - Enter "git_commit"
 - A list of all changes to the git repo will be displayed along with a prompt to continue
 - Enter "y" or "n" to continue with the commit or to quit, respectively
 - Enter the commit message when prompted
 - All changes to the branch will then be staged, committed, and pushed to a remote repo if applicable
