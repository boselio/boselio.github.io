---
layout: page
title: Network Models for Multi-type Interactions
description: multi-layer networks
img: /assets/img/7.jpg
redirect: https://unsplash.com
importance: 3
---

## Information extraction from multi-layer networks

We often find heterogeneous relationships in data, reflected in more than one type of
relationship between agents. These types of relationships may impose different
topological properties. For instance, in a social network context, people may be
connected by more than one social platform. Alternatively, we may observe
explicit links between agents but also infer implicit affinities based on agent
features. Multi-layer networks can be used to account for this additional
complexity.

A multi-layer network is a network where a set of nodes are connected
by intra-layer and inter-layer edges. This structure is a
generalization of single-layer networks, where there are only intra-layer
relationships. These layers represent heterogeneity in the structure or labeling
of the data; a layer might correspond to a type of connection, or a snapshot of
the network at a specific time. The inter-layer structure represents ties among
nodes in the different
layers; this structure may be observed, assumed, or estimated depending on the
application. The inter-layer structure in a social network often preserves the labels of the nodes, so that each node in a single layer is connected to its
unique counterpart in the other layers. If the layers represent timesteps at any
time instant, each entity
might be connected to its counterpart in layers before and after the present
layer, which represents the localization of that layer’s characteristics in time.

As the multi-layer structure is more complicated than its single-layer
counterpart, methods for single-layer analysis must be modified, and new methods
can be developed specifically for multi-layer
networks. In Chapter, this thesis provides a framework for
modeling multi-layer networks, concentrating on centrality measures and community
detection. In Chapter the thesis provides a novel
multi-layer community detection approach that selects approximately
Pareto-optimal partitions between nodes.

Dynamic networks can be thought of as a special case of multi-layer networks.
However, it is also possible to have a dynamic multi-layer network, where each
layer is evolving concurrently over time. In Chapter, this
thesis proposes a multi-layer summarization
procedure for this case based on the dynamic stochastic
blockmodel, which allows for an efficient representation of
the dynamic network.

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
