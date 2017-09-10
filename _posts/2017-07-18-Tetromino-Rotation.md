---
layout: default
title:  "Easy Tetromino Rotation"
date:   14-7-2017
categories: algorithm programming
excerpt: By representing a tetromino in the minimum sized matrix it is possible to obtain clockwise and counter-clockwise 90 degrees rotations very easily in two simple steps. 
---

{{page.title}}
================

By representing a tetromino in the minimum sized matrix it is possible to obtain clockwise and counter-clockwise 90 degrees rotations very easily in two simple steps. 

### Representation

Represent each piece in the minimum sized matrix where 1's represent spaces occupied by the tetriminoe and 0's represent empty space. Example:

<pre><code>originalMatrix = 
[0,   0,   <b>1</b>]
[<b>1</b>,   <b>1</b>,   <b>1</b>]</code></pre>
    

### Rotation Formula

    clockwise90DegreesRotatedMatrix = reverseTheOrderOfColumns(Transpose(originalMatrix))

    anticlockwise90DegreesRotatedMatrix = reverseTheOrderOfRows(Transpose(originalMatrix))


### Illustration

<pre><code>originalMatrix = 
  x    y    z
a[0,   0,   <b>1</b>]
b[<b>1</b>,   <b>1</b>,   <b>1</b>]</code></pre>   

<pre><code>transposed = transpose(originalMatrix)
  a   b
x[0,  <b>1</b>]
y[0,  <b>1</b>]
z[<b>1</b>,  <b>1</b>] </code></pre>

<pre><code>counterClockwise90DegreesRotated = reverseTheOrderOfRows(transposed)
  a   b
z[<b>1</b>,  <b>1</b>]
y[0,  <b>1</b>]
x[0,  <b>1</b>] </code></pre>


<pre><code>clockwise90DegreesRotated = reverseTheOrderOfColumns(transposed)
  b   a
x[<b>1</b>,  0]
y[<b>1</b>,  0]
z[<b>1</b>,  <b>1</b>] </code></pre>

