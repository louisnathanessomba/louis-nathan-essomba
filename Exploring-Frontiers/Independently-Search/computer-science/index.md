---
title: Computer Science
layout: section_with_posts
---

# *Algorithms, AI, and edge computing for scalable, ethical systems.*

This subsection dives into **computational experiments** that power my projects. It is here that I apply the skills I learn regularly in computer-science.

---

## **Featured Research**
### **[Local-First AI: Algorithms and Ethics]({{ "/Exploring-Frontiers/Independently-Search/computer-science/local-ai" | relative_url }})**
![Local AI]({{ "/assets/diagrams/local-ai-algorithms.png" | relative_url }})
A technical and ethical analysis of **offline-capable AI models** for edge devices.

### **[Edge Computing for IoT]({{ "/Exploring-Frontiers/Independently-Search/computer-science/edge-iot" | relative_url }})**
![Edge IoT]({{ "/assets/diagrams/edge-iot-architecture.png" | relative_url }})
How **decentralized computing** enables scalable IoT systems in low-connectivity regions.

---

## **All Computer Science Research**
{% for post in site.exploring_frontiers %}
{% if post.category == "computer-science" %}
<div class="cs-post-block">
  <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
  {% if post.featured_image %}
  ![{{ post.featured_alt }}]({{ post.featured_image | relative_url }})
  {% elsif post.featured_video %}
  <video controls>
    <source src="{{ post.featured_video | relative_url }}" type="video/mp4">
  </video>
  {% endif %}
  <p>{{ post.excerpt }}</p>
  <div class="post-meta">
    {% if post.related_project %}
    <span class="related-link">
      🔗 Related Project: <a href="{{ post.related_project | relative_url }}">{{ post.related_project_title }}</a>
    </span>
    {% endif %}
    {% if post.tags %}
    <span class="tags">
      🏷️ Tags: {{ post.tags | join: ", " }}
    </span>
    {% endif %}
  </div>
  <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
</div>
{% endif %}
{% endfor %}
