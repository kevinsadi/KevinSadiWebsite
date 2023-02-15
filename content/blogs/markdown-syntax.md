---
title: "Third Person Hitscan Firing Systems"
date: 2022-02-10T23:29:21+05:30
draft: false
github_link: "https://github.com/gurusabarish/hugo-profile"
author: "Kevin Sadi"
tags:
  - Unreal Engine
  - Third Person Shooting
  - example
image: /images/blogs/tempimagelol.png
description: ""
toc:
---

Honestly, I was a bit surprised when I embarked on creating a third person shooter how little literature there is on how to properly implement a third person hitscan firing weapon aside from working through an entire course. However, I think the general idea of it is really easy and geometrically satisfying. Let's jump right into it.

## C++ or Blueprints?

Either way, it really doesn't matter. I'm going to be explaining the theory behind how this works so you can implement it in any system. I chose to do so in C++ so I will show it in that way.