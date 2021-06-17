---
title: Posts

# View.
#   1 = List
#   2 = Compact
#   3 = Card
view: 2

# Optional header image (relative to `static/media/` folder).
header:
  caption: ""
  image: ""
---

<ul>
    {{ range .Pages.ByDate.Reverse }}
        <li>
            <h1><a href="{{ .Permalink }}">{{ .Title }}</a></h1>
            <time>{{ .Date.Format "Mon, Jan 2, 2006" }}</time>
        </li>
    {{ end }}
</ul>