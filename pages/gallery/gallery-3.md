---
layout: gallery
title: gallery
nav:
permalink: /gallery-3/
---

<div class="galleries page">
	
	{% for gallery in site.data.galleries %}
	  	
	  	{% if gallery.id <=3 %}
	  	
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
			<a href="{{ site.baseurl }}/gallery-2" class="button-pagination button">back</a>
		</div>
		
		<div class="right">
			<span class="button button-disabled button-pagination">next</span>  
		</div>

</div>
