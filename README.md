# Reals-as-Oracles
This is a paper for a new definition of real numbers, namely, viewing a real number as an oracle that affirms when a rational interval contains the real number. 

Here is the link to the [PDF](https://github.com/jostylr/Reals-as-Oracles/releases/download/v0.9.0/Reals_as_Oracles.pdf). It is also under releases.

## Why

The currently used definition of real numbers have difficulties, many of which are not needed to be. For example, defining a real number as a Cauchy sequence introduces non-uniqueness which leads to defining it as an equivalence class of Cauchy sequences, but this is just a mind-numbingly large and irrelevant object for a real number. 

Infinite decimals are popular conceptions, but it feels as if one ought to write it all out, which is impossible, and doing arithmetic is potentially impossible. As a quick example, try multiplying 1/9 with itself by using the decimal form. Do it out to about 20 places and appreciate what will be happening at the trillionth place. 

Dedkind cuts are not too bad, but there is something abstract and off-putting about them. 

It is hoped that oracles feel less abstract and more to the point. 

## Definition

We consider closed intervals whose endpoints are rationals. A singleton is a rational interval where the endpoints are equal. 

An oracle assigns a Yes or No to each rational interval and satisfies the following properties: 

1. Consistency. If an interval contains a Yes interval, then it is a Yes interval too. 
2. Existence. There is a Yes interval. 
3. Interval Separation. If you take a Yes interval and a rational c in it, then either the singleton of c is a Yes or it divides the Yes interval into two intervals for which exactly one of them is a Yes interval. 
4. Rooted. There is at most one rational number c whose singleton is Yes. 
5. Closed. If a rational c is in every Yes interval, then the singleton c is a Yes. 

If the singleton c is a Yes, then the oracle represents the rational number c. 

## What's in the paper

The paper explores this idea. It establishes a variety of deductions, such as two Yes intervals must intersect and their intersection must be a Yes interval. The paper gives explicit examples such as roots, pi, and e.  In sections 4 and 5, an arithmetic of oracles is defined. Basically, combine the intervals with the arithmetic operations applied to the endpoints. Since we can narrow the input representative intervals, we can get the output as narrowed as we want. The paper then establishes that the oracles are an ordered field with the rationals as a dense sub-field. It also establishes that the oracles are complete in the sense of Cauchy sequences always having limits as well as every set bounded above having a least upper bound. 

There is a little pause after that to explore using mediants to do interval narrowing. Some discussion related to continued fractions and the Stern-Brocot tree are also given. 

After that interlude, the paper then gives a new definition of functions based on oracles. Basically, functions are oracles on rational rectangles that satisfy similar properties to oracles, but adapted to rectangles. The idea of the rectangle is that it should bound the function over that interval. This leads to functions that are continuous on the rationals and potentially discontinuous on the rationals. They are integrable. 

The paper then concludes with comparisons to other real number definitions as well as a generalization to how to complete metric spaces where the interval separation is replaced with being able to separate two points and intervals are replaced with closed balls. 

## Future directions

Hopefully, the paper can get peer reviewed and possibly published. There is also an education flavored version being worked on. Finally, I am toying with the idea of making a site to do these calculations as well as a series of videos going into depth about what is in the paper. 
