---
layout: page
title: Home
tagline: 
description: "Xenuts Homepage"
group: "navigation"
---
{% include JB/setup %}

![QRCode](qrcode.png)<br />
This is a readable QR code (though, you might need to enlarge it). Thanks to [Niloy J. Mitra](http://www0.cs.ucl.ac.uk/staff/n.mitra/), [Hung-Kuo Chu](http://vision.csie.ncku.edu.tw/~hkchu/) and other authors of [Halftone QR Codes](http://vecg.cs.ucl.ac.uk/Projects/SmartGeometry/) paper! Aug 2, 2013

## Recently Post
<ul class="posts">
  {% for post in site.posts %}
    <li><span>{{ post.date | date_to_string }}</span> &raquo; <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a></li>
  {% endfor %}
</ul>
  

