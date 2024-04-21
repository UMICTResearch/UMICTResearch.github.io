UMICTResearch Team website
====================

##Notes
This README file exclusively provides instructions for adding a new article or paper to the Sustainability Development Goals (SDG) section of the website. For guidance on other sections of the website, please refer to the instructions in the separate README file.

## Table of Contents
1. [Sustainability Development Goals (SDG) Projects](#SDG-projects)
2. [Notes](#Notes)

---

#SDG-projects
1. **Files Overview:**
   - Two important files: `_data` and `_asset`.

2. **Adding PDF and Image:**
   - Get the PDF of the article and image (jpg) of the first page of the article.
   - Open the `_assets` folder with 17 subfolders for each SDG.
   - Identify the most suitable SDG for the article and add the PDF and image to the corresponding folder (e.g., gender-equality).

3. **Updating paper details on the website:**
   - Open the `_data` folder with 17 `.yml` files for each SDG.
   - Choose the relevant `.yml` file based on the chosen article.
   - Open the chosen `.yml` file and add paper details.(e.g., gender-equality.yml)
   - Ensure correct naming of PDF and image as created in the `_asset` folder.
   - Make sure you list the most recent paper at the top of the .yml file

#Notes
1. **Number of published papers in each SDG:**
   - The number of papers will auto-update as and when more papers are added in the future: The code for this is in the `_includes` file under the `projects_present.html`.

2. **SDG Categories with most number of papers listed first:**
   - The SDG cards will list in descending order with categories that have most number of papers, first. The code for this is also in the `_includes` file under the `projects_present.html`.

3. **SDGs with no papers published:**
   - The SDGs that do not have any papers in them will not be shown on the website: The code for this is in the `_includes` file under the `projects_present.html`.
   - Note that files have been established for each Sustainable Development Goal (SDG) within the internal file structure. Hence, as papers are incorporated into any SDG file in the future, the system will automatically reflect the updates. For ex, if there are currently no papers in SDG Goal number 7 and you choose to include one, the website will dynamically display the SDG Goal 7 card and update the paper count to "1".
  
4. **Updating UN descriptions:**
   - To update the current UN Description, open `_posts` and choose an SDGfile. Update `subtitle` and `description` fields. 

====================
For more details on the site, contact tdillahu@umich.edu
