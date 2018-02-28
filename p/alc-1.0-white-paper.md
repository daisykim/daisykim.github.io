---
layout: default
---

<h1>ALC Specification 1.0</h1>
<b>ALC</b> programming language is a superset of ECMAScript in <a href="http://www.ecma-international.org/ecma-262/5.1/">ECMA-262, edition 5</a>. This supports following additional functions that are similar to <a href="http://en.wikipedia.org/wiki/Logo_(programming_language)">Logo programming language</a>.
<br>
<br>

<h2>Syntax Summary</h2>
<table border=1 width="100%">
<tr align=center>
  <td>Class</td><td>Logo Equivalent<br>(Berkeley Logo)</td>
  <td><b>ALC</b></td><td>Description</td>
</tr>
<tr>
  <td>basic</td>
  <td>to/end (function)</td>
  <td>function() { }</td>
  <td>function definition<br>
    ex) function foo() { fd(5); }
  </td>
</tr>
<tr>
  <td></td>
  <td>repeat {num}[]</td>
  <td>for(init;cond;post) {}</td>
  <td>iteration</td>
</tr>
<tr>
  <td></td>
  <td>make "x sum :y 3</td>
  <td>var x = y + 3;</td>
  <td>variable definition and addtion</td>
</tr>
<tr>
  <td></td>
  <td>if </td>
  <td>if</td>
  <td>conditional statement</td>
</tr>
<tr>
  <td>drawing</td>
  <td>fd {num} or forward </td>
  <td>fd(num) or forward</td>
  <td>draw forward if pen is down</td>
</tr>
<tr>
  <td></td>
  <td>bk {num} or back</td>
  <td>bk(num) or back</td>
  <td>draw backward if pen is down</td>
</tr>
<tr>
  <td></td>
  <td>lt {degree} or left</td>
  <td>lt(degree) or left</td>
  <td>make (degree) left turn</td>
</tr>
<tr>
  <td> </td>
  <td>rt {degree} or right</td>
  <td>rt(degree) or right</td>
  <td>make (degree) right turn</td>
</tr>
<tr>
  <td></td>
  <td> </td>
  <td>up(num)</td>
  <td>draw upward if pen is down</td>
</tr>
<tr>
  <td></td>
  <td> </td>
  <td>dn(num) or down</td>
  <td>draw downward if pen is down</td>
</tr>
<tr>
  <td></td>
  <td> </td>
  <td>rot(degree) or rotation</td>
  <td>rotate turtle to absolute degree</td>
</tr>
<tr>
  <td></td>
  <td>pendown</td>
  <td>pd() or pendown</td>
  <td>pen down</td>
</tr>
<tr>
  <td></td>
  <td>penup</td>
  <td>pu() or penup</td>
  <td>pen up</td>
</tr>
<tr>
  <td></td>
  <td>setpencolor {num}</td>
  <td>sp(num) or setpen</td>
  <td>set the pen color</td>
</tr>
<tr>
  <td></td>
  <td> </td>
  <td>push()</td>
  <td>push current tutle position into the stack</td>
</tr>
<tr>
  <td></td>
  <td> </td>
  <td>pop()</td>
  <td>pop the poistion from the stack and set turtle into that position</td>
</tr>
<tr>
  <td>arithmetic</td>
  <td>sum</td>
  <td>+</td>
  <td></td>
</tr>
<tr>
  <td></td>
  <td>difference</td>
  <td>-</td>
  <td></td>
</tr>
<tr>
  <td></td>
  <td>product</td>
  <td>*</td>
  <td></td>
</tr>
<tr>
  <td></td>
  <td>quotient</td>
  <td>/</td>
  <td></td>
</tr>
<tr>
  <td></td>
  <td>modulo</td>
  <td>%</td>
  <td></td>
</tr>
<tr>
  <td>math</td>
  <td>round {num}</td>
  <td>round(num)</td>
  <td>nearest integer</td>
</tr>
<tr>
  <td></td>
  <td>sqrt {num}</td>
  <td>sqrt(num)</td>
  <td>square root</td>
</tr>
<tr>
  <td></td>
  <td>power {num}</td>
  <td>power(num)</td>
  <td></td>
</tr>
<tr>
  <td></td>
  <td>exp {num}</td>
  <td>exp(num)</td>
  <td>e (2.718281828+)</td>
</tr>
<tr>
  <td></td>
  <td>log10 {num}</td>
  <td>log10(num)</td>
  <td>common logarithm</td>
</tr>
<tr>
  <td></td>
  <td>ln {num}</td>
  <td>ln(num)</td>
  <td>natural logarithm</td>
</tr>
<tr>
  <td></td>
  <td>sin, cos, tan, arctan {num}</td>
  <td>sin(num), cos(num), tan(num), arctan(num)</td>
  <td>triangular function</td>
</tr>
<tr>
  <td></td>
  <td>random start, end</td>
  <td>random(start, end)</td>
  <td>return a random number between 0 (inclusive) and 1 (exclusive)</td>
</tr>
<tr>
  <td></td>
  <td> </td>
  <td>floor</td>
  <td>rounds a number DOWNWARDS to the nearest integer</td>
</tr>
<tr>
  <td></td>
  <td> </td>
  <td>ceil</td>
  <td>rounds a number UPWARDS to the nearest integer</td>
</tr>
<tr>
  <td>predicates</td>
  <td><, >, <=, >=, ==</td>
  <td><, >, <=, >=, ==</td>
  <td>less than, greater than, less than equal, greater than equal, equal</td>
</tr>
<tr>
  <td>bitwise  operations</td>
  <td>BITAND, BITOR, BITNOT, ASHIFT, LSHIFT</td>
  <td>&, |, !, >>, <<</td>
  <td></td>
</tr>
<tr>
  <td>logical operations</td>
  <td>AND, OR, NOT</td>
  <td>&&, ||, !=</td>
  <td></td>
</tr>
</table>
