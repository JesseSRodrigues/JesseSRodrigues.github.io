---
layout: page
title: Blog PET-Inf 2.3
---
<section class="bg-light page-section" id="{{ site.data.sitetext.blog.section | default: "blog" }}">
  <div class="container">
    <div class="row">
      <div class="col-lg-12 text-center">
        <h2 class="section-heading text-uppercase">{{ site.data.sitetext.blog.title | markdownify | default: "Blog do PET-Informática" }}</h2>
      </div>
    </div>
    <div class="row">
      {% for post in site.posts %}
        <div class="col-md-4 col-sm-6 portfolio-item">
          <a class="portfolio-link" href="/blog{{ post.url }}">
            <div class="portfolio-hover">
              <div class="portfolio-hover-content">
                <i class="{{ site.data.style.portfolio-icon | default: "fas fa-plus fa-3x" }}"></i>
              </div>
            </div>
            <img class="img-fluid" src="{{ post.caption.thumbnail }}" alt="">
          </a>
          <div class="blog-caption">
            <p class="post-data">{{ post.caption.data }}</p>
            <h4>{{ post.caption.title }}</h4>
            <p class="blog-subtitle">{{ post.caption.subtitle }}</p>
          </div>
        </div>
      {% endfor %}
    </div>
  </div>
</section>
