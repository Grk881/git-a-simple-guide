# git-a-simple-guide

                                                 Git and github

-	The fundamental core concept of git and github is version control system
-	GIT is a distributed version control system and source code management (SCM) system with an emphasis to handle small and large projects with speed and efficiency. 

-	So,  the primary concept of version control system is two things
It addresses two major problems
1-	Sharing of code 
2-	Versioning

•	Sharing –      suppose working in a organization , and there are two developers in organization . 
Lets say devloper1 & developer 2 now what happens usually is both of them working on same team & they are working for same application.    Ex – calculator application

So  , dev1  is write for a addition functionality & dev2 is write for a substarction functionality
Then dev 1 is happy with addition code and dev 2 is happy with sustraction code.
But end of the day build calculator they have to get both of there code together 
And then they have to build comman application.
-	So ,  the comman application will hold the code for both , now share your code within each other and build a centralised application or one comman application.
-	In real world scenario you have thousand of these files and packages it is practically impossible , there dependency files , jar files 
•	versioning
-	So , sharing is not that easy that is one major thing that version control system addresses 
-	So there was changes in a codes , so go back to 10 days 20 days for that you need very strong versioning in place
-	Ex- usually on day1 modified 100 files, day2 just modified 30 files on day 3 modified 50 files
Keep track of these files is versioning
So somebody come and ask what is change that 3 days back 100 files that you modified just scrap your day2and day3 files , so that’s why we need versioning

•	Version control system 
-	Cvs  - centralized  
-	Svn -  centralized 
-	Git  -  distributed

-	Difference git and svn 
Scenario 1 -  centralized 
There is both dev1 and dev2 are use to cummunicate each other there is central server that is svn that is centralized version system everything happen in a central place.
Scenario 2 -  distributed
So ,  there is a dev1 and dev 2 
Dev1 can do is if he wants to share a code to dev2 he can either do through distributrd v,s and dev 2 can pick it
-	Or create a copy of these files in  distributed v.s
-	Create multiple copy’s in distributed v.s
-	Devlopers are cummunicate each other using theire copy’s here

•	What is FORK
-	Fork is nothing but , you create entire copy of your original source

•	Git vs Github

-	Git – git is open source
-	Git is distributed version system
-	Any organization can download git and implement the git in there organization
-	Create ec2 instance and in this instance installed git ,  every developer  has to commit to changes in git server

•	github

-	But thre are organizations absorb the gap and they have built better solutions 
In terms of 
-	Usuability
-	Issues 
-	Commenting
-	Talking to peers
-	Reviewing the code 
-	Github also support project management
-	Github has done they built solution on top of git
-	Same thing applys to gitlab or bitbucket they improvising the existing git

•	Installation git in ubuntu

sudo apt update

sudo apt install git

git –version

•	Steps of git to push files in 
git config --global user.name ""
    git config --global user.email ""
    git init
     nano myjava.java
     git remote add origin giturllink
     git add .
     git commit -m "first commit"
     git push origin master
     git push origin master --force


•	Git commands

Task1 -   create folder  
-	         Mkdir example.com
-	            cd example.com/
-	vi calculator.sh
-	ls
 
•	(create a repository )

-	git init                           (initialize empty git repos)

-	( to show a git repo )

  ls -la

.git (  it is a  hidden folder ,  essentially git tracks using .git ,  to delete this folder it means entire repo not track

git status
-	Suppose some changes in file ( vi calculator.sh (a+b+c+d)
To show this changes in files are git status
Changes to be commited    ( new files : calculator.sh )
              git diff
-	Using git diff show exact changes in files

•	git add calculator.sh
git status
( changes to be committed)
git  commit -m “this is my second version”
git log


•	Git branching strategy

Branch -  branch is nothing but a separation
Creating a branch because any new changes or huge changes or breaking changes
That adding to a existing application is not affecting the existing functionality

-	 Example-  suppose uber is an application they was only supporting cabs 
But one day uber said that is to get many customers they want introduced bikes 
So they want to add uber bikes , so this cabs working fine , but the develepers
Are not confident about bike functionality introduced will it affect the application 
Deliver to customers .
-	Usually they do is they crete a new branch for bikes , they continued to the application testing  and once they are confident they will add this  thing to uber application and previous branch will be deleted
So this is the reason we create be branches in git


                           GIT AND GITHUB


GIT/GITHUB
1) sudo apt update 
2) sudo apt install git -y 
3) git --version : to check git version.
4) git config --list : 
5) git config -- global user.name  "username"
6) git config -- global user.email  "user-email" 
7) mkdir dir-name
8) cd dir-name 
9)  git init: gives hidden and helps in tracking. 
10) git pull git_hub_link(http): use to pull resources for repository 
11)ls
12)git status  : shows status of present stage.

--------difference between all stages--------------------
13) git diff working area to stagging area 
14) git diff --staged : stagging area to committed area
15)git diff HEAD : committed area to working area 

------------------------------------------
16) git difftool working area to stagging area ,shows two windows
17) git difftool --staged : stagging area to committed area, shows two windows
18)git difftool HEAD : committed area to working area, shows two windows 
19) sudo nano .gitignore : create file and add files that need to be ignored.

20) git reset HEAD code.txt : restore from stagging to working area ,
21) git reset HEAD : revert from committed to working stage
22) git log : gives descriptions of commit, like committed id, author , date and number of times committed.
23) git log --oneline : describes in in-short.
24) git log -p : details information about all log with commit
25) git status -s or git status --short: gives stage status in short 
26) git log --since="1 week ago" :for check last one week logs, can change time. 
27) git reset --soft HEAD~1 : committed message will be deleted and file back to working stage.
28) git reset --hard HEA~1 : 

29) git revert <commit id>: file back to working stage from central repo.
30) git restore filename : need  to restore file that came from central repo.

40) git tag "message" : will add tag to commit , by default gets assigns to latest commit.  
41) git tag "message" <commit id> : will add tag to particular commit with id .
42) git tag : to see assigned tags. 
**note : one commit multi tag.
43) git push origin tag 
44) git  tag -a v1.1 -m "mytag" : will  assign tag and a message to commit. 

--------------BRANCH-------------------------------
45) git branch testing : for creating of new branch
46) git branch : show list of all branches.
47) git checkout branch_name: to switch between git branches.
48) git remote show origin : shows available origin
49) git push origin origin_name : sends files to particular origin.
50) git branch -d branch_name : will delete branch.
51) git branch -D branch_name : will delete branch forcefully.
52) git branch -b branch_name : will create branch and switch to it 

--------------------stash-------------------
53) git stash list : will show list of all stashes stored in repo.
54) git stash : it will stash or temporarily save current progress.
55) git stash applies : will bring back the stashed data to file, will bring latest one.
56) git stash clear : will clear all the stashed changes.
57) git stash pop : will apply to the most recently stashed changes and remove them from stash list.
58) git stash pop id : will apply to the most recently stashed changes and remove them from stash list for particular id   
59) git stash show -p stash@{id} : will show stash data of particular id.

60) git reflog: used to review history in reference updates in local repo.
61) git branch branch_name commit_hash : will retrieve the deleted branch (commit_hash can be found in git reflog)
-------data pull variation--------

git pull  --> All data of branch (master)
git fetch --> current project (only particular project){git init and pull  done default}
git clone --> all branches ,all files

--------push commands----------
1) git add filename or git add . : add files to stagging stage from working stage (can rollback from stagging stage)
2) git commit -m "message": creates a snapshot of file and is ready to send central 
3) git remote add origin master : need to do only once .
4) git push origin master : to send to files to central.

------trouble shoot commands-----------
1)git remote set-url origin http/your-gitlink
2)git remote set-url origin git/your-gitlink
3)git config --global credential useHttppath true
4) git rebase origin/master  

---------windows to github----------------
1) search for  "git bash for windows" and install it.
2) create folder "myfolder" 
3) right click on myfolder and click "open with git bash"
4) git config --global user.name "username"
5) git config --global user.email "email"
6) git init

note:- other pull commands are same.
note:-  gitbash has master not main.

------------------------------------------
1) git config --global: ubuntu level permission , no permission required once given even if second repository to be pulled 
2) git config --system : root / multi user config , need to give for per user 
3) git config : used only for specific project .
