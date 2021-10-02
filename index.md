---
layout: page
title: "Home"
class: home
---

# Hi, I'm Aakash!

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I'm a budding researcher in Deep-Learning with focus on medical imaging and self-supervised learning. I am currently investigating Self-Supervised methods from the lens of Vector Quantization with [Dr. Prashnna K. Gyawali](http://www.pkgyawali.com/). Previously I worked with [Prof. Linwei Wang](https://pht180.rit.edu/cblwang/linwei-wang/) and [Dr. Prashnna K. Gyawali](http://www.pkgyawali.com/) on Disease-aware image editing on Chest X-rays. Before that I worked as a Machine Learning Engineer at [CARING Research, India](https://caring-research.com/), primarily working on Image-to-Image translation and Image Editing problems with [Prof. Hacer Yalim Keles](https://scholar.google.com/citations?user=noo7zCUAAAAJ&hl=en) and [Dr. Kai Dierkes](http://kaidierkes.net/).

I graduated from Delhi College of Engineering, India in 2019 with a bachelor’s degree in Industrial engineering and was fortunate to be advised by Prof. Shamsher. In the summer of 2018, I worked as a Machine Learning intern at [Complex System Lab](https://cosylab.iiitd.edu.in/) under [Dr. Ganesh Bagler](https://scholar.google.co.in/citations?hl=en&user=qyth_0QAAAAJ&view_op=list_works&sortby=pubdate). In the same year, I also interned in the Computer Vision Team at UNSW, Australia under [Prof. Arcot Sawmya](https://www.cse.unsw.edu.au/~sowmya/)

My research interests include Image Editing using GANs, Image-to-Image translation, Unsupervised methods in image clustering and segmentation.
</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/aakash_440.webp' type='image/webp' />
  <img
    src='/images/aakash_440.jpg'
    alt='Aakash Saboo'>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
</div>

</div>


## Featured Projects

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>
<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show More Projects
</a>

## Featured Publications

<div class="featured-publications">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    {% if pub.highlight %}
      <a href="{{ pub.pdf }}" class="publication">
        <strong>{{ pub.title }}</strong>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>.
        <i>{% if pub.venue %}{{ pub.venue }}, {% endif %}{{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
    {% endif %}
  {% endfor %}
</div>

<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a>

<div class="news-travel" markdown="1">

<div class="news" markdown="1">
## Latest News

<ul>
{% for news in site.data.news limit:10 %}
  {% include news.html news=news %}
{% endfor %}
</ul>

</div>

<div class="travel" markdown="1">
## Latest Travel

<table>
<tbody>
{% assign future_travel = site.data.travel | where_exp:'item','item.start == null' %}
{% for travel in future_travel %}
  {% include travel.html travel=travel %}
{% endfor %}
{% assign sorted_travel = site.data.travel | where_exp:'item','item.start' | sort: 'start' | reverse %}
{% for travel in sorted_travel limit:10 %}
  {% include travel.html travel=travel %}
{% endfor %}
</tbody>
</table>

</div>

</div>
