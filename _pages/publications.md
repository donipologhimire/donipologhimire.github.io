---
layout: page
permalink: /publications/
title: publications
description: publications by categories in reversed chronological order.
nav: true
nav_order: 1
---

<!-- _pages/publications.md -->

<!-- Bibsearch Feature -->

{% include bib_search.liquid %}

<div class="publications">

{% bibliography %}

</div>

---

## Reviewer Experience

<div class="reviewer-experience">
  <h3 class="mt-4">Conference :</h3>
  <ul class="conference-list">
    <li><strong>IEEE/RSJ International Conference on Intelligent Robots and Systems (IROS)</strong> - 2024, 2025</li>
    <li><strong>European Control Conference (ECC)</strong> - 2025</li>
  </ul>
  
  <h3 class="mt-4">Journal :</h3>
  <ul class="journal-list">
    <li><strong>IEEE Robotics and Automation Letters (RA-L)</strong> - 2024 ,2025</li>
    <li><strong>Automatica</strong> - 2025</li>
  </ul>
</div>

<style>
  .reviewer-experience {
    margin-top: 3 rem;
  }
  .conference-list, .journal-list {
    list-style-type: none;
    padding-left: 0;
    font-size: 0.8rem;
  }
  .conference-list li, .journal-list li {
    margin-bottom: 0.5rem;
    padding: 0.5rem;
    border-radius: 4px;
    background-color: #f8f9fa;
  }
  .conference-list , .journal-list  {
    font-size: 0.8rem;
  }
</style>