---
title: Physics
layout: section_with_posts
---

# *Theoretical and applied physics, from energy systems to quantum mechanics.*

This subsection dives into **physic experiments** that power my projects. It is here that I apply the skills I learn regularly in physics.
---

## **Featured Research**
### **[Energy Efficiency in Local AI Devices]({{ "/Exploring-Frontiers/Independently-Search/physics/local-ai-energy" | relative_url }})**
![Local AI Energy]({{ "/assets/images/concepts/local-ai-energy.jpg" | relative_url }})
How to minimize energy consumption in **edge AI hardware** while maintaining performance—directly applied in [WhirlWing]({{ "/Applied-Works/whirlwing/technical" | relative_url }}).

### **[Thermodynamics of IoT Sensors]({{ "/Exploring-Frontiers/Independently-Search/physics/iot-thermodynamics" | relative_url }})**
![IoT Thermodynamics]({{ "/assets/diagrams/iot-thermodynamics.png" | relative_url }})
Using thermodynamic principles to design **low-power, high-efficiency IoT sensors** for industrial use.

---

## **All Physics Research**
{% for post in site.exploring_frontiers %}
{% if post.category == "physics" %}
<div class="physics-post-block">
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
