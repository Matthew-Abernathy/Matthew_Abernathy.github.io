---
layout: home
title: Home
---

<div id="intro-wrapper" class="l-text">
	<div id="intro-title-wrapper">
		<div id="intro-image-wrapper">
			<img id="intro-image" src="/images/portrait.jpg"></div>
		<div id="intro-title-text-wrapper">
			<h1 id="intro-title">Hi, I'm Qianyu Zheng</h1>
			<div id="intro-subtitle">I'm a Bachelor Student at Georgia Tech.</div>
			<div id="intro-title-socials">
				{% for link in site.data.social-links %}
					{% if link.on-homepage == true %}
						{% include social-link.html link=link %}
					{% endif %}
				{% endfor %}
			</div>
		</div>
	</div>
	<!-- <hr class="l-middle home-hr"> -->
	<div id="everything-else" class="l-middle">
		<a href="{{ site.url }}/cv"><div><i class="fa fa-portrait icon icon-right-space"></i>CV</div></a>
		<a href="{{ site.url }}/projects"><div><i class="fa fa-shapes icon icon-right-space"></i>Projects</div></a>
		<a href="{{ site.url }}/everything-else"><div><i class="fa fa-list-ul icon icon-right-space"></i>Everything Else</div></a>
	</div>
	<div>
		Welcome to my personal website! I am an ambitious third-year Computer Science student with specialization in <b>theory</b> and <b>intelligence</b> at Georgia Institute of Technology. I maintain a perfect 4.0 GPA and own a strong foundation in programming languages like Python and Java, machine learning theory and cloud computing.
	</div>
	<div style="height: 1rem"></div>
	<div>
		As a researcher, I primarily work on applying computational methods, specifically <b>machine learning</b>, in scientific discoveries of natural science. My current research focuses on leveraging big data mining, machine learning, and high performance computing in <b>computational modeling</b> to answer scientific questions and empower data-driven decision making.
	</div>
	<div style="height: 1rem"></div>
	<div>
		I am currently working in the <a href="https://www.fung-group.org/"> Fung group</a> under the instruction of Assistant Professor <a href="https://scholar.google.com/citations?user=2QsddMIAAAAJ"> Victor Fung</a>, Georgia Tech School of Computational Science. My research is supported by the <i>President's Undergraduate Research Awards</i>, a scholarship granted to undergraduate research projects by Georgia Tech.
	</div>
	<div style="height: 1rem"></div>
	<div>
		My resume (in PDF format) can be viewed <a href="./CV.pdf"> here</a>.
	</div>
	<div style="height: 1rem"></div>
</div>

<hr class="l-middle home-hr">

<!-- <h2 class="feature-title">Featured <a href="/cv/#publications">Research Publications</a></h2> -->

<!-- <p class="feature-text">
	Latest research for fans of human-computer interaction, data visualization, and machine learning.
</p> -->

{% comment %}
<div class="cover-wrapper cover-wrapper-3-col l-page">
	{% assign sortedPublications = site.categories.papers | sort: 'feature-order' %}
	{% for feature in sortedPublications %}
		{% if feature.featured == true %}
			{% include feature.html feature=feature %}
		{% endif %}
	{% endfor %}
</div>

<br>
<h2 class="feature-title">Featured <a href="/dissertation">Dissertation Publications</a></h2>

<p class="feature-text">
	My dissertation contributed interactive interfaces to enable machine learning interpretability at scale and for everyone.
</p>

<div class="cover-wrapper cover-wrapper-1-col l-text">
	{% include dissertation/document.html details=false location=home %}
</div>

<div class="cover-wrapper cover-wrapper-3-col l-page">
	{% assign sortedPublications = site.categories.papers | sort: 'feature-order' %}
	{% for feature in sortedPublications %}
		{% if feature.dissertation == true %}
			{% include feature.html feature=feature %}
		{% endif %}
	{% endfor %}
</div>

<br>
<h2 class="feature-title">Apple <a href="https://developer.apple.com/design/human-interface-guidelines/">Chart Design Guidelines</a></h2>

<p class="feature-text">
	Guidance and best practices to help designers and developers create the best charts for Apple platforms.
</p>

<div class="cover-wrapper cover-wrapper-2-col l-middle">
	{% for feature in site.data.designs %}
		{% if feature.featured == true %}
			{% include feature.html feature=feature %}
		{% endif %}
	{% endfor %}
</div>

<br>
<h2 class="feature-title">Featured <a href="/cv/#interactive-articles">Interactive Articles</a></h2>

<p class="feature-text">
	Enhanced reading experiences that demonstrate what's possible when dynamic media are effectively combined.
 
</p>

<div class="cover-wrapper cover-wrapper-3-col l-page">
	{% assign sortedArticles = site.data.articles | where: "featured", true %}
	{% assign ia = site.categories.papers | where:"permalink", "papers/interactive-articles" %}

	{% assign feature = sortedArticles[1] %}
	{% include feature.html feature=feature %}

	{% assign feature = sortedArticles[0] %}
	{% include feature.html feature=feature %}

	{% assign feature = ia[0] %}
	{% include feature.html feature=feature %}
</div>

<br>
<h2 class="feature-title"><a href="https://parametric.press/about">Parametric Press</a></h2>

<p class="feature-text">
	A born-digital, experimental magazine dedicated to showcasing the expository power of the web.
</p>

<div class="cover-wrapper cover-wrapper-2-col l-middle">
	{% assign parametric = site.data.articles | where: "parametric-issue", true %}
	{% for feature in parametric %}
		{% include feature.html feature=feature %}
	{% endfor %}
</div>
{% endcomment %}



[gt]: http://www.gatech.edu "Georgia Tech"
[cse]: http://cse.gatech.edu "Georgia Tech Computational Science and Engineering"
[coc]: http://www.cc.gatech.edu "Georgia Tech College of Computing"

[cv]: {{ site.url }}/cv
[polo]: http://www.cc.gatech.edu/~dchau/ "Polo Chau"
[alex]: http://va.gatech.edu/endert/ "Alex Endert"
[poloclub]: http://poloclub.gatech.edu "Polo Club of Data Science"
[nstrf]: https://www.nasa.gov/strg/nstrf "NASA Space Technology Research Fellowship"