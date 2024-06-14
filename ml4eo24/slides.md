---
title: "Mapping buildings <i class='fa fa-paw'></i> with fAIr"
subtitle: "Validation accuracy after training in building footprints segmentation for OpenStreetMap"
# author:
#   - name: "John Doe"
date: "2024-06-24"
date-format: long
author:
  - "*Anna Zanchetta, Omran Najjar, Kshitij Sharma*"
institute:
  - "The Alan Turing Institute {.smaller}"
  - HOT Humanitarian OpenStreetMap Team
format: 
  revealjs: 
    slide-number: true
    # self-contained: false
    navigation-mode: vertical
    preview-links: auto
    # width: 1280
    # height: 720
    theme: default #solarized # custom.scss # simple # serif
    footer: "These slides at [ciupava.github.io/talks/ml4eo24/slides.html](ciupava.github.io/talks/ml4eo24/slides.html)"
include-in-header: 
  text: |
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">

---


# <i class='fa fa-align-left'></i> Summary

## <i class='fa fa-align-left'></i>

:::: {.columns}

::: {.column width="45%"}

* <i class='fa fa-map'></i> Introduction
    * <i class="fas fa-pepper-hot"></i> HOT OSM
        -   <i class='fa fa-compass'></i> fAIr
        -   <i class="fas fa-server"></i> ML model
        -   <i class="fas fa-lightbulb"></i> reason for research
:::

::: {.column width="10%"}
:::

::: {.column width="45%"}
* <i class='fas fa-microscope'></i> <i class="fas fa-search"></i> Research
    *  <i class="fas fa-crosshairs"></i> Aim
    * <i class="fas fa-wrench"></i> Methods
        * <i class="fas fa-table"></i> Data
          - <i class="far fa-images"></i> Chips, OAM
          - <i class="fas fa-home"></i> Masks
        - <i class="fas fa-globe-africa"></i> Dataset
          - <i class="fas fa-map-marker-alt"></i> Locations
          - <i class="fas fa-list"></i> Categories
* <i class='fa fa-puzzle-piece'></i> Results
:::

::::

<!-- ## <i class='fa fa-align-left'></i>

::: {layout-ncol=2}

::: -->


## Awesome icons
<i class="fas fa-globe"></i>
<i class="fas fa-globe-americas"></i>
<i class="fas fa-globe-africa"></i>
<i class="fab fa-diaspora"></i>
<i class='fa fa-braille'></i>
<i class="fas fa-dice-three"></i>
<i class="fas fa-disease"></i>
<i class="fa-regular fa-square"></i>
<i class="fa-duotone fa-grid"></i>
<i class="fas fa-grip-horizontal"></i>
<i class="fas fa-border-none"></i>
<i class="fa-solid fa-grid"></i>
<i class="fa-solid fa-grid"></i>
<i class='fa fa-square-o'></i>
<i class='fa fa-th-list'></i>
<i class='fa fa-th'></i>
<i class='fa fa-th-large'></i>
<i class='fa fa-tasks'></i>
<i class='fa fa-window-restore'></i>
<i class='fa fa-window-maximize'></i>
<i class='fa fa-minus'></i>
<i class='fa fa-circle-thin'></i>
<i class='fa fa-navicon'></i>
<i class='fa fa-reorder'></i>


<i class="fas fa-shapes"></i>
<i class="fas fa-border-all"></i>
<i class='fa fa-th'></i>
<i class='fa fa-th-large'></i>


<i class='fa fa-stop'></i>
<i class='fa fa-home'></i>
<i class='fa fa-building'></i>
<i class="far fa-building"></i>
<i class="fas fa-hotel"></i>
<i class='fa fa-industry'></i>
<i class="fas fa-landmark"></i>
<i class="fas fa-landmark"></i>
<i class="fas fa-store-alt"></i>
<i class='fa fa-compass'></i>
<i class='fa fa-signal'></i>
<i class='fa fa-tag'></i>
<i class='fa fa-tags'></i>
<i class='fa fa-university'></i>
<i class='fa fa-tree'></i>
<i class='fa fa-wrench'></i>
<i class='fa fa-paperclip'></i>
<i class='fa fa-scissors'></i>
<i class='fa fa-file'></i>
<i class='fa fa-file-o'></i>
<i class='fa fa-comment'></i>
<i class='fa fa-comments'></i>
<i class="far fa-comment"></i>
<i class='fa fa-search'></i>
<i class='fa fa-send'></i>
<i class='fa fa-photo'></i>
<i class="fas fa-umbrella-beach"></i>

<i class="fas fa-chart-bar"></i>
<i class="fas fa-terminal"></i>
<i class="fas fa-tools"></i>

<i class="fas fa-pepper-hot"></i>
<i class="fab fa-hotjar"></i>
<i class="fas fa-fire-alt"></i>
<i class="fas fa-fire"></i>
<i class="fas fa-burn"></i>

<i class="fab fa-periscope"></i>
<i class="fas fa-microscope"></i>
<i class="fas fa-search"></i>

<i class='fa fa-'></i>


# <i class='fa fa-map'></i> Introduction

## <i class='fa fa-map'></i> 
<i class="fab fa-hotjar"></i> HOT
<br/><br/><br/><br/>
<br/><br/><br/><br/>
![](../images/OSMlogo.png){.absolute top="70" left="30"}
<br/><br/>
![](../images/HOTlogo.png){.absolute top="330" left="30"}

## <i class='fa fa-map'></i> {background-image="../images/fair_why.png"}
<i class='fa fa-compass'></i> fAIr
<br/><br/><br/><br/><br/><br/>
[https://fair-dev.hotosm.org/](https://fair-dev.hotosm.org/)

## <i class='fa fa-map'></i>
<i class="fas fa-server"></i> ML engine

image from RAMP

## <i class='fa fa-map'></i>

::: {layout-ncol=2}

<i class="fas fa-search"></i> 

<i class="fas fa-lightbulb"></i>

:::

# <i class="fas fa-search"></i> Research

## <i class="fas fa-search"></i>
<i class="fas fa-crosshairs"></i> Aim

## <i class="fas fa-search"></i>
<i class="far fa-database"></i> Data

::: {layout-ncol=2}

<i class="far fa-images"></i> RGB from OAM
<br/><br/>
[Open Aerial Map](https://openaerialmap.org/)

<i class="fas fa-home"></i> Masks

:::

## <i class="fas fa-search"></i>
<i class="fas fa-globe-africa"></i> Dataset
Description

## <i class="fas fa-search"></i>{background-image="../images/world_map_citieslocations.png"}
<i class="fas fa-map-marker-alt"></i> Locations


## <i class="fas fa-search"></i>{background-image="../images/world_map_bydensity.png"}
<i class="fas fa-list"></i> Categories

## <i class="fas fa-search"></i>{background-image="../images/world_map_bycovertype.png"}
<i class="fas fa-list"></i> Categories

## <i class="fas fa-search"></i>{background-image="../images/world_map_byurbantype.png"}
<i class="fas fa-list"></i> Categories

# <i class='fa fa-puzzle-piece'></i> Results
<i class='fa fa-bar-chart'></i> 

## <i class='fa fa-puzzle-piece'></i>

## <i class='fa fa-puzzle-piece'></i>

# <i class="fas fa-hand-point-down"></i> Conclusions
<!-- ## <i class='fa fa-rocket'></i> -->

## <i class="fas fa-hand-point-down"></i>
nice numbers


## <i class="fas fa-hand-point-down"></i>

<i class='fa fa-at'></i> Links
<br/><br/>

GitHub fork from HOT's `fair-utilities` [link](https://github.com/ciupava/fAIr-utilities)
<br/>
fAIr pro
<br/>
This presentation [link](https://ciupava.github.io/talks/team_call_Dec2023_fAIr/slides.html)


# THANK YOU
