---
layout: archive
title: "Substack Blog"
permalink: /blog/
author_profile: true
---

For some of my personal thoughts you can see my [Substack Blog](https://substack.com/@robfiskdata/posts), where I try to write about things I find interesting relating to the use of statistics, data and AI as they relate to every day issues. This has been more barren than I'd like since I've been busy, so currently only features the essay 'Statistics for hope' - an adaptation of a talk I gave in the penultimate year of my degree. However, in the pipeline I have essays like 'Is Erling Haaland a Statistical Anaomaly?' and 'Predictive policing and the limits of using AI for faster decision making'.

{% for post in site.blog %}
  {% include archive-single-talk.html %}
{% endfor %}
