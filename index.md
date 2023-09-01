---
layout: single
title: Course Overview
toc: true
toc_label: "Table of Contents"
toc_icon: "cog"
author_info: true
---

# Information for CSE 431

**CSE 431: Algorithm Engineering**

Below are the documents and links needed for Fall 2023.

**[Syllabus](syllabus.html)** - provides basic information about the course including how you will be graded.

**[Piazza](https://piazza.com/class/ky8ltkngb2bf2)** a place for asynchronous discussions and Q&A sessions.

Below are the week-by-week topics that will be covered.


# Due dates

- Every friday: weekly lecture review
- Homework: 9/13, 9/27, 10/11, 10/25, 11/8, 11/22, 12/6
- Mid-term exam: scheduled individually between October 15 - 20
- Final exam: scheduled individually between December 10 - 15

# Current course content

{% for post in site.weeks %}

  {% assign this_week = "now" | date: "%W" | minus: 1 %}
  {% assign last_week = "now" | date: "%W" | minus: 2 %}
  {% assign next_week = "now" | date: "%W" | plus: 0 %}

  {% assign postWeek = post.date | date: "%W" | minus: 0 %}

  {% if postWeek == last_week %}
   <h2 id="LastWeek">Last week: <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
  {% endif %}

  {% if postWeek == this_week %}
   <h2 id="ThisWeek">This week: <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
  {% endif %}

 {% if postWeek == next_week %}
   <h2 id="NextWeek">Next week: <a href="{{ site.url }}{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h2>
  {% endif %}


{% endfor %}

# Reference material

## Data structure runtimes table

![Table of big-O time complexities for common operations on various data structures](DataStructureRuntimes.png)


## Debugging Guide

[Debugging Guide](https://github.com/amantham20/docs4debug/blob/main/Debug.md)
