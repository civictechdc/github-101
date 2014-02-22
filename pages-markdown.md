---
layout: main
---

##How to convert your GitHub page to Markdown from HTML

###1 Includes Folder

1 From the main repo page, click on the + sign to create a new file.

2 In the new file name, type: "_includes" and then hit tab.

3 Title the file "header.html" and click commit changes at the bottom of the page. Then create another file in that folder titled "footer.html" and commit changes.

4 Go to the index.html file and cut all of the text above the `<section>` tag. Paste that in the header.html file.

5 In the index.html file, cut all of the text below the `</section>` tag and paste that in the footer.html file.

##2 Layouts Folder

1 From the main repo page, click on the + sign to create a new file.

2 In the new file name, type: "_layouts" and then hit tab.

3 Create one file titled "main.html"

4 In that file, paste this code and then click commit changes.

`{% include header.html %}`
    
`    <!-- MAIN CONTENT -->`

`    <div id="main_content_wrap" class="outer">`

`      <section id="main_content" class="inner">`
      
`      {{ content }}`
      
`      </section>`

`    </div>`
    
`{% include footer.html %}`

##Additional Files

1 Add a new file called ".gitignore" and paste the following code in there:

`.DS_Store`

`_site`

2 Create a file called "_config.yml" and paste the following code in there:

`markdown: kramdown`

3 Edit the "index.html" file by changing its name to "index.md" and replace all of the code in that file with the following code:

`---`

`layout: main`

`---`

4 For any additional website pages you'd like to create, paste the same code at the top of the file as in step 3.
