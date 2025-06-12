# Home Page
Hi, this seems to be my home page for now 🙂

## Test variables
- `github.url`: {{ site.github.url }}
- `github.hostname`: {{ site.github.host_name }}
- `github.pages_hostname`: {{ site.github.pages_hostname }}

I'm a long-time player of [Guardian Tales](https://guardian-tales.fandom.com/wiki/) so most of my current works are based around it, but I intend to soon add stuff outside that topic too

Current github pages sitemap:

{% assign repo_homepages = site.github.public_repositories | map: "homepage" | sort_natural %}
{% assign root_url = site.github.url | append: "/" %}

{% for url in repo_homepages %}
	{% if url contains root_url %}
	{% assign rel_path = url | replace: root_url, "./" %}
* [{{ rel_path }}]({{ rel_path }})
	{% endif %}
{% endfor %}

## My Works / Designs
### Hero Cards

<div class="d-flex flex-justify-center">
	<div class="cp_embed_wrapper" style="width: 100%; height: 600px;">
		<iframe scrolling="no" title="Hero Card v2" src="https://codepen.io/Suggon/embed/zxYwepJ?default-tab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
			See the Pen <a href="https://codepen.io/Suggon/pen/zxYwepJ">
			Hero Card v2</a> by Suggon (<a href="https://codepen.io/Suggon">@Suggon</a>)
			on <a href="https://codepen.io">CodePen</a>.
		</iframe>
	</div>
</div>

---

### Tab Navigation

<iframe height="320" style="width: 100%;" scrolling="no" title="Tab Navigation" src="https://codepen.io/Suggon/embed/MWzqByj?default-tab=result&theme-id=dark" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
	See the Pen <a href="https://codepen.io/Suggon/pen/MWzqByj">
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

<div markdown="1" class="footer border-top border-gray-light mt-5 pt-3 text-right text-gray">
Site source: [{{ site.github.repository_name }}]({{ site.github.repository_url }})\\
Last updated: {{ "now" | date: "%b %e, %Y" }}
</div>
