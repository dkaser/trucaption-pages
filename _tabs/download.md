---
# the default layout is 'page'
icon: fas fa-download
order: 2
---

## Trucaption {{ site.github.latest_release.name }}

### Changes in this release:
{{ site.github.latest_release.body }}

### Download links:
{% for asset in site.github.latest_release.assets %}
{% assign extension = asset.name | slice: -3, 3 | downcase %}
{% if extension == "exe" or extension == "dmg" %}
  * [{{ asset.name}}]({{ asset.browser_download_url }})
{% endif %}
{% endfor %}

For older releases, visit [Releases](https://github.com/trucaption/trucaption/releases).
