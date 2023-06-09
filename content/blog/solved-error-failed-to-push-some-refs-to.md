---
title: "Solved Error Failed to Push Some Refs To"
date: 2023-06-09T16:41:56+07:00
draft: false
---

--------------

[SOLVED]

*error: failed to push some refs to*
! [Rejected] main -> main (fetch first) (blaaa…..blaaa... blaaa)

in this case, you just use this command below to solve the problem

$ git pull origin master -allow-unrelated-histories

and then you can try again to push your code .....

$ git push -u origin master

I hope this article is useful, happy learning!