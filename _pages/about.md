---
layout: about
title: about
permalink: /

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular

selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

announcements:
  enabled: false # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: false
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts

# Settings for the on-page projects section
projects_display_categories: [work, fun]
projects_horizontal: false
---

<style>
/* Inline contact icons under the photo */
.contact-icons-inline {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 0.6rem;
}
.contact-icons-inline a {
  font-size: 1.6rem;
  color: #1e3a8a;
}

/* Remove extra top spacing for publications inside cards */
.cv .publications {
  margin-top: 0;
}

/* Title weights and sizing */
.post-title {
  font-weight: 700 !important;
}
.post article h2 {
  font-weight: 400 !important;
}
/* Extra spacing before Research Interest heading */
.anchor#research-interest + h2 {
  margin-top: 20rem;
}
</style>

Hi! I am Yinuo Tu, a second-year ScM student in Biostatistics at the Johns Hopkins Bloomberg School of Public Health. 

My academic journey began in Chemical Engineering and Techonology at Zhejiang University (2020-2024), where I explored various research areas. I worked on several aging-related cohort studies under the guidance of [Prof. Zuyun Liu](https://person.zju.edu.cn/en/zuyunliu), which sparked my passions for biostatistics.

Currently, I am fortunate to work under the guidance of [Prof. Ciprian Crainiceanu](http://www.ciprianstats.org/), [Prof. Mei-Cheng Wang](https://publichealth.jhu.edu/faculty/733/mei-cheng-wang), and [Prof. Xinkai Zhou](https://fst.bnbu.edu.cn/en/faculty/faculty.htm#/xinkaizhou/en). My research focuses on two areas: \\
(1) developing survival models for dynamic disease progression;\\
(2) designing algorithms for cardiovascular waveform analysis using high-dimensional functional data collected from clinical monitors.

Outside of academia, I enjoy traveling and exploring new cuisines.

<a class="anchor" id="research-interest"></a>

## Research Interest

<div class="cv">
  <div class="card mt-3 p-3">
    My research interests center on the intersection of wearable devices, electronic health records (EHRs), and aging-related problems such as cognitive function, cardiovascular health. I am particularly passionate about developing and applying advanced statistical methods including, functional data analysis, longitudinal and survival analysis, and machine learning.
  </div>
</div>

<a class="anchor" id="education"></a>

## Education

{% assign education_section = site.data.cv | where: "title", "Education" | first %}
{% if education_section %}
  <div class="cv">
    <div class="card mt-3 p-3">
      <div>
        {% assign entry = education_section %}
        {% if entry.type == 'list' %}
          {% include cv/list.liquid %}
        {% elsif entry.type == 'map' %}
          {% include cv/map.liquid %}
        {% elsif entry.type == 'nested_list' %}
          {% include cv/nested_list.liquid %}
        {% elsif entry.type == 'time_table' %}
          {% include cv/time_table.liquid %}
        {% elsif entry.type == 'list_groups' %}
          {% include cv/list_groups.liquid %}
        {% else %}
          {{ entry.contents }}
        {% endif %}
      </div>
    </div>
  </div>
{% endif %}

<a class="anchor" id="publications"></a>

## Publications

<div class="cv">
  <div class="card mt-3 p-3">
    <div class="publications mb-0">
    {% bibliography %}
    </div>
  </div>
</div>

<a class="anchor" id="honors-awards"></a>

## Honors & Awards

<div class="cv">
  <div class="card mt-3 p-3">
    <ul class="items mb-0">
      <li><span class="item">Outstanding Graduates of Zhejiang Province</span></li>
      <li><span class="item">Outstanding Graduates of Zhejiang University</span></li>
      <li><span class="item">China National Scholarship (Top 1%)</span></li>
      <li><span class="item">Provincial Government Scholarship</span></li>
      <li><span class="item">First Prize Scholarship of Zhejiang University</span></li>
    </ul>
  </div>
</div>

<a class="anchor" id="teaching"></a>

## Teaching

<div class="cv">
  <div class="card mt-3 p-3">
    <div class="d-flex justify-content-between align-items-start">
      <div>
        <h6 class="title font-weight-bold mb-1">Graduate Teaching Assistant – Biostatistics in Public Health</h6>
        <div class="institution text-muted">Johns Hopkins University Bloomberg School of Public Health</div>
      </div>
      <div class="text-muted small ml-3 text-right">Aug. 2025 -- Present</div>
    </div>
    <ul class="items mt-2 mb-0">
      <li>
        Led weekly discussion sections (2 sections, 30 students each) to review core concepts, discuss problem sets, and support student learning; assisted with grading and provided feedback on assignments and exams; collaborated with instructors in weekly meetings to refine teaching strategies.
      </li>
    </ul>
  </div>
</div>
