---
title: "SOLVED :Error says to remove site from .gitmodules but it’s not there Hugo submodule with PaperMod "
date: 2022-10-03T08:40:16+07:00
draft: false
tags:  ["hugo", "static site", "Git"]
Categories: ["programming"]
description: "Error says to remove site from .gitmodules"
---

_**i will to explain why hugo PaperMod can't deploy to github because error says to remove site from .gitmodules but it's not ......**_

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

