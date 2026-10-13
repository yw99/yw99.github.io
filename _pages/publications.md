---
layout: page
permalink: /publications/
title: publications
description: publications in reversed chronological order.
description_extra: >-
  Also see <a href="https://scholar.google.com/citations?hl=en&user=uXJoQCAAAAAJ" target="_blank">Google Scholar</a>.
  * marks equal contribution; <sup>αβ</sup> marks alphabetical author order.
nav: true
nav_order: 2
---

<!-- _pages/publications.md -->
{% include ongoing_works.liquid %}

<div class="publications">
{% bibliography --query @*[ongoing!=true]* %}

</div>
