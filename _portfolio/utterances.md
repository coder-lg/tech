---
layout: post
title: Utterances
feature-img: "assets/img/portfolio/utterances pic.PNG"
img: "assets/img/portfolio/utterances pic.PNG"
date: June 13, 2021
tags: [projects]
---
This here is Utterances. There is a blog for it too, but here is the code you need.
At `config.yml`:
```yaml
utterances:
	repo:
	issue-term:
	theme:
	label: #if you add it.
```
At `_includes\social\utterances.html`:
```html
<script src="https://utteranc.es/client.js"
        repo='<!--{{ site.comments.utterances.repo }}-->'
        issue-term="<!--{{ site.comments.utterances.issue-term}}-->"
        theme="<!--{% if site.comments.utterances.theme %}{{ site.comments.utterances.theme }}{% elsif site.color_theme == 'dark' %}github-dark{% else %}github-light{% endif %}-->"
		label="<!--{{ site.comments.utterances.label }}-->"
        crossorigin="anonymous"
        async>
</script>
replace repo with your chosen repo in the config and label can be changed. It is advised to change it.

don't forget to remove those comment lines, ie: `<!---->`
```
At `_layouts\post.html`:
```html
<!--Utterances-->
{% if site.comments.utterances.repo and site.comments.utterances.issue-term and site.comments.utterances.theme %} {% include social/utterances.html %} {% endif %}
```
And that's literally it.

The entire code needed to use Utterances.
