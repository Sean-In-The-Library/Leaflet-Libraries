---
layout: post
title: Leaflet Libraries of Phoenix
subtitle: A code through of how to make a Phoenix Library map in R
tags: [libary, libraries, leaflet, phoenix, arizona]
comments: true
---

<div id="toc_container">
<p class="toc_title"><strong>Table of Contents</strong></p>
<ul class="toc_list">
<li><a href="#question_1">Introduction</a></li>
<li><a href="#question_2">Concept</a></li>
<li><a href="#question_3">Data</a></li>
<li><a href="#question_6">The Maps</a></li>
</ul>
</div>
<p>&nbsp;</p>
<h1 id="question_1">Introduction</h1>
<p>This code-through will show how to take open data addresses and turn them into an interactive map using the <strong><a href="https://cran.r-project.org/web/packages/leaflet/index.html">Leaflet</a></strong>&nbsp;package. I will take addresses from the Phoenix Public Library system and plot these on a map, with markers that provide additional useful information about the libraries. The goal is to have a single page where people can go to find which library would be most useful to their needs. This map could also be embedded on the public library website to inform patrons.</p>
<h2 id="question_2">Concept</h2>
<p>This project built on the information in a <strong><a href="https://towardsdatascience.com/making-interactive-maps-in-r-with-less-than-15-lines-of-code-bfd81f587e12">Towards Data Science</a></strong>&nbsp;Medium post by Brandon Walker.</p>
<h2 id="question_3">Data</h2>
<p>These maps were built using data from the <strong><a href="https://www.phoenixopendata.com/dataset/libraries/resource/b7158429-b69e-4f87-8a96-b4857c6d65b5">Phoenix, AZ Open Data Portal</a></strong>. The data was not linked through the API (since it was broken at the time of creation) so the data is static as of 10/1/2020.</p>
<h1 id="question_6">The Maps (and R Code-Through)</h1>

<p><a href="https://rpubs.com/sharri65/PHXLib"><img src="https://i.imgur.com/FY8HgsO.jpg" width="750" height="537" /></a></p>

*(Click me)*
