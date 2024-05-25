what is GIT?
what is Version control system and what it is also called?
what happens if we dont have an VCS?	
mechanism used to save the files in the Remote Repository (vtz.GIT)?
Benefits of VCS?
Types of VCS?
DIfference between the centralized and the Distributed version control system?
Advantages of the GIT?
Ways to use the GIT?	
Configuration of GIT?
Line Ending in CRLF?


What is GIT?
	GIt is a stream of snapshots. which is free an open source VCS.

What is a Version?
	It is a snapshot or state of the files and folders in a codebase at a given time can be called a "version."

What is VCS also called?
	A version control system can also be referred to as a 
	source control system
	source code management
	version control software
	version control tools

what is Version control system?	
	in a nutshell with a version control system we can track our project history. version control system records the changes made to our code over time in a special database called repository. we can look at our project history and see who has made what changes when and why and if we screw something up we can easily revert our project back to an earlier state 	
	It is a series of snapshots
	It keeps track of all the changes of files, who have created, updated, deleted.
	Ex: Lets assume there are 2 developers A & B. If for suppose developer A worked on a file and pushed to the Remote repository, due to some enhancements developer B worked on the same file and pushed the code to the remote repository, there might be a break of production as there are editing same file, so then we should track back or checkout to the previous version of the File to keep the applicaton up and runnnig. This is the main resaon version control is used.

what happens if we dont have an VCS?	
	without a version control system we'll have to constantly store copies of the entire project in various folders this is very slow and doesn't scale at all especially if multiple people have to work on the same project you would have to constantly toss around the latest code via email or some other mechanisms and then manually merge the changes so

What is the mechanism used to save the files in the Remote Repository (vtz.GIT)?
	There is a metadata used to store all the information
	
Benefits of VCS?
	Track changes - Track changes of who are working and editing the files
	Backup - It also works as Backup, we can go to the previos version when needed
	Collaboration - multiple people can work at the same time without overriding each others code
	Flexibility - we can experiment new ideas without effecting the old code that already saved in a main branch
	security - since the repository is central it can be backed up and protected to help the integrety and security of the project.
	Saves the history of the file changes
	Simultaneously working
	Branching and Merging
	Tracebility
	
Types of VCS?
	Localized Version Control System - First Generation
	Ex: SCCS (Source Code Control System)
		RCS (Revision Control System)
	Centralized Version Control System  - Second Generation
	Ex: CVS (Concurrent Versions System)
		SVN (Apache Subversion)
		Team Foundation Server(Microsoft)
		Perforce Helix Core
	Distributed Version Control System  - Third Generation
	Ex: Git
		Mercurial
		BitKeeper
		Darcs (Darcs Advanced Revision Control System)
		Monotone
		Bazaar
		Fossil
		Pijul

Difference between the Centralized, Distributed VCS?
	In a centralized system all team members connect to a central server to get the latest copy of the code and to share their changes with others the problem with the centralized architecture is the single point of failure if the server goes offline we cannot collaborate or save snapshots of our project. so we have to wait until the server comes back online
	In distributed systems we don't have these problems every team member has a copy of the project with its history on their machine so we can save snapshots of our project locally on our machine. if the central server is offline we can synchronize our work directly with others
	
Advantages of the GIT?
	Free
	Open source
	Super fast
	Scalable
	operations like branching and merging are slow and painful in other version control systems like subversion or tfs but they're very fast and git	
	
Ways to use the GIT?
	Command Line: Git Bash(Bourne again shell)
	GUI Ex: GUI client, GitKraken, SOurce Tree
	COde Editors
	Ex: Git lens extension in visual studio code
	
Configuration of GIT?
	Before using the git we should specify some configuration settings. They are:
	Name
	EMail
	Default Editor
	Line Ending
	 We can specify these configuration settings in 3 levels
		System - sets to all levels in current computer
		Global - sets to all users and respositories of current user
		Local - sets to the current repository
	 
Line Ending in CRLF?
	This is an important setting need to be done while configuring the GIT, else we encounter warnings in future. 
	
Timeline of VCS:
	https://initialcommit.com/img/initialcommit/vcs-timeline.png

Command-line text editors in Linux:
	There are two command-line text editors in Linux
	VIM
	NANO	https://docs.rackspace.com/support/how-to/command-line-text-editors-in-linux/

Linux Commands:
	https://github.com/chanduujjina/GitPractice_2023_B2/blob/main/basic_linux_commands.adoc

What does .git folder contains after initializing git init?

What are the different repository in git?
	Local 
	

what are the stages in the GIT?
	There are 3 stages in the git
	Unstaged area/working directory/untracked state
	staged area/ Tracked state
	commit 


Some of the GIt commands:
	
	To Know the GIt version
		git --version
		
	configure the user name
		git config --global user.name "Bhargav"
	
	configure the user email
		git config --global user.email abc@gmail.com
		
	configure default editor, as wait flag is set it tells the editor to wait unitl the default editor is closed
		git config --global core.editor "code --wait"
			opens the default editor and opens the file called .gitconfig to show all the global settings 
				git config --global -e
				
	setting core CRLF
		In windows
			git config --global core.autocrlf true
		In Mac/Linux
			git config --global core.autocrlf input
			
	To Intailize empty repository
		git init

	Create file in git
		cat > fileName
		touch filename

	Move single file from unstaged to staged
		git add fileName

	Move all file from unstaged to staged
		git add .

	Move file from staged area to commit area
		git commit -m"commit message"

	Move file from staged area to unstaged area
		git restore --staged fileName

	To check the file status in git(wether in untracked/tracked/commit area)
		git status
		
	To delete single file permanentely from untracked state
		git clean -f filename 
	
	To delete all files permanentely from untracked state
		git clean -f .
	
	commit the code
		git commit -m "commit message"
	
	to see committed files in one line
		git log --oneline
		
UNDO commands:
	To delete repository or folder
		rm -rf .git
		
	To delete file in repository
		git rm fileName
		
	move files from commit area to staged area
		git reset --soft HEAD~1
		
	move single file from staged to unstaged area
		git restore --staged filename
	
	move all file from staged to unstaged state
		git rm -r --cached .
		
	move single file from staged to unstages state
		git rm --cached filename
	
	Move file from commit area to staged area	
		git reset --soft head~1
	
	Delete file from commit area Permently
		git reset --hard head~1
		
How to convert normal desktop folder to git repository?
	create an Normal folder on desktop
		Java_practice
	
	create an git repository in the Github withe the same name as the local folder
		Java_practice
	
	Now open the local folder in the GitBash and initialize the git command 
		git init
		git add .
		git clone -m "commit message"
		git remote add origin gitlink
		git remote -v (To check origin is set or not)
		git branch -M branchname
		for the first time push we should set the upstream
			git push --set-upstream origin master
		
	
Difference between upstream and the origin?
	https://stackoverflow.com/questions/9257533/what-is-the-difference-between-origin-and-upstream-on-github
	



Issues:

GIT:
	On a Windows machine, I added some files using git add. I got warnings saying?
	warning: in the working copy of 'Test1.txt', LF will be replaced by CRLF the next time Git touches it
		https://stackoverflow.com/a/20653073
		


Reference Links:

Version Control System - https://initialcommit.com/blog/Technical-Guide-VCS-Internals

commonly used Git commands:
https://training.github.com/downloads/github-git-cheat-sheet.pdf


