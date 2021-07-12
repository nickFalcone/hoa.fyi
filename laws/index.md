---
layout: layouts/post.njk
title: Laws
templateClass: tmpl-post
eleventyNavigation:
  key: Laws
  order: 3
---

Latest information about Homeowners' Associations

<form id="stateSelect" action="/" target="_top">
<label for="state">State</label>
  <select on="change:AMP.navigateTo(url=event.value)">
  <option selected disabled>Select a state</option>  
  {%- for law in collections.law -%}
    <option value="{{ law.data.state | slug }}">{{ law.data.state }}</option>
  {%- endfor -%}
  </select>
</form>
