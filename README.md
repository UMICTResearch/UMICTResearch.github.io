UMICTResearch Team website
====================

## Instructions for Updating the website

###Structure

##Homepage Slider
1. Template used: _includes/header.html
2. The slider images are changed using a JS plugin.
3. The images are stored in img/sliders/

#### How to modify?
1. Add image to /img/sliders
2. Image width should be a minimum of 1600 (the height is proportional)
3. Add the filename of the image to _data/slider.yml
4. Follow convention while adding to the data file (yml):
    - name: (filename)
      alt: (text description of the image) 

---

##Projects
1. All projects are stored in '_posts' with the file name as <date>project-(shortname).markdown
2. The order is defined by the weight.
    - low weight forces project to appear first
    - higher weight forces project to appear later
3. Each post contains following fields:
    - layout (this is to select which template will be used to render the main project page)
    - title (project name)
    - subtitle (short description of the project)
    - date
    - thumbnail (name of thumbnail image for the project which is displayed on the homepage and the project page)
    - alt (alternative description of image to meet accesibility standards)
    - description (duplicate field could be used elsewhere on the website)
    - weight 
    - datafile (contains name of data file which has list of associated papers. This data file is present in the '_data' directory)
4. To change any detail, updates to the fields is the only required task

---

##Papers
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
4. Add the name of the pdf and image file to _data/papers.yml file

---

##Team
1. There are two types of team members.
    - Alum
    - Current
2. Each of these types have a data file each in _data. Namely, members_alum.yml and members_current.yml.
3. Images are in '/img/team/'

1. A member has the following fields:
    - name: name of member
      pic: picture filename (size: 225px wide and 225px high)
      position: title/status of the member
      social: (the following is used to display links under the member thumbnail)
        - title: (iconname from the fontawesome directory of icons, http://fortawesome.github.io/Font-Awesome/icons/)
          url: (url of the link)
      
####How to modify?
1. To add a new member, first decide the type.
2. Depending on the type of member edit the _data/members_alum.yml or _data/members_current.yml file.
3. Use the same data structure the create the new member
4. Save the image in img/team

---

##Contact Page
1. The template for the contact page is stored in _includes/contact.html.
2. To make any changes, this file needs to be edited (there are not data files)

=========

For more details on the site, contact tdillahu@umich.edu
