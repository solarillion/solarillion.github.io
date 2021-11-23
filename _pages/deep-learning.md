---
layout: single
title: Deep Learning
permalink: /dl/
excerpt: Deep Learning teams at Solarillion Foundation.
---
<div style="margin-top: 2rem;">
<h2>What is Deep Learning?</h2>
<p>There are two broad sub-categories that our teams are divided into in Deep Learning.</p>
<p>
The <b>Computer Vision</b> research subgroup focuses on the detection of objects and events from image and video data. Latest research by the team include real-time surveillance-based crime detection.
</p>
<p>
The <b>Natural Language Processing</b> team works on tasks like classification, sentiment analysis and machine translation. The most recent work in this domain introduced a Multi Context Transformer architecture for Sign Language Translation.
</p>
<h2>Publications</h2>
{% for year in (2000..2100) reversed %}
{% assign y = year | downcase %}
{% assign current = site.data.publications | where: "year", y | where_exp: "item", "item.team contains 'DL'"  %}
{% if current.size > 0 %}
<h3>{{ y }}</h3>
{% for publication_id in current %}
    {% include publication.html publication=publication_id %}
{% endfor %}
{% endif %}
{% endfor %}
</div>