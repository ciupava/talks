---
title: "Mapping <i class='far fa-building'></i> <i class='fas fa-shoe-prints'></i>  with fAIr"
subtitle: "Assessing the performance of AI-assisted mapping of building footprints for OSM"
format: 
  revealjs: 
    slide-number: true
    # self-contained: false
    navigation-mode: vertical
    # preview-links: auto
    # width: 1280
    # height: 720
    theme: [default, style.scss] #solarized # custom.scss # simple # serif
    footer: "These slides at <https://ciupava.github.io/talks/SoTM24/slides.html>"
title-slide-attributes:
  data-background-image: "../images/black_background6.png"
  data-background-size: contain
  data-background-opacity: "0.9"
date: "2024-09-08"
date-format: long
author:
  - "*Anna Zanchetta, Omran Najjar, Kshitij Sharma*"
institute:
  - "The Alan Turing Institute"
  - "HOT Humanitarian OpenStreetMap Team"
css: style.scss
include-in-header: 
  text:
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@5.15.4/css/fontawesome.min.css"/>

---

# <i class='fa fa-map'></i> Introduction

## <i class='fa fa-map'></i>{background-image="../images/Intro_sotm.png" background-size="1200px"}



## <i class='fa fa-map'></i>{background-image="../images/fair_morewebpage.png" background-size="800px"}
<i class='fa fa-compass'></i> fAIr

<br/><br/><br/><br/>
<br/><br/><br/>

[https://fair-dev.hotosm.org/](https://fair-dev.hotosm.org/)


## <i class='fa fa-map'></i>{background-image="../images/fair_sample1.png" background-size="1200px"}
<i class="fas fa-lightbulb"></i> Reason for research

## <i class='fa fa-map'></i>{background-image="../images/fair_sample1_pred.png" background-size="1200px"}
<i class="fas fa-lightbulb"></i> 

## <i class='fa fa-map'></i>{background-image="../images/fair_sample2.png" background-size="1200px" background-color="black"}
<i class="fas fa-lightbulb"></i> 

## <i class='fa fa-map'></i>{background-image="../images/fair_sample2_pred.png" background-size="1200px" background-color="black"}
<i class="fas fa-lightbulb"></i> 

## <i class='fa fa-map'></i>{background-image="../images/fair_sample2_pred.png" background-size="1200px" background-color="black"}
<i class="fas fa-lightbulb"></i> 
<br/><br/><br/>

How accurate is fAIr in detecting buildings

in different conditions?



# <i class="fas fa-search"></i> Methods

## <i class='fa fa-search'></i>{background-image="../images/ramp_morewebpage.png" background-size="800px" background-color="black"}
<i class="fas fa-server"></i> ML engine

<br/><br/><br/><br/><br/><br/>
<br/><br/><br/>

[https://rampml.global/](https://rampml.global/)

## <i class='fa fa-search'></i>{background-image="../images/ramp_effunet_morewebpage2.png" background-size="600px"}
<i class="fas fa-server"></i> ML engine

<br/><br/><br/><br/><br/><br/>
<br/><br/><br/>

[2020 paper by Baheti et al.](https://rampml.global/ramp-model-card/)


## <i class="fas fa-search"></i>
<i class="fas fa-table"></i> Data

## <i class="fas fa-table"></i>{background-image="../images/oam_morewebpage.png" background-size="800px"  background-color="black"}
<i class="far fa-images"></i> RGB from OAM
<br/><br/><br/><br/><br/><br/>
<br/><br/><br/>
[Open Aerial Map](https://openaerialmap.org/)

## <i class="fas fa-table"></i>{background-image="../images/labels_fair.png" background-size="1200px"}
<i class="fas fa-home"></i> Labels from OSM
<br/><br/><br/><br/><br/><br/>
<br/><br/><br/>
[Preprocessing through fAIr website](https://fair-dev.hotosm.org/training-datasets)

## <i class="fas fa-search"></i>
<i class="fas fa-globe-africa"></i> Dataset

|[]()    |        |
|--------|--------|
| **Urban regions**  | 25   |
| **Countries**  | 21   |
| **Zoom levels**    |  19, 20, 21 | 
| **N. images**   | 8400 <br> (~350 per region)  |
| **Images size** | 256x256 |
| **Resolution**  | cm |
|[]()    |        |

<!-- :  {tbl-colwidths="[70,30]"} -->

## <i class="fas fa-globe-africa"></i>{background-image="../images/world_map_citieslocations.png"}
<i class="fas fa-map-marker-alt"></i> Locations

## <i class="fas fa-globe-africa"></i>{background-image="../images/world_map_byurbantype.png"}
<i class="fas fa-list"></i> Categories

## <i class="fas fa-globe-africa"></i>{background-image="../images/urban1.png" background-color="black"}
<i class='fa fa-university'></i> Rural

Desa Kulaba

## <i class="fas fa-globe-africa"></i>{background-image="../images/urban2.png"}
<i class='fa fa-university'></i> Peri-urban

Ggaba

## <i class="fas fa-globe-africa"></i>{background-image="../images/urban4.png" background-color="black"}
<i class='fa fa-university'></i> Urban

Bogota

## <i class="fas fa-globe-africa"></i>{background-image="../images/urban3.png" background-color="black"}
<i class='fa fa-university'></i> Refugee camp

Kakuma

## <i class="fas fa-globe-africa"></i>{background-image="../images/world_map_bycovertype.png"}
<i class="fas fa-list"></i> Categories

## <i class="fas fa-globe-africa"></i>{background-image="../images/cover1.png"}
<i class='fas fa-shapes'></i>  Shingles

Silvania

## <i class="fas fa-globe-africa"></i>{background-image="../images/cover2.png" background-color="black"}
<i class='fas fa-shapes'></i> Metal

Ngaoundere

## <i class="fas fa-globe-africa"></i>{background-image="../images/cover3.png"}
<i class='fas fa-shapes'></i> Cement

Melbourne

## <i class="fas fa-globe-africa"></i>{background-image="../images/cover4.png"}
<i class='fas fa-shapes'></i> Mixed

Kutupalong

## <i class="fas fa-globe-africa"></i>{background-image="../images/world_map_bydensity.png"}
<i class="fas fa-list"></i> Categories

## <i class="fas fa-globe-africa"></i>{background-image="../images/density1.png" background-color="black"}
<i class='fa fa-th'></i> Dense

Montevideo dense

## <i class="fas fa-globe-africa"></i>{background-image="../images/density3.png"}
<i class='fa fa-th'></i> Sparse

Gornja Rijeka

## <i class="fas fa-globe-africa"></i>{background-image="../images/density2.png"}
<i class='fa fa-th'></i> Grid


Quincy

## <i class="fas fa-search"></i>
<i class="fas fa-hourglass-half"></i> Training

|[]()    |        |
|--------|--------|
| **Urban regions**  | all (25) |
| **N. of epochs**  | 20   |
| **Batch sizes**    |      4 <br> (2, 4, 8, 16) | 
| **Accuracy metrics**   | 5 <br>Categorical accuracy, Precision,<br>Recall, F1 Score, IoU  |
|[]()    |        |

# <i class='fa fa-chart-bar'></i> Results

## <i class='fa fa-chart-bar'></i>{background-image="../images/graph_sample.png" background-size="900px"}

## <i class='fa fa-chart-bar'></i>{background-image="../images/graph_with_circle.png" background-size="900px"}

## <i class='fa fa-chart-bar'></i>{background-image="../images/plot_map_density.png" background-size="800px"}
~~<i class='fa fa-university'></i> Urbanity~~

~~<i class='fas fa-shapes'></i> Roof type~~

<i class='fa fa-th'></i> Density


## <i class='fa fa-chart-bar'></i>{background-image="../images/plot_box_all.png" background-size="800px"}
<i class='fa fa-puzzle-piece'></i>

~~Batch size~~


# <i class="fas fa-hand-point-down"></i> Conclusions

## <i class="fas fa-hand-point-down"></i> Conclusions

<br/><br/>

:::: {.columns}

::: {.column width="5%"}

:::

::: {.column width="15%"}

<i class='fa fa-th'></i>

:::

::: {.column width="25%"}

<i class="fas fa-border-all"></i>

<em>4.8%</em>

:::

::: {.column width="15%"}

:::

::: {.column width="40%"}

<i class="fas fa-braille"></i>

<em>4.2%</em>

:::

::::

<!-- ::: -->

## <i class="fas fa-hand-point-down"></i> Conclusions
<br/><br/>

:::: {.columns}

::: {.column width="5%"}

:::

::: {.column width="15%"}

<i class='fa fa-th'></i>

:::

::: {.column width="25%"}

<i class="fas fa-border-all"></i>

<em>[4.8%]{style="color:#bfbfbf;"}</em>

<em>7.7%</em>

:::

::: {.column width="15%"}

[ooo]{style="color:white"}

<em>[ooo]{style="color:white"}</em>

<em>IoU</em>

:::

::: {.column width="40%"}

<i class="fas fa-braille"></i>

<em>[4.2%]{style="color:#bfbfbf;"}</em>

<em>7.8%</em>

:::

::::

## <i class="fas fa-hand-point-down"></i>{background-image="../images/banyuwangi_batch16.png" background-size="1100px"}
<i class="fas fa-map-marked-alt"></i>

Banyuwangi

## <i class="fas fa-hand-point-down"></i>{background-image="../images/pallabi_batch16.png" background-size="1100px"}
<i class="fas fa-map-marked-alt"></i>

Pallaby Dhaka

## <i class="fas fa-hand-point-down"></i>
<i class="fas fa-rocket"></i> Future

<br/>
<br/>

:::{.r-stack}
<i class="fas fa-cogs"></i>  Models <br> <br><i class="fas fa-tree"></i> <i class="fas fa-water"></i>  Features
:::


# THANK YOU {background-image="../images/black_background.jpg" background-color="black"}
<br/><br/>
<i class='fa fa-at'></i>

GitHub repo [https://github.com/ciupava/fAIr-utilities](https://github.com/ciupava/fAIr-utilities)
<br/>
fAIr website [https://fair-dev.hotosm.org/](https://fair-dev.hotosm.org/)
<br/>
This presentation <i class="fas fa-angle-down"></i>

<!-- 
# <i class='fa fa-align-left'></i> Summary

## <i class='fa fa-align-left'></i> {.smaller}
<br/><br/>

:::: {.columns}

::: {.column width="30%"}

* <i class='fa fa-map'></i> Introduction
    * <i class="fas fa-pepper-hot"></i> HOT and fAIr
        <!-- -   <i class='fa fa-compass'></i> fAIr
        -   <i class="fas fa-server"></i> ML model 
    <!-- * <i class="fas fa-lightbulb"></i>  Reason for research -->

<!-- :::

::: {.column width="4%"}

:::

::: {.column width="30%"}

* <i class="fas fa-search"></i> Methods
    * <i class="fas fa-table"></i> Data
      <!-- - <i class="far fa-images"></i> Chips, OAM
      - <i class="fas fa-home"></i> Masks 
    - <i class="fas fa-globe-africa"></i> Dataset
      <!-- - <i class="fas fa-map-marker-alt"></i> Locations
      - <i class="fas fa-list"></i> Categories 

:::

::: {.column width="3%"}

:::

::: {.column width="30%"}

* <i class='fa fa-puzzle-piece'></i> Results
    * <i class='fa fa-chart-bar'></i> Graphs
    * <i class="fas fa-map-marked-alt"> </i> Cases

:::

:::: -->