---
layout: page
title: Statistical Models for Interaction Data
description: 
img: /assets/img/concep_fig_h.png
importance: 1
---

Complex, structured data is ubiquitous in both industrial and academic settings
and has elicited a commensurate interest in utilizing
structured data to inform inference and decisions. Often, this underlying structure can be
exploited to make inference and summarization procedures more tractable. In the context of large
datasets, it is
imperative to consider the data in the context of this
structure to build parsimonious models that represent the data well and provide
theoretically grounded inference procedures. Similarly, searching for underlying
structure can help to summarize the data more efficiently and find relevant
attributes of the data of interest that might otherwise go undetected. In other
datasets the structure is explicit, and thus requires careful
consideration when reasoning about modeling decisions. 

In this thesis, the focus is on data that has network structure and on problems
that benefit from the application of network based algorithms. In both
cases we are concerned with data that can be summarized with a relational
structure of constituent nodes and edges, appropriately defined based on the
context of the problem. Below, four research areas are introduced that utilize network
structure that form the backbone of this thesis.

## Graph based estimation of information theoretic quantities

Graph based estimation methods aim to skip the density estimation stage and
directly estimate the quantity of interest by calculating a graph structure over
the data sample, such as a minimal spanning tree or k-NN graph. One of the
original algorithms in this area was for the estimation of Henze-Penrose (HP)
divergence, which is a
member of 
the broad class of $f$ divergences. This divergence measure
has two important properties. First, it is possible to estimate the HP
divergence directly from a minimal spanning tree across the data sample. As the
minimal spanning tree can be computed in $O(n\log n)$, this approach to
estimation is amenable to large datasets. Second, tight bounds have been proved
that relate the HP divergence to the Bayes error rate of a binary
classification problem. Thus, accurate estimation of the HP divergence allows
for learning of the intrinsic hardness of the supervised learning task. Although tight
bounds exist for the Bayes error rate for a binary classification
task, this is not true for multi-class classification. In Chapter, we derive
tight bounds for the multi-class case using a generalized Henze-Penrose measure,
and provide a graph based estimation procedure using a minimal spanning tree.

Like other estimation methods, graph based estimation methods are subject to the
curse of dimensionality. Specifically, as the feature dimension of the data
increases, the bias of the estimate also increases. In
Chapter the thesis introduces a new estimator
of the HP divergence, based on a different computed graph, that reduces the bias
for growing dimension.

Every project has a beautiful feature showcase page.
It's easy to include images in a flexible 3-column grid format.
Make your photos 1/3, 2/3, or full width.

To give your project a background in the portfolio page, just add the img tag to the front matter like so:

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/1.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/3.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/5.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/5.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, *bled* for your project, and then... you reveal it's glory in the next row of images.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/6.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/11.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>


The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/" target="_blank">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/6.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/11.jpg' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
```
