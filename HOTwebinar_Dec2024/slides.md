---
title: "AI-assisted mapping \nof <i class='far fa-building'></i> <i class='fas fa-shoe-prints'></i> for OSM"
format: 
  revealjs: 
    slide-number: true
    # self-contained: false
    navigation-mode: vertical
    # preview-links: auto
    # width: 1280
    # height: 720
    theme: [default, style.scss] #[default, style.scss] #solarized # custom.scss # simple # serif
    footer: "These slides at <https://ciupava.github.io/talks/HOTwebinar_Dec2024/slides.html>"
# title-slide-attributes:
#   # data-background-image: "../images/black_background6.png"
#   data-background-size: contain
#   # data-background-opacity: "0.9"
date: "12/13/2024"
date-format: long
institute:
  - Open Mapping Hub <i class="fas fa-globe-asia"></i> Asia-Pacific
  - WEBINAR
author:
  - "Anna Zanchetta"
css: style.scss
---

# <i class='fa fa-map'></i> Introduction

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">

## <i class='fa fa-map'></i>

:::: {.columns}

::: {.column width="15%"}
::: 

::: {.column width="30%"}
<br/><br/>
![](../images/TURINGlogo.png)
:::

::: {.column width="10%"}
:::

::: {.column width="30%"}
<br/><br/><br/>
![](../images/HOTlogoWHITE.png)
:::


::::


## <i class='fa fa-map'></i>{background-image="../images/fair_morewebpage.png" background-size="900px"}
<i class='fa fa-compass'></i> fAIr

<br/><br/><br/><br/>
<br/><br/><br/>

[https://fair.hotosm.org/](https://fair.hotosm.org/)

## <i class='fa fa-map'></i>{background-image="../images/fair_sample2.png" background-size="1200px" background-color="black"}


## <i class='fa fa-map'></i>{background-image="../images/fair_sample2_pred.png" background-size="1200px" background-color="black"}



## <i class='fa fa-map'></i>{background-image="../images/fair_sample1.png" background-size="1200px"}


## <i class='fa fa-map'></i>{background-image="../images/fair_sample1_pred.png" background-size="1200px"}


## <i class="fas fa-question-circle"></i>

:::: {.columns}

::: {.column width="35%"}
::: 

::: {.column width="50%"}
<br/><br/>
<br/><br/>
 What is affecting fAIr's performance?

:::

::: {.column width="15%"}
:::

::::


## <i class="fas fa-map"></i>{background-image="../images/MLmethod3.png" background-size="1250px"}


## <i class="fas fa-map"></i>{background-image="../images/oam_morewebpage.png" background-size="800px"  background-color="black"}
<i class="far fa-images"></i> RGB from OAM
<br/><br/><br/><br/><br/><br/>
<br/><br/><br/>
[Open Aerial Map](https://openaerialmap.org/)

## <i class="fas fa-map"></i>{background-image="../images/labels_fair.png" background-size="1200px"}
<i class="fas fa-home"></i> Labels from OSM
<br/><br/><br/><br/><br/><br/>
<br/><br/><br/>
[Preprocessing in fAIr](https://fair-dev.hotosm.org/training-datasets)

<!-- # <i class="fas fa-server"></i> ML engine -->

<!-- # <i class="fas fa-graduation-cap"></i> Semantic segmentation -->


# <i class="fas fa-globe-africa"></i> Dataset

## <i class="fas fa-globe-africa"></i>

|[]()    |        |
|--------|--------|
| **Urban regions**  | 25   |
| **Countries**  | 21   |
| **Zoom levels**    |  19, 20, 21 | 
| **N. images**   | 8400 <br> (~350 per region)  |
| **Images size** | 256x256 |
| **Resolution**  | cm |
|[]()    |        |

## <i class="fas fa-globe-africa"></i>{background-image="../images/world_map_citieslocations.png"}
<i class="fas fa-map-marker-alt"></i> Locations

## <i class="fas fa-globe-africa"></i>{background-image="../images/world_map_byurbantype.png"}
<i class="fas fa-list"></i> Degree of urbanity

## <i class="fas fa-globe-africa"></i>{background-image="../images/urban1.png" background-color="black"}
<i class='fa fa-university'></i> Rural

<br/>
Desa Kulaba

[Indonesia]


## <i class="fas fa-globe-africa"></i>{background-image="../images/urban2.png"}
<i class='fa fa-university'></i> Peri-urban

<br/>
Ggaba

[Uganda]

## <i class="fas fa-globe-africa"></i>{background-image="../images/urban4.png" background-color="black"}
<i class='fa fa-university'></i> Urban

<br/>
Bogota

[Colombia]

## <i class="fas fa-globe-africa"></i>{background-image="../images/urban3.png" background-color="black"}
<i class='fa fa-university'></i> Refugee camp

<br/>
Kakuma

[Kenya]

## <i class="fas fa-globe-africa"></i>{background-image="../images/world_map_bycovertype.png"}
<i class="fas fa-list"></i> Roof cover type

## <i class="fas fa-globe-africa"></i>{background-image="../images/cover1.png"}
<i class='fas fa-shapes'></i>  Shingles

<br/>
Silvania

[Brasil]

## <i class="fas fa-globe-africa"></i>{background-image="../images/cover2.png" background-color="black"}
<i class='fas fa-shapes'></i> Metal

<br/>
Ngaoundere

[Cameroon]

## <i class="fas fa-globe-africa"></i>{background-image="../images/cover3.png"}
<i class='fas fa-shapes'></i> Cement

<br/>
Melbourne

[Australia]

## <i class="fas fa-globe-africa"></i>{background-image="../images/cover4.png"}
<i class='fas fa-shapes'></i> Mixed

<br/>
Kutupalong

[Bangladesh]

## <i class="fas fa-globe-africa"></i>{background-image="../images/world_map_bydensity.png"}
<i class="fas fa-list"></i> Urban density

## <i class="fas fa-globe-africa"></i>{background-image="../images/density1.png" background-color="black"}
<i class='fa fa-th'></i> Dense

<br/>
Montevideo

[Uruguay]

## <i class="fas fa-globe-africa"></i>{background-image="../images/density3.png"}
<i class='fa fa-th'></i> Sparse

<br/>
Gornja Rijeka

[Croatia]

## <i class="fas fa-globe-africa"></i>{background-image="../images/density2.png"}
<i class='fa fa-th'></i> Grid

<br/>
Quincy

[USA]


# <i class="fas fa-hand-point-down"></i> Analysis & Results

## <i class="fas fa-hand-point-down"></i>{background-image="../images/metrics2.png" background-size="1200px"}
<i class="fas fa-chart-line"></i> Metrics
<br/><br/><br/><br/><br/><br/>
<br/><br/><br/><br/>

Source: [https://metrics-reloaded.dkfz.de/metric-library](Metric reloaded, Reinke et al.)

## <i class="fas fa-hand-point-down"></i>{background-image="../images/metrics3.png" background-size="1200px"}
<i class="fas fa-chart-line"></i> Metrics
<br/><br/><br/><br/><br/><br/>
<br/><br/><br/><br/>

Source: [https://metrics-reloaded.dkfz.de/metric-library](Metric reloaded, Reinke et al.)

## <i class="fas fa-hand-point-down"></i>

<i class="fas fa-hourglass-half"></i> Training

|[]()    |        |
|--------|--------|
| **Urban regions**  | all (25) |
| **N. of epochs**  | 20   |
| **Batch sizes**    |      4 <br> (2, 4, 8, 16) | 
| **Accuracy metrics**   | 5 <br>Categorical accuracy, Precision,<br>Recall, F1 Score, IoU  |
|[]()    |        |


## <i class="fas fa-hand-point-down"></i> </i>{background-image="../images/graph_sample.png" background-size="900px"}

<i class='fa fa-chart-bar'></i>

## <i class="fas fa-hand-point-down"></i>{background-image="../images/graph_with_circle2.png" background-size="900px"}

<i class='fa fa-chart-bar'></i>

## <i class="fas fa-hand-point-down"></i>{background-image="../images/plot_map_density2.png" background-size="800px"}

<i class='fa fa-chart-bar'></i>

## <i class="fas fa-hand-point-down"></i>

:::: {.columns}

::: {.column width="35%"}
::: 

::: {.column width="50%"}
<br/><br/>

<i class="far fa-square"></i> Urbanity

<i class="far fa-square"></i> Roof type

<i class="far fa-check-square"></i> Density

:::

::: {.column width="15%"}
:::

::::

## <i class="fas fa-hand-point-down"></i>{background-image="../images/plot_map_density2_withscore.png" background-size="800px"}

<i class='fa fa-chart-bar'></i>

## <i class="far fa-thumbs-down"></i>{background-image="../images/Banyuwangi1.png" background-size="1200px"}

<br/>
Banyuwangi

[Indonesia]

## <i class="far fa-thumbs-down"></i>{background-image="../images/Banyuwangi1_pred.png" background-size="1200px"}

<br/>
Banyuwangi

[Indonesia]

## <i class="far fa-thumbs-down"></i>{background-image="../images/Banyuwangi2.png" background-size="1200px"}

<br/>
Banyuwangi

[Indonesia]

## <i class="far fa-thumbs-down"></i>{background-image="../images/Banyuwangi2_pred.png" background-size="1200px"}

<br/>
Banyuwangi

[Indonesia]


## <i class="far fa-thumbs-down"></i>{background-image="../images/Pallaby1.png" background-size="1200px"}

<br/>
Pallaby, Dhaka

[Bangladesh]

## <i class="far fa-thumbs-down"></i>{background-image="../images/Pallaby1_pred.png" background-size="1200px"}

<br/>
Pallaby, Dhaka

[Bangladesh]

## <i class="far fa-thumbs-down"></i>{background-image="../images/Pallaby3.png" background-size="1200px"}

<br/>
Pallaby, Dhaka

[Bangladesh]

## <i class="far fa-thumbs-down"></i>{background-image="../images/Pallaby3_pred.png" background-size="1200px"}

<br/>
Pallaby, Dhaka

[Bangladesh]

## <i class="far fa-thumbs-up"></i>{background-image="../images/Denver_pred.png" background-size="1200px"}

<br/>
Denver

[USA]

## <i class="far fa-thumbs-up"></i>{background-image="../images/Denver.png" background-size="1200px"}

<br/>
Denver

[USA]

## <i class="far fa-thumbs-up"></i>{background-image="../images/Pergamino.png" background-size="1200px"}

<br/>
Pergamino

[Argentina]

## <i class="far fa-thumbs-up"></i>{background-image="../images/Pergamino_pred.png" background-size="1200px"}

<br/>
Pergamino

[Argentina]

## <i class="far fa-thumbs-up"></i>{background-image="../images/Kakuma.png" background-size="1200px"}

<br/>
Kakuma

[Kenya]

## <i class="far fa-thumbs-up"></i>{background-image="../images/Kakuma_pred.png" background-size="1200px"}

<br/>
Kakuma

[Kenya]

## <i class="fas fa-hand-point-down"></i>

<i class="far fa-paper-plane"></i> Future

<br/>
<br/>

:::{.r-stack}
<i class="fas fa-cogs"></i> Alternative models <br> <br><i class="fas fa-tree"></i> <i class="fas fa-water"></i>  Other features
:::



# <i class="fas fa-praying-hands"></i> THANK YOU

<br/><br/><br/><br/>

<br/>
<i class='fa fa-at'></i> [fair.hotosm.org/](https://fair.hotosm.org/)
<br/>
<i class="fab fa-github"></i> [github.com/hotosm/fAIr-utilities](https://github.com/hotosm/fAIr-utilities)
<br/>
<i class="fas fa-pencil-alt"></i> [en.osm.town/@ciupava](https://en.osm.town/@ciupava)
<!-- <br/>
Link to this presentation <i class="fas fa-angle-down"></i> -->