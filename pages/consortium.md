---
layout: page
title: The Alliance
subtitle: The structure and responsibilities of the alliance
permalink: /about/consortium/
show_sidebar: false
hero_image: "../../images/heros/pexels-photo-13010774.jpeg"
---

# What is the DELS? 

The studies, that are  
- An umbrella for research groups. 


# Why is this model necessary

Scientific community that focuses on Earth-Life coevolution is incredibly fragmented, and for multiple reasons.

The goal of DELS is to transcend the well-established publish-cite-recognize reward system the permeates the academic community, which is one othe main reasons for the fragemntation of the community, initiatives and resources. 

In the face of fragmentation, and scarcity of resources we decided unite as a single body to  



The community's need for a globally integrated data system an only be fulfilled if the 

# Joint achievements

# Structure 


## Coordination

{% assign i = 0 %}
{% assign basic = site.data.people | where: 'special', 'pi' %}
{% assign basic = basic | sort: 'last' %}
{% for person in basic %}
{% assign i = i | plus:1 %}
{% assign something = i | modulo:2 %}
{% if something == 1 %}
<div class="columns is-vcentered">
{% endif %}

<div class="column">
	<div class="box">
	<div class="columns">
		<div class="column is-3">
		<a href="{{person.webpage}}"><img src="{{site.url}}{{site.baseurl}}/images/people/{{person.image}}" style="border-radius:3%;border:1px solid #ddd"></a>
		</div>
		<div class="column">
		<h4 id="{{ person.first | append: " " | append: person.last | slugify }}"><a href="{{person.webpage}}">{{person.first}} {{person.last}}</a></h4>
		{{person.institute}}
		</div>
	</div>
	</div>
</div>

{% if something == 0 %}
</div>
{% endif %}
{% endfor %}

{% if something == 1 %}
<div class="column">
</div>
</div>
{% endif %}

## The future organization

As senior academics are universally overcommited and early-career researchers are overburdened with publication pressure to maintain their academic affiliation, the consortium is coordinated by late-early to mid-career researchers.

- future proofing

## The future organization

It is our intention to rally the community, and over the next decade, establish a formal, intergovernmental organization
