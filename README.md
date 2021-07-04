# CRIO
## Started Module 1 in CRIO
  + Git Basics
    * Attached file (Git_Basics)
### Gitlab Repositories
  + git@gitlab.crio.do:COHORT_ME_GIT_BASICS_ENROLL_1596802014715/ram75353-ME_GIT_BASICS.git
  + https://gitlab.crio.do/COHORT_ME_GIT_BASICS_ENROLL_1596802014715/ram75353-ME_GIT_BASICS.git
    * To download/upload contents from/to the above Gitlab repositories you’ll have to prove you’re having access to it.
    * Execute the below command to generate an SSH key. SSH protocol allows you to remotely access machines using the SSH key.
    * SSH -> SSH or Secure Shell is a network communication protocol that enables two computers to communicate
    ___________
    * **ssh-keygen -t ed25519 -C "crio-git-byte"** [ssh-keygen Codes](https://www.ssh.com/academy/ssh/keygen)
    ____________
    * Did you notice you were given two links to your Gitlab repository earlier? The one which starts with git@gitlab.crio.do is to be used to authenticate using SSH. The https link authenticates using your gitlab.crio.do username and password Execute cat ~/.ssh/id_ed25519.pub and copy the public key printed. You’ll add this to https://gitlab.crio.do/ in the next step

    * crio-user@ram75353:~$ cat ~/.ssh/id_ed25519.pub
      ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIL3J0omWRsa8BM7Ft6FyMoF25skFKG5o6cSL/OlOO6eU crio-git-byte
    
 ##### [Adding SSH key to Gitlab](https://youtu.be/mNtQ55quG9M)
  + ssh -T git@gitlab.com (use this tto test connection to gitlab)
 __________________________________________________________________________________________________________________________________________________________________________
 #### Milestone 1 (Get that Code)
  + mkdir -p ~/workspace/bytes
  + cd ~/workspace/bytes
* Ensure you clone using the ssh link and not the https link
  + git clone <add-ssh-link-here>
  + git clone git@gitlab.crio.do:COHORT_ME_GIT_BASICS_ENROLL_1596802014715/ram75353-ME_GIT_BASICS.git
    * Cloning into 'ram75353-ME_GIT_BASICS'...
    * warning: You appear to have cloned an empty repository.
  + cd ram75353-ME_GIT_BASICS (to move to my github proj)
  + git status (to check status)
    * On branch master
    * No commits yet
    * nothing to commit (create/copy files and use "git add" to track)
  + crio-user@ram75353:~/workspace/bytes/ram75353-ME_GIT_BASICS$ git remote -v
    * origin  git@gitlab.crio.do:COHORT_ME_GIT_BASICS_ENROLL_1596802014715/ram75353-ME_GIT_BASICS.git (fetch)
    * origin  git@gitlab.crio.do:COHORT_ME_GIT_BASICS_ENROLL_1596802014715/ram75353-ME_GIT_BASICS.git (push)
  
##### References
1) [Git Cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)

2) [A Short History of Git](https://git-scm.com/book/en/v2/Getting-Started-A-Short-History-of-Git)

3) [Branches in Git](https://www.atlassian.com/git/tutorials/using-branches)

4) [What is the git folder?](https://stackoverflow.com/questions/29217859/what-is-the-git-folder/56145562)
 _______________________________
#### Milestone 2 (Add new Changes)
  + Open Folder 'crio-user@ram75353:~/workspace/bytes/ram75353-ME_GIT_BASICS$' and add file 'First.txt'
  + 1 ) **git add 'First.txt'(Filename)**
  + A commit is like a checkpoint in Git where we save the current state of our files. (2)**git commit -m "comment"**) (If no comments -> Aborting commit due to empty commit message.)
  + 3)**git push -u origin master** (To Add the changes and file to repository)
  + If got some error like this  "! [rejected] master -> master (non-fast-forward)" use the following command  "**git pull --rebase origin master**"
  + **git log** to see the 

##### References
  
1) [Git: Add All Files to a Repo](https://stackabuse.com/git-add-all-files-to-a-repo/)

2) [Commit message style guide](http://udacity.github.io/git-styleguide/)

3) [The Git Commit Hash](https://www.mikestreety.co.uk/blog/the-git-commit-hash)
  
______________________________________________________________________________________________________________________________________________________________________________
#### Milestone 3 (Being in Sync)
  
  + Add a Readme.md file in GIT LAB UI
  + Now if you try to push from local to clone it will throw an error like (CONFLICT (content): Merge conflict in README.md)
  + So, Pull the latest code from repository to local "**git pull**"(it will update in local)
  + After use "**git push**" from local to move to repository.
  
##### References
  
1) [Git Pull Explained](https://www.freecodecamp.org/news/git-pull-explained)

2) ["Remote contains work that you don’t have locally" error explained](https://blog.plover.com/prog/git-ff-error.html)

3) [Other ways to resolve the "Remote contains work that you don’t have locally" error](https://stackoverflow.com/q/24357108/9734484)  
______________________________________________________________________________________________________________________________________________________________________________
 #### Points to remember
  + There’s another command, git fetch. How’s it different from a git pull?
git fetch fetches only metadata related to changes and doesn’t actually make any changes to the project files we have locally. We’ll need to do a separate git merge for that whereas git pull naively speaking does both **git pull = git fetch + git merge**
Further reading
-----------------
Git offers several more features which help in maintaining code and collaborating with team members during software development. For example - config, branch, stash, squash etc. You can explore these as needed.

+ [What is Version Control?](https://www.perforce.com/blog/vcs/what-is-version-control)

+ [Oh Shit, Git!?!](https://ohshitgit.com/)

+ [The Advanced Git Guide](https://www.toptal.com/git/the-advanced-git-guide)

Excited? Dig deeper to Git internals for answering the below questions

+ [What actually happens within Git when we do a commit?](https://dzone.com/articles/git-behind-the-curtain-what-happens-when-you-commi)

+ [Each commit gets a unique ID, how is it created?](https://blog.thoughtram.io/git/2014/11/18/the-anatomy-of-a-git-commit.html)
______________________________________________________________________________________________________________________________________________________________________________
## Milestone1: Developer Tools 1
  + [Opening Chrome Developer Tools](https://youtu.be/lU5AS5ntN2w)
#### Get started using Chrome Developer Tools
  + Goto any site and press CLRTL+SHIFT+I or right -> click Inspect.
  + Goto Network tab and click on XHR (XMLHttpRequest). To fetch data from an API endpoint without refreshing the webpage, XMLHttpRequest (XHR) is used. It enables the webpage to update a part of it without disrupting the overall view for the user.
  + Ex. goto https://leetcode.com/problemset/all/ filter with XHR and click on 'all' request. The API endpoint (or the HTTP request URL) is https://leetcode.com/api/problems/all/ which return the JSON format. JavaScript Object Notation (JSON) is a commonly used format to transfer data between computers. JSON is a human readable format with key-value pairs.

##### References
  
1) [Getting started with VS Code](https://code.visualstudio.com/docs/introvideos/basics)

2) [[Video] Inspect Network Activity - Chrome DevTools 101](https://www.youtube.com/watch?v=e1gAyQuIFQo)

3) [Using DevTools to inspect network activity](https://developers.google.com/web/tools/chrome-devtools/network)

4) [Understanding And Using REST APIs](https://www.smashingmagazine.com/2018/01/understanding-using-rest-api/)

5) [What is XMLHttpRequest](https://javascript.info/xmlhttprequest)
______________________________________________________________________________________________________________________________________________________________________________
## Milestone2: Inspecting HTML using Developer Tools
  + Chrome Developer Tools (or DevTools) allows you to inspect the HTML content of a webpage.
  + Open the Chrome Developer Tools window (Right-click and select "Inspect"). Goto the Elements window. Scroll up to find the opening <html> tag.
  + To find the corresponding HTML code press CLRL+SHIFT+C or top left of inspect element window and hover on webpage and click the desired area to see the HTML contents.

##### References

1) [Get Started With Viewing And Changing The DOM](https://developers.google.com/web/tools/chrome-devtools/dom)

2) [What is the HTML DOM?](https://www.w3schools.com/whatis/whatis_htmldom.asp)
  
3) [Introduction to the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)

4) [HTML Tables](https://www.w3schools.com/html/html_tables.asp)
______________________________________________________________________________________________________________________________________________________________________________
##### Summary
  
+ Chrome DevTools is useful to find the API endpoints by inspecting the HTTP requests made by the browser

+ Javascript can be used to fetch data from the APIs and re-model the response according to our need

+ Further Learning
  
1) [[Video] Google Chrome Developer Tools Crash Course](https://www.youtube.com/watch?v=x4q86IjJFag)

2) [Chrome DevTools - 20+ Tips and Tricks](https://www.keycdn.com/blog/chrome-devtools)

3) [Debugging web applications using Chrome browser](https://medium.com/@baphemot/intro-to-debugging-reactjs-applications-67cf7a50b3dd)
______________________________________________________________________________________________________________________________________________________________________________
## HTML& CSS
### HTML (Milestone 1)
+ Common HTML Tags
  * Here are some more, commonly used HTML tags

  * a - for hyperlinks - [Reference](https://www.w3schools.com/tags/tag_a.asp)

  * img - include image - [Reference](https://www.w3schools.com/tags/tag_img.asp)

  * ul/ol/li - unordered and ordered list - [Reference](https://www.w3schools.com/html/html_lists.asp)

  * strong - bolding text - [Reference](https://www.w3schools.com/tags/tag_b.asphttps://www.w3schools.com/tags/tag_b.asp)

  * em - emphasizing text - [Reference](https://www.w3schools.com/tags/tag_em.asp)
  
  * table /thead /tbody /tr /th /td  - add tables - [Reference](https://www.w3schools.com/html/html_tables.asp)
  
  * form/input/label - add forms and input fields - [Reference](https://www.w3schools.com/html/html_forms.asp)

  * button - add a button that users can click - [Reference](https://www.w3schools.com/tags/tag_button.asp)

  * select/option - create a dropdown list - [Reference](https://www.w3schools.com/tags/tag_select.asp)

##### References
  
1) [HTML Basics](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics)

2) [HTML 5 vs HTML 4](https://www.educba.com/html5-vs-html4/)

3) [DOCTYPE Declaration](https://html.com/tags/doctype/)

4) [Display HTML tags as plain text](https://devpractical.com/display-html-tags-as-plain-text)

5) [HTML 4 "i" and “b” tags vs HTML 5 “em” and “strong” tags](https://stackoverflow.com/a/21334472)

6) [More semantic HTML5 alternatives to div tag](https://www.w3.org/WAI/tutorials/page-structure/regions/)

7) [HTML Attributes](https://www.w3schools.com/html/html_attributes.asp)

______________________________________________________________________________________________________________________________________________________________________________
### CSS Milestone 2 
#### Getting started with CSS
  + <b>Inline CSS</b>
    * An inline CSS is used to apply a unique style to a single HTML element Eg : <'h1 style="color:blue;">A Blue Heading</h1'>
  + <b>Internal CSS</b>
    * An internal CSS is used to define a style for a single HTML page.An internal CSS is defined in the <head> section of an HTML page, within a <style> element.
    * Eg: <head>
            <style>
              body {background-color: powderblue;}
                h1   {color: blue;}
                p    {color: red;}
            </style>
          </head>
  + <b>External CSS</b>
    * An external style sheet is used to define the style for many HTML pages. 
    * To use an external style sheet, add a link to it in the <head> section of each HTML page: <'link rel="stylesheet" href="styles.css">
  + <b>[CSS Box Model](https://css-playground.com/view/53/box-model-introduction-playground)</b>
    * 1) margin - is the distance to keep from the neighboring elements
      2) border - is the border for the HTML element’s region (border-width, border-type and border-color)
      3) padding - is the space, content of the element likes to keep from its border( The 4 values modify the top, right, bottom and left)
      4) height and width - specifies the height and width of the content area
    * Total width of element = width + padding-left + padding-right + border-left + border-right + margin-left + margin-right
  + Here’s the checkpoint code
    * [HTML](https://gitlab.crio.do/crio_bytes/me_html_css/-/blob/master/solution/html/m2-solution.html)
    * [CSS](https://gitlab.crio.do/crio_bytes/me_html_css/-/blob/master/solution/css/m2-solution.css)

##### References

1) [How CSS works](https://developer.mozilla.org/en-US/docs/Learn/CSS/First_steps/How_CSS_works)

2) [CSS Specificity](https://www.w3schools.com/css/css_specificity.asp)

3) [How to comment in CSS](https://www.w3schools.com/css/css_comments.asp)

4) [CSS: font-family](https://www.w3schools.com/css/css_font.asp)

5) [CSS: display](https://www.w3schools.com/css/css_display_visibility.asp)

6) [CSS Box Model](https://css-playground.com/view/53/box-model-introduction-playground)

7) [CSS measurement units](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units)

8) [View CSS using Chrome Developer Tools](https://developers.google.com/web/tools/chrome-devtools/css/reference#computed)
______________________________________________________________________________________________________________________________________________________________________________
#### Milestone 3 - Grouping HTML Elements
  + class is useful to identify a group of same or different tag types easily and apply CSS styling for the entire group elements. Multiple elements can have the same class names. Eg: all the elements below belong to the class, "tile"
  + Here’s the checkpoint code
    * [HTML](https://gitlab.crio.do/crio_bytes/me_html_css/-/blob/master/solution/html/m3-solution.html)
    * [CSS](https://gitlab.crio.do/crio_bytes/me_html_css/-/blob/master/solution/css/m3-solution.css)

##### References
1) [HTML id attribute](https://www.w3schools.com/html/html_id.asp)

2) [HTML class attribute](https://www.w3schools.com/html/html_classes.asp)

3) [CSS Selectors](https://www.w3schools.com/cssref/css_selectors.asp)

4) [HTML ID and Class](https://css-tricks.com/the-difference-between-id-and-class/)

5) [When to use Class vs ID in CSS](https://www.developintelligence.com/blog/2016/04/css-class-vs-id-which-one-to-use/)
  ______________________________________________________________________________________________________________________________________________________________________________
#### Milestone 4 - CSS Flexbox
  + [CSS Flexbox in 100 seconds](https://youtu.be/K74l26pE4YA)
  + CSS Flexbox is used to automatically arrange HTML elements according to the screen size i.e, the page will look clean viewed on a laptop or on mobile. Flexbox works by setting an HTML element as a flex container and positions the child elements within the flex container element.
  + **display: flex;** You’ll see all six tiles arranged in the same row. The horizontal axis is the main axis of the flex container by default which makes the vertical axis, the cross axis. Try using the flex-direction property to change the main axis of the flex container.
  + **flex-wrap: wrap;** property on the flex container to split the elements into multiple lines when required
  + **justify-content: center;** The justify-content property of the flex container can be used to change how the elements are aligned across the main axis (horizontal axis here).
  + **align-items: baseline;** The align-items property is used to align the elements across the cross axis (vertical axis here).
    *  Setting align-items: flex-start; sets the height of the containers based on their text content
  + Here’s the checkpoint code
    * [HTML](https://gitlab.crio.do/crio_bytes/me_html_css/-/blob/master/solution/html/m4-solution.html)
    * [CSS](https://gitlab.crio.do/crio_bytes/me_html_css/-/blob/master/solution/css/m4-solution.css)
      
##### References

1) [Flexbox Playground](https://codepen.io/enxaneta/full/adLPwv/)

2) [[Game] Flexbox Froggy](https://flexboxfroggy.com/)

3) [A Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

4) [Common Flexbox Patterns](https://tobiasahlin.com/blog/common-flexbox-patterns/)

5) [FlexBox Properties Cheatsheet](https://yoksel.github.io/flex-cheatsheet/)
 ______________________________________________________________________________________________________________________________________________________________________________
#### Milestone 5 - Positioning in CSS
  + The CSS position property can be used to modify the position of an HTML element. The top/bottom/left/right properties set the distance of the element from each of the four sides of the viewport or it’s parent element or it’s current position based on its position property.
  + **position: absolute**  measures distance from the viewport (screen). 0px from the top edge of the screen and 0px from the right edge of the screen puts the element at the top-right corner of the screen. Try it out! also try **position:fixed**
  + Here’s the checkpoint code
    * [HTML](https://gitlab.crio.do/crio_bytes/me_html_css/-/blob/master/solution/html/m5-solution.html)
    * [CSS](https://gitlab.crio.do/crio_bytes/me_html_css/-/blob/master/solution/css/m5-solution.css)
##### References

1) [CSS: position](https://developer.mozilla.org/en-US/docs/Web/CSS/position)

2) [[Video]CSS Absolute vs Relative](https://www.youtube.com/watch?v=3PDQDRJq5Ls)

3) [CSS Positioning made easy](https://alistapart.com/article/css-positioning-101/)

4) [Learn CSS Positioning in just 10 steps](http://www.barelyfitz.com/screencast/html-training/css/positioning/)
 ______________________________________________________________________________________________________________________________________________________________________________
### Milestone 6 - Build it!
  + [What are inline and block HTML elements?](https://www.w3schools.com/html/html_blocks.asp)
    * A block-level element always starts on a new line.A block-level element always takes up the full width available (stretches out to the left and right as far as it can).A block level element has a top and a bottom margin, whereas an inline element does not.The <div> element is a block-level element.
    * An inline element does not start on a new line.An inline element only takes up as much width as necessary.This is a <span> element inside a paragraph.
  + Here’s the checkpoint code
    * [HTML](https://gitlab.crio.do/crio_bytes/me_html_css/-/blob/master/solution/html/m6-solution.html)
    * [CSS](https://gitlab.crio.do/crio_bytes/me_html_css/-/blob/master/solution/css/m6-solution.css)
##### References

1) [HTML <a> tag](https://www.w3schools.com/tags/tag_a.asp)

2) [CSS Styling Links](https://www.w3schools.com/css/css_link.asp)

3) [CSS: overflow](https://www.w3schools.com/cssref/pr_pos_overflow.asp)

4) [CSS: text-align](https://www.w3schools.com/cssref/pr_text_text-align.ASP)

5) [HTML: image](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Images_in_HTML)

6) [CSS: styling images](https://www.w3schools.com/css/css3_images.asp)

7) [Freely usable images](https://unsplash.com/)

8) [How to create a sticky footer](https://www.w3schools.com/howto/howto_css_fixed_footer.asp)

9) [Meaning of space in CSS selectors](https://stackoverflow.com/a/10036181)

##### Further reading

1) [How do browsers render HTML](https://medium.com/@mustafa.abdelmogoud/how-the-browser-renders-html-css-27920d8ccaa6)

2) ["auto" in CSS](https://stackoverflow.com/a/3170774)

3) [What is aria-label and how should I use it?](https://stackoverflow.com/a/22040485)

4) [HTML Role Attribute Explained](https://www.freecodecamp.org/news/html-role-attribute/)

5) [Handling common HTML and CSS problems](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Cross_browser_testing/HTML_and_CSS)
______________________________________________________________________________________________________________________________________________________________________________
## Bootstrap
  
### Milestone 1 - Using plain CSS to style your elements
  + [About Bootstrap](https://getbootstrap.com/docs/4.5/getting-started/introduction/)
  + Adding Bootstrap links 
    * Inspect page after adding link (<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" integrity="sha384-JcKb8q3iqJ61gNV9KGb8thSsNjpSL0n8PARn9HuZOnIxN0hoP+VmmDGMN5t9UJ0Z" crossorigin="anonymous"/>) in HTML page. Goto Network tab-> All -> Find and click Bootstrap.min.css (style type) -> under preview tab can find all styles (Find alert - used in link for display)
  + [Alerts](https://getbootstrap.com/docs/4.5/components/alerts/)

##### References

1) [Bootstrap - Introduction](https://getbootstrap.com/docs/4.5/getting-started/introduction/)

2) [Ways to add Bootstrap](https://www.bootstrapdash.com/use-bootstrap-with-html/)

3) [Bootstrap 3 vs Bootstrap 4](https://www.bootstrapdash.com/bootstrap-3-vs-4/)

4) [Bootstrap - Alerts](https://getbootstrap.com/docs/4.5/components/alerts/)

5) [Bootstrap - Colors](https://getbootstrap.com/docs/4.0/utilities/colors/)

6) [Inspect Network Activity In Chrome DevTools](https://developers.google.com/web/tools/chrome-devtools/network)

7) ["auto" in CSS](https://stackoverflow.com/a/3170774)
 
______________________________________________________________________________________________________________________________________________________________________________
  
### Milestone 2 -Create a responsive navigation bar
  + [Responsive Navigation bar video](https://youtu.be/v1Cs2ZVgFgU)
  + 
    
##### References

1) [Bootstrap - Navigation using navbar](https://getbootstrap.com/docs/4.5/components/navbar/)

2) [Bootstrap - Layout](https://getbootstrap.com/docs/4.1/layout/overview/)

3) [Bootstrap - Responsive behaviours for Navigation bars](https://getbootstrap.com/docs/4.0/components/navbar/#responsive-behaviors)

4) [Bootstrap - Collapse](https://getbootstrap.com/docs/4.0/components/collapse/)

5) [data-toggle attribute](https://www.geeksforgeeks.org/data-toggle-attributes-in-twitter-bootstrap/)

6) [What are meta tags?](https://moz.com/blog/the-ultimate-guide-to-seo-meta-tags#:%7E:text=What%20are%20Meta%20Tags%3F,search%20engines%20and%20web%20crawlers.)

7) [Using the viewport meta tag to control layout on mobile browsers](https://developer.mozilla.org/en-US/docs/Mozilla/Mobile/Viewport_meta_tag)
