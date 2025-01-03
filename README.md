# Reals-as-Oracles
This is a project exploring a new definition of real numbers, namely, viewing a real number as an oracle that affirms when a rational interval contains the real number. While that was the initial purpose and remains the primary one, explorations into its generalizations are also being housed in this project. 

The current version of this project has two main (shortish) papers to explain the basic idea. 

The paper that develops the idea from scratch is [Real Numbers as Rational Betweenness Relations](https://github.com/jostylr/Reals-as-Oracles/blob/main/articles/rational-betweenness-relations-oracles.pdf)  It uses rules, called oracles, that given an interval and some fuzziness, return an interval that contains the real number or returns the empty set. It then uses that structure to generate a betweenness relation, nonconstructively. It is established that the oracles form the real numbers. 

The other paper of recent vintage is that using betweenness relations directly and linking them to Dedekind cuts: [Rational Betweenness Relations From Dedekind Cuts](https://github.com/jostylr/Reals-as-Oracles/blob/main/articles/rational-betweenness-relations-dedekind-cuts.pdf)


Another part of this project is the very long paper. It is currently in various stages of readiness. 
This is a version 2 
[Defining Real Numbers as Oracles, v2 alpha](https://github.com/jostylr/Reals-as-Oracles/blob/main/articles/Reals_as_Oracles_v2_alpha.pdf) 

There is also a version 3 being worked on. 


The following papers have been posted to the arXiv and were donish though I consider them outdated at this point. The arXiv versions are provided, but they tend to be older than the primary link which is a link to the pdf hosted in this repository under articles. 

* [Rationally Querying the Reals](https://github.com/jostylr/Reals-as-Oracles/blob/main/articles/reals-as-oracles-teaser.pdf)  This is a very short teaser paper to start with.  [arXiv](https://arxiv.org/abs/2305.00981)
* [Defining Real Numbers as Oracles, an Overview](https://github.com/jostylr/Reals-as-Oracles/blob/main/articles/reals-as-oracles-overview.pdf)  This is an excellent place to start. It gives a basic overview of what this is about and should be quite accessible. [arXiv](https://arxiv.org/abs/2305.04935v1)
* [Defining Real Numbers as Oracles](https://github.com/jostylr/Reals-as-Oracles/blob/main/articles/reals-as-oracles-main.pdf)  This is the main paper and should contain all proofs of all the assertions. While nothing in it is particularly difficult, doing it all out in detail is lengthy. We also discuss with examples some methdos that are strongly suggested by the oracle approach, such as the role of mediants and continued fractions in an intermediate value theorem style approach to generating better interval approximations to real numbers. [arXiv](https://arxiv.org/abs/2305.04935)

The following papers are currently in a partial release and very far from done or reliable:


* [Toplogical Completions with Oracles](https://github.com/jostylr/Reals-as-Oracles/blob/main/articles/reals-as-oracles-metric.pdf) It is not just rational numbers that can be completed. We detail here a number of generalizations, primarily focusing on metric spaces with a nod to other topological spaces. 
* [Linear Structures and Oracles](https://github.com/jostylr/Reals-as-Oracles/blob/main/articles/reals-as-oracles-linear.pdf) This is applying the oracle notion to the the Theory of Linear Structures as developed by Tim Maudlin. Maudlin's idea is to use lines as a basis of topology instead of open sets. This gives us a useful structure of betweenness which the oracle approach should be able to use. 
* [Elementary Analysis with Function Oracles](https://github.com/jostylr/Reals-as-Oracles/blob/main/articles/reals-as-oracles-functions.pdf) We use the notion of oracles as applied to functions to generate a more restrictive class, one which factors in the uncertain nature of the elements in the completed space using oracles. For real oracles, function oracles are oracles on rational rectangles that satisfy similar properties to oracles, but adapted to rectangles. The idea of the rectangle is that it should bound the function over that interval. This leads to functions that are continuous on the irrationals and potentially discontinuous on the rationals. They are integrable. 
* [Rational Mathematics Education](https://github.com/jostylr/Reals-as-Oracles/blob/main/articles/reals-as-oracles-education.pdf) Aspirational at this point, the idea is to explain how best to teach real numbers from an oracle point of view. 

There is also a slideshow presentation: [Introduction to Oracles](https://github.com/jostylr/Reals-as-Oracles/blob/main/articles/reals-as-oracles-slides-intro.pdf) 


## Why

The currently used definition of real numbers have difficulties, many of which are not needed to be. For example, defining a real number as a Cauchy sequence introduces non-uniqueness which leads to defining it as an equivalence class of Cauchy sequences, but this is just a mind-numbingly large and irrelevant object for a real number. 

Infinite decimals are popular conceptions, but it feels as if one ought to write it all out, which is impossible, and doing arithmetic is potentially impossible. As a quick example, try multiplying 1/9 with itself by using the decimal form. Do it out to about 20 places and appreciate what will be happening at the trillionth place. The finite approximations are also unclear as arithmetic approximations tend to lead to larger uncertainties but the typical presentation obscures this. 

Dedkind cuts are not too bad, but there is something abstract and off-putting about them. They also feel less than useful. 

It is hoped that oracles feel less abstract and more to the point. 

## Definition

We consider rational intervals whose endpoints are included. We write a:b to indicate the rational interval bounded by a and b. A singleton is a rational interval where the endpoints are equal. The notion of the delta-spark of c is the closed interval bounded by c-delta and c+delta, namely, c-delta:c+delta. 

An oracle assigns a Yes or No to each rational interval and satisfies the following properties: 

1. Existence. There is a Yes interval.
2. Interval Separation. If you take a Yes interval a:b and a rational c in it and provide a delta > 0, then there exists an interval e:f in the delta-spark of c such that exactly one of a:e, e:f, or f:b is a Yes interval with the others being known to be No. 
3. Consistency. If an interval contains a Yes interval, then it is a Yes interval too. If an interval is contained in a No interval, then it is a No interval.
4. Closed. If the delta spark of c is a Yes interval for all delta>0, then the singleton c:c is a Yes interval. If c:c is a No interval, then there exists a delta>0 such that the delta spark of C is a No interval.

Here are the properties of the original version. These work assuming one can get answers about a singleton, which is not always possible. 

1. Consistency. If an interval contains a Yes interval, then it is a Yes interval too. 
2. Existence. There is a Yes interval. 
3. Interval Separation. If you take a Yes interval and a rational c in it, then either the singleton of c is a Yes or it divides the Yes interval into two intervals for which exactly one of them is a Yes interval. 
4. Rooted. There is at most one rational number c whose singleton is Yes. 
5. Closed. If a rational c is in every Yes interval, then the singleton c is a Yes. 

If the singleton c is a Yes, then the oracle represents the rational number c. 

## What's in the main paper

The paper explores this idea. It establishes a variety of deductions, such as two Yes intervals must intersect and their intersection must be a Yes interval. The paper gives explicit examples such as roots, pi, and e.  In sections 4 and 5, an arithmetic of oracles is defined. Basically, combine the intervals with the arithmetic operations applied to the endpoints. Since we can narrow the input representative intervals, we can get the output as narrowed as we want. The paper then establishes that the oracles are an ordered field with the rationals as a dense sub-field. It also establishes that the oracles are complete in the sense of Cauchy sequences always having limits as well as every set bounded above having a least upper bound. 

There is a little pause after that to explore using mediants to do interval narrowing. Some discussion related to continued fractions and the Stern-Brocot tree are also given. 

The paper then concludes with comparisons to other real number definitions.

## Future directions

In addition to the papers, I am also working on a site for [Rational Mathematics](https://ratmath.com/) and probably companion libraries in JavaScript and Elixir. That's a stretch goal.


