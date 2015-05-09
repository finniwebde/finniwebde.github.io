---
layout: gallery
title: gallerie
nav: top, bottom
site-id: 3
permalink: /gallery/
---

<div class="galleries page">
	
	{% for gallery in site.data.galleries %}
	  	
	  	{% if gallery.id <= 9 and gallery.id > 6 %}
	  	
	  	<div class="album">
		    <header class="header-page">
		    <h2 class="title">{{ gallery.title }}</h2>
		    </header>
			  
			  <div class="thumb"> 
			    {% for image in gallery.images %}
			     <div class="img-container">
					    <a href="{{ gallery.path }}{{ image.name }}" data-lightbox="{{ gallery.id }}" title="{{ image.text }}">
					      <div class="img-sizer"><img src="{{ gallery.path }}{{ image.thumb }}"></div>
					    </a>
				    </div> 
			    {% endfor %}
			   </div> 
		   </div>
		  {% endif %}
	{% endfor %}
	
</div>

<div class="pagination">
	

		<div class="left">
			<span class="button button-disabled button-pagination">back</span>
		</div>


		<div class="right">
			<a href="{{ site.baseurl }}/gallery-2" class="button-pagination button">next</a>
		</div>


</div>
