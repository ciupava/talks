---
title: "Mapping buildings with AI"
subtitle: "Scoping the semi-automatic generation of buildings footprints for humanitarian mapping (and more)"
format:
  revealjs: 
    slide-number: true
    chalkboard: 
      buttons: false
    preview-links: auto
    logo: images/quarto.png
    css: styles.css
    theme: moon
    footer: <These slides at https://ciupava.github.io/talks/team_call_Dec2023_fAIr/slides.html>

---

## Introduction

::: {.fragment .fade-in-then-semi-out}
Presenting HOT and fAIr
:::
::: {.fragment .fade-in-then-semi-out}
Demo
:::
::: {.fragment .fade-in-then-semi-out}
Computer Vision
:::
::: {.fragment .fade-in-then-semi-out}
State of the art in Image Segmentation
:::
::: {.fragment .fade-in-then-semi-out}
Current status of the project
:::

## Introduction to HOT and fAIr

HOT
![](mini/images/HOTlogo.png){.absolute top="170" left="30"}
![](mini/images/OSMlogo.png){.absolute top="170" left="170"}

<br/>

## Introduction to HOT and fAIr {background="#43464B" background-image="images/fair_slide.png"}

fAIr

## Introduction to HOT and fAIr {background="#43464B" background-image="images/fair_why.png"}

fAIr

## Demo

## Let's make it work better!

## (short) Intro to Computer Vision
Image Segmentation


## (short) Intro to Computer Vision
Image Segmentation for buildings footprints


## Let's make it work better!

<br/>
Challenges

## Let's make it work better! {background="#43464B" background-image="images/models_list.png"}

<br/>
Challenges

## Let's make it work better! 

<br/>
Challenges

![](mini/images/maxar_osm.png){.absolute top="100" left="30"}
https://wiki.openstreetmap.org/wiki/Maxar

![](mini/images/maxar_open.png){.absolute top="170" left="30"}
https://www.maxar.com/open-data

![](mini/images/oam.png){.absolute top="210" left="30"}



## Status of the project

::: incremental
-   First trials
-   Cloud computing
-   A name?
:::





Arrange content into columns of varying widths:

::: columns
::: {.column width="35%"}

#### Motor Trend Car Road Tests

The data was extracted from the 1974 Motor Trend US magazine, and comprises fuel consumption and 10 aspects of automobile design and performance for 32 automobiles.
:::

::: {.column width="3%"}
:::

::: {.column width="62%"}

:::
:::

::: footer
Learn more: [Multiple Columns](https://quarto.org/docs/presentations/revealjs/#multiple-columns)
:::

## Incremental Lists

Lists can optionally be displayed incrementally:

::: incremental
-   First item
-   Second item
-   Third item
:::

. . .

<br/> Insert pauses to make other types of content display incrementally.

::: footer
Learn more: [Incremental Lists](https://quarto.org/docs/presentations/revealjs/#incremental-lists)
:::

## Fragments

Incremental text display and animation with fragments:

<br/>

::: {.fragment .fade-in}
Fade in
:::

::: {.fragment .fade-up}
Slide up while fading in
:::

::: {.fragment .fade-left}
Slide left while fading in
:::

::: {.fragment .fade-in-then-semi-out}
Fade in then semi out
:::

. . .

::: {.fragment .strike}
Strike
:::

::: {.fragment .highlight-red}
Highlight red
:::

::: footer
Learn more: [Fragments](https://quarto.org/docs/presentations/revealjs/advanced.html#fragments)
:::

## Slide Backgrounds {background="#43464B"}

Set the `background` attribute on a slide to change the background color (all CSS color formats are supported).

Different background transitions are available via the `background-transition` option.

::: footer
Learn more: [Slide Backgrounds](https://quarto.org/docs/presentations/revealjs/#color-backgrounds)
:::

## Media Backgrounds {background="#43464B" background-image="images/milky-way.jpeg"}

You can also use the following as a slide background:

-   An image: `background-image`

-   A video: `background-video`

-   An iframe: `background-iframe`

::: footer
Learn more: [Media Backgrounds](https://quarto.org/docs/presentations/revealjs/#image-backgrounds)
:::

## Absolute Position

Position images or other elements at precise locations

![](mini/images/kitten-400-350.jpeg){.absolute top="170" left="30" width="400" height="400"}

![](mini/images/kitten-450-250.jpeg){.absolute .fragment top="150" right="80" width="450"}

![](mini/images/kitten-300-200.jpeg){.absolute .fragment bottom="110" right="130" width="300"}

::: footer
Learn more: [Absolute Position](https://quarto.org/docs/presentations/revealjs/advanced.html#absolute-position)
:::

## Auto-Animate {auto-animate="true" auto-animate-easing="ease-in-out"}

Automatically animate matching elements across slides with Auto-Animate.

::: r-hstack
::: {data-id="box1" auto-animate-delay="0" style="background: #2780e3; width: 200px; height: 150px; margin: 10px;"}
:::

::: {data-id="box2" auto-animate-delay="0.1" style="background: #3fb618; width: 200px; height: 150px; margin: 10px;"}
:::

::: {data-id="box3" auto-animate-delay="0.2" style="background: #e83e8c; width: 200px; height: 150px; margin: 10px;"}
:::
:::

::: footer
Learn more: [Auto-Animate](https://quarto.org/docs/presentations/revealjs/advanced.html#auto-animate)
:::

## Auto-Animate {auto-animate="true" auto-animate-easing="ease-in-out"}

Automatically animate matching elements across slides with Auto-Animate.

::: r-stack
::: {data-id="box1" style="background: #2780e3; width: 350px; height: 350px; border-radius: 200px;"}
:::

::: {data-id="box2" style="background: #3fb618; width: 250px; height: 250px; border-radius: 200px;"}
:::

::: {data-id="box3" style="background: #e83e8c; width: 150px; height: 150px; border-radius: 200px;"}
:::
:::

::: footer
Learn more: [Auto-Animate](https://quarto.org/docs/presentations/revealjs/advanced.html#auto-animate)
:::

## Slide Transitions {.smaller}

The next few slides will transition using the `slide` transition

| Transition | Description                                                            |
|------------|------------------------------------------------------------------------|
| `none`     | No transition (default, switch instantly)                              |
| `fade`     | Cross fade                                                             |
| `slide`    | Slide horizontally                                                     |
| `convex`   | Slide at a convex angle                                                |
| `concave`  | Slide at a concave angle                                               |
| `zoom`     | Scale the incoming slide so it grows in from the center of the screen. |

::: footer
Learn more: [Slide Transitions](https://quarto.org/docs/presentations/revealjs/advanced.html#slide-transitions)
:::

## Tabsets {.smaller .scrollable transition="slide"}

::: panel-tabset




## Interactive Slides {.smaller transition="slide"}

Turn presentations into applications with Observable and Shiny. Use component layout to position inputs and outputs.





## Preview Links

Navigate to hyperlinks without disrupting the flow of your presentation.

Use the `preview-links` option to open links in an iframe on top of your slides. Try clicking the link below for a demonstration:

::: {style="text-align: center; margin-top: 1em"}
[Matplotlib: Visualization with Python](https://matplotlib.org/){preview-link="true" style="text-align: center"}
:::

::: footer
Learn more: [Preview Links](https://quarto.org/docs/presentations/revealjs/presenting.html#preview-links)
:::

## Themes

10 Built-in Themes (or [create your own](https://quarto.org/docs/presentations/revealjs/themes.html#creating-themes))

::: {layout-ncol="2"}
![](images/moon.png)

![](images/sky.png)
:::

::: footer
Learn more: [Themes](https://quarto.org/docs/presentations/revealjs/themes.html)
:::

## Easy Navigation

::: {style="margin-bottom: 0.9em;"}
Quickly jump to other parts of your presentation
:::

::: {layout="[1, 20]"}
![](images/presentation-menu.png){width="41"}

Toggle the slide menu with the menu button (bottom left of slide) to go to other slides and access presentation tools.
:::

You can also press `m` to toggle the menu open and closed.

::: footer
Learn more: [Navigation](https://quarto.org/docs/presentations/revealjs/presenting.html#navigation-menu)
:::

## Chalkboard {chalkboard-buttons="true"}

::: {style="margin-bottom: 0.9em;"}
Free form drawing and slide annotations
:::

::: {layout="[1, 20]"}
![](images/presentation-chalkboard.png){width="41"}

Use the chalkboard button at the bottom left of the slide to toggle the chalkboard.
:::

::: {layout="[1, 20]"}
![](images/presentation-notes-canvas.png){width="41"}

Use the notes canvas button at the bottom left of the slide to toggle drawing on top of the current slide.
:::

You can also press `b` to toggle the chalkboard or `c` to toggle the notes canvas.

::: footer
Learn more: [Chalkboard](https://quarto.org/docs/presentations/revealjs/presenting.html#chalkboard)
:::

## Point of View

Press `o` to toggle overview mode:

![](images/overview-mode.png){.border}

Hold down the `Alt` key (or `Ctrl` in Linux) and click on any element to zoom towards it---try it now on this slide.

::: footer
Learn more: [Overview Mode](https://quarto.org/docs/presentations/revealjs/presenting.html#overview-mode), [Slide Zoom](https://quarto.org/docs/presentations/revealjs/presenting.html#slide-zoom)
:::

## Speaker View

Press `s` (or use the presentation menu) to open speaker view

![](images/speaker-view.png){fig-align="center" style="border: 3px solid #dee2e6;" width="780"}

::: footer
Learn more: [Speaker View](https://quarto.org/docs/presentations/revealjs/presenting.html#speaker-view)
:::

