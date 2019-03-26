## Using Github with R
**Aims of this section:**   
1) To introduce the concept of vesrion control and to name some version control software and to focus on one (git).  
2) To widen your knowledge about Github ie. what it is and why you should be using it.  
3) How do we integrate the use of Git into Rstudio. 
***
**Version Control - we have a problem**   
Anyone who has editted anything other than a trivial document (think a thesis here) or a collaborative document (think a paper here) will have experienced the problem of having to revert to an earlier version of the manuscript e.g. upon discovering a mistake.   
Many ways have been evolved involving convoluted naming and numbering schemes that necessitate human involvement and knowledge to operate e.g. *Finaldoc4.5_final.Doc*.  
<ins> Enter version control </ins>.  
The above scenarios are commonly encountered in software development and consequently systems have been put into place to allow consistent transition between versions of documents.   
***
**What is this Github?**

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
