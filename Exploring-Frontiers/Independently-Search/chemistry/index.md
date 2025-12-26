---
title: Chemistry
layout: section_with_posts
---

# *Sustainable materials, reactions, and applications for IoT and industrial use.*

This section explores how **chemical principles**—biodegradability, material science, and recycling—inform my projects. My work here connects to:
- **[Applied Projects]({{ "/Applied-Works/" | relative_url }})** (e.g., eco-friendly hardware for WhirlWing).
- **[Ethics & Ecology]({{ "/Ethics-&-Ecology/" | relative_url }})** (e.g., sustainable manufacturing).

---

## **Featured Research**
### **[Biodegradable Materials for IoT Sensors]({{ "/Exploring-Frontiers/Independently-Search/chemistry/iot-materials" | relative_url }})**
![IoT Materials]({{ "/assets/images/concepts/iot-sensors.jpg" | relative_url }})
Exploring **eco-friendly polymers** and composites for low-impact IoT devices.

### **[Industrial Waste Recycling]({{ "/Exploring-Frontiers/Independently-Search/chemistry/industrial-recycling" | relative_url }})**
![Industrial Recycling]({{ "/assets/diagrams/industrial-recycling.png" | relative_url }})
Chemical processes to **recycle industrial waste** into reusable materials.

---

## **All Chemistry Research**
{% for post in site.exploring_frontiers %}
{% if post.category == "chemistry" %}
<div class="chemistry-post-block">
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
