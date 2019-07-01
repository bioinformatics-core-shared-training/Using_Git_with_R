## Using Github with R (and Rstudio)
**Aims of this section:**   
1) To introduce the concept of version control and to name some version control software and to focus on one (git).  
2) To widen your knowledge about Github ie. what it is and why you should be using it.  
3) How we can integrate the use of Git into Rstudio. 

**Version Control - we have a problem**.   
Anyone who has editted anything other than a trivial document (think a thesis here) or a collaborative document (think a paper here) will have experienced the problem of having to revert to an earlier version of the manuscript e.g. upon discovering a mistake.   
Many ways have been evolved involving convoluted naming and numbering schemes that necessitate human involvement and knowledge to operate e.g. *Finaldoc4.5_final.Doc* as this classic PHDComics cartoon illustrates.    
![Final from PHDComics.com](phdcomic.gif).  
<ins> Enter version control </ins>.  
The above scenarios are commonly encountered in software development and consequently systems have been put into place to allow consistent transition between versions of documents.    
Versioning software is similar to the incremental backup system often used on computers. In that example a full backup of the disk is initially made and thereafter periodic (smaller & quicker) backups of the changes are created. The restoration step uses the initial reference backup and 'replays' the incremental ones to re-create the last backed-up state. Commonly used version controls systems are sub-version and git (which is used in developing the Linux Operating System). ![git](git_logo.png)    
Git stores the initial files and then the user adds (marks changes to be committed), commits (explaining what the purpose of the changes are) and then pushes the commit to the repository. Git stores all of these changes in a  network structure that can have branches off of the main trunk.    
![XKCD git cartoon](https://imgs.xkcd.com/comics/git.png).   
XKCD.COM humour aside, git can be driven bt text commands (but don't panic - there are other options).    
_Example command-line git commands:_
> git config --global user.name 'Your Name'.  
> git config --global user.email 'your@email.com'.  
> git status.   
> git add [filename(s)].  
> git commit -m "[meaningful message]".  
> git push.  
> git pull.  

The above are examples of using a git command-line tool. There are many different tools that we can use with git. These include the command-line, the Github web interface, the Github Desktop program as well as from within Rstudio. Due to time considerations, this course only uses the web & Rstudo Git tools. You can learn about the others by following the links in the bibliography. Regardless of the tool used, we aim to demonstrate the usefulness and principles of git versioning.    
By storing the initial and the differences of subsequent commits we can traverse this network.
![versioning](https://homes.cs.washington.edu/~mernst/advice/version-control-fig4.png)   This enables a member of a collaborating group to work seperately on an aspect of the files and then use git to merge the branched version back into the main trunk. git can also help the maintainer resolve conflicts e.g. where two people working on different branches make differing changes to the same file. ![Versioning](https://upload.wikimedia.org/wikipedia/commons/a/af/Revision_controlled_project_visualization-2010-24-02.svg). 
     
***
**What is this Github of which you speak?**
![Github](github_logo.png).  
Github can be thought of as a web-hosting for git repositories. A place to store (and even to share) code and materials. The granularity of access enables you to decide if a repo is private or public and who can create and edit materials within it. It is an example of _distributed version control_
![distributed repositories](https://homes.cs.washington.edu/~mernst/advice/version-control-fig3.png)    
Github also enables you to create [web-pages & blogs](http://mikelove.github.io) by writing material in the [Markdown](https://guides.github.com/features/mastering-markdown/) language and HyperText Markup Language (HTML). Rstudio also uses a flavour of Markdown (called unexcitedly enough _RMarkdown_) to allow annotation of R scripts. Github can render this (_a .Rmd file_) as a web-page. Hopefully, earlier this week you will have encountered Markdown and some of its usages.    
In fact, this week you have been using materials that are hosted on Github repositories. It also enables you to create [wikis](https://github.com/mfernandes61/RSE_Docker_course/wiki) to document your projects and an issue tracker for people to report any problems that need fixing.    
It has been used to crowd source science e.g. [the European EHEC E.coli outbreak](https://github.com/ehec-outbreak-crowdsourced/BGI-data-analysis/wiki).    
NB Markdown can be read by other programs e.g. [Pandoc](https://pandoc.org) to generate other Document formats including HTML, PDF, Word and Reveal.js presentations.    

## Practical 1. 
[We will now use the Github web interface to create a GH repository & a document that we can edit to show how git records edits.](Practical1.md)
   
**Using git within Rstudio**
![Rstudio](Rstudio_logo.jpg)
Rstudio can support git and subversion version control systems. We will restrict ourselves to the former.
To use them within Rstudio you must install the relevant version control system. For git you should download the relevant version from [here](https://git-scm.com/downloads). Linux users can install the _git-core_ package with **apt-get** or **yum**. Once that's been done you need to tell R to use it and where it can find the software.
In Rstudio go to the Tools menu and select Global Options. Then click git and enable 'Version control interface for Rstudio projects'. If SSH is needed then you can add an RSA key here as well.   
The git support revolves around the R Projects (how Rstudio organises your code).  
* If you have directories currently set up for version control (i.e that you were using git on already) then you just need to create an Rstudio Project for that subdirectory to trigger version control support. From the Project menu, choose 'New project' and the create a new project from an existing directory, navigate to your versioned directory and click on 'Create project'.   
* If there is an existing remote repository e.g. on Github you can create an 'New project' from the project menu and opt to create the new project from 'Version control'. You will need to chose git and provide a link e.g. URL to the repository.    
## Practical 2. 
[We will now use the git interface available from within Rstudio.](Practical2.md).    

---------
## Summary
* Git and Github provide us with a dialogue that can explain and manage the progress of programs and documents from the initial conception to the final version.   
Any changes made have logs of what change was made, who by and why the change was made.   
* Rstudio can integrate the use of version control within an R Project.  
* Using git & Github aid reproducibility and provide a means of ditributing research work including, but not limited to, software.   

## Reference materials
* [Free online git book](https://git-scm.com/book/en/v2).  
* [Sergio's Intro to git & Github](https://github.com/semacu/20181003_Intro_git_GitHub).  
* [Article on installing git support in Rstudio](http://r-bio.github.io/git-installation/).  
* [Rstudio Support article on installing version control](https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN).   
* [Markdown pdf cheatsheet](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf).  
* [RMarkdown and its many uses](https://rmarkdown.rstudio.com)
* [Github Desktop](https://desktop.github.com)

