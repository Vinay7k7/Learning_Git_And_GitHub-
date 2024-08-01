# This is the `My_Git_Journey!`
>  ^_____^  This is a vary basic notes on how to use the Git in your Life !

## There many ways to use the git !
### 1) ----- First time using Git in your Local Syatem !
#### While you are doing this first time then follow this steps (After Downloding the Git )!

#### A) --- To check the Git verction in your system !
		$ git --version
#### B) --- First you have to set the user_name for your git(in your system ) Same name as the username as your github !
		$ git config --global user.name "Vinay7k7"
##### From the above you have got a doubt that what is the --global it is nothing but the higher imp account which is yours that you use more often ! if not you can set the local user.name if you are using the other account :)
#### C) --- After theat you need to set the email fo your github account !
		$ git config --global user.email "knightkings77@gmail.com"
##### Just like the user_name you can set the local email as well !
#### D) --- If you want to cross check this then you can do this !
		$ git config --list 
#### NOTE:- While you are doing this first time the git will ask you to give access to this :)


### 2) ----- When you are use the git to copy the ripo from the github into your local_system !
#### You can find the HTTPS lisk of that repo that you wanna copy from the github !
		$ git clone https://github.com/Vinay7k7/MY_PORTFOLIO.git

### 3) ----- You have made some changes in the repo thst cloned into your system !
#### Then again if you want this changes to reflect in the github then you have to push this locally made changes to the github !

#### Before pushing the changes from the local to the github there some steps to follow 

#### A) --- First you need to move the newly created the changes to the staging place 
		$ git add file_Name
#### 			`OR`
		$ git add .
##### This the `.` in the second command will move all the changes in the all the files in that 
folder to the staging place ! If you get any error like converting the LF to CRLF you can run this !

		$ git config --global core.autocrlf true
#### B) --- Then you can verfy the what stage the chnages are in by using
		$ git status

#### C) --- Then you have to puch the changes to the local repo in your system !
		$ git commit -m "_Any message that you wanna give on those changes !_"

#### D) --- Then now we have to commit this local changes to the Remote Repo in the GitHub !
		$ git push origin main
##### In this the The Origin is nothing but the name of our local copy that you have in the github and the main is the branch in the github that is where we are pushing this changes too !


### 4) ----- Trying to create a new repo in local and pushing the local repo to the GitHub !
#### In this we will first create the new repo in the github !

#### A) --- First you need to create the new folder in the local system and enter in there and make that folder into git folder using !
		$ git init

#### B) --- Then you can check if we maid this folder in to git folder or not using !
		$ ls -a
##### If you found the .git file then it means it is a git folder !

#### C) --- Then you can add all the files in that folder to the staging place using !
		$ git add .	

#### D) --- Then you need to push this changes in your staging place to the local repo using !
		$ git commit -m "_Any message that you wanna give on those changes !_"

#### E) --- Then you need to link your local repo to the github repo using !
##### But before moving to the push command you need to do some steps to our newly created repo in the github !

#### F) --- Connect the github repo to the local using !
		$ git add origin main https://github.com/Vinay7k7/Learning_Git_And_GitHub-.git
##### The link is the newly created repo in the github !

#### G) --- To verify if the new repo is in the local you can check that using !
		$ git remote -v

#### H) --- To know what branch we are in we can use this !
		$ git branch 
##### This above command will show `master` which is the name of the main branch in the github ! ( We can change that uisng ! )

#### I) --- Now we are changing the branch name into the `main` !
		$ git branch -M main

#### J) --- Now we can puch the local repo to the github repo !
		$ git push origin main
##### You can use `git push -u origin main` what this make is that when ever we are pushing the changes again after that we can just use `git push` this time !


### 5) ----- Now we have made some changes in the files or a folder in the github(remote) then you need this changes to reflect in the local folder !
#### There are two ways we can do this 

#### A) --- First we can use the pull command to bring the changes from remote to the local !
		$ git pull origin main
#### B) --- If you need more control over what you commit to the local copy then you can follow this steps !
		$ git fetch origin
  		$ git merge origin/main
#### This will have more controle over to you !
