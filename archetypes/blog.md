+++
title = "{{ replace .Name "-" " " | title }}"
date = "{{ .Date }}"
url = "/{{ .Date.Year }}/{{ .Date.Format "01" }}/{{ .Date.Format "02" }}/{{ replace .Name " " "-" }}/"

#
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."

tags = [{{ range $plural, $terms := .Site.Taxonomies }}{{ range $term, $val := $terms }}"{{ printf "%s" $term }}",{{ end }}{{ end }}]
+++

This is a page about »{{ replace .Name "-" " " | title }}«.
