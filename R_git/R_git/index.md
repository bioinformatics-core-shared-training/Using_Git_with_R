## Using Github with R
**Aims of this section:**   
1) To introduce the concept of vesrion control and to name some version control software and to focus on one (git).  
2) To widen your knowledge about Github ie. what it is and why you should be using it.  
3) How do we integrate the use of Git into Rstudio. 
***
**Version Control - we have a problem**   
Anyone who has editted anything other than a trivial document (think a thesis here) or a collaborative document (think a paper here) will have experienced the problem of having to revert to an earlier version of the manuscript e.g. upon discovering a mistake.   
Many ways have been evolved involving convoluted naming and numbering schemes that necessitate human involvement and knowledge to operate e.g. *Finaldoc4.5_final.Doc* ![Final from PHDComics.com](http://www.phdcomics.com/comics/archive/phd101212s.gif).  
<ins> Enter version control </ins>.  
The above scenarios are commonly encountered in software development and consequently systems have been put into place to allow consistent transition between versions of documents.    
Versioning software is similar to the incremental backup system often used on computers. In that example a full backup of the disk is initially made and thereafter periodic (smaller & quicker) backups of the changes are created. The restoration step uses the initial reference backup and 'replays' the incremental ones to re-create the last backed-up state.    
Git stores the initial files and then the user adds (marks changes to be committed), commits (explaining what the purpose of the changes are) and then pushes the commit to the repository. Git stores all of these changes in a  network structure that can have branches off of the main trunk. This enables a member of a collaborating group to work seperately on an aspect of the files and the use git to merge the branched version back into the main trunk. git can also help the maintainer resolve conflicts e.g. where two people working on different branches make differing changes to the same file. ![Versioning](https://upload.wikimedia.org/wikipedia/commons/a/af/Revision_controlled_project_visualization-2010-24-02.svg). 
     
***
**What is this Github of which you speak?**
Github can be thought of as a web-hosting for git repositories. A place tos store (and even to share) code and materials.
***
**Using git within Rstusio**
Rstudio can support git and subversion version control systems. We will restrict ourselves to the former.
To use them within Rstudio you must install the relevant version control system. For git you should download the relevant version from [here](https://git-scm.com/downloads). Linux users can install the _git-core_ package with **apt-get** or **yum**. Once that's been done you need to tell R to use it and where it can find the software.
In Rstudio go to the Tools menu and select Global Options. Then click git and enable 'Version control interface for Rstudio projects'. If SSH is needed then you can add an RSA key here as well.   
The git support revolves around the R Projects (how Rstudio organises your code).  
* If you have directories currently set up for version control (i.e that you were using git on already) then you just need to create an Rstudio Project for that subdirectory to trigger version control support. From the Project menu, choose 'New project' and the create a new project from an existing directory, navigate to your versioned directory and click on 'Create project'.   
* If there is an existing remote repository e.g. on Github you can create an 'New project' from the project menu and opt to create the new project from 'Version control'. You will need to chose git and provide a link e.g. URL to the repository.    


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
