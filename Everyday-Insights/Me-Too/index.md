---
title: Me-Too
layout: section_with_posts
---

# *My unfiltered opinions on tech news, trends, and the ethical dilemmas no one’s talking about.*


This is where I **critique, celebrate, and question** the tech world—from **AI ethics** to **cloud lock-in**, **surveillance capitalism** to **sustainable hardware**. Expect **hot takes, deep dives, and contrarian views** rooted in my work on [WhirlWing]({{ "/Applied-Works/whirlwing/intro" | relative_url }}) and [Firmware AI]({{ "/Foundations/firmware-ai" | relative_url }}).

---


## **Featured Opinions**


### **[The Future of AI: Why Local-First is the Only Ethical Path]({{ "/Everyday-Insights/Me-Too/future-ai-local" | relative_url }})**
![Local-First AI]({{ "/assets/images/concepts/local-first-ai.jpg" | relative_url }})
Cloud-based AI is **unsustainable and unethical**. Here’s why **local-first AI**—like Tesla’s FSD and my [WhirlWing]({{ "/Applied-Works/whirlwing/technical" | relative_url }})—is the future.

### **[Cloud Lock-In: The Silent Crisis No One’s Talking About]({{ "/Everyday-Insights/Me-Too/cloud-lock-in" | relative_url }})**
![Cloud Lock-In]({{ "/assets/diagrams/cloud-lock-in.png" | relative_url }})
How **Microsoft, Google, and Amazon** use cloud dependency to **control users**—and what we can do about it.

### **[Why Raspberry Pi is the Anti-Silicon Valley We Need]({{ "/Everyday-Insights/Me-Too/raspberry-pi-revolution" | relative_url }})**
![Raspberry Pi]({{ "/assets/images/concepts/raspberry-pi-revolution.jpg" | relative_url }})
The **$35 computer** is **democratizing tech** in ways Silicon Valley never will. Here’s how I use it in [WhirlWing]({{ "/Applied-Works/whirlwing/technical" | relative_url }}).

---
## **All Opinions**
{% for post in site.everyday_insights %}
{% if post.category == "me-too" %}
<div class="me-too-post-block">
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
    {% if post.tags %}
    <span class="tags">
      🏷️ Tags: {{ post.tags | join: ", " }}
    </span>
    {% endif %}
    {% if post.related_project %}
    <span class="related-link">
      🔗 Related: <a href="{{ post.related_project | relative_url }}">{{ post.related_project_title }}</a>
    </span>
    {% endif %}
  </div>
  <a href="{{ post.url | relative_url }}" class="read-more">Read More →</a>
</div>
{% endif %}
{% endfor %}
