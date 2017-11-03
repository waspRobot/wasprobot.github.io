---
layout: post
title:  "Number Series Reduction"
date:   2017-11-02
categories: math
excerpt: ---
---
### Troubled childhood
Since I was a child, I have been fond of solving number-series. You know, the kind where you find the "next 3 numbers in the series". A simple example being the \\( x^2 \\) series:

\\[(1, 4, 9, 16, ...)\tag{1}\\\]

[I will assume for the rest of the article, that x is a positive integer, starting at 1.]

Now that series was easy to eyeball, and you could come up with the next 3 numbers (\\(25, 36, 49\\) in case you are still scratching your head). One would argue that a simple \\(x^4\\) or even something like \\(3x + 5\\) would be relatively easier on the eye:

\\[(8, 11, 14, 17, ...)\\]

So, through my middle-school years, I breezed through those easy ones without thinking. Trouble began when I started seeing something like:

\\((-2, 42, 152, 358, 690, ...) \tag{2}\\)

How do you eyeball anything like that? Where do you even begin?

### Reduce that series (break-down!)
For the easier series, one of the tricks I had learned was to **find the difference in the consecutive numbers** and try to find a pattern. For example, in case of (1: square-series) above, the *reduced series* (as I call it) becomes:
<br/>
<table align="center">
<tr>
<td colspan="2">1</td>
<td colspan="2">4</td>
<td colspan="2">4</td>
<td colspan="2">16</td>
<td colspan="2" class="extend">25</td>
<td colspan="2" class="extend">36</td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td colspan="2">3</td>
<td colspan="2">5</td>
<td colspan="2">7</td>
<td colspan="2" class="extend" colspan="2">9</td>
<td colspan="2" class="extend" colspan="2">11</td>
<td class="corner-right-bottom"></td>
</tr>
</table>
<br/>

You can see the pattern here (these are the *positive odd integers*)

### Reduce the reduction??
Wait! But how do the *positive odd integers* progress? Well, on closer look, you actually reduce *that* series (in your head) to find the next numbers (Remember the "count by 2?" Notice the last 2 rows below):
<br/>
<table align="center">
<tr>
<td colspan="2">1</td>
<td colspan="2">4</td>
<td colspan="2">4</td>
<td colspan="2">16</td>
<td colspan="2" class="extend">25</td>
<td colspan="2" class="extend">36</td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td colspan="2">3</td>
<td colspan="2">5</td>
<td colspan="2">7</td>
<td colspan="2" class="extend" colspan="2">9</td>
<td colspan="2" class="extend" colspan="2">11</td>
<td class="corner-right-bottom"></td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td colspan="2">2</td>
<td colspan="2">2</td>
<td colspan="2" class="extend" colspan="2">2</td>
<td colspan="2" class="extend" colspan="2">2</td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
</tr>
</table>
<br/>

Phew! Boy, that was **a lot** of reduction!! Does this mean we can apply this pattern to our **(2: monster-series)** above? Here it is:
<br/>
<table align="center">
<tr>
<td colspan="2">-2</td>
<td colspan="2">42</td>
<td colspan="2">152</td>
<td colspan="2">358</td>
<td colspan="2">690</td>
</tr>
</table>
<br/>

#### Reduction #1
Derive the next layer:
<br/>
<table align="center">
<tr>
<td colspan="2">-2</td>
<td colspan="2">42</td>
<td colspan="2">152</td>
<td colspan="2">358</td>
<td colspan="2">690</td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td colspan="2">44</td>
<td colspan="2">110</td>
<td colspan="2">206</td>
<td colspan="2">332</td>
<td class="corner-right-bottom"></td>
</tr>
</table>
<br/>

#### Reduction #2
And the next:
<br/>
<table align="center">
<tr>
<td colspan="2">-2</td>
<td colspan="2">42</td>
<td colspan="2">152</td>
<td colspan="2">358</td>
<td colspan="2">690</td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td colspan="2">44</td>
<td colspan="2">110</td>
<td colspan="2">206</td>
<td colspan="2">332</td>
<td class="corner-right-bottom"></td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td colspan="2">66</td>
<td colspan="2">96</td>
<td colspan="2">126</td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
</tr>
</table>
<br/>

#### Reduction #3
And finally:
<br/>
<table align="center">
<tr>
<td colspan="2">-2</td>
<td colspan="2">42</td>
<td colspan="2">152</td>
<td colspan="2">358</td>
<td colspan="2">690</td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td colspan="2">44</td>
<td colspan="2">110</td>
<td colspan="2">206</td>
<td colspan="2">332</td>
<td class="corner-right-bottom"></td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td colspan="2">66</td>
<td colspan="2">96</td>
<td colspan="2">126</td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td colspan="2" class="interesting">30</td>
<td colspan="2" class="interesting">30</td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
</tr>
</table>
<br/>

Hey! I see the pattern! The 3<sup>rd</sup> reduction was easy - the numbers are all \\(30\\) apart.

### Extend the series (build-up!)
Let's apply that \\(30\\) to develop the bottom-most layer first:

#### Extension #1
<br/>
<table align="center">
<tr>
<td colspan="2">-2</td>
<td colspan="2">42</td>
<td colspan="2">152</td>
<td colspan="2">358</td>
<td colspan="2">690</td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td colspan="2">44</td>
<td colspan="2">110</td>
<td colspan="2">206</td>
<td colspan="2">332</td>
<td class="corner-right-bottom"></td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td colspan="2">66</td>
<td colspan="2">96</td>
<td colspan="2">126</td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td colspan="2">30</td>
<td colspan="2">30</td>
<td colspan="2" class="extend">30</td>
<td colspan="2" class="extend">30</td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
</tr>
</table>
<br/>

#### Extension #2
Make-up the layer next-up, by adding \\(30\\) to the known-values:
<br/>
<table align="center">
<tr>
<td colspan="2">-2</td>
<td colspan="2">42</td>
<td colspan="2">152</td>
<td colspan="2">358</td>
<td colspan="2">690</td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td colspan="2">44</td>
<td colspan="2">110</td>
<td colspan="2">206</td>
<td colspan="2">332</td>
<td class="corner-right-bottom"></td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td colspan="2">66</td>
<td colspan="2">96</td>
<td colspan="2">126</td>
<td colspan="2" class="extend">156</td>
<td colspan="2" class="extend">186</td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td colspan="2">30</td>
<td colspan="2">30</td>
<td colspan="2" class="extend">30</td>
<td colspan="2" class="extend">30</td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
</tr>
</table>
<br/>

#### Extension #3
Make-up the layer above that! Why not?!
<br/>
<table align="center">
<tr>
<td colspan="2">-2</td>
<td colspan="2">42</td>
<td colspan="2">152</td>
<td colspan="2">358</td>
<td colspan="2">690</td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td colspan="2">44</td>
<td colspan="2">110</td>
<td colspan="2">206</td>
<td colspan="2">332</td>
<td colspan="2" class="extend">488</td>
<td colspan="2" class="extend">674</td>
<td class="corner-right-bottom"></td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td colspan="2">66</td>
<td colspan="2">96</td>
<td colspan="2">126</td>
<td colspan="2" class="extend">156</td>
<td colspan="2" class="extend">186</td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td colspan="2">30</td>
<td colspan="2">30</td>
<td colspan="2" class="extend">30</td>
<td colspan="2" class="extend">30</td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
</tr>
</table>
<br/>

#### Extension #4
Keep going!:
<br/>
<table align="center">
<tr>
<td colspan="2">-2</td>
<td colspan="2">42</td>
<td colspan="2">152</td>
<td colspan="2">358</td>
<td colspan="2">690</td>
<td colspan="2" class="extend interesting">1178</td>
<td colspan="2" class="extend interesting">1852</td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td colspan="2">44</td>
<td colspan="2">110</td>
<td colspan="2">206</td>
<td colspan="2">332</td>
<td colspan="2" class="extend">488</td>
<td colspan="2" class="extend">674</td>
<td class="corner-right-bottom"></td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td colspan="2">66</td>
<td colspan="2">96</td>
<td colspan="2">126</td>
<td colspan="2" class="extend">156</td>
<td colspan="2" class="extend">186</td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
</tr>
<tr>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td class="corner-left-bottom"></td>
<td colspan="2">30</td>
<td colspan="2">30</td>
<td colspan="2" class="extend">30</td>
<td colspan="2" class="extend">30</td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
<td class="corner-right-bottom"></td>
</tr>
</table>
<br/>

Do you see what I see?! We have **2 new numbers** in our *monster-series*!

### Test!
The proof that the 2 new numbers are it? Well, we have to ask the creator of the series (*that's Yours Truly*). So full disclosure: I had used the following polynomial for this series:
\\[f(x)=5x^3+3x^2-10\\]

And sure enough, for \\(x=6\\) and \\(x=7\\) the values of \\(f(x)\\) are:

\\[f(6) = 1178\\]

\\[f(7) = 1852\\]

### Properties of reduction
One of the properties of the reduction method I have come across (that my colleague, Nick Hill, helped come up with) is the magic number:
<br/>
<table align="center">
<tr>
<td class="interesting">30</td>
</tr>
</table>
<br/>

There's little magical about this number. You can arrive at it by repeatedly differentiating the *monster-function* w.r.t \\(dx\\):

\\[\dfrac {d}{dx} (5x^3+3x^2-10) = 15x^2 + 6x\\]
\\[\dfrac {d}{dx} (15x^2 + 6x) = 30x + 6\\]
and finally:
\\[\dfrac {d}{dx} (30x + 6) = 30\\]
