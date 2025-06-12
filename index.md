# Home Page
Hi, this seems to be my home page for now 🙂

{% include profile/README.md %}

{% assign repo_homepages = site.github.public_repositories | map: "homepage" | sort_natural %}
{% assign root_url = site.github.url | append: "/" %}
{% assign root_url_alt = site.github.repository_name | append: "/" | prepend: "https://" %}
{% assign repo_homepages = root_url | concat: repo_homepages %}

## Sitemap
{% for url in repo_homepages %}
	{%- if url contains root_url or url contains root_url_alt %}
	{%- assign rel_path = url | replace: root_url, "./" | replace: root_url_alt, "./" %}
- [{{ rel_path }}]({{ rel_path }})
	{%- endif -%}
{% endfor %}
- [./my-works/](./my-works/)

{% include footer.md %}
