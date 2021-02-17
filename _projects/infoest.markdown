---
layout: page
title: Graph Based Estimation of Information Theoretic Quantities
description: 
img: /assets/img/mst_ex.png
importance: 1
---

The estimation of information theoretic quantities is a problem of interest
arising not only in information theory, but also
feature selection, structure estimation for
graphical models, and
training and
understanding deep neural
networks. Common examples of these quantities include
Shannon mutual information and KL divergence. In general, these quantities can be
difficult to compute for continuous random variables, and most methods rely on
an intermediate density estimator
for the underlying distribution. These "plug-in" estimators suffer from bias
near the support boundaries of the marginal densities and can be
computationally prohibitive.  Graph based estimation methods aim to skip the density estimation stage and
directly estimate the quantity of interest by calculating a graph structure over
the data sample. We give two examples from our past work below.

## Estimating Multi-Class Bayes Error Using a Graph Based Estimator 

Past work has used a minimal spanning tree or k-NN graph to estimate information-theoretic quantities of interest. One of the
original algorithms in this area was for the estimation of Henze-Penrose (HP)
divergence, which is a
member of 
the broad class of $$f$$-divergences. This divergence measure
has two important properties. First, it is possible to estimate the HP
divergence directly from a minimal spanning tree across the data sample. As the
minimal spanning tree can be computed in $O(n\log n)$, this approach to
estimation is amenable to large datasets. Second, tight bounds have been proved
that relate the HP divergence to the Bayes error rate of a binary
classification problem. Thus, accurate estimation of the HP divergence allows
for learning of the intrinsic hardness of the supervised learning task. Although tight
bounds exist for the Bayes error rate for a binary classification
task, this is not true for multi-class classification. In our work we derive
tight bounds for the multi-class case using a generalized Henze-Penrose measure,
and provide a graph based estimation procedure using a minimal spanning tree.

<div class="row justify-content-md-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/mst_ex.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    An example of an MST applied to a dataset. The connections in between differently labeled points are counted in order to estimate the Bayes error.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/big_bound_fig.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    The true Bayes error (black) and bounds as a function of a separation parameter for a 3-class classification problem. Our proposed bound (green) is tighter than the other competitors, and this efficiency gap grows as the number of classes increase.
</div>

## Curbing the Curse of Dimensionality with a New Estimator

Like other estimation methods, graph based estimation methods are subject to the
curse of dimensionality. Specifically, as the feature dimension of the data
increases, the bias of the estimate also increases. In recent work, we introduce a new estimator
of the HP divergence, based on a different computed graph, that reduces the bias
for growing dimension.

<div class="row justify-content-md-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="{{ '/assets/img/cross_match.png' | relative_url }}" alt="" title="example image"/>
    </div>
</div>
<div class="caption">
    The optimal weighted matching of a synthetic dataset. We have epirically shown that in certain regimes, this type of graph and correponding cross-match statistic outperforms the traditional Friedman-Rafsky based on a minimal spanning tree (MST).
</div>

## Relevant pubications:
<div class="publications">
  {% bibliography -f papers -q @*[infoest=True] %}
</div>

