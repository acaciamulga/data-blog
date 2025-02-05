---
title: Understanding basis of record - a living specimen becomes a preserved specimen 
author: John Waller
date: '2019-10-07'
slug: living-specimen-to-preserved-specimen-understanding-basis-of-record
categories:
  - GBIF
tags:
  - data quality
lastmod: '2019-09-06T10:40:05+02:00'
draft: no
keywords: []
description: ''
authors: ''
comment: no
toc: ''
autoCollapseToc: no
postMetaInFooter: no
hiddenFromHomePage: no
contentCopyright: no
reward: no
mathjax: no
mathjaxEnableSingleDollar: no
mathjaxEnableAutoNumber: no
hideHeaderAndFooter: no
flowchartDiagrams:
  enable: no
  options: ''
sequenceDiagrams:
  enable: no
  options: ''
---

 
Recently a user noticed that there were **Asian Red Pandas** (Ailuridae) occurring in [North America](https://www.gbif.org/occurrence/map?basis_of_record=PRESERVED_SPECIMEN&country=US&taxon_key=9673), and wondered if someone had made a mistake. When an occurrence observation comes from a **zoo** or **botanical garden**, it is usually considered a [living specimen](https://dwc.tdwg.org/terms/#livingspecimen), but when it comes from a museum it is usually called a [preserved specimen](https://dwc.tdwg.org/terms/#preservedspecimen). This label helps users remove records that they might not want, which come from zoos. 

<!--more-->
 
<style>

.column {
  float: left;
  width: 50%;
  padding: 0px;
}

/* Clearfix (clear floats) */
.row::after {
  content: "";
  clear: both;
  display: table;
}
</style>

<div class="row">
<div class="column">
<h2>living specimen (zoo)</h2>
<img width="90%" src="/post/2019-09-06-living-specimen-to-preserved-specimen-understanding-basis-of-record_files/redPandaOutside.png"></img>
<div style="text-align:left; width='90%'"><sub>
redpandacat <a href="https://www.gbif.org/occurrence/2311336698">record</a> CC BY-NC-SA 4.0
</div>
</div>
<div class="column">
<h2>preserved specimen (museum)</h2>
<img width="48.5%" src="/post/2019-09-06-living-specimen-to-preserved-specimen-understanding-basis-of-record_files/cuteRedPanda.png"></img>
<div style="text-align:left; width='90%'"><sub>
<a href="https://www.gbif.org/occurrence/1802522627">record</a> CC BY 4.0
</div>
</div>
</div>

The Asian Red Panda the user [found](https://www.gbif.org/occurrence/1702720584) in the United States was labeled as a **preserved specimen** because it had been collected in the United States from a zoo. So the red panda really was from the **United States**!

> **occurrence record ID**: [1702720584](https://www.gbif.org/occurrence/1702720584) <br>
> **Locality**: Seattle; Woodland Park **Zoo**<br>
> **Event remarks**: euthanized due to heart failure


<img width="100%" src="/post/2019-09-06-living-specimen-to-preserved-specimen-understanding-basis-of-record_files/occPage1.png"></img>

Such edged cases are difficult to filter using **basis of record** only. Perhaps in the future GBIF should consider flagging records that occur near zoos or botanical gardens. 

<img width="100%" src="/post/2019-09-06-living-specimen-to-preserved-specimen-understanding-basis-of-record_files/downloadOptions.png"></img>


<!--more-->
