UMICTResearch Team website
====================

## Table of Contents
0. [Getting Started on your local system](#getting-started)
1. [Homepage Slider](#homepage-slider)
2. [Projects](#projects)
3. [Project Papers](#project-papers)
4. [Homepage Papers](#homepage-papers)
5. [Team](#team)
6. [Contact Page](#contact-page)
7. [Additional Notes](#additional-notes)
8. [Code Push](#code-push)

---
##Getting Started
1. Install jekyll on your system if it is not installed already.  
    Follow the instructions here based on your OS: http://jekyllrb.com/docs/installation/
2. Change to your UMICTResearch.github.io source directory
3. Type: jekyll serve
4. Once the server is ready, type: http://127.0.0.1:4000/ into your web browser's address bar
5. Note: If there is a '_site' folder inside the '_data' folder, remove it or do not make any changes

##Homepage Slider
1. Template used: _includes/header.html
2. The slider images are changed using a JS plugin.
3. The images are stored in img/sliders/

####How to Add/Modify?
1. Add image to /img/sliders
2. Image width should be a minimum of 1600 (the height is proportional)
3. Add the filename of the image to _data/slider.yml
4. Follow convention while adding to the data file (yml):
    - name: (filename)
    - alt: (text description of the image) 

---

##Projects
1. All projects are stored in '_posts' with the file name as yyyy-mm-dd-project-(shortname).markdown
2. The order is defined by the weight defined in the markdown file
    - lower number weight forces project to appear earlier in the order of the projects on the homepage
    - higher number weight forces project to appear later in the order of the projects on the homepage
3. Each post contains following fields:
    - layout (this is to select which template will be used to render the main project page)
    - title (project name)
    - subtitle (short description of the project)
    - date
    - thumbnail (name of thumbnail image for the project which is displayed on the homepage and the project page)
    - alt (alternative description of image to meet accessibility standards)
    - description (duplicate field could be used elsewhere on the website)
    - weight (defines order of appearance)
    - datafile (contains name of data file which has list of associated papers. This data file is present in the '_data' directory)
4. To change any detail, update the above fields

####How to Add/Modify a project?
1. To add a new project, duplicate an existing post in the '_posts' directory and change the name of the file
    - Decide on a shortname for the project which is related to the title of the project and name it as per:
        - yyyy-mm-dd-project-(shortname).markdown
2. Modify 'title' field
3. Modify 'subtitle' field
4. Modify 'date' field which matches the filename date
5. Create a folder in 'assets' directory and name it as 'project-'(shortname)
6. Add an image of min-width 800px with the filename 'thumbnail.jpg' in 'assets' folder
7. Modify 'alt' field to make this thumbnail accessible
8. Modify 'description' field
9. Modify 'weight' field which defines order of this project on the homepage (lower = appears earlier)
10. In the '_data' directory, duplicate an existing project-(shortname).yml data file
11. Change the filename to project-(shortname).yml (specific to this project)
12. Save and commit to repository

All papers of the main project are stored in the _data/project-(shortname).yml file

####How to add/modify projects with sub-projects?
1. Change 'layout' field to 'project_multi'
2. 'project_multi' uses the 'project_multi.html' template
3. Modify the data file stored under _data/project-(shortname).yml file

---

##Project Papers
1. All papers appearing on project pages are stored in _data/project-(shortname).yml
2. Each paper contains the following fields:
    - name: name of the paper
    - pic: thumbnail image (max width: 150px)
    - abstract: short paper description
    - authors: name of authors
    - mainlink: name of the pdf file (without extension)
    - resources: collection of various resource types
        - type: name of the resource type. eg - pdf | ppt
        - link: name of the resource without extension
    
#### How to modify?
1. To add a new paper use the data structure already present in another project under '_data' directory
2. Duplicate any 'project-shortname' folder and rename it to the appropriate one 
3. Open _data/project-shortname.yml
4. Save the PDF or resource under '_assets/project-shortname' folder
5. Create a thumbnail image as per follows:
    - To create a thumbnail image use: https://pdfjpg.net/
    - Select Output Quality: 150dpi
    - Select the pdf file to convert to jpb
    - Click on Convert, wait for the process to finish
    - Save the first image which is generated using the following naming convention:
        - nameofpdf_thumb.jpg

---

##Homepage Papers
1. All papers appearing on the homepage are stored in _data/papers.yml
2. Each paper contains the following fields:
    - name: name of the paper
    - pic: thumbnail image (max width: 150px)
    - abstract: short paper description
    - authors: name of authors
    - keywords: comma separated list of keywords
    - link: name of the pdf file

#### How to modify?
1. To add a new paper use the data structure already in the _data/papers.yml file
2. Save the PDF in assets/papers
3. Save the thumbnail image too in assets/papers
    - To create a thumbnail image use: https://pdfjpg.net/
    - Select Output Quality: 150dpi
    - Select the pdf file to convert to jpb
    - Click on Convert, wait for the process to finish
    - Save the first image which is generated

---

##Team
1. There are two types of team members.
    - Alum
    - Current
2. Each of these types have a data file each in _data. Namely, members_alum.yml and members_current.yml.
3. Images are in '/img/team/'

1. A member has the following fields:
    - name: name of member
    - pic: picture filename (size: 225px wide and 225px high)
    - position: title/status of the member
    - social: (the following is used to display links under the member thumbnail)
        - title: (iconname from the fontawesome directory of icons, http://fortawesome.github.io/Font-Awesome/icons/)
        - url: (url of the link)
      
####How to modify?
1. To add a new member, first decide the type
2. Depending on the type of member edit the _data/members_alum.yml or _data/members_current.yml file
3. Use the same data structure the create the new member
4. Save the image in img/team

---

##Contact Page
1. The template for the contact page is stored in _includes/contact.html
2. To make any changes, this file needs to be edited (there are not data files)

---

##Additional Notes
1. Do not modify any files inside _site folder as this is generated by jekyll and is not part of the repository
2. If there is a '_site' folder inside the '_data' folder, remove it or do not make any changes
3. Keep image sizes to the minimum, ideal size for image sliders is about 1600px (width). The height should be proportional

---

##Code Push

####For smaller bug fixes

1. Clone repository
Execute: "$ git clone <repo>"
2. Create a new branch which is based off origin/master. This is the hotfix branch.
Execute: "$ git checkout -b hotfix origin/master"
3. Make changes and commit. The commit message should be in present tense.
4. Before pushing to remote, fetch changes
Execute: "$ git fetch"
5. If updates to the local repo are required
Execute: "$ git pull --ff origin"
6. If no updates are required
Execute: "$ git push origin hotfix"
7. Go to github.com/<repo>
8. Open a pull request against the master branch
9. Assign the pull request to another team member
10. Inform the team member to review code and merge into master

For new features
All steps are the same except, replace name of branch "hotfix" with a different name like "feature-1"

=========

For more details on the site, contact tdillahu@umich.edu
