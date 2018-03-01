---
layout: default
---

# [](#header-1)ALC White Paper (v0.1)
ALC programming language is a superset of ECMAScript in [ECMA-262, edition 5](http://www.ecma-international.org/ecma-262/5.1/). This supports following additional functions that are similar to [Logo programming language](http://en.wikipedia.org/wiki/Logo_(programming_language))

## [](#header-2)Syntax Summary

<table>
<colgroup>
<col width="10%" />
<col width="25%" />
<col width="25%" />
<col width="40%" />
</colgroup>
<thread>
<tr class="header">
  <th>Class</th>
  <th>Logo Equivalent<br>(Berkeley Logo)</th>
  <th>ALC</th>
  <th>Description</th>
</tr>
</thread>
<tbody>
<tr>
  <td markdown="span">basic</td>
  <td markdown="span">to/end (function)</td>
  <td markdown="span">function() { }</td>
  <td markdown="span">function definition<br>
    ex) function foo() { fd(5); }
  </td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">repeat {num}[]</td>
  <td markdown="span">for(init;cond;post) {}</td>
  <td markdown="span">iteration</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">make "x sum :y 3</td>
  <td markdown="span">var x = y + 3;</td>
  <td markdown="span">variable definition and addtion</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">if </td>
  <td markdown="span">if</td>
  <td markdown="span">conditional statement</td>
</tr>
<tr>
  <td markdown="span">drawing</td>
  <td markdown="span">fd {num} or forward </td>
  <td markdown="span">fd(num) or forward</td>
  <td markdown="span">draw forward if pen is down</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">bk {num} or back</td>
  <td markdown="span">bk(num) or back</td>
  <td markdown="span">draw backward if pen is down</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">lt {degree} or left</td>
  <td markdown="span">lt(degree) or left</td>
  <td markdown="span">make (degree) left turn</td>
</tr>
<tr>
  <td markdown="span"> </td>
  <td markdown="span">rt {degree} or right</td>
  <td markdown="span">rt(degree) or right</td>
  <td markdown="span">make (degree) right turn</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span"> </td>
  <td markdown="span">up(num)</td>
  <td markdown="span">draw upward if pen is down</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span"> </td>
  <td markdown="span">dn(num) or down</td>
  <td markdown="span">draw downward if pen is down</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span"> </td>
  <td markdown="span">rot(degree) or rotation</td>
  <td markdown="span">rotate turtle to absolute degree</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">pendown</td>
  <td markdown="span">pd() or pendown</td>
  <td markdown="span">pen down</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">penup</td>
  <td markdown="span">pu() or penup</td>
  <td markdown="span">pen up</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">setpencolor {num}</td>
  <td markdown="span">sp(num) or setpen</td>
  <td markdown="span">set the pen color</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span"> </td>
  <td markdown="span">push()</td>
  <td markdown="span">push current tutle position into the stack</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span"> </td>
  <td markdown="span">pop()</td>
  <td markdown="span">pop the poistion from the stack and set turtle into that position</td>
</tr>
<tr>
  <td markdown="span">arithmetic</td>
  <td markdown="span">sum</td>
  <td markdown="span">+</td>
  <td markdown="span"></td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">difference</td>
  <td markdown="span">-</td>
  <td markdown="span"></td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">product</td>
  <td markdown="span">\*</td>
  <td markdown="span"></td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">quotient</td>
  <td markdown="span">/</td>
  <td markdown="span"></td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">modulo</td>
  <td markdown="span">%</td>
  <td markdown="span"></td>
</tr>
<tr>
  <td markdown="span">math</td>
  <td markdown="span">round {num}</td>
  <td markdown="span">round(num)</td>
  <td markdown="span">nearest integer</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">sqrt {num}</td>
  <td markdown="span">sqrt(num)</td>
  <td markdown="span">square root</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">power {num}</td>
  <td markdown="span">power(num)</td>
  <td markdown="span"></td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">exp {num}</td>
  <td markdown="span">exp(num)</td>
  <td markdown="span">e (2.718281828+)</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">log10 {num}</td>
  <td markdown="span">log10(num)</td>
  <td markdown="span">common logarithm</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">ln {num}</td>
  <td markdown="span">ln(num)</td>
  <td markdown="span">natural logarithm</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">sin, cos, tan, arctan {num}</td>
  <td markdown="span">sin(num), cos(num), tan(num), arctan(num)</td>
  <td markdown="span">triangular function</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span">random start, end</td>
  <td markdown="span">random(start, end)</td>
  <td markdown="span">return a random number between 0 (inclusive) and 1 (exclusive)</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span"> </td>
  <td markdown="span">floor</td>
  <td markdown="span">rounds a number DOWNWARDS to the nearest integer</td>
</tr>
<tr>
  <td markdown="span"></td>
  <td markdown="span"> </td>
  <td markdown="span">ceil</td>
  <td markdown="span">rounds a number UPWARDS to the nearest integer</td>
</tr>
<tr>
  <td markdown="span">predicates</td>
  <td markdown="span"><, >, <=, >=, ==</td>
  <td markdown="span"><, >, <=, >=, ==</td>
  <td markdown="span">less than, greater than, less than equal, greater than equal, equal</td>
</tr>
<tr>
  <td markdown="span">bitwise  operations</td>
  <td markdown="span">BITAND, BITOR, BITNOT, ASHIFT, LSHIFT</td>
  <td markdown="span">&, |, !, >>, <<</td>
  <td markdown="span"></td>
</tr>
<tr>
  <td markdown="span">logical operations</td>
  <td markdown="span">AND, OR, NOT</td>
  <td markdown="span">&&, ||, !=</td>
  <td markdown="span"></td>
</tr>
</tbody>
</table>
