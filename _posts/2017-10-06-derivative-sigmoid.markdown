---
layout: post
title:  "Derivative of Sigmoid"
date:   2017-10-06
categories: math
excerpt: Ever wanted to find the derivative of 'sigma'. Yeah...me neither! But sometimes ya got to do some down and dirty math to wrap your head around some machine-learning courses. This is one such example.
image: /assets/images/math-art.jpg
tags: 
  - Math
  - Machine Learning
---
In exploring machine learning, its common to come across an _activation function_ called Sigmoid \\( \sigma \\). It's a good idea to [wrap your head around it](https://en.wikipedia.org/wiki/Sigmoid_function). But in its basic form:

\\[ \sigma = \dfrac {1} {1+e^{-x}} \label{a} \tag{1} \\]

I might write a post listing various other activation functions, and maybe describing the purpose of an activation function. But today let's talk about the Derivative of Sigmoid, \\( \sigma' \\). Function like \\( \sigma' \\) are important to keep handy while performing learning by [Gradient Descent](https://en.wikipedia.org/wiki/Gradient_descent) (but more on that in another post). Now by definition:

\\[ \sigma' =  \dfrac {d \sigma} {dx} \\]

Using [derivative of quotient](https://en.wikipedia.org/wiki/Quotient_rule): if \\( y = \dfrac {u} {v} \\), \\( y' = \dfrac {vu' - uv'} {v^{2}} \\). \\( \sigma \\) can be represented as: \\( \sigma =  \dfrac {u} {v} \\) where \\( u=1; v=1+e^{-x} \\).

\\[ \Rightarrow \sigma' = \dfrac {vu' - uv'} {v^{2}} \\]
\\[ = \dfrac {(1+e^{-x}) \cdot \dfrac {d}{dx}1 - 1 \cdot \dfrac {d}{dx}(1+e^{-x})} {(1+e^{-x})^2} \\]
<br/>
<br/>
Now, \\( \dfrac{d}{dx}(1+e^{-x}) = \dfrac{d}{dx}1 + \dfrac{d}{dx}(e^{-x}) = 0 + -e^{-x} = -e^{-x} \\), using [derivative of exponential](https://en.wikipedia.org/wiki/Differentiation_rules#Derivatives_of_exponential_and_logarithmic_functions), and since \\( \dfrac {d}{dx}1 = 0 \\).

\\[ \Rightarrow \sigma' = \dfrac {0 - (-e^{-x})} {(1+e^{-x})^2} \\]
\\[ = \dfrac {e^{-x}} {(1+e^{-x})^2} \\]
\\[ = \dfrac {1+e^{-x}-1} {(1+e^{-x})^2} \\]
\\[ = \dfrac {1}{1+e^{-x}} \cdot \dfrac {(1+e^{-x})-1} {1+e^{-x}} \\]
\\[ = \dfrac {1}{1+e^{-x}} \cdot (1 - \dfrac {1} {1+e^{-x}}) \\]
<br/>
<br/>
Hence, using (\\( \ref{a} \\)), the Derivative of Sigmoid can be represented as:

\\[ \boxed{ \sigma' = \sigma(1-\sigma) } \tag{2}\\]
<br/>
<br/>
This is my first post in a series of machine learning-related posts. I am starting with explaining the basics first (especially the math behind the basics) because sometimes it's the basic concepts that get lost.
