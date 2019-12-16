# GitHub Classroom Guide for Students in Math 285

Most of this content in this guide was taken from https://github.com/jfiksel/github-classroom-for-students and edited for our classroom use. This is a guide for students to setup Git and GitHub for use with GitHub Classroom. If you are using the mirage Rstudio server you can connect to github without any extra software downloads. If you are using Rstudio on your computer, you will need to download Git software (as directed below) to use github connected projects. 

### What is GitHub?
We will use GitHub for all Rstudio work done in our course. You will use GitHub to submit homework and collaborate on projects. 

### Using Rstudio in Math 285

Before you go over this guide, you need to review the [Using Rstudio in Math 285 page](https://github.com/data-science-math285-w20/course-content/blob/master/Rstudio-in-math285.md).

### Steps for getting setup with GitHub 
1. **(everyone)** Register for account on GitHub (https://github.com/). We recommend using a username that incorporates your name (jfiksel, mtaub, lrjager). Please also use your Carleton email with this account and apply for an education discount to get free private repositories. 

2. **(non-mirage users)** If needed, download RStudio (https://www.rstudio.com/) and R (https://cran.r-project.org/)

3. **(non-mirage users)** Install Git. Directions for both Windows & Mac here: http://happygitwithr.com/install-git.html. Windows users should follow Option 1 in 6.2. Mac users can follow Option 1 in 6.3 if comfortable, otherwise follow Option 2

4. **(everyone)** Setup options in Git. Open up the shell in R Studio by selecting the **Terminal** tab next to the Console tab or by clicking Tools -> Shell. Enter the three lines of code here: http://happygitwithr.com/hello-git.html, changing the first two lines to your own name and email (this should be the email associated with your GitHub account). 

5. **(everyone, optional)** This step explains how to use GitHub on Rstudio without having to enter your password everytime to connect. As noted in Happy Git, this step may not be needed if you have a newer version of Rstudio. If you find yourself entering your username/password everytime you want to connect to GitHub then you should follow one of the two steps below to cache your GitHub credentials: 

Recommdended: Cache credential using a HTTPS linked project. Go into the shell/terminal and complete on this page http://happygitwithr.com/credential-caching.html, which is Chapter 10 in Happy Git with R. 

Method 2: Another method is to generate a SSH key so you don’t need to enter your password every time you interact with GitHub. First check to see if you have a SSH key. Go into the shell (again, through RStudio Tools -> Shell) and complete on this page http://happygitwithr.com/ssh-keys.html, which is Chapter 11 in Happy Git with R. 


### Steps for downloading and editing assignments from GitHub Classroom

1.  If you followed the suggestions in the [Using Rstudio in Math 285 page](https://github.com/data-science-math285-w20/course-content/blob/master/Rstudio-in-math285.md), then you should already have created a folder for this class (called something like Math285). Within this folder, I would recommend a folder titled assignments that you will use to store Rstudio projects for each class assignments and project. You should also use your Math285 folder to store the course-content repository that I will share with the class (details about how to obtain this folder are below). Here is what the file system for mirage users should look like:

```
Username
│
│
│
└───Math285
    |
    |
    |
    |--- assignments
        │
        │
        |
        |--- assignment1
```

2.  Assignments will be posted on the course-content site using a url link. This will happen for each new assignment. Click on the link then follow the instructions for getting the homework repository set up for this particular assignment on GitHub. Note that after you accept an assignment for the first time, I will send you an invite to join the classroom organization as a member. Please accept this. You will probably get an email with the invitation, but you should also see a link at the top of your main GitHub page.

3. Enter the homework repository on GitHub (this is online--GitHub is different from Git!). Click **“Clone or Download”**. Most of you should just use the default setting which is to "clone" (copy) using HTTPS. Click the clipboard to the right of the URL to copy the repo location. (If you are using SSH from step 5 above, make sure it says “Clone with SSH” in bold in the top left of the pop-up box. If not, click on the blue “Use SSH” button on the top right of the pop-up box. Now copy the link in the box to your clipboard.)

4.  In Rstudio, go to **File -> New Project**. Click **Version Control**, then **Git**. Paste the link you just copied into the Repository URL box. Leave the Project directory name blank (or keep the auto-filled name).  Browse to find your **Math285/homework** folder and create this assignment as a subdirectory of your homework folder. 

An RStudio project should now open up, which will allow you to start working on your homework assignment. You see the project assignment name in the rop righthand side of Rstudio. You will probably see a blank console screen when you open a new project. Look in the **Files** tab for your homework .Rmd file. Click on whatever file you want to edit (probably the .Rmd file) and edit away. You will always want this assigning project started when working on your assignment. (Don't work on assignment 2 in an assignment 1 project). To switch between projects, go to **File -> Open Project** and navigate to the project directory and double click on the .Rproj file. You can also use the dropdown Project menu in the upper righthand side of Rstudio.
    
5.  After you make changes to the homework assignment, commit them. What are commits you ask? Commits are essentially taking a snapshot of your projects. Commits save this snapshot to your local version of Git (located on your hard drive or the mirage server). For example, if I make changes to a code so that it prints "Hello world", and then commit them with an informative message, I can look at the history of my commits and view the code that I wrote at that time. If I made some more changes to the function that resulted in an error, I could go back to the commit where the code was originally working. This prevents you from creating several versions of your homework (homework-v1, homework-v2, ...) or from trying to remember what your code originally looked like.

You can make commits in the Git tab in the top right window. You can read how to do  this in RStudio in more detail here: http://r-pkgs.had.co.nz/git.html#git-commit.  Click the **Commit** button in the Git toolbar dropdown menu. Check the files that you want to commit, enter your commit message (briefly state what changes have been made), then hit **Commit**.

Two things about committing. One, you should commit somewhat frequently. At minimum, if you're doing a homework assignment, you should make a commit each time that you've finished a question. Two, leave informative commit messages. "Added stuff" will not help you if you're looking at your commit history in a year. A message like "Added initial version of hello-world function" will be more useful.

6.  At somepoint you'll want to get the updated version of the assignment back onto GitHub, either so that teachers/TAs can help you with your code, so you can work on it using mirage, or so that it can be graded. You will also want to push work frequently when you have a shared GitHub repo for project collaborations (i.e. more than one person is working on a project and code). If you are ready to push, you can again click on the "Up" **Push** arrow in the Git tab or in the Commit popup window. 

7. (**optional**) If you are working on an assignment from both the mirage server and your own version of Rstudio, or working on a collaborative project, then you will be working from two versions of the same project. To get the latest version of an assignment, you should start out your R session by pulling the most recent version from GitHub by clicking the "Down"  **Pull** arrow in the Git tab. 

### Obtaining and pulling a shared repository (course-content)

The GitHub repo **course-content** will contain material for our class and it will be updated throughout the term. You should see this repo on GitHub (online) once you are accepted to the Math285-w20 organization. You can obtain a copy of this repo by **cloning** it to your computer (or mirage), then pulling updates throughout the term. You don't have permission to push any changes to the class repo! Here are the steps for cloning:

1. In GitHub, navigate to the shared directory. Repeat step 3 from above, where we copy the link that we will use to clone this repository. Then follow step 4 above and create the course-content repo as a subdirectory to your Math285 folder.
    
2. To pull in changes, click the "Down"  **Pull** arrow. If you get an error about conflict, don't freak out! This can happen if you edit a file that was also changed by myself. I'll do my best to ensure this doesn't happen (e.g. by not editing too much after an initial material post), but if it does, take a look at [this site](http://r-pkgs.had.co.nz/git.html#git-pull) and try to fix the merge conflict in Rstudio. I also created a diagram shown below that "explains" how and when conflicts will likely happen and how you can resolve the problems in Rstudio. If that doesn't work contact me!

### Resources
* [Happy Git and GitHub for the useR](http://happygitwithr.com/)
* [Rstudio, Git and GitHub](http://r-pkgs.had.co.nz/git.html#git-rstudio)
* [Interactive learning guide for Git](http://learngitbranching.js.org/)
* [GitHub Guides](https://guides.github.com/)
* [Git setup for Windows (video)](https://youtu.be/F_fPEMnr1OQ)
* [Git setup for Mac (video)](https://www.youtube.com/watch?v=kbmSZwK0k-A&t)
* [How to clone, edit, and push homework assignments with GitHub Classroom (video)](https://youtu.be/pAcMgGbCtQw)
* ![My conflict resolution diagram!](https://github.com/data-science-math285-w18/course-content/blob/master/ConflictResolution.JPG)
