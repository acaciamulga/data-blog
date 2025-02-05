---
title: GBIF checklist datasets and data gaps
author: John Waller
date: '2019-05-14'
slug: gbif-checklist-datasets-and-data-gaps
categories:
  - GBIF
tags:
  - data gaps
  - data quality
  - checklists
lastmod: '2019-04-23T09:02:19+02:00'
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

> A **checklist dataset** is a catch-all term describing any dataset that contains primarily a list of taxonomic names. The lines between a checklist dataset and an occurrence dataset can be blurry.

<!--more-->

**GBIF** classifies at least 6 types of datasets as checklists. 

1. **National (or regional) lists of species** [example](https://www.gbif.org/dataset/de8934f4-a136-481c-a87a-b0b202b80a31)
2. **Taxonomic list of species** [example](https://www.gbif.org/dataset/7ddf754f-d193-4cc9-b351-99906754a03b)
3. Species description [example](https://www.gbif.org/dataset/02db0742-97fe-4ff8-8917-c8d2591d12a1)
4. Checklists made up of other checklists [GBIF backbone taxonomy](https://www.gbif.org/dataset/d7dddbf4-2cf0-4f39-9b2a-bb099caae36c) & [Catalogue of Life](https://www.gbif.org/dataset/7ddf754f-d193-4cc9-b351-99906754a03b)
5. Checklists with occurrences [example](https://www.gbif.org/dataset/e09e1e1f-2460-4017-a964-e999abd2bf66)
6. Checklists made from occurrences [example](https://www.gbif.org/dataset/b6a01612-c202-4310-9559-caa82aa3f957)

The top two are probably what most people imagine when they think of a **checklist dataset**. GBIF has published a [guide](https://assets.ctfassets.net/uo17ejk9rkwj/62uueQ2eNGyUyu0yeoEc8i/a9736e0554edff75fdc129f11d031181/gbif_national_checklists_best_practice_guide_en_v1.0.pdf) on best practices for making checklist datasets. 

The **GBIF Backbone Taxonomy** is a [checklist dataset](https://www.gbif.org/dataset/d7dddbf4-2cf0-4f39-9b2a-bb099caae36c) of names GBIF uses in order to classify all the species used in the different datasets. The backbone taxonomy dataset is in fact a large group of other selected checklist [datasets](https://www.gbif.org/dataset/d7dddbf4-2cf0-4f39-9b2a-bb099caae36c/constituents), including large parts of the **Catalogue of Life**. 

> The **GBIF backbone taxonomy** is a list of **>2 million names** used to match and group the records on GBIF.

Not [every name](https://www.gbif.org/species/5141022) in the GBIF backbone has occurrences and names with occurrences are not distributed equally. One way to tell if the GBIF network is collecting occurrences for at least the **named taxonomic** groups is by comparing the **species names in the backbone versus the species names with occurrences**. 


# How much of the GBIF backbone is covered by occurrences?  

Here I plot **the percentage of the GBIF backbone with at least 1 occurrence** for popular groups. 

![](/post/2019-04-23-gbif-checklist-datasets-and-data-gaps_files/popularGroupsCoverageBackbone.svg)

<div style="text-align:right;"><sub>common name dictionary: [csv](/post/2019-04-23-gbif-checklist-datasets-and-data-gaps_files/commonNameDictionary.csv)</sup></div>

We see that the GBIF network has successfully collected occurrences for **94% of birds** but only **51% of named insects**. 

**Beetles**, **moths**, **butterflies**, **ants**, and **flies** make up the majoriy of the missing insects. Each group having around only 50% of their named species with occurrences, with **dragonflies** (78%) not contributing greatly to the missing insects. 

**Flowering plants** (Magnoliopsida) are a large and well-studied group of plants. The herbariums contributing to GBIF are no doubt responsible for the 86% coverage seen in this group.   

Other small groups with fairly large animals (**mammals**, **reptiles**, **amphibians**) are all well covered. 

**Bacteria** have 89% coverage but this must be due to the lack of named records within GBIF. 


# Using checklists to look for regional data gaps 

To explore whether checklists datasets are useful for identifying regional data gaps, I have decided to look at checklists from two regions **West Europe** and **West Africa**. These regions represent areas where **data coverage** and **checklist supply** are different. 

# West Europe† checklisted species 

The **percentage of checklisted species with at least 1 occurrence** for popular groups. 

![](/post/2019-04-23-gbif-checklist-datasets-and-data-gaps_files/westEuropeCoveragePopularGroups.svg)

<div style="text-align:right;"><sub >† Austria, Belgium, Denmark, Finland, France, Germany, Iceland, Ireland, Lithuania, Netherlands, Norway, Sweden, Switzerland</sup></div>
<div style="text-align:right;">
</div>


# West Africa† checklisted species

![](/post/2019-04-23-gbif-checklist-datasets-and-data-gaps_files/westAfricaCoveragePopularGroups.svg)

<div style="text-align:right;"><sub>† Benin, Ghana, Liberia, Mali, Mauritania, Niger, Nigeria, Senegal, Togo</sup></div>


# Fewer checklisted species in West Africa

<style>
table {
  border-collapse: collapse;
}

table, td, th {
  padding:0px 0px 0px 40px;
  <!-- margin: 0 auto; -->
}
</style>

<table>
  <tr>
    <th></th>
    <th><b>West Europe</b></th>
    <th><b>West Africa</b></th> 
  </tr>
  <tr>
    <td><b>Insects<b/></td>
    <td>53,000</td> 
    <td>800</td>
  </tr>
  <tr>
    <td><b>Fungi<b/></td>
    <td>29,000</td> 
    <td>50</td>
  </tr>
  </tr>
  <tr>
    <td><b>Flies<b/></td>
    <td>16,500</td> 
    <td>190</td>
  </tr>
  </tr>
  <tr>
  <tr>
    <td><b>Spiders<b/></td>
    <td>1,600</td> 
    <td>5</td>
  </tr>
  </tr>
  <tr>
    <td><b>Mammals<b/></td>
    <td>210</td> 
    <td>240</td>
  </tr>
  <tr>
    <td><b>Birds<b/></td>
    <td>780</td> 
    <td>600</td>
  </tr>
  <tr>
    <td><b>Dragonflies<b/></td>
    <td>108</td> 
    <td>160</td>
  </tr>
  <tr>
    <td><b>Amphibians<b/></td>
    <td>95</td> 
    <td>60</td>
  </tr>
</table>

Here we see that while the percentages seem quite good, the number of checklisted species in West Africa are in some cases **orders of magnitude less** than what is in West Europe. Although some West African groups (**Mammals**, **Birds**, **Dragonflies**) do have more checklisted species than West Europe.


# Checklist supply is much lower in <b><span style="color: #FDAF02">West Africa</span></b>


![](/post/2019-04-23-gbif-checklist-datasets-and-data-gaps_files/histogramOfChecklistDatasetSize.svg)

<b><span style="color: #509E2F">West Europe</span></b> has many more **large national publishers** than <b><span style="color: #FDAF02">West Africa</span></b>. 

Most checklist species in West Africa are small checklists published by [Plazi](https://www.gbif.org/dataset/search?type=CHECKLIST&publishing_org=7ce8aef0-9e92-11dc-8738-b8a03c50a862) and [Biodiversity Data Journal](https://www.gbif.org/dataset/search?type=CHECKLIST&publishing_org=750a8724-fa66-4c27-b645-bd58ac5ee010). [Benin LFS](https://www.gbif.org/dataset/dba21dbc-ea38-4bbf-b50f-ba3d256e1f73) publisher seems to be the only semi-large national publisher in West Africa. Most likely the number of species with occurrences is greater than the number of species in checklists in West Africa. 

<!--more-->
