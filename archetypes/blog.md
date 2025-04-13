---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: false

description:

author:
  name: Yong Khang

hero: /images/jujuballs.jpg
menu:
  sidebar:
    name: "{{ replace .Name "-" " " | title }}"
    identifier: {{ .Name }}
    weight: 10
    parent: blog
tags:
  - Personal
---

