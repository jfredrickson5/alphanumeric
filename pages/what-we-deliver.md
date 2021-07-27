---
title: Emerging Technologies
permalink: /what-we-deliver/
layout: primary
lead: Summaries, strategies, and statuses of the latest in tech for Federal innovators.
content_wide: true
content_focus: false
redirect_from:
  - /consulting/
  - /what-we-deliver/military-onesource/
  - /what-we-deliver/every-kid-in-a-park/
  - /what-we-deliver/micro-purchase-marketplace/
  - /what-we-deliver/ready-2-serve/
  - /what-we-deliver/new-ten/
banner_cta: true
gridless: true
---
<div class="grid-container usa-section break-bottom-gray">
  <section class="grid-row">
    <div class="tablet:grid-col-8">
      <p>
        TechRadar partners with GSA offices and Federal agencies to accelerate emerging tech assessment, alignment, and action by connecting Federal innovators with new content and collaborators to create new value.
      </p>
    </div>
  </section>
</div>

<div class="grid-container">
  <section class="usa-section break-bottom-gray">
    <div class="usa-section-bottom">
      
      <h2>Emerging Technologies</h2>
      <div class="grid-row grid-gap">
        {% assign featured_services = site.data.featured_services %}
        {% assign projects_list = site | find_collection: 'services_projects' | weighted_sort: 'project_weight', 'title' %}
        {% for featured in featured_services %}
          {% assign project = projects_list | where: "agency", featured.agency | first %}
          {% include card.html
          image_src=project.image
          image_alt=project.image_accessibility
          image_icon=project.image_icon
          agency=project.agency
          tagline=project.title
          description=project.excerpt
          link=project.permalink
          %}
        {% endfor %}
      </div>
    </div>
    {%- comment -%} <p>
      <a class="link-arrow-right post-link-continue_reading" href="{{ '/how-we-work/' | prepend: site.baseurl }}">
        See all case studies
        {% include svg/icons/arrow-right.svg %}
      </a>
    </p> {%- endcomment -%}
  </section>
</div>

<section class="grid-container usa-section break-bottom-gray">
  <section class="pad-right-left">
    <div class="home-testimonial">
      TechRadar offered my team and me a new space to not only find potential answers to whether a compeling use case existed for the emerging technology we were exploring, but also provided an invaluable sounding board of many Federal colleagues who helped us consider new questions we didn't even think to ask that moved the ball forward faster and smarter for our project.
      <span>
        - Chang Charley, Former Deputy Assistant Secretary, Office of Budget & Policy      </span>
    </div>
  </section>

<!-- <div class="usa-section background-gray">
  <section class="grid-container">
    {% assign agency_partners = site.data.agencies %}
    {% assign partner_groups = agency_partners | in_groups: 3 %}
    <h2 id="some-agencies-weve-worked-with">Some agencies we’ve worked with</h2>
    <div>
      <ul class="list-columns grid-row grid-gap">
      {% for group in partner_groups %}
        <li class="tablet:grid-col-4">
          <ul class="list-columns list-images">
          {% for partner in group %}
            <li class="list-images-item">
              <img class="list-images-image" src="{{ partner.logo | prepend: site.baseurl }}" alt="{{ partner.logo }} logo" />
              {% if partner.agency_url %}
                <a class="list-images-text" href="{{ partner.agency_url | prepend: site.baseurl }}">{{ partner.name }}</a>
              {% else %}
                <span class="list-images-text">{{ partner.name }}</span>
              {% endif %}
            </li>
          {% endfor %}
          </ul>
        </li>
      {% endfor %}
      </ul>
    </div> -->
