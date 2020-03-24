---
title: jupyter notebook と HUGO を連携する手順
author: ~
date: '2020-03-24'
slug: test
categories: [資産運用]
tags: []
Description: ''
menu: ''
---

# jupyter notebook と HUGO を連携する手順

notebookに先ず下記を記載

```
---
title: test
author: ~
date: '9999-12-31'
slug: test
categories: [資産運用]
tags: []
Description: ''
menu: ''
---
```

## 案１
notebookをipynbとしてローカルに保存
anacondaからterminalを起動する
nbconvertでmdに変換する
```
jupyter nbconvert --to markdown Untitled.ipynb
```
.mbをHUGO用ディレクトリへコピー＆build_site()

## 案２
notebookをmbとしてローカルに保存
.mbをHUGO用ディレクトリへコピー＆build_site()

どちらも面倒だな。。。
