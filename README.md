# GitCommands

###### Git Commands

touch file-name (to create a file)

git init (to intialize a git repository) (.git file will be created by this)

//(to add name and email to the git)
git config --global user.name 'name'

git config --global user.email 'email'
//

git add file (to track the file)

git status (to check what is tracked or what is untracked or which file is modified)

git rm --cached file-name (to untrack)

git rm file-name (to delete file)

git add *.extention (to track this type files)

git rm *.extention (to remove all tracked this type files)

git add . (to track all files)

git commit (after pushing i key to insert, remove # from initial commit then write a commit, then esc, then :wq)

git rm flename -f (to remove file from folder)

###### After changing any file 

git add .

git commit -m "commit"

touch .gitignore

touch filename (if its included in .gitignore file, during the push or add and commit, it won't be changed or pushed to github repository)

###### Branches

git branch branch-name (to create a branch)

git push origin --delete branch-name (to delete a branch from repository)

git checkout branch-name (to switch any branch from any other branch)

git merge branch-name (to merge any branch history to any other branch) (then i (insert), then commit, then esc, then :wq then enter)

###### Pushing this created folder into created github repository

git remote add origin https://.......git

git push -u origin master

###### After creating a new repository at github

git init

git add READ.md (optional)

git commit -m "first commit"

git remote add origin https://.....git

git push -u origin master


..... or push an existing repository

git remote add origin https://....git

git push -u origin master


touch READ.md (to create READ.md file)

git add .

git commit -m 'Added readme'

git push (to push this changed file to github repo) (if ths is master branch)

###### Cloning

git clone https://github.com/.......git (url from clone or download address)


****** if laravel project then

composer install

php artisan key:generate

###### to pull

git pull origin branch-name (to pull the changed history of any branch)

From any branch

git checkout branch-name (if master then 2nd one is another one)

git pull origin branch-name (if anybranch then this can be master or another)

git diff branch1..branch2 (to check the differnce between two branches)

git log branch1..branch2 (to check the changed commits between two branches)

git diff branch1..branch2 --file-name (to check the differences between two files of two branches)

###### To check the branches

git branch

git branch -r (to check the branches in which remote branches are included)

if any file is created from any branch, is not tracked. (git add ....)

After creating any branch and switching all files from untracked branch will be added to the new branch, then add then commit then push.

****** if command window

i (after changes, press esc)

:wq

****** if not command window (showing (END))

:q

###### before pushing if you have committed then you have to push

****** to get all files from another branch if your files of master branch are removed during tracking

git log --diff-filter=D --summary | grep delete (deleted files list)

git rev-list -n 1 HEAD --file-name

git checkout $(git rev-list -n 1 HEAD --"$file-name")^ -- "$file-name"

if you are using zsh and have the extended-Glob option  enabled, the caret symbol won't work, you can use ~1 instead

git checkout $(git rev-list -n 1 HEAD --"$file-name")~1 -- "$file-name"

****** to remove file from repository of github

@ if you want to remove the file from the git repository and the filesystem also, the you have to use

git rm file-name

git commit -m "removed file-name"

But if you want to remove the file only from the git repository and not remove it from the filesystem, then you have to use

git rm --cached file-name

git commit -m "removed file-name"

then

git push origin branch-name

###### To delete .git

rm -rf .git

###### Forking

## After cloning

git remote -v (to check)

git remote add upstream https://..... (to add a new remote repo address)

## Migrating one specific table

php artisan migrate:refresh --path=database/migrations/filename.php

###### New and old php version problem

composer clear-cache

composer self-update

composer update --ignore-platform-reqs

or

composer install --ignore-platform-reqs


then done .....

Source : Youtube git and github crash courses

https://www.youtube.com/watch?v=SWYqp7iY_Tc

https://www.youtube.com/watch?v=RGOj5yH7evk&t=147s

https://www.youtube.com/watch?v=xuB1Id2Wxak

https://www.edureka.co/blog/git-commands-with-example/#git%20config

https://dev.to/mariorodeghiero/git-cheatsheet-2imn

https://www.w3docs.com/snippets/git/how-to-delete-git-repository-created-with-init.html
