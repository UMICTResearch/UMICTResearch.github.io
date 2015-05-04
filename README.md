UMICTResearch Team website
====================

## Instructions for Updating the website

###Structure

###Homepage Slider
1. Template used: _includes/header.html
2. The slider images are changed using CSS3 animations. The CSS is stored towards the end of the CSS file: _includes/css/agency.css
3. The images are available in img/sliders/<slidenumber>.jpg

###Projects
1. All projects are stored in '_posts' with the file name as <date>project<number>.yml
2. The order is defined by the <dates>
3. Each post contains following fields:
    - layout (this is to select which template will be used to render the main project page)
    - title (project name)
    - subtitle (short description of the project)
    - date
    - thumbnail (name of thumbnail image for the project which is displayed on the homepage and the project page)
    - alt (alternative description of image to meet accesibility standards)
    - description (duplicate field could be used elsewhere on the website)
    - datafile (contains name of data file which has list of associated papers. This data file is present in the '_data' directory)
4. To change any detail, updates to the fields is the only required task

Projects are in '/_posts'

Images are in '/img/project'

###About

Images are in '/img/about/'

###Team

Team members and info are in '_config.yml'

Images are in '/img/team/'


### Credit for theme

[Available Here](https://y7kim.github.io/agency-jekyll-theme)

=========

For more details on the site, contact tdillahu@umich.edu
