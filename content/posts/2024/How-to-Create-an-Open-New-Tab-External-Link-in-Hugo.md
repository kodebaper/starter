---
title: "How to Create an Open New Tab External Link in Hugo"
date: 2024-04-30T17:23:39+07:00
draft: false
slug: /open-new-tab-external-link-in-hugo/
description: Create an Open New Tab External Link in Hugo.
image: images/hugoexli.png
caption: Photo by Santricyber.
categories:
  - programming
tags:
  - programming
  - hugo-ssg
  - framework
---

Here's how to create*external link by hugo*, so it's easy when we open a link on one page then the link we open will open in a new tab in the browser. The question is is this important? for myself this is important in terms of how far we will know the quality of the content on our blog or website, whether users like it or not. Where do you do it from? namely through monitoring the Bounce Rate on*Google Analytic*, now the function is to make external links to be able to open in new tabs will lower the number*bounce rate* quality on *Google Analytic*


As for the way like this, create a file named`render-link.html` in your theme layouts folder. The order goes like this`layouts/_default/_markup/render-link.html`,


````
layouts
   └── _default  
       └── _markup
           └── render-link.html
````


Then for the contents of the file`render-link.html` itself is more or less like this:

``````
   <a href="{{ .Destination | safeURL }}"{{ with .Title}} title="{{ . }}"{{ end }}{{ if strings.HasPrefix .Destination "http" }} rel="noopener noreferrer" target="_blank"{{ end }}>{{ .Text }}</a>
   
```````


Now if you make an external link in the content, then if the link is in *click* it will open in a new tab. Hope it is useful!