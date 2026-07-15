---
title: Data resources 
layout: page
show_sidebar: false
permalink: /hub/dataresources/
---

<!-- Read in dependencies for the table -->
<script src="{{site.url}}{{site.baseurl}}/assets/js/jquery-3.7.0.js"></script>  <!--Add JQuery-->
<script src="{{site.url}}{{site.baseurl}}/assets/js/jquery.dataTables.min.js"></script>
<link rel="stylesheet" type="text/css" href="{{site.url}}{{site.baseurl}}/assets/css/jquery.dataTables.min.css" />

<div class="box">
  <h2 id="tutorials">Data Resources</h2>
  <p>
  This page tabulates resources that focus on one or a very few, specifically defined data entities. 
  </p>
  <hr>
  <!-- Filter out the relevant tutorials-->

  <table class="display" id="my-table">
	<thead>
		<tr><th>Logo</th><th>Resource</th><th>Description</th><th>Category</th></tr>
	</thead>
	<tbody>
		{% for res in site.data.resources %}
			<tr height=150> 
			<td style="vertical-align: middle; " width=150> <img src="{{site.url}}{{site.baseurl}}/{{res.logo}}"></td>
			<td style="vertical-align: middle;"> <a href="{{res.website}}"><p><span style="font-weight:1000; font-size:1.5rem">{{res.short}}</span></p><p style="color:gray"><small><i>{{res.long}}</i></small></p></a></td>
			<td style="vertical-align: middle;"> {{res.description_short}}</td>
			<td> {{res.category}}</td>
			</tr>
		{% endfor %}
		
	</tbody>
	</table>
</div>
<script>
new DataTable('#my-table', {
	"pageLength": 25,fixedColumns: {
        start: 1,
        end: 1
    }})
</script>
