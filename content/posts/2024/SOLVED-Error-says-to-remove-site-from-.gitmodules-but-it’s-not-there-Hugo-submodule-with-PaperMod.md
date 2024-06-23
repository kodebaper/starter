---
title: "SOLVED Error Says to Remove Site From .Gitmodules but It’s Not There Hugo Submodule With PaperMod"
date: 2024-03-19T06:30:45+07:00
slug: /hugo-papermod-theme-use-as-submodule/
description: in this case, i install Hugo PaperMod theme use as submodule
image: images/gitsubmodule.jpg
caption: Photo by santricyber
categories:
  - programming
tags:
  - hugo
  - blogtips
  - solved
draft: false
---

**i will to explain why hugo PaperMod can't deploy to github because error says to remove site from .gitmodules but it's not ......**_

in this case, i install Hugo PaperMod theme use as submodule.

why error can't deploy to github because from .gimodules it appears? this happens because no file .gitmodules inside my hugo project, for that i need to create a file .gitmodules, Inside the .gitmodules file contains.

```
[submodule "themes/PaperMod"]
	path = themes/PaperMod
	url = https://github.com/adityatelange/hugo-PaperMod.git
```

 the location of **.gitmodules** file is more or less like this


``````````flow
-->your hugo project
     |
      -->.gitmodules file
``````````

and should this matter be resolved 😃
