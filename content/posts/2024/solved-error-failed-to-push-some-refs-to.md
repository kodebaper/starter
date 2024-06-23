---
title: "Solved Error Failed to Push Some Refs To"
date: 2024-03-19T06:36:55+07:00
slug: /solved-error-failed-to-push-some-refs/
description: error failed to push some refs to (Rejected main -> main)
image: images/gitrejected.jpg
caption: Photo by santricyber
categories:
  - programming
tags:
  - hugo
  - blogtips
  - solved
draft: false
---

[SOLVED]

*error: failed to push some refs to*
! [Rejected] main -> main (fetch first) (blaaa…..blaaa... blaaa)

in this case, you just use this command below to solve the problem

$ git pull origin master -allow-unrelated-histories

and then you can try again to push your code .....

$ git push -u origin master

I hope this article is useful, happy learning!

