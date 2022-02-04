---
layout: page
title: "Home"
class: home
---

# Hi, I'm Aakash!

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I'm a budding researcher in Deep-Learning with focus on medical imaging and self-supervised learning. I am currently investigating Self-Supervised methods from the lens of Vector Quantization with [Dr. Prashnna K. Gyawali](http://www.pkgyawali.com/). Previously I worked with [Prof. Linwei Wang](https://pht180.rit.edu/cblwang/linwei-wang/) and [Dr. Prashnna K. Gyawali](http://www.pkgyawali.com/) on Disease-aware image editing on Chest X-rays. Before that I worked as a Machine Learning Engineer at [CARING Research, India](https://caring-research.com/), primarily working on Image-to-Image translation and Image Editing problems with [Prof. Hacer Yalim Keles](https://scholar.google.com/citations?user=noo7zCUAAAAJ&hl=en) and [Dr. Kai Dierkes](http://kaidierkes.net/).

I graduated from Delhi College of Engineering, India in 2019 with a bachelor’s degree in Industrial engineering and was fortunate to be advised by Prof. Samsher. In the summer of 2018, I worked as a Machine Learning intern at [Complex System Lab](https://cosylab.iiitd.edu.in/) under [Dr. Ganesh Bagler](https://scholar.google.co.in/citations?hl=en&user=qyth_0QAAAAJ&view_op=list_works&sortby=pubdate). In the same year, I also interned in the Computer Vision Team at UNSW, Australia under [Prof. Arcot Sawmya](https://www.cse.unsw.edu.au/~sowmya/)

My research interests include Image Editing using GANs, Image-to-Image translation, Unsupervised methods in image clustering, segmentation and disentangled representation learning. If you have similar interest, don't be hesitant to connect with me. 
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


<table width="100%" align="center" border="0" cellspacing="0" cellpadding="20">
  <tr>
    <td width="100%" valign="middle">
     <table style="width:100%;border:0px;border-spacing:0px;border-collapse:separate;margin-right:auto;margin-left:auto;"><tbody>
    <tr>

      <p align="right">
        <font size="2">
          <a href="https://github.com/jonbarron/jonbarron_website">source code</a> </p>
<script type="text/javascript" id="clustrmaps" src="//clustrmaps.com/map_v2.js?d=FjqctmDvHyc-xjFkkaWKoFCLrG4-wwKerC2J7vK-UH8&cl=ffffff&w=a"></script>

