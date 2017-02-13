#How to use Git#

This will have a short description about we can do with Git and how.  
Make this not your only source to learn git there is ALOT of documentation out there.
NOT ALL COMMMANDS ARE LISTED IN HERE  

Or by simply typing,  
`git`  
You will get a summary of commands you can use.  

##The Git command line interface##

These functions require you to be in a command line interface that can be used with Git.  
Like the Terminal on Mac/Linux or CMD/Git Bash on Windows.

You have to be in the root folder of the project where the hidden folder .git is located.  

###Configuring before using###
To use git you have to configure it first.  
Set a username and user email to begin with so everyone knows the commit came from you.  

Setting a username (Replace 'John Doe' with your name)  
`git config --global user.name "John Doe"`  

Setting a user email (Replace 'johndoe@example.com' with your email)  
`git config --global user.email "johndoe@example.com"`  

###Cloning###
Cloning a repository could be helpful since its literally downloading a repository.  
So you can work locally on a project and contribute code to it or just use it for your own use.  
Cloning requires a URL from something like Github or Bitbucket it can be cloned by HTTPS or a SSH connection.  

You have to browse to the project you want to clone on one of these tools and find a URL once you got that use.. (without brackets)  
`git clone [URL]`

It will clone the project into a folder named after the project

###Initializing/Creating repository###
If you want to make a new repository we advice ou to create a folder with the repository name you have in mind,  
then go into that folder and use the command.  
`git init`  
This will make the .git hidden folder and you are good to go!

###Checking the status###
With the Git status command you can see in short what is different from the local repo.  
It also shows all the files that are modified, untracked or in the [staging area](https://githowto.com/staging_changes).   
`git status`  

###Adding files to staging area###
With this command you can set modified or untracked files to the staging area ready for the commit.  

First of all if your files is already tracked then you can simply change the file and save it once you changed it it will be noted as 'modified' in the 'git status' command log.  
Then you can either add that modified file or track a new file with the command, (without brackets)  
`git add [filename]`  

Add multiple files by using a space between the files,  
`git add index.html app.js`  

To add all untracked and modified files at once use,  
`git add .`  

###working with branches###
Branches can be really useful to write and save code while not touching the main code.

Making a new branch can be done like this,  
`git branch [branch name]`

Select your branch with the 'checkout' command  
`git checkout [branch name]`

You can now edit/add code without touching the master.  
After you are done you need to commit the changes from your branch just like you are used to,  
`git add [file name] `  

`git commit -m "added new features to the branch"`


After this you can merge it into the master,  

First select the master branch,  
`git checkout master`

Then merge the branch,  
`git merge [branch name]`

You can now delete your branch.  
This can only be done if you don't have unmerged chances,  
`git branch -d [branch name]`

deleting your branch without merging,  
`git branch -D [branch name]`
