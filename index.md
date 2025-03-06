# Home Page
Hi, this seems to be my home page for now 🙂

I'm a long-time player of [Guardian Tales](https://guardian-tales.fandom.com/wiki/) so most of my current works are based around it, but I intend to soon add stuff outside that topic too

Current github pages sitemap:

{% assign root_url = site.github.url | append: "/" %}
{% for repo in site.github.public_repositories %}
	{% if repo.homepage contains root_url %}
	{% assign rel_path = repo.homepage | replace: root_url %}
* [./{{ rel_path }}](./{{ rel_path }})
	{% endif %}
{% endfor %}

<div class="footer border-top border-gray-light mt-5 pt-3 text-right text-gray">

Site source: [{{ site.github.repository_name }}]({{ site.github.repository_url }})\
Last updated: {{ "now" | date: "%b %e, %Y" }}

</div>
