# GIT WORLD


## what is git ?
VCS can handle s/w versions , which allow devs to contibute to the same project , __revert changes__ , collaborate to **create new feature**  
and it allows to __track the changes__

# Befor git ? 
Devs use CVCS but those systemd had limitiaions and make a lot of backup of entire codeBase 
## now let's begin with the Concepts 

- Repo :
  is a container contain the files of a project with the help of the repo u can track the changes
- Push :
    to upload the code to the desired repo u can push code or branch **while be explanied up next**
- Pull : to get the project from the remote
- Branch : u can use branch when you need to make testing or add new feature without affect on the original copy
- untracked : server has no info about it u should  commit them 
- remote repo :  company'server where Devs pushe the code , github-gitlab 
- commit : after  finishing a feature fix bug ,etc like a checkpoit in ur local repo 
- tag : like a bookmark
- Annotated Tags : like bookmarks to tag an important commits you can mark it as a version and name the version with it's number insted of wasting hours searching in logs 
# how to create a repo 
- first choose the PATH : cd /PATH/TO/FILE
```
git init "repo_test" 

```
# get info about files :
```
git status
```
then you will get the info about the files if u hadn't commit anything yet , so it will get u the untracked msg 
first step you need to stage the changes 

___git add___ command put the fiels into staging area to be tracked 

```
git add <file_name> or use . if u wanna add all files in the file you are in
```
## remote : 
the version of the repo that hosted on a server or other location like github , gitlab outside ur local machine 

- to view remotes
```
git remote -v
```
if u get a blank space then u need to add ur remote by 
```
git remote add origin <repo_url>
```

let's assume that u get an idea and u need to test it away from the original repo , so u need to create new branch with 
```
git branch <Branch_name>
```
when u are done with ur new branch u need to merge the branches by 
```
git merge source 
```
- to switch to the branch you have created
  ```
  git swtich  <Branch_name>
  ```
- delete a branch
  ```
  git branch -d <branch_name> 
  ```
you need to mark a specific commit so u need a tag 

- first choose the commit by __git log___
then
```
git tag -a <Version-name> <commit-hash>

```
replace the version_name with yours 
to list the tags avaliable in the repo 
```
git tag
```
if u done tagging push the tag to remote 
```
git push origin <tag-name>
```
| Command | Description |
| --- | --- |
| git clone <URL> | clone ur local to remote  |
|git init <repo_name>| create a repo |
| git status | List all new or modified files |
| git add | command put the fiels into staging area to be tracked |
| git commit| save your changes to the local repository. When you make changes to your project add -am for comment|
|  git add . -A | is used to stage all changes in your working directory  |
| git remote -v| to view remotes|
| if u get a blank space then u need to add ur remote  |git remote add origin ___<repo_url>___ |
| let's assume that u get an idea and u need to test it away from the original repo , so u need to create new branch with| git branch <Branch_name> |
when u are done with ur new branch u need to merge the branches by| git merge source |
| to switch to the branch you have created | git swtich  <Branch_name> |
|delete a branch | git branch -d <branch_name> |
| you need to mark a specific commit so u need a tag | git tag -a <Version-name> <commit-hash> |
| replace the version_name with yours to list the tags avaliable in the repo |  git tag |
|if u done tagging push the tag to remote  |  git push origin <tag-name> |
|fetch changes  | git pull <url>|
| git stash  | command is used to temporarily save changes that you don't want to commit at the moment |assasasa
| git stash pop |  to apply changes from last stash it's oppiste of git stash |


aannn
