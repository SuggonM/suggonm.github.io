# Home Page
Hi, this seems to be my home page for now 🙂

I'm a long-time player of [Guardian Tales](https://guardian-tales.fandom.com/wiki/User:Suggon){:target="_blank"} so most of my current works are based around it, but I intend to soon add stuff outside that topic too

Current github pages sitemap:

{% assign repo_homepages = site.github.public_repositories | map: "homepage" | sort_natural %}
{% assign root_url = site.github.url | append: "/" %}
{% assign root_url_alt = site.github.repository_name | append: "/" | prepend: "https://" %}
{% assign repo_homepages = root_url | concat: repo_homepages %}

{% for url in repo_homepages %}
	{%- if url contains root_url or url contains root_url_alt %}
	{%- assign rel_path = url | replace: root_url, "./" | replace: root_url_alt, "./" %}
* [{{ rel_path }}]({{ rel_path }})
	{%- endif -%}
{% endfor %}

## My Works / Designs
### Hero Cards

<div class="d-flex flex-justify-center">
	<div class="cp_embed_wrapper" style="width: 100%; height: 600px;">
		<iframe scrolling="no" title="Hero Card" src="https://codepen.io/Suggon/embed/zxYwepJ?default-tab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
			See the Pen <a href="https://codepen.io/Suggon/pen/zxYwepJ">
			Hero Card</a> by Suggon (<a href="https://codepen.io/Suggon">@Suggon</a>)
			on <a href="https://codepen.io">CodePen</a>.
		</iframe>
	</div>
</div>

---

### Tab Navigation

<iframe height="320" style="width: 100%;" scrolling="no" title="Tab Navigation" src="https://codepen.io/Suggon/embed/wBvErvL?default-tab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
	See the Pen <a href="https://codepen.io/Suggon/pen/wBvErvL">
	Tab Navigation</a> by Suggon (<a href="https://codepen.io/Suggon">@Suggon</a>)
	on <a href="https://codepen.io">CodePen</a>.
</iframe>

---

### Map Binary Analyzer

<iframe height="400" style="width: 100%;" scrolling="no" title="gt-map-tile-reader" src="https://codepen.io/Suggon/embed/BabeqaE?default-tab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
	See the Pen <a href="https://codepen.io/Suggon/pen/BabeqaE">
	gt-map-tile-reader</a> by Suggon (<a href="https://codepen.io/Suggon">@Suggon</a>)
	on <a href="https://codepen.io">CodePen</a>.
</iframe>

---

### Comic Scanlation (in progress)

<div class="d-flex flex-column flex-items-center">
	<iframe style="border: 1px solid rgba(0, 0, 0, 0.1);" width="800" height="450" src="https://embed.figma.com/design/wF2sgjwiGyxcBAi9VSRnt4/gt-comics?embed-host=share" allowfullscreen></iframe>
	<iframe style="border: 1px solid rgba(0, 0, 0, 0.1);" width="800" height="450" src="https://embed.figma.com/proto/wF2sgjwiGyxcBAi9VSRnt4/gt-comics?embed-host=share&footer=false" allowfullscreen></iframe>
</div>

{% include footer.md %}
