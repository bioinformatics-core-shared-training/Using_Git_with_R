## Using Github with R
**Aims of this section:**   
1) To introduce the concept of vesrion control and to name some version control software and to focus on one (git).  
2) To widen your knowledge about Github ie. what it is and why you should be using it.  
3) How we can integrate the use of Git into Rstudio. 
***
**Version Control - we have a problem**   
Anyone who has editted anything other than a trivial document (think a thesis here) or a collaborative document (think a paper here) will have experienced the problem of having to revert to an earlier version of the manuscript e.g. upon discovering a mistake.   
Many ways have been evolved involving convoluted naming and numbering schemes that necessitate human involvement and knowledge to operate e.g. *Finaldoc4.5_final.Doc* ![Final from PHDComics.com](http://www.phdcomics.com/comics/archive/phd101212s.gif).  
<ins> Enter version control </ins>.  
The above scenarios are commonly encountered in software development and consequently systems have been put into place to allow consistent transition between versions of documents.    
Versioning software is similar to the incremental backup system often used on computers. In that example a full backup of the disk is initially made and thereafter periodic (smaller & quicker) backups of the changes are created. The restoration step uses the initial reference backup and 'replays' the incremental ones to re-create the last backed-up state. Commonly used version controls systems are sub-version and git (which is used in developing the Linux Operating System). ![git](git_logo.png)    
Git stores the initial files and then the user adds (marks changes to be committed), commits (explaining what the purpose of the changes are) and then pushes the commit to the repository. Git stores all of these changes in a  network structure that can have branches off of the main trunk.    
_Example command-line git commands:_
> git config --global user.name 'Your Name'
> git config --global user.email 'your@email.com'
> git status.   
> git add [filename(s)].  
> git commit -m "[meaningful message]".  
> git push.  
> git pull.  

By storing the initial and the differences of subsequent commits we can traverse this network.
![versioning](https://homes.cs.washington.edu/~mernst/advice/version-control-fig4.png)   This enables a member of a collaborating group to work seperately on an aspect of the files and the use git to merge the branched version back into the main trunk. git can also help the maintainer resolve conflicts e.g. where two people working on different branches make differing changes to the same file. ![Versioning](https://upload.wikimedia.org/wikipedia/commons/a/af/Revision_controlled_project_visualization-2010-24-02.svg). 
     
***
**What is this Github of which you speak?**
![Github](github_logo.png).  
Github can be thought of as a web-hosting for git repositories. A place to store (and even to share) code and materials. The granularity of access enables you to decide if a repo is private or public and who can create and edit materials within it. It is an example of _distributed version control_
![distributed repositories](https://homes.cs.washington.edu/~mernst/advice/version-control-fig3.png)    
Github also enables you to create [web-pages & blogs](http://mikelove.github.io) by writing material in the [Markdown](https://guides.github.com/features/mastering-markdown/) language and HyperText Markup Language (HTML). Rstudio also uses a flavour of Markdown (called unexcitedly enough _RMarkdown_) to allow annotation of R scripts. Github can render this (_a .Rmd file_) as a web-page. In fact, this week you have been using materials that are hosted on Github repositories. It also enables you to create [wikis](https://github.com/mfernandes61/RSE_Docker_course/wiki) to document your projects and an issue tracker for people to report any problems that need fixing.    
## Practical 1. 
![Practical session](https://upload.wikimedia.org/wikipedia/commons/thumb/2/24/Cartoon_Guy_In_Deep_Thought_Using_A_Computer.svg/95px-Cartoon_Guy_In_Deep_Thought_Using_A_Computer.svg.png)   
Log into github using your GH account.
Create a new repository create a simple text file (use Markdown if you know it)
Add person next to you and allow them edit privileges and get them to do same for you. Edit each others files commit the files. See how GH logs and datestamps this activity.
   
***
**Using git within Rstudio**
![Rstudio](Rstudio_logo.jpg)
Rstudio can support git and subversion version control systems. We will restrict ourselves to the former.
To use them within Rstudio you must install the relevant version control system. For git you should download the relevant version from [here](https://git-scm.com/downloads). Linux users can install the _git-core_ package with **apt-get** or **yum**. Once that's been done you need to tell R to use it and where it can find the software.
In Rstudio go to the Tools menu and select Global Options. Then click git and enable 'Version control interface for Rstudio projects'. If SSH is needed then you can add an RSA key here as well.   
The git support revolves around the R Projects (how Rstudio organises your code).  
* If you have directories currently set up for version control (i.e that you were using git on already) then you just need to create an Rstudio Project for that subdirectory to trigger version control support. From the Project menu, choose 'New project' and the create a new project from an existing directory, navigate to your versioned directory and click on 'Create project'.   
* If there is an existing remote repository e.g. on Github you can create an 'New project' from the project menu and opt to create the new project from 'Version control'. You will need to chose git and provide a link e.g. URL to the repository.    
## Practical 2. 
![Practical session](https://upload.wikimedia.org/wikipedia/commons/thumb/2/24/Cartoon_Guy_In_Deep_Thought_Using_A_Computer.svg/95px-Cartoon_Guy_In_Deep_Thought_Using_A_Computer.svg.png)   
Create ssh-key (in Rstudio?)
configure Rstudio to use git on an existing or new Project
add/edit an Rmd file
use the git i/f within Rstudio to commit changes.   

***
* What is git? What is version control?
* What is Github?
* Okay, how does using git help me?
- Creating some R code in Rstudio and publishing it to Github
- Getting comments/wishes/bug reports from users (Issues)
- Fixing code and re-publishing
- Honey I broke my program! aka. How to recover from making a mistake
<details>
    <summary>Other uses for Github</summary>
  <ul>Creating group webpages and wikis</ul>
  <ul>Collaborative documents</ul>
  <ul>Course materials (like this one!)</ul>
</details>
