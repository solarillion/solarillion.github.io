---
layout: single
title: Edge Machine Learning
permalink: /edge-ml/
excerpt: Edge Machine Learning teams at Solarillion Foundation.
---
<div style="margin-top: 2rem;">
<h2>What is Edge ML?</h2>
<p>
This ML Team focuses on solving data-driven problems in the real-world, industrial and research scenarios. They often handle large amounts of data and have also worked on optimised intelligence algorithms.
</p>
<p>
Current research teams are focused on deploying sophisticated models on wearables and other resource-constrained devices (edge devices). Research groups implement models with low-memory footprint to analyse sensor data for healthcare applications.
</p>
<h2>Publications</h2>
{% for year in (2000..2100) reversed %}
{% assign y = year | downcase %}
{% assign current = site.data.publications | where: "year", y | where_exp: "item", "item.team contains 'EML'" %}
{% if current.size > 0 %}
<h3>{{ y }}</h3>
{% for publication_id in current %}
    {% include publication.html publication=publication_id %}
{% endfor %}
{% endif %}
{% endfor %}
</div>