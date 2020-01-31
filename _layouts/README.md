# layouts

Page templates for your site. 

Layouts are referenced in the YAML headers:

````
---
layout: default
title: My First Website
---
````

Uses the "default" page layout. 

## default layout

When a YAML header includes a layout item, Jekyll will look for the template in the **_layouts** folder. The file that contains the layout should an HTML file with the same name:  **default.html**.

Note the need for spelling consistency: **Default.html** will NOT work. 

The defaul layout typically contains the main page sections that every website needs. 

* head - page settings and imports 
* header - top of the website 
  - navbar (optional )
* body 
  - footer (optional) 
  
The default page will typically look something like this: 

```
<!DOCTYPE html>

    {% include head.html %}

    <body>

    {% include header.html %}

    {{ content }}

    {% include footer.html %}

    </body>

</html>
```


## Additional Templates


### Templates

The purpose of each website is different. GitHub pages are typically used as (1) blogs or (2) documentation. They will often have a couple of other templates in the _layouts folder. 

Let's consider the case of a plain webpage or a blog. Jykyll utilizes inheritance to make new page templates easy to build because we don't have to start from scratch. We can leverage what already exists.

We will call the template **page.html**, so it would be applied on the site page like this:

```
---
layout: page
title: Bio
---
````

The page template might then look like:

````
---
layout: default
---

<h1>{{ page.title }}</h1>

{{ content }}

{% include fancy-table.html %}

````

Note the following: 

**TEMPLATE RECYLING**

The **page** template calls the **default** template, which means the content from this page will be added to the default template where the {{content}} tag exists. 

This is a bit recursive because this page also contains a {{content}} tag. The easiest way to think about what the final page will look like is to copy everything except the YAML header on the new template, and replace the {{content}} tag on the template that is reference. In this case we paste the content from **page** to **default**. The webpage that is created would then have this format:


```
<!DOCTYPE html>

    {% include head.html %}

    <body>

    {% include header.html %}

        <h1>{{ page.title }}</h1>

        {{ content }}

        {% include fancy-table.html %}

    {% include footer.html %}

    </body>

</html>
```

Note that we did not need to include the `<HTML>` document type declaration, the head, header, or footer on the **page** template because it is already included on the **default** template. 

### Page element recursion

![](https://jekyllrb.com/img/jekylllayoutconcept.png)


**INCLUDES**

We can see several `{% liquid tags %}` that use the format *includes some-name.html*. These include statemends operate just like the {{content}} tag where they represent a placeholder. We need to look in the **_includes** folder for the files referenced to see what will be imported. 

In the example here we have the tag `{% include fancy-table.html %}`, which references a fancy table. Tables take a bit to design (you need to lay out columns, rows, content, etc. So to keep the main page clean and easy to understand you can keep that component in a separate file. It also makes it easier to update the design when necessary because different sections of the website will be isolated. You can change just the table without impacting the rest of the page. 

As an example, if you look at the syllabus page in the course shell you see there is a table at the top which contains all of the course info (days and times it meets, room number, office hours, instructor contact info, etc.). This is just a fancy table.

https://ds4ps.org/cpp-523-spr-2020/

The page could look something like this: 

````
---
layout: syllabus
---

{{ content }}

````
And the syllabus template would look like: 

````
---
layout: default
---

<h1>Syllabus</h1>

{% include fancy-table.html %}

{{ content }}

````

The title is static because every syllabus page will have the title Syllabus. The fancy table goes at the top of the page here, before the content. In the syllabus page, then, everything other than the course info at the top is written in plain markdown and imported where the {{content}} tag is on the template. 

