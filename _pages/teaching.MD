---
permalink: /teaching/
title: "Teaching"
author_profile: true
---

{% include custom-styles.html %}

<p class="lede">I teach on the data science side of the Master's programmes at DSV, and supervise Master's theses in the spring. Thesis work in my group is meant to go somewhere — two of the projects below have since been published with the student as first author.</p>

## Courses

<div class="entries">
  <div class="entry">
    <div class="entry-when">Fall</div>
    <p class="entry-what">
      Lecture on Data Modalities
      <span class="venue">Foundations of Data Science</span>
    </p>
  </div>
  <div class="entry">
    <div class="entry-when">Fall</div>
    <p class="entry-what">
      Laboratory sessions
      <span class="venue">Foundations of Data Science</span>
    </p>
  </div>
</div>

## Supervising a Master's thesis

I take on thesis students in the spring semester. If you are thinking about it, the topics I propose usually fall into one of three areas — though what matters more than the topic is that you are actually interested in it and will stay with it when the first approach stops working.

<div class="strands">
  <div class="strand">
    <h3>Psychotherapy interactions</h3>
    <p>Machine learning applied to what happens between therapist and patient across audio, video and text.</p>
  </div>
  <div class="strand">
    <h3>Cancer development</h3>
    <p>Predicting progression and metastasis from real clinical cohorts.</p>
  </div>
  <div class="strand">
    <h3>Electronic health records</h3>
    <p>Data mining from routinely collected clinical data, and the explainability problems that come with it.</p>
  </div>
</div>

Proposals outside these areas are welcome. Write to me at [franco.rugolon@dsv.su.se](mailto:franco.rugolon@dsv.su.se) with a paragraph on what you want to work on and why.

## Completed theses

<div class="entries">
{% assign theses = site.data.theses | sort: "year" | reverse %}
{% for t in theses %}
  <div class="entry">
    <div class="entry-when">{{ t.year }}</div>
    <p class="entry-what">
      {{ t.title }} — {{ t.student }}{% if t.co %} (co-supervised){% endif %}
      {% if t.paper_url %}<span class="venue">Published as <a href="{{ t.paper_url | relative_url }}">{{ t.paper_note }}</a></span>{% endif %}
    </p>
  </div>
{% endfor %}
</div>
