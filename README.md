# CRIO
## Started Module 1 in CRIO
  + Git Basics
    * Attached file (Git_Basics)
### Gitlab Repositories
  + git@gitlab.crio.do:COHORT_ME_GIT_BASICS_ENROLL_1596802014715/ram75353-ME_GIT_BASICS.git
  + https://gitlab.crio.do/COHORT_ME_GIT_BASICS_ENROLL_1596802014715/ram75353-ME_GIT_BASICS.git
    * To download/upload contents from/to the above Gitlab repositories you’ll have to prove you’re having access to it.
    * Execute the below command to generate an SSH key. SSH protocol allows you to remotely access machines using the SSH key.
    * SSH -> SSH or Secure Shell is a network communication protocol that enables two computers to communicate
    ___________
    * **ssh-keygen -t ed25519 -C "crio-git-byte"** [ssh-keygen Codes](https://www.ssh.com/academy/ssh/keygen)
    ____________
    * Did you notice you were given two links to your Gitlab repository earlier? The one which starts with git@gitlab.crio.do is to be used to authenticate using SSH. The https link authenticates using your gitlab.crio.do username and password Execute cat ~/.ssh/id_ed25519.pub and copy the public key printed. You’ll add this to https://gitlab.crio.do/ in the next step

    * crio-user@ram75353:~$ cat ~/.ssh/id_ed25519.pub
      ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIL3J0omWRsa8BM7Ft6FyMoF25skFKG5o6cSL/OlOO6eU crio-git-byte
    
 ##### [Adding SSH key to Gitlab](https://youtu.be/mNtQ55quG9M)
  + ssh -T git@gitlab.com (use this tto test connection to gitlab)
 __________________________________________________________________________________________________________________________________________________________________________
 #### Milestone 1 (Get that Code)
  + mkdir -p ~/workspace/bytes
  + cd ~/workspace/bytes
* Ensure you clone using the ssh link and not the https link
  + git clone <add-ssh-link-here>
  + git clone git@gitlab.crio.do:COHORT_ME_GIT_BASICS_ENROLL_1596802014715/ram75353-ME_GIT_BASICS.git
    * Cloning into 'ram75353-ME_GIT_BASICS'...
    * warning: You appear to have cloned an empty repository.
  + cd ram75353-ME_GIT_BASICS (to move to my github proj)
  + git status (to check status)
    * On branch master
    * No commits yet
    * nothing to commit (create/copy files and use "git add" to track)
  + crio-user@ram75353:~/workspace/bytes/ram75353-ME_GIT_BASICS$ git remote -v
    * origin  git@gitlab.crio.do:COHORT_ME_GIT_BASICS_ENROLL_1596802014715/ram75353-ME_GIT_BASICS.git (fetch)
    * origin  git@gitlab.crio.do:COHORT_ME_GIT_BASICS_ENROLL_1596802014715/ram75353-ME_GIT_BASICS.git (push)
  
##### References
1) Git Cheatsheet (https://education.github.com/git-cheat-sheet-education.pdf)

2) A Short History of Git (https://git-scm.com/book/en/v2/Getting-Started-A-Short-History-of-Git)

3) Branches in Git (https://www.atlassian.com/git/tutorials/using-branches)

4) What is the git folder? (https://stackoverflow.com/questions/29217859/what-is-the-git-folder/56145562)
 _______________________________
#### Milestone 2 (Add new Changes)
  + Open Folder 'crio-user@ram75353:~/workspace/bytes/ram75353-ME_GIT_BASICS$' and add file 'First.txt'
  + 1 ) **git add 'First.txt'(Filename)**
  + A commit is like a checkpoint in Git where we save the current state of our files. (2)**git commit -m "comment"**) (If no comments -> Aborting commit due to empty commit message.)
  + 3)**git push -u origin master** (To Add the changes and file to repository)
  + If got some error like this  "! [rejected] master -> master (non-fast-forward)" use the following command  "**git pull --rebase origin master**"
  + **git log** to see the 

##### References
  
1) Git: Add All Files to a Repo (https://stackabuse.com/git-add-all-files-to-a-repo/)

2) Commit message style guide (http://udacity.github.io/git-styleguide/)

3) The Git Commit Hash (https://www.mikestreety.co.uk/blog/the-git-commit-hash)
  
______________________________________________________________________________________________________________________________________________________________________________
#### Milestone 3 (Being in Sync)
  
  + Add a Readme.md file in GIT LAB UI
  + Now if you try to push from local to clone it will throw an error like (CONFLICT (content): Merge conflict in README.md)
  + So, Pull the latest code from repository to local "**git pull**"(it will update in local)
  + After use "**git push**" from local to move to repository.
  
##### References
  
1)Git Pull Explained (https://www.freecodecamp.org/news/git-pull-explained)

2)"Remote contains work that you don’t have locally" error explained (https://blog.plover.com/prog/git-ff-error.html)

3)Other ways to resolve the "Remote contains work that you don’t have locally" error (https://stackoverflow.com/q/24357108/9734484)  
______________________________________________________________________________________________________________________________________________________________________________
 #### Points to remember
  + There’s another command, git fetch. How’s it different from a git pull?
git fetch fetches only metadata related to changes and doesn’t actually make any changes to the project files we have locally. We’ll need to do a separate git merge for that whereas git pull naively speaking does both **git pull = git fetch + git merge**
Further reading
-----------------
Git offers several more features which help in maintaining code and collaborating with team members during software development. For example - config, branch, stash, squash etc. You can explore these as needed.

+ What is Version Control? (https://www.perforce.com/blog/vcs/what-is-version-control)

+ Oh Shit, Git!?! (https://ohshitgit.com/)

+ The Advanced Git Guide (https://www.toptal.com/git/the-advanced-git-guide)

Excited? Dig deeper to Git internals for answering the below questions

+ What actually happens within Git when we do a commit? (https://dzone.com/articles/git-behind-the-curtain-what-happens-when-you-commi)

+ Each commit gets a unique ID, how is it created? (https://blog.thoughtram.io/git/2014/11/18/the-anatomy-of-a-git-commit.html)
______________________________________________________________________________________________________________________________________________________________________________
## Developer Tools 1
#### Get started using Chrome Developer Tools
  + 

