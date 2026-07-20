---
title: Earth-Life Data Catalogue 
layout: page
show_sidebar: false
permalink: /catalogue/
hero_image: "../images/heros/pexels-eddievaldes155-17570437.jpg"
---

<!-- Read in dependencies for the table -->
<script src="{{site.url}}{{site.baseurl}}/assets/js/jquery-3.7.0.js"></script>  <!--Add JQuery-->
<script src="{{site.url}}{{site.baseurl}}/assets/js/dataTables.responsive.min.js"></script>  <!--Add JQuery-->
<script src="{{site.url}}{{site.baseurl}}/assets/js/jquery.dataTables.min.js"></script>
<script src="{{site.url}}{{site.baseurl}}/assets/js/responsive.dataTables.min.css"></script>
<link rel="stylesheet" type="text/css" href="{{site.url}}{{site.baseurl}}/assets/css/jquery.dataTables.min.css" />

<div class="box">
  <h2 id="tutorials">Data Catalogue</h2>
  <p markdown="1">
  This page is a preliminary tabulation of data resources, including data portals, community databases and single datasets. Many of the entires were tabulated automatically. We are working on cleaning this compilations and on making this into a queriable relational database with extended metadata.
  Please use the [survey]({{site.url}}{{site.baseurl}}/contribute/) if you would like to let us know of any projects that we have not been aware of.
  </p>
  <p style="font-style:italic;color:darkgray">(Use landscape orientation on smartphones if you experience rendering issues.)
  </p>
  <hr>
  <!-- Filter out the relevant tutorials-->
<div id="table-wrapper-full">
  <table class="display" id="my-table">
	<thead>
		<tr><th>Logo</th><th>Resource</th><th>Description</th><th>Category</th></tr>
	</thead>
	<tbody>
		{% for res in site.data.resources %}
			<tr height=150> 
			{% if res.logo %}
			<td style="vertical-align: middle; " width=150> <img src="{{site.url}}{{site.baseurl}}/images/logos/{{res.logo}}"></td>
			{% else %}
			<td style="vertical-align: middle; " width=150> <img src="{{site.url}}{{site.baseurl}}/images/logos/generic.svg"></td>
			{% endif %}
			<td style="vertical-align: middle;"> <a href="{{res.link}}"><p><span style="font-weight:1000">{{res.short}}</span></p><p style="color:gray"><small><i>{{res.long}}</i></small></p></a></td>
			<td style="vertical-align: middle;"> {{res.description}}</td>
			<td> {{res.category}}</td>
			</tr>
		{% endfor %}
		
	</tbody>
	</table>
	</div>
</div>
<script>
new DataTable('#my-table', {
	"pageLength": 25,fixedColumns: {
        start: 1,
        end: 1
    }})
</script>



