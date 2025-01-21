
---
date: '{{ .Date }}'
draft: false
type: alert
title: '{{ replace .File.ContentBaseName `-` ` ` | title }}'
---


Alert content goes here.