---
permalink: /
title: "Franco Rugolon"
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

{% include custom-styles.html %}

<p class="lede">I build machine learning models that combine several kinds of clinical and behavioural data at once — records, text, speech, gaze, facial movement — and methods that let a practitioner see why a model said what it said.</p>

I am a PhD student at the [Department of Computer and Systems Sciences](https://www.su.se/english/divisions/department-of-computer-and-systems-sciences) at Stockholm University, in the [Data Science Research Group](https://www.su.se/english/research/research-catalogue/research-groups/6/data-science-research-group), supervised by Professor [Panagiotis Papapetrou](https://www.su.se/profiles/ppapa-1.194080) and Senior Lecturer [Ioanna Miliou](https://www.su.se/profiles/iomi2003-1.548427). My doctoral project, [Let's talk about nonverbal communication](https://www.su.se/forskning/forskningsprojekt/l%C3%A5t-oss-prata-om-icke-verbal-kommunikation), is a collaboration with the Department of Psychology, funded by the Marcus and Amalia Wallenberg Foundation.

I came to this from clinical practice rather than from computer science. I trained as a physiotherapist in Padua and spent a year as the sole physiotherapist for lung transplant recipients at the Azienda Ospedale Università Padova, following patients from post-operative intensive care through to discharge. That is still what shapes how I think about clinical machine learning: a model is only useful if the person at the bedside can understand what it is telling them.

<div class="strands">
  <div class="strand">
    <h3>Psychotherapy as interaction</h3>
    <p>Modelling what passes between therapist and patient — tone, pause, gaze — and what it says about the working alliance.</p>
  </div>
  <div class="strand">
    <h3>Disease progression</h3>
    <p>Predicting how a patient's illness will develop, using structured records and clinical text together rather than separately.</p>
  </div>
  <div class="strand">
    <h3>Explainability</h3>
    <p>Counterfactual and attribution methods for multimodal models, and whether the explanations help the people receiving them.</p>
  </div>
</div>

<p class="more"><a href="/research/">More on each of these</a></p>

## Recent work

<div class="entries">
{% assign recent = site.publications | sort: "date" | reverse %}
{% for post in recent limit: 3 %}
  <div class="entry">
    <div class="entry-when">{{ post.date | date: "%Y" }}</div>
    <p class="entry-what">
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      {% if post.venue %}<span class="venue">{{ post.venue }}</span>{% endif %}
    </p>
  </div>
{% endfor %}
</div>

<p class="more"><a href="/publications/">All publications</a></p>

## News

<div class="entries">
{% for item in site.data.news %}
  <div class="entry">
    <div class="entry-when">{{ item.date }}</div>
    <p class="entry-what">{{ item.text }}</p>
  </div>
{% endfor %}
</div>

You can reach me at [franco.rugolon@dsv.su.se](mailto:franco.rugolon@dsv.su.se).
