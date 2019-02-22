#Git Stuff
This directory has an initialized git repository. Play around here if you wish
Man united is the best
##Git Commands

 - git init
 - git clone \<locationOfRemoteRepo\> .
 - git commit -m ""
 - git pull --rebase <remoteRepoName> <branchname>		//fetch from repo and branch, pull(merge) those changes into the currenct branch replay the local committed changes on top
 - git push \<remoteRepoName\> \<branchname\>
 - git remote -vv
 - git remote add \<remoteRepoName\> \<remotelocation\>
 - git remote remove \<remoteRepoName\>
 - git fetch \<remoteRepoName\> \<branchname\>
 - git reset --hard \<remoteRepoName\>/\<branchname\> //reset current branch to this
 - git reset --soft HEAD^		//undo last commit but keep the changes this is like hg rollback
 - git checkout -b \<branchname\>   	//create and move head to newly created branch. shorthand for git branch <branchname>; 
 - git checkout -b \<branchname\> \<remoteLocation\>/\<branchname\>
 - git checkout \<branchname\>	//move head to branch
 - git branch -vv			//find the remote branch repo that the current branch is tracking
 - git branch -d \<branchname\>	//delete branch
 - git branch <currentBranchYouWantToDoTrackingOn\> -u <remote\>/<branch\>
 - git log
 - git checkout \<file\>		//undo changes to a file
 - git merge \<branchname\>		//merge branchname into the current branch
 - git rebase \<branch\> //replay any unpushed commits in current branch on top of the \<branch\>
 - git mergetool			//start the configured merge too to resolve conflicts
 - git tag //view tags
 - git tag -a \<tagRev\> -m "my version" //annotated tag
 - git cherry-pick \<rev\> //cherry pick commit into current branch
 - git status
 - git stash
 - git stash list
 - git stash pop
 - git stash apply stash@{ID}


###change settings for the local repo...
 - git config user.name General-Meow
 - git config user.email spl.ivalis@gmail.com 	

### HEAD
 - HEAD //where you are now
 - HEAD^ //parent of head (commit before head)
 - HEAD^2 //parent of parent of head
 - HEAD^^ //same thing as HEAD^2


### Alias on my mac
 - a	 => !git add . && git status
 - aa	 => !git add . && git add -u . && git status
 - ac	 => !git add . && git commit
 - acm	 => !git add . && git commit -m
 - alias	 => !git config --list | grep 'alias\.' | sed 's/alias\.\([^=]*\)=\(.*\)/\1\	 => \2/' | sort
 - au	 => !git add -u . && git status
 - c	 => commit
 - ca	 => commit --amend
 - cm	 => commit -m
 - d	 => diff
 - l	 => log --graph --all --pretty=format:'%C(yellow)%h%C(cyan)%d%Creset %s %C(white)- %an, %ar%Creset'
 - lg	 => log --color --graph --pretty=format:'%C(bold white)%h%Creset -%C(bold green)%d%Creset %s %C(bold green)(%cr)%Creset %C(bold blue)<%an>%Creset' --abbrev-commit --date=relative
 - ll	 => log --stat --abbrev-commit
 - llg	 => log --color --graph --pretty=format:'%C(bold white)%H %d%Creset%n%s%n%+b%C(bold blue)%an <%ae>%Creset %C(bold green)%cr (%ci)' --abbrev-commit
 - master	 => checkout master
 - s	 => status
 - spull	 => svn rebase
 - spush	 => svn dcommit
 - st	 => status
