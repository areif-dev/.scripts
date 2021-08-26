# .scripts

Custom Linux scripts to help with setup and common operations.

## Installation

It is recommended that the .scripts/ directory is installed in the user's home directory

``` bash
cd
git clone http://github.com/areif-dev/.scripts.git
```

To quickly reference scripts from anywhere in the system add .scripts/ to PATH

-   nano ~/.bashrc
-   Add this line to the bottom:
    -   export PATH=~/.scripts:$PATH
-   Press <ctrl+x>
-   Press \<Y>
-   Press \<Enter>
-   Enter "source ~/.bashrc"

All the scripts should be executable immediatly after installation, but in case they are not

## Usage

To execute a script from anywhere in the terminal, simply type the name of the script and press <Enter>

### update Script

The update script is used to combine the apt update, upgrade, and autoremove commands

-   Enter "update"
-   Enter sudo password when prompted
-   A list of upgradable packages will be printed to the screen along with a prompt to continue
-   Enter "y" or "n" to continue installing or quit, respectively
-   All upgradable packages will then be upgraded and autoremoved

### git-commit Script

The git-commit script is used to automatically stage, commit, and push all changes in a git repo

#### Without Commandline Args

-   Enter "git-commit" somewhere in the repo of choice. Ideally in the root directory where the .git folder is
-   A list of all changes to the git repo will be displayed along with a prompt to continue
-   Enter "y" or "n" to continue with the commit or to quit, respectively
-   Enter the commit message when prompted
-   All changes to the branch will then be staged, committed, and pushed to a remote repo if applicable

#### With Commandline Args

``` bash
git-commit -y -m "Changes made"
```

### dl Script

dl is a distribution of the youtube-dl program that is specifically for downloading music in the m4a loss-less format. It will require youtube-dl and ffmpeg packages to be preinstalled

-   Enter dl followed by the url of the video to download audio from
-   E.G. dl https://www.youtube.com/watch?v=012345678901

### create_python Script

Used to initialize a new Python 3 project. Uses the default Python 3 instance. Will create a root directory with LICENSE, README.md, .gitignore, an empty git repo, and a beginning package of the same name as the project

-   Takes one argument: the name of the project to start in the current directory
```
create_python new_project
```
