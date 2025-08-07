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


We consider rational intervals whose endpoints are included. We write a:b to indicate the rational interval bounded by a and b. A singleton is a rational interval where the endpoints are equal. The notion of the delta-halo of c is the  interval bounded by c-delta and c+delta, namely, c-delta:c+delta, but NOT including the endpoints. 

The real numnber itself is defined as a rational betweenness relation (RBR). An RBR is a symmetric relation on rational numbers such that it ought to include the real number between them. In what follows, x will represent the relation. So a:x:b is saying that a and b are x-related. This is defining x. If a and b are related by x, then a:b is an x-interval. If a and b are not x-related, then this could be written as ~a:x:b~

An RBR must satisfy the following properties: 
1. Existence. There is an x-interval.
2. Separtion. If a:x:b and c is strictly contained in a:b, then exactly one of the following holds: 1) a:x:c, ~c:x:b~; 2) c:x:c; 3) b:x:c, ~a:x:c~. 
3. Consistency. If a:b contains the x-interval c:d, then a:b is an x-interval.
4. Singular. If c:x:c and d:x:d, then c=d.
5. Closed. If c is contained in every x-interval, then c:c. 

It can be shown that theoretically the relations form the real number field. It is, however, difficult to be precise with real numbers. Thus, the structure that is proposed and relied on the most is that of an oracle. This is a multi-valued function that takes in a rational interval and a rational tolerance delta, asking the question whether the real number is, more or less, in that interval. The more or less is the delta fuzziness. Sometimes the oracle returns an interval. Such an interval is a prophecy and the real number is supposed to be in that interval. The same input could have multiple different outputs. 

This function ought to satisfy the follow properties to be an oracle: 
1. Range. It should return i) (1, c:d), ii) (0, c:d), iii) (0), or iv) (-1) depending on if i) prophecy c:d intersects a:b and is contained in delta-halo of a:b, ii) prophecy c:d is disjoint from a:b, iii) there is a delta' such that i) definitely does not happen, or iv) kind of a null result. Doesn't actually happen but was necessary to avoid hidden assumptions in stating the range.
2. Existence. There exists a:b and delta such that R(a:b, delta) = (1, c:d).
3. Separation. If a:b is a prophecy of R, m is contained in a:b, and delta >0, then one or both of R(a:m, delta) =1 and R(m:b, delta) = 1 holds true.
4. Disjointness. If a:b is disjoint from a prophecy c:d, then delta < (distance between a:b and c:d) implies R(a:b, delta) = 0  (maybe with a returned prophecy, maybe not).
5. Consistency. If a:b contains a prophecy of R, then R(a:b, delta) always returns a 1 with a prophecy.
6. Closed. If for every delta, the delta-halo of a contains a prophecy, then R(a:b, delta) always returns a 1 with a prophecy for all b and delta. The root of the oracle is then a.
7. Reasonableness. Basically, -1 is never returned, but the specific language is that if R(a:b, delta) is not -1 for a small delta, than R(a:b, DELTA) does not return -1 either where DELTA > delta. 

Multiple oracles can represent the same rational betweenness relation. All the standard analysis real number examples can easily be cast into an oracle form. Arithmetic is easy to define for them. They are practical and provide the foundational entry point into working with real numbers. 

## Future directions

In addition to the papers, I am also working on a site for [Rational Mathematics](https://ratmath.com/) and probably companion libraries in JavaScript. That's a stretch goal. 


