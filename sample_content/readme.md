---
title: "Read Me"
date: 2023-04-19T13:04:54+09:00
draft: true
main_menu: true
main_menu_order: 10
description: "How to use this."
---
### First of all
- This text describes what you should do after creating a new site with hugo and applying the theme.  
### Initial Setup  
- Copy the entire contents of the directory sample_content to the content folder.  

### Create content to be displayed in the root menu
- There are two methods.  
	1. Create it directly under the content folder.  
`hugo new content/sample.md`  
	2. Create it in a subdirectory.  
`hugo new content/projects/sample.md`  

### Create an extended section
1. Create default md file  
	- Copy the file archetypes/extra_project.md to create, for example, archetypes/sample_project.md.  

2. Create _index.md for the top page  
`hugo new content/sample_project/_index.md`  

3. Initialization of _index.md
	- To display it in the main menu at the top of the site Set main_menu: true to display on the top page. Next, specify the position in the main menu with main_menu_order: 90. Specify the description if necessary.  
`main_menu: true`  
`menu_order: 90`  
`description: "Sample Description"`  

4. Prepare files for extended sections  
	- Create the directory layouts/sample_project/ and copy the files from the directory layouts/extra_projects/.list.html and single.html.  

5. Create the contents of the extended section  
`hugo new content/sample_project/sample1.md`  
	- Also, change the configuration values in sample1.md as needed. For example, set menu_order: 10 for the menu order and description: "Sample Description" for the description.  

### Blog Setup
1. Configuration for config.toml  
`[params]`  
`blog_title = 'Blog Name'`  
`[taxonomies]`  
`tag = 'tags'`  
`category = 'categorise'`  

2. Create _index.md for the top page  
`hugo new content/blog/_index.md`  

3. Initialization of _index.md  
	- To display it in the main menu at the top of the site Set main_menu: true to display on the top page. Next, specify the position in the main menu with main_menu_order: 91. Specify the description if necessary.  
`main_menu: true`  
`main_menu_order: 91`  
`description: "Sample Description"`  

4. Creating blog posts  
`hugo new content/blog/sample.md`  

5. Configure blog post parameters  
	- If you want to make it a hot topic, specify a value greater than 0 for weight. Set values for tags, categorise, and description as needed.  
`weight: 10`  
`tags: [sample,test]`  
`categorise: [sample]`  
`description: "sample description"`  

### Options
- Configuration for config.toml  
`[params]`  
`twitter_user = '@sample'`  

- Change of top page image  
`static/top.png`  

- Change of Twitter card image  
`static/twitter.png`  

### End
