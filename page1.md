---
layout: nice-text
title: 'Nice Layout'
---




![]({{site.url}}/assets/img/hey-world.png)  



## Lorem Ipsum

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

<a href="https://github.com/DS4PS/barebones-jekyll/blob/master/_layouts/nice-text.html" target = "_blank"> 
          <button onclick="href=''"> See Page Layout <i class="fa fa-github 2x" id="github_icon"></i> </button>
</a>


<br>
<hr>
<br>




<blockquote>
<pre>
<code>

          ###
          ###  YAML HEADER FOR PAGE
          ###  
          ###  ---
          ###  layout: nice-text
          ###  title: 'Nice Layout'
          ###  ---
          ###


          ### 
          ###  CREATE A DIV FOR PRETTY-TEXT
          ###
          ###  div limits formatting only to
          ###  text between the div tags
          ###

               &lt;div class="pretty-text">

                 &lt;h1>  &lbrace;&lbrace; page.title }}  </h1>

                          &lbrace;&lbrace; content }}

               &lt;/div>


          ###
          ###  ADD THESE ELEMENTS TO CSS STYLE SHEET
          ###
          ###  CSS RULES:
          ###
          ###  body &lbrace;...}  applies to everything in body
          ###  body p &lbrace;...}  only paragraphs in body
          ###  
          ###  .pretty-text &lbrace;...} references a class
          ###  &lt;div class="pretty-text">
          ###
          ###  #ryan &lbrace;...} references an id
          ###  &lt;div id="ryan">
          ###



               &lt;style>

               .pretty-text {
                  margin-top: 100px;
                  margin-bottom: 100px;
                  padding-left: 30px;
                  padding-right: 30px;
                  text-align: justify;
               }

               .pretty-text p {
                   line-height: 1.8
               }

               .pretty-text h1 {
                   color: darkred;
                   font-size: 40px;
                }

               .pretty-text h2 {
                   color: darkred;
                   font-size: 30px;
                   margin-top: 60px;
                }

                .pretty-text img {
                   border: 1px solid #ddd;
                   border-radius: 8px;
                   padding: 5px;
                   width: 400px;
                   display: block;
                   margin-left: auto;
                   margin-right: auto;
                   width: 50%;
                   box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 
                               0 6px 20px 0 rgba(0, 0, 0, 0.19);
                }

                .pretty-text img:hover {
                   box-shadow: 0 0 3px 1px rgba(0, 140, 186, 0.5);
                }

                &lt;/style>

</code>
</pre>
</blockquote>

