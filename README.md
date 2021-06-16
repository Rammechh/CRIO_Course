# CRIO
## Started Module 1 in CRIO
  + Git Basics
    * Attached file (Git_Basics)
### Githab Repositories
  + git@gitlab.crio.do:COHORT_ME_GIT_BASICS_ENROLL_1596802014715/ram75353-ME_GIT_BASICS.git
  + https://gitlab.crio.do/COHORT_ME_GIT_BASICS_ENROLL_1596802014715/ram75353-ME_GIT_BASICS.git
    * To download/upload contents from/to the above Gitlab repositories you’ll have to prove you’re having access to it.
    * Execute the below command to generate an SSH key. SSH protocol allows you to remotely access machines using the SSH key.
    * SSH -> SSH or Secure Shell is a network communication protocol that enables two computers to communicate
    * **ssh-keygen -t ed25519 -C "crio-git-byte"** [ssh-keygen Codes](https://www.ssh.com/academy/ssh/keygen)
    * Did you notice you were given two links to your Gitlab repository earlier? The one which starts with git@gitlab.crio.do is to be used to authenticate using SSH. The https link authenticates using your gitlab.crio.do username and password Execute cat ~/.ssh/id_ed25519.pub and copy the public key printed. You’ll add this to https://gitlab.crio.do/ in the next step

    * crio-user@ram75353:~$ cat ~/.ssh/id_ed25519.pub
      ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIL3J0omWRsa8BM7Ft6FyMoF25skFKG5o6cSL/OlOO6eU crio-git-byte
    
 ##### [Adding SSH key to Gitlab](https://youtu.be/mNtQ55quG9M)
  + ssh -T git@gitlab.com (use this tto test connection to gitlab)
 
 #### Milestone 1
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

