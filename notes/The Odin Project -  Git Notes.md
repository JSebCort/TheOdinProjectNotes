# Command Line Basics
## Knowledge Check
What is the command line?
1. How do you open the command line on your computer?
    * Ctrl + Alt + T
2. How can you navigate to a particular directory?
    * cd [directory_name]
3. Where will cd on its own navigate you to?
    * The home directory
4. Where will cd .. navigate you to?
    * Upwards a level from the current directory
5. How do you display the name of the directory you are currently in?
    * pwd
6. How do you display the contents of the directory you are currently in?
    * ls
7. How do you create a new directory?
    * mkdir [directory_name]
8. How do you create a new file?
    * touch [file_name.file_type]
9. How do you destroy a directory or file?
    * rmdir [directory_name] *OR* rm [file_name.file_type]
10. How do you rename a directory or file?
    * mv [current_directory_name] [new_directory_name] *OR* m[current_file_name] [new_file_name]
# Introduction to Git
## Knowledge Check
1. What kind of program is Git?
    * Git is a Distributed Version Control (DVC) system. It allows for version control of files, so that one may keep track of updates made to the file.
    * As a DVC, the database, that holds all the files and their versions, is stored locally so that every user can work on a file without having to be connected to a server.
    * Git does not store an unchaged file again everytime it is committed. Instead, through snapshots, it stores a reference to that snapshot and links to the previous indentical file that was already stored.
    * Git checksums everything before it is stored through a SHA-1 hash. This hash is calculated based on the contents of a file or directory structure in Git.
	There are three main states to Git:
	* Modified - You have changed the file but haven't committed it to the database.
	* Staged - You have marked the file to be committed.
	* Comitted - You have safely stored the updated file to the database.
2. What are the differences between Git and a text editor in terms of what they save and their record keeping?
    * Git allows for multiple changes to a file to be stored, while a text editor can only modify and store one file without version control.
3. Does Git work at a local or remote level?
    * Local.
4. Does GitHub work at a local or remote level?
    * Remote; changes must be committed, with Git, to GitHub.
5. Why is Git useful for an individual developer?
    * Git allows for version control. The developer can easily rollback to a previous version if an error occurs at the most current version.
6. Why are Git and GitHub useful for a team of developers?
    * By utilizing both Git and GitHub, a team of developers can work on multiple files separately and their personal changes would be combined.
# Git Basics
## Notes
**Git Commands**
1. Commands related to a remote repository:
    * Clones the repository to the local computer.
	    * git clone git@github.com:USER-NAME/REPOSITORY-NAME.git *OR* git clone https://github.com/user-name/repository-name.git
    * Pushes the local repository to GitHub.
	    * git push origin main
2. Commands related to workflow:
    * Adds all unstaged files **in the current directory** to th    e taging are.
	    * git add .
    * Commits the staged item with a description of the changes.
	    * git commit -m "A message describing what you have done to make this snapshot different"
3. Commands related to checking status or log history
    * Shows the status of the repository's file.
	    * git status
    * Shows the history log of the changes made to the repository.
	    * git log
4. The basic Git syntax is program | action | destination.
    * For example:
        * git add . is read as git | add | ., where the period represents everything in the current directory;
        * git commit -m "message" is read as git | commit -m | "message"; and
        * git status is read as git | status | (no destination).
5. [Git Cheat Sheet](https://education.github.com/git-cheat-sheet-education.pdf)
## Knowledge Check
1. How do you create a new repository on GitHub?
	1. Click the plus (+) sign at the top-left of the webpage.
	2. Click "New Repository".
	3. Name the repository and click "Create Repository".
1. How do you copy a repository onto your local machine from GitHub?
    * git clone SSH_Line *OR* git clone GitHub_URL
1. What is the default name of your remote connection?
    * origin
1. Explain what origin is in 'git push origin main'.
    * 'origin' is the copy of the repository stored on the local computer.
1. Explain what main is in 'git push origin main'.
    * 'main' is the repository that is shown on GitHub.
1. Explain the two-stage system that Git uses to save files.
	1. Git utilizes the 'add' command to stage files to be committed.
	2. Then the files are committed to the local repository.
1. How do you check the status of your current repository?
    * git status
1. How do you add files to the staging area in git?
    * git add file_name
1. How do you commit the files in the staging area and add a descriptive message?
    * git commit -m "Message"
1. How do you push your changes to your repository on GitHub?
    * git push origin main
1. How do you look at the history of your previous commits?
    * git log