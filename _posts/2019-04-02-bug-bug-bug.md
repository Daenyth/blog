---
layout: post
cover: 'assets/images/pure-function-bg.jpg'
navigation: True
title: Beware the power of configuration
date: 2018-12-02 12:00
tags:
  - scala
  - jvm
  - play
subclass: 'post tag-test tag-content'
logo: 'assets/images/jk_white.svg'
author: kubukoz
disqus: true
categories: kubukoz
---

A few months ago I was working on a task. Part of it required that I upgrade the version of [Play Framework](https://www.playframework.com/) in one of our applications.

Play is one of the frameworks/libraries that my team's applications are built with. Most of these have been upgraded to the newer versions of Play like 2.6.x, whereas a few of them are still running Play 2.3, as they aren't changed very often and the upgrade would involve a significant amount of work.

This application was running Play 2.3, and at the time the latest stable release was 2.6.20. For some reasons that are not important for this story, I needed to upgrade it to a 2.6.x release. So I did.

Everything went well. I got the application working locally, all the tests were passing, and I deployed the application on the testing environment.

For reasons that are beyond my understanding, some applications on the testing environment have a load balancer in front of them, even though they only have one instance.