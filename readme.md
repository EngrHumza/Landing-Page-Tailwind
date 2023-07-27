

npm i -D tailwind css

npx tailwindcss init

in tailwind.config.js

content: ['./*.html'],

In global.css 
@tailwind base;
@tailwind components;
@tailwind utilities;

tailwindcss -i ./global.css -o  ./css/style.css --watch can write in terminal to generate css

in package.json:
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build":  "npx tailwindcss -i ./src/input.css -o ./dist/output.css",
    "watch":  "npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch"
  },

  insted of writing in terminal write it in scripts

'tailwindcss' is not recognized as an internal or external command

Solution
Install postcss and postcss-cli

npm install postcss postcss-cli

<!-- Git -->
version control system
git and GitHb are different

git --version

Once the installation is complete, then you have to go to the terminal, it can be anyone.


For example, I windows you can go in 'command prompt' , or if you have installed Git, then Gitbash would have been installed with it.


so, You can open Gitbash. And you have to write 'git --version'. With this you'll be able to know if your Git has been installed properly or not.

We have to tell it our name and email id. so that if you change in any line, others will know that you have changed in this line.

So, you have to tell your Git name and Git email ID. So we'll set that. To set that, the command is' git config'. So there is a config file of Git, in which we change all these things.
2:18
'git config --global' So this will be the command. You can change your name here. and click 'enter' , your name will be set. Similarly we have to set the email Id, so I'll set my email Id as well.

git config --global user.name <'Your Name'>
git config --global user.email <'Your Email'>

and I'll put my email Id here. So, my name and email Id has been changed. 

You have to check if it actually did or not.
So for that, you all will write the command ' 

'git config user.email'. 

and if your named is being ECHOED, but email is alright.
Installation of Git

There is another way to change them 'git config --global --edit

With this you can directly make changes in the config file. So here mediator will get open. and now you can directly change here, just like my name and email Id.

and after you saved your change, you have to escape and 'colon W Q' and you'll exit from the file.
Setting up Git

There are 2 ways to set. Now you know that your name and email ID has been completely changed. Now we can start making projects in it.

 You can use it in any type of projects and files, either Python, java, c++, It doesn't matter.

Lets make a new project. -- 'make directly'

And if you didn't understand the command, then from the command 'makedir' you can make a new folder.

Then with 'cd' you change the directory. So I made a new folder. Then I came inside it and I have also opened this folder in my Visual Studio Code.

We can also make repository in it. In Git, we have the concept of repository.

Repository means the project that can be tracked through Git. So, if you want to make this folder a Git repo, then you have to write the command--- 'git init'.

'git init' will initialize this folder, so I'll press enter. so here it's written - "Initialized empty Git repository'' and it has made an empty repository inside this path.

so a file named '.git. is created in it through which you know that it contains the files which is being tracked by git.
4:42
Its being created and we don't ever have to do the changes in it. But this file exits here. Lets code something in this project and make a new file in it.
4:50
lets call it 'Sum.java'. This is a very basic Java file and I'll do a small java code in it.
4:57
So I have done the code changes here. I haven't done anything dynamic, basically I have taken 2 no. and their sum.
5:02
You can do it in Java just as I have done, or in html, css, javascript, in any language, basically you just need to have a file.
5:10
The first command will be 'git status' which tells you the status about the changes made in this repo.
5:18
what modifications have been done, which files have been deleted, which files have been changed. You can tell all of it through this command 'git status'.
Creating a Git Repository
5:26
So, 'On branched master' that is how the branches are set. I'll tell you later on. Till now you have not done any commit, so we'll do that. But before that you can see that it says- Untracked file'
5:36
and it says- use 'git add ' to include in what will be committed. Here the concept will be of 'staging'
5:44
Firstly, we are not tracking any file. In git first of all we track the file and then commit it.
5:50
let me add it first because it says. So 'git add Sum.java'.
5:56
If we do 'git add Sum.java' then our file start to be tracked on. Lets check through 'git status'.
6:02
It is said- new file Sum.java. Earlier it said that the file was untracked but now its being tracked.
6:08
now this file is under the staging area. The concept of 'staging area' in git is amazing.

It is the area where you you can hold your changes before finally committing.

There might be 30-40 files in your project, which is to be committed.

But you want that there should be 10-15 files in this commit, so you'll put those files in the staging area

and from there your files will be committed. so, first we put our files in the staging area and then the files are committed from the staging area.

So files enter the staging area through the command 'git add' and then move out to be committed through the command 'git commit'.

So we did' git add', therefore or file 'Sum.java' has entered the staging area.

It has entered the staging area, now we'll commit it. To commit, the command is- 'git commit -m ''initial commit''.

Basically this is your command, through which it'll be committed This were the changes and insertions in the file and it has become a commit.

If you want to see the amount of your commits until now, then the command is 'git log'. Which is used to see the no. of previous commits, who did, where, and we get all the information here.

For example, here, this author did this commit on this date, at this time. A hash code is generated for all the commits. 'Unique'
Git staging area
7:29
so, this is the information of the commit. As you'll commit further, the git log will become bigger.
7:35
Lets come to the 'git commit' command. here '-m' means that you'll be writing a message after it.
7:42
If you'll ignore '-m', then somethin like wing or nano will open. So put '-m' and then your message in the double quotes.
7:51
And this message should be meaningful. By this message one should know what you have changed in it.
7:57
So what changes are you making in this file, in this commit or what are you changing in a feature, everything should be known
8:03
so that if someone checks it later what was done and where, then he should know it clearly that this change was done in this commit.
8:09
So, I'll do a minor change here. Let me put a message here. We'll check it again what is coming now.
8:16
So, I'll do 'git status'. You can see that it says here 'modified Sum.java' which tells you the files that were modified.
8:23
Now lets add one more file in it. So I'll put Diff.java.
8:28
and lets not change anything for now. So, you can clear all of the terminal by using the command 'cmd +k' and then I'll do 'git status' again.
8:37
Its written here 'modified Sum.java' and untracked file is 'Diff.java' So git doesn't known that the file 'Diff.java' exits aa well.
Git commit
8:46
So lets add this as well. So 'git add Diff.java'. Now the file 'Diff.java' has entered the staging file but Sum.java has still not entered.
8:57
You can check again by 'git status'. So you can see that, since this file is committed and this file is modified, which means
9:05
if you want then you can commit now, but only file 'Diff.java' will enter.
9:10
'Sum.java' wouldn't. So I'll commit here. 'git commit -m'. Your terminal wouldn't have this auto complete, for this we have fish shell
9:19
I'll give its link, when you install it then the auto complete will be applied here.
9:24
I'll change this commit message here. 'adding Diff.java' this is my message and I'll commit this.
9:30
Then when you do 'git log', you can see that there are 2 commits. One is the recent one- adding Diff.java and this is the previous one. Both of their hash codes are different.
9:41
Your HEAD is right now, which is basically a pointer. It moves on form commit to commit.
9:48
So, right now it's on this commit. So, I'll clear this again by 'cmd k' or even by 'clear'
9:54
And now lets do 'git status'. If I am writing correctly, fine. So here the modified file is 'Sum.java'.
10:01
So the modification for your file are still not committed, so lets add this as well.
10:06
'git add Sum.java' or you can also write 'git add.'
10:12
By dot(.) all the files will come in the staging area. All the modified and newly created files have entered in the staging area and we can commit them together-- 'git commit -m'
10:25
It has been committed here, lets check it by 'git log'. So now there are 3 commits, right!
10:30
You can go in all the 3 commits, if you want then you can go on directly to this commit. So, now lets talk about how you travel between commits in different commits.
10:40
the one which I told that you can discard all the changes, lets deal with it. So, right now you have Sum.java and Diff.java and there are 3 commits.
10:49
You want to go on to the 31st commit, when initial commit was dome. so, for that the command is checkout command. For that you just need to copy the hash code.
10:59
We'll write 'git checkout' and then I have pasted the hash code.

git checkout <hashcode> //it will discard the changes 

After that I'll enter and you can see that 'Diff.java' has been deleted.
11:15
And 'Sum.java' has come back to previous changes, the first commit that we had. So this is the benefit of checkout through which you can go back to any of your changes.
11:23
If you want to go back to the previous one, the you'll write 'git checkout master'.
11:32
So after doing 'master', you'll come back to master and the files 'Sum.java' and 'Diff.java' are recovered. Lets understand this 'checkout' command a little more clearly.
11:39
So, I'll clear the terminal again. lets go back there again. So I went to the previous command and 'Diff.java' is again deleted and we are back in 'Sum.java'.
11:51
Now we'll do 'git branch'. Slowly we are diving in the concept of branch. So now,
11:57
HEAD is in this branch which is the master branch. So, I told you that you always start from a master branch inside it.
12:05
now you make multiple branches in it. The 'checkout' command helps in moving from branch to branch.
12:14
So 'checkout' command is for that and now you are inside this commit. I'll do 'git log' once.
12:22
You can see that only one commit is visible as you are inside this branch, which had only one commit in it.
12:28
You must know it already. All the 3 commits were in the master branch, if you want to see those changes then you have to switch towards the master branch.
12:35
'git checkout master' which will lead me to the master branch.
Git checkout
12:41
With this I am back at the master branch and all the changes have been recovered as well and if I'll do 'git log' then I can see all the changes.
12:50
So this is the benefit. If you want to change something in previous commit or you want to make a new branch from there, you can do that as well.
12:57
So lets see how to make a new branch. lets learn about branch, waht is its concept! It has a master branch in it, you can multiple branches from it as you like.
13:06
and you are basically doing the same in the production, If you go in any organization, they ahve multiple branches where every one their own feature in their branch.
13:14
When you work on any project, and you want this feature to work in another branch, this feature in other one which means
13:20
You are making a feature wand you want that other features don't get affected.
13:25
Because work is still ongoing, until it gets stable, production usable, till then it shouldn't have direct affect on other features.
13:33
For that you create a new branch and start you work there. and all your changes are inside the new branch, and other branches don't even know about that.
Git branch
13:42
You can make multiple branches from a single branch inside it. So a tree like structure is basically constructed
13:48
There is a master branch and you can make multiple branches from it. So, in production, company has master branch and then there is a Develop branch, which has been derived from then master branch itself.
13:56
Method to make that is - 'git branch' , so I'll give the name of the branch as -- 'dev'.

git branch <branch_name>

14:04
So a 'dev branch' has been created. If you want to check then you can write 'git branch'
14:09
So now you have 2 branches here-- dev and master, right! If you want to go to 'dev' the write -- 'git checkout dev'
14:18
So, now you have switched to dev branch. As you can see earlier 'master' was written in the bracket but now its 'dev'.
14:24
So now you are in the 'dev' branch and now you can make any changes in it. But I'll recommend that you make another branch
14:32
and name it according to your feature. So I want to add a multiply feature. I'll make another branch in it, so there is another method.
14:41
You can directly do 'git checkout -b' through which a new branch will bc created and you can directly checkout in it as well.
14:50
So, 'git checkout -b anuj/multiply'. Why am I not writing multiply directly?
14:57
Basically this is the name of your branch because I want all the users to follow this convention.
15:04
First they'll write their name and then the name of their feature, which helps us to know who has worked on which feature.
15:10
So now in this branch you can see 'anuj/multiply' and I had made this branch from the 'dev' branch'
15:16
First you had 'master' branch, from there you had 'dev' branch and now from there we have the branch 'anuj/multiply'.
15:22
So all the changes done inside this one, ither branch won't know about it. Let me make the changes and add a multiply.
15:30
So here I have done all the changes under 'Multikpy.java' and I have written the code for multiply.
15:37
Now I want to commit this code as well. So for that we'll add it first, let me show you by 'git status' first.
15:44
'git status' So here 'On branch anuj/multiply' and this file isn't tracked right now.
15:51
So we'll keep this file in the staging area, so 'git add Multiply.java'. Your file will enter in the staging area now and after that you can commit this with the message.
16:04
So now all the files are committed here but if I again go back to the dev branch
16:12
'git checkout dev' and here Multiply.java is removed from here. So basically
16:21
dev branch doesn't know that 'Multiply.java' was even created and some work was done over there.
16:26
now I want the codes that was there in the 'multiply' branch should be there in the 'dev' branch as well. We are feeling that our feature is complete and now we want to bring that feature in 'dev'.
16:35
so for that there'll be a convention --'merge'. We'll do that but first we'll come to the 'dev' branch.
16:41
Now I'll write in it 'git merge anuj/multiply'. The 'anuj/multiply' will merge with this 'dev' branch'.
16:50
so you can see that here there isn't any file named 'multiply.java'. As soon as I'll do it
16:55
'Multiply.java' has been added and all the insertions are there in it as well.
17:03
Now, 'git log' -- it'll add Multiply.java. It wasn't there before and
17:11
if I'll go on to the master, then it wouldn't even know that multiply was even being done. If I'll do 'git checkout master' again then
17:20
'git log' then here multiply isn't being executed because 'master' branch doesn't know other branches are doing.
17:28
Now we see that 'Multiply' is working fine inside 'dev' and we want to bring it into 'master'. So we'll merge it again with master
17:36
Its showing 'deleted' so we'll remove it. We'' again merge--- 'git merge dev'
17:43
and all the changes under 'dev' has been transferred here along with 'Multiply.java'. Now I'll do 'git log'
17:50
so the 'multiply' commit is also coming here. So this were branches and you must have understood how they work and how you merge inside the branches and what is its benefit?
17:59
Basically, multiple people can work on different branches different features and nobody even knows what is going on in the other feature.
18:06
What code is being changed? And when it is felt that everything is working properly fine, you merge them in 'master' and always send the 'master' to the production.
Git merge
18:14
Basically, these things happens inside Git. Lets see some more things, for example, there is a 'git ignore file'
18:19
So you want that some files should enter the Git ecosystem, git shouldn't track them, so for that you can pit them in 'git ignore'.
18:26
Suppose, I am making a file in it named-- 'secretkey'. So I have made a key, I am using this key in my code and I want that this key
18:35
shouldn't be exposed, it shouldn't go anywhere into Github. Otherwise someone else can use it, so you don't want these sensitive information to enter into Github ecosystem.
18:44
so, for that you can put it in 'git ignore'. When you'll make this file then there 2 ways to make it.
18:49
'touch .Gitignore' After that 'gitignore' file would be created or let me rename it. You can directly make it from here.
19:00
So we have to make through '.gitignore'. So, here 'gitgnore' file will be created and all the files and folders that will be written in it, git will ignore them.
19:10
Lets try 'git status' here. So here it says 'gitignore' and 'secretkey.txt'. I don't want this 'secretkey.txt' to enter in git.
19:21
so for that, I'll write here 'secretkey.txt' and aagain execute 'git status'. so you can see here 'gitignore' is occurring and 'secretkey.txt' isn't appearing here.
19:30
So in a way it has gone from git ecosystem and git wouldn't track it. This is the benefit, if you want you can put 'gitignore' file in it as well. So now this won't be tracked as well.
19:42
We'll execute 'git status' then none of your files will be tracked.
19:47
So, thsi was all about GIT. Now lets talk about GITHUB. What is github, how does it work and how do we push this code in github. Lets deal with that.
19:55
This is my Github profile which is an amazing thing and very useful as well.
20:00
You also put this Github profile in your resume, the recruiters check how do you all code and in what way.
Add a .gitignore file
20:07
You are also able to do Open source contribution with its help because the code in it is hosted in a remote repository.
20:16
And multiple people can view and contribute towards your code. If you want you can either make public or a private repo
20:24
who shouldn't be accessed by anyone except you or your contributors. It has both the ways and lets see how a repo is made in it. So if you don't have an account then you can make one.
20:35
After that we'll make a new repo. and its name would the same as here- 'Lets Learn Git'
20:46
After that Learning Git. Then we'll ignore these 3 things for now. Lets crate this repository.
20:53
As soon as you'll create it, they will tell you to setup here that what you want to do do you already have a repo or you want to start from a basic.
21:03
we already have one, so we'll push it here. For that they have given 3 steps here. We'll also follow them.
21:09
First of all 'git remote add origin'. Here the concept is of origin, so you can tell you local git repo that what is its remote git repo.
21:17
That is from where the code has to be pushed on. This is the command for that we'll just copy it and paste here.
21:24
For now I am running a command 'git remote -v'. I am not pasting it.
21:31
So we can see that nothing is being written here but now when I'll paste this command and I'll again execute 'git remote -v'
Introduction to Github
21:38
Then here its written- this is the origin to fetch and push. And this is the same origin that I have made now.
21:47
This is now the remote and we'll be doing all the push and pull inside it. So now lets push the code.
21:53
This is the command to push 'git branch -m Master'.
22:00
The next command is 'git push', which will push all the changes inside it towards the origin.
22:10
So this is your origin, we named it 'origin' while doing 'git add origin'. You can name it anything, but the convention is 'origin'.
22:18
If you want you can name it anything. So 'git push -u origin master'. Keep in mind where you are pushing and which branch.
Creating Github repository
22:30
So we'll enter here and our code should be pushed to the origin. But here it says- Permission to add is being denied to Shivam Sharma Nsut.
22:38
So when I tried to push it, an error occurred that- I had earlier logged in it with my brother's account so I had entered the email ID and password.
Pushing code to Github
22:47
So it was similar in the keychain, it was earlier logged in with Shivam and because I'm tried to put it in my own Github account so
22:55
that is why an error occurred that you can't do it. So for that I deleted it from the keychain access
23:01
Now I hope it should work now. So now its asking me the username, so the previous username and password has been deleted in the keychain.
23:09
For the first time it might ask you the username and password, then it'll save it inside its keychain.
23:15
Put your user name, with which you had created the username, so I made it with this one.
23:20
and then you have to enter your password. then this code will be pushed. Then we have to come back to the branch.
23:29
So now I'll come to the branch and reload. Now here our code is pushed now.
23:34
And all the commits are also present here and only master branched is pushed here for now because we only pushed the master branch.
23:41
All the commits are pushed on our github and visible as well. Congratulations we have included a commit on our github.
23:49
A repo is created on github, so like this you can do multiple changes in it and push your code. Just as I am doing in 'Diff.java'
23:56
and suppose I have to change something, a small one not a bigger one.
24:02
And we'll add and commit it for Diff.java
24:08
after that we'll do 'git push'. Its okay if you don't write push or write only till 'push'. It'll work.
24:13
We'll simply do 'git push' and then by default its origin and master so we don't need to write it.
24:19
So it pushed it on its own. Now I'll come back to the repo and reload it, then our recent changes will be executed.
24:26
17 seconds ago as you can see and empty method is also there in 'Diff.java'.
24:33
So for now it only consists of master branch and here we have created 2-3 branches, those branches aren't included in it.
24:38
So we want to push 'dev' branch in it. For that we just have to do 'git checkout dev' and then push it here-- 'git push'
24:49
If you want you can also write '-u origin dev' So now dev branch will also be pushed. So now you'll see here
24:56
I'll reload it, so along with master branch 'dev' branch is also included.
25:02
So both of the branches are present here, so you can push your branch as well. You must have understood it. Lets see other things that how you can do the collaboration with multiple as well.
25:13
You want that multiple people should work in a project, there are 2 ways for it. Either do the Open source
25:20
and then people will fork as well and then they do the changes and then they send you the pull request. Or you want that other person should be able to change in this code, then you can add the collaborators.
25:30
So I'll also add a collaborator in it. I'll go to settings and then manage access
25:36
there you can invite your collaborator, so whoever is on github you can write his name here.
25:42
So I'll add shivam here. A mail was sent to shivam and he accepted it, here its pending now, so I'll reload it and now it should show 'accepted'.
25:50
So he is also added as a collaborator, which means now he also has the access to this repo and
25:56
he can directly clone this repo in his laptop, make changes and push it directly
26:03
Now lets see how we can do open source contribution, right! How can you fork other's code in your code, then clone it and how to send a pull request as well.
26:13
This is very exciting. So for that I'll make a repo, new repository and anyone can fork it ,I'll tell you how its done.
Pushing branches to Github
26:25
so I'll name it First contribution and put anything in the description. I'll also add a README in it and I created the repo.
26:36
and this repo is with the name Anuj kumar sharma. I'll put the link in the description, if you want you can fork it as well. So lets see how you all can contribute in the open source.
26:47
To contribute in open source doesn't mean that you are directly doing a change in the code itself. You can make changes in the README file as well, it is also an open source contribution you learn a lot from it as well.
How to collaborate on Github
26:55
So now I'll go to shivam's account, so the dark themed is shivam's account. And I'll open my profile in it and I'll move on to the repos.
27:07
so, this is my first contribution's repo, you might be ale to see it. I want to contribute open source in it. You'll also see a page like this.
27:16
So how will you do it? You won't directly clone it, you'll fork it. As soon as you'll fork it, the remote copy will be created in your github as well.
27:28
You can see the fork button at the top-right corner, you have to click on it and as soon as you'll click on it
27:35
A copy for you will be created, so same to same copy will be created in your github as well. You can see - Shivam sharma
27:42
and here it is First Contribution-- fork from --this is my name. And you can make any changes in this copy, you can input 50-100 files in it.
How to make an open-source contribution
27:53
this is your copy, it doesn't matter here. There won't be any change in my file. You can make any changes in it, so lets see how to make changes in it. First of all we'll have to bring it to local, right!
28:05
so to bring it into local, you have to copy this link. So I copied it and we'll clone it.
28:12
Clone is already in the repo so we don't have to do it, so I'll come back-- cd.. and we'll clone it here. 'git clone'
28:20
so this is the command 'git clone' and then the entire name of the repo.
28:27
We'll clone it and lets see what is inside it. It only consists of a README.md file. Lets change this file a little bit.
28:35
One more thing, the account in it if you see-- 'git config --global --edit'
28:42
Here its my actual account, but I want to do it with my brother's account. So I'll change my information here.
28:50
now all the commits will be from my brother's name instead of mine.
28:56
Now lets do the changes in the README.md file. I'm opening it in 'vim' itself.
29:03
So if you know to edit in 'vim' then its very easy, first you have to write 'i' to come into insert mode.
29:08
then you can make the changes-- This is my first contribution. After that, you have to press 'ESC' button then 'colon' then 'w', 'q' and you have to come out of it.
Fork a Github repo
29:18
You can check your changes by the -- 'cat' command. So we have done these changes in these file. Now as I am inside the master branch,
29:27
so if you want you can make changes in the master branch but I won't recommend it. If you want you can make a different branch and change inside it, but for now I'm changing in the master branch.
29:38
First, we'll do 'git add README.md' then 'git commit -m "readme.md updated"
29:44
then we'll push it. So you can see that 'This is my first contribution' is visible and if we visit the commits.
Clone a Github repo
29:52
then our commit is here. But this commit was in the forked repo and my actual repo doesn't even know about it.
30:00
So as a user you can make a pull request here.
30:06
So you'll go here and it says - This branch is one commit ahead. So you want to merge it.
30:17
For that you'll go to contribute and open pull request and then make a pull request.
30:23
First you'' check in which files you have made the changes, so first I wrote this and then you did these changes in it.
30:32
So for that you'll request create code after seeing then you can write the messages that what you have changed. So "README.md updated".
30:38
I'll put it here as well, then you'll review it again and then create a pull request.
30:45
Now pull request ahs been created and now it'll come to me and I'll check what changes have you made in it.
30:50
And should I implement these changes in my code or not. So basically you are waiting here to merge with me. So now I have got a pull request here.
31:03
here its a pull request by shivam sharma. now I'll check this pull request, what changes has he done here and should I merge it or not. I'll go to file change
31:13
I had written this but he has written this. I found it quite good, so I'll review it and approve it.
31:21
Looks good, I put a random message. I'll put my review and now I can merge it. So I'll merge it and then when I'll come back to my code
31:35
now my code is changed here. README.md file has been changed and if I visit my commits.
31:42
then Shivam's commit is visible here, the previous one. And then this is the merged commit, when you merge it is also a commit.
Making a pull request
31:51
In this way there can be multiple contributors and now you can learn how pull request is done and how open source contribution is done.
32:00
so whenever you see a an open source contribution then you just have to search the repo in which you have to do the change.
32:06
You'll get that repo in the github. You can search anywhere in the github. And you have to repeat the same thing with it.
32:13


<!-- Fork, clone, changes, push, pull request, done. Your work is done. -->


32:19
After that these things are repeated. So you must have understood the open source contribution and how git works.
32:27
One more thing, if you didn't understand something properly, then try to go through it once again.
32:32
This is what happens in GIT and GITHUB, the more the repetition with it, the more you learn.
32:39
This was it for the video. If you liked this video and it helped you then do share this video. Like and subscribe to the channel.
32:47
I'll meet you all in the next video. If you have any more requests then do tell me as well. That's it for today's video. I'll meet you in the next one.
32:53
BYE! BYE!












