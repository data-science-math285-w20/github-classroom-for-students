# GitHub Classroom Guide for Students in Math 285

Most of this content in this guide was taken from https://github.com/jfiksel/github-classroom-for-students and edited for our classroom use. This is a guide for students to setup Git and GitHub for use with GitHub Classroom. If you are using the mirage Rstudio server you can connect to github without any extra software downloads. If you are using Rstudio on your computer, you will need to download Git software (as directed below) to use github connected projects. 

### Using Rstudio in Math 285

Before you go over this guide, you need to review the [Using Rstudio in Math 285 page](https://github.com/data-science-math285-w18/course-content/blob/master/Rstudio-in-math285.md).

### Steps for getting setup with GitHub 
1. **(everyone)** Register for account on GitHub (https://github.com/). We recommend using a username that incorporates your name (jfiksel, mtaub, lrjager). Please also use your Carleton email with this account. 

2. **(non-mirage users)** If needed, download RStudio (https://www.rstudio.com/) and R (https://cran.r-project.org/)

3. **(non-mirage users)** Install Git. Directions for both Windows & Mac here: http://happygitwithr.com/install-git.html. Windows users should follow Option 1 in 7.2. Mac users can follow Option 1 in 7.3 if comfortable, otherwise follow Option 2

4. **(everyone)** Setup options in Git. Open up the shell in R Studio by clicking Tools -> Shell. Enter the three lines of code here: http://happygitwithr.com/hello-git.html, changing the first two lines to your own name and email (this should be the email associated with your GitHub account). 

5. **(everyone)** This step explains how to use GitHub on Rstudio without having to enter your password everytime to connect. This is an optional step since you can still use GitHub without setting up a SSH key or caching credentials, you will just need to enter your password every time you push or pull with GitHub. Pick one method below: SSH or cache creds for HTTPS. I've had more success with caching creds for HTTPS (second method), so this is the one you may want to use or try if the SSH method doesn't work!

One method is to generate a SSH key so you don’t need to enter your password every time you interact with GitHub. First check to see if you have a SSH key. Go into the shell (again, through RStudio Tools -> Shell) and complete on this page http://happygitwithr.com/ssh-keys.html, which is Chapter 12 in Happy Git with R. 

A second method is to cache credentials for using a HTTPS linked project. Go into the shell (again, through RStudio Tools -> Shell) and complete on this page http://happygitwithr.com/credential-caching.html, which is Chapter 11 in Happy Git with R. 

6. **(everyone, optional)**  Follow the instructions here (http://happygitwithr.com/push-pull-github.html) to ensure you can connect to GitHub from your computer. (If you can't get this command line push/pull to work that is fine. Try connecting to GitHub via Rstudio, as detailed next. If you can't connect via Rstudio then come see me!)

### Steps for downloading and editing assignments from GitHub Classroom

1.  If you followed the suggestions in the [Using Rstudio in Math 285 page](https://github.com/data-science-math285-w18/course-content/blob/master/Rstudio-in-math285.md), then you should already have created a folder for this class (called something like Math285). Within this folder, I would recommend a folder titled lectures (this can be pulled from the organization--we will show you how to do this), as well a folder title homework. 

```
Username
│
│
│
└───Math285
    │
    │
    │--- slides
    |
    |
    |
    |--- homework
        │
        │
        |
        |--- assignment1
```

2.  We will give you a link to an assignment, either through email or the class page. This will happen for each new assignment. Then follow the instructions for getting the homework repository set up for this particular assignment on GitHub. Note that after you accept an assignment for the first time, we will send you an invite to join the classroom organization as a member. Please accept this. You will probably get an email with the invitation, but you should also see a link at the top of your main GitHub page.

3. Enter the homework repository on GitHub (this is online--GitHub is different from Git!). Click “Clone or Download”. If you are using SSH (step 5 above), make sure it says “Clone with SSH” in bold in the top left of the pop-up box. If not, click on the blue “Use SSH” button on the top right of the pop-up box. Now copy the link in the box to your clipboard. If you are not using an SSH key, make sure it says "Clone with HTTPS" (I think this is the default setting).

4.  In Rstudio, go to File -> New Project. Click Version Control, then Git. Paste the link you just copied into the Repository URL box. Leave the Project directory name blank (or keep the auto-filled name).  Browse to find your Math283/homework folder and create this assignment as a subdirectory of your homework folder. 

An RStudio project should now open up, which will allow you to start working on your homework assignment. You see the project assignment name in the rop righthand side of Rstudio. (Warning: on my windows machine, Rstudio has a habit of creating a project but not opening it upon creation. You can always open a project by navigating to your project folder and double clicking the .Rproj file.) You will probably see a blank console screen when you open a new project. Look in the Files tab for your homework .Rmd file. Click on whatever file you want to edit (probably the .Rmd file) and edit away. If you save and close Rstudio and want to go back to editing your project, open up Rstudio, then go to File -> Open Project. Navigate to the project directory and double click on the .Rproj file. 

Note that if you received an error in the above steps, you may have to clone with HTTPS instead of SSH. You can do this by again clicking on the "Clone or Download" button in the repository page, then clicking "Use HTTPS" in the top right of the pop-up box. Now copy the link and repeat this step.
    
5.  After you make changes to the homework assignment, commit them. What are commits you ask? Commits are essentially taking a snapshot of your projects. Commits save this snapshot to your local version of Git (located on your hard drive or the mirage server). For example, if I make changes to a code so that it prints "Hello world", and then commit them with an informative message, I can look at the history of my commits and view the code that I wrote at that time. If I made some more changes to the function that resulted in an error, I could go back to the commit where the code was originally working. This prevents you from creating several versions of your homework (homework-v1, homework-v2, ...) or from trying to remember what your code originally looked like.

    You can make commits using the Git toolbar in RStudio (in RStudio make sure the toolbar is visible by doing View -> Show Toolbar) or in the Git tab in the top left window. You can read how to do  this in RStudio in more detail here: http://r-pkgs.had.co.nz/git.html#git-init.  Click the Commit button in the Git toolbar dropdown menu. Check the files that you want to commit, enter your commit message, then hit Commit.

Two things about committing. One, you should commit somewhat frequently. At minimum, if you're doing a homework assignment, you should make a commit each time that you've finished a question. Two, leave informative commit messages. "Added stuff" will not help you if you're looking at your commit history in a year. A message like "Added initial version of hello-world function" will be more useful.

6.  At somepoint you'll want to get the updated version of the assignment back onto GitHub, either so that teachers/TAs can help you with your code, so you can work on it using mirage, or so that it can be graded. You will also want to push work frequently when you have a shared GitHub repo for project collaborations (i.e. more than one person is working on a project and code). If you are ready to push, you can again click on the Git toolbar dropdown menu or tab in RStudio, and then click `Push branch`. You can also do this after you commit in RStudio by clicking Push in the top right corner of the Commit pop-up box.

7. (**optional**) If you are working on an assignment from both the mirage server and your own version of Rstudio, then you will be working from two projects (one located on mirage and one on your local computer). You create a project for each location as described above. To get the latest version of an assignment, you should start out your R session by pulling the most recent version from GitHub. You can again click on the Git toolbar dropdown menu or tab in RStudio, and then click `Pull` or `Pull branches`. 

### Obtaining and pulling a shared repository (course-content)

Your classroom may have a repository where everyone in the class has access to it, such as a class materials repository (course-content). This repository will probably be updated throughout the class, and it will be useful to constantly have the most updated materials on your local computer. You can do this by first cloning the repository, and then pulling in changes. Your don't have permission to push any changes to the class repo! Here are the steps.

1. Clone the repository using Rstudio following steps 3-4 above. Create the repo as a subdirectory to your Math285 folder.

In GitHub, navigate to the shared directory. Repeat step 3 from above, where we copy the link that we will use to clone this repository. If you get an error using SSH, you should instead use HTTPS. 
    
2. To pull in changes, click on the Git toolbar dropdown menu or tab in RStudio and then click `Pull` or `Pull branches`. If you get an error about conflict, don't freak out! This can happen if you edit a file that was also changed by a professor. Professors should be doing their best to ensure this doesn't happen (e.g. by not editing too much after an initial material post), but if it does, take a look at [this site](http://r-pkgs.had.co.nz/git.html#git-pull) and try to fix the merge conflict in Rstudio. I also created a diagram shown below that "explains" how and when conflicts will likely happen and how you can resolve the problems in Rstudio. If that doesn't work contact me!

### Resources
* [Happy Git and GitHub for the useR](http://happygitwithr.com/)
* [Rstudio, Git and GitHub](http://r-pkgs.had.co.nz/git.html#git-rstudio)
* [Interactive learning guide for Git](http://learngitbranching.js.org/)
* [GitHub Guides](https://guides.github.com/)
* [Git setup for Windows (video)](https://youtu.be/F_fPEMnr1OQ)
* [Git setup for Mac (video)](https://www.youtube.com/watch?v=kbmSZwK0k-A&t)
* [How to clone, edit, and push homework assignments with GitHub Classroom (video)](https://youtu.be/pAcMgGbCtQw)
* ![My conflict resolution diagram!](https://github.com/data-science-math285-w18/course-content/blob/master/ConflictResolution.JPG)
