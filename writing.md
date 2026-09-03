---
layout: page
title: Public writing
permalink: /writing/
---

Use the filters to explore by style, region, or search for specific topics.

<!-- Filter Controls -->
<div class="portfolio-filters">
  <div class="filter-group">
    <label>Style:</label>
    <div class="filter-buttons" data-filter-type="style">
      <button class="filter-btn active" data-filter="all">All</button>
      <button class="filter-btn" data-filter="quantitative">Quantitative</button>
      <button class="filter-btn" data-filter="policy">Policy</button>
      <button class="filter-btn" data-filter="commentary">Commentary</button>
    </div>
  </div>

  <div class="filter-group">
    <label>Region:</label>
    <div class="filter-buttons" data-filter-type="region">
      <button class="filter-btn active" data-filter="all">All</button>
      <button class="filter-btn" data-filter="twin-cities">Twin Cities</button>
      <button class="filter-btn" data-filter="chicago">Chicago</button>
      <button class="filter-btn" data-filter="comparative">Comparative</button>
    </div>
  </div>

  <div class="search-box">
    <input type="text" id="portfolio-search" placeholder="Search articles...">
  </div>
</div>

<!-- Portfolio Grid -->
<div class="portfolio-grid">
  {% assign writing_sorted = site.data.writing | sort: "date" | reverse %}
  {% for item in writing_sorted %}
  {% include portfolio-item.html item=item %}
  {% endfor %}
</div>

<p class="no-results" style="display: none;">No articles match your filters.</p>
