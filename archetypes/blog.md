+++
title = "{{ replace .Name "-" " " | title }}"
date = "{{ .Date }}"
url = "/{{ dateFormat "2006" .Date }}/{{ dateFormat "01" .Date }}/{{ dateFormat "02" .Date }}/{{ replace .Name " " "-" }}/"

#
# description is optional
#
# description = "An optional description for SEO. If not provided, an automatically created summary will be used."
+++

This is a page about »{{ replace .Name "-" " " | title }}«.
