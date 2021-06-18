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
  + 1) **git add 'First.txt'(Filename)**
  + A commit is like a checkpoint in Git where we save the current state of our files. (2)**git commit -m "comment"**) (If no comments -> Aborting commit due to empty commit message.)
  + 3)**git push -u origin master** (To Add the changes and file to repository)
  + If got some error like this  "! [rejected] master -> master (non-fast-forward)" use the following command  "**git pull --rebase origin master**"
