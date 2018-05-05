---
title: ALC White Paper
layout: default
---

# [](#header-1)ALC White Paper

_ALC_ is a programming language which is a superset of ECMAScript in [ECMA-262, edition 5](http://www.ecma-international.org/ecma-262/5.1/).
This supports following additional syntax that is similar to [Logo programming language](http://en.wikipedia.org/wiki/Logo_(programming_language)).
Current _ALC_ edition is 1.0.

## [](#header-2)Syntax Summary

| Logo | ALC | Description |
|:---|:---|:---|
| to/end (function)    | function() { }       | function definition ex) function foo() { fd(5); }|
| {num}[]              | repeat(num, function(repcount) { }) | iteration|
| make “x sum :y 3     | var x = y + 3;       | variable definition and addtion|
| if                   | if                   | conditional statement|
| fd {num} or forward  | fd(num) or forward   | draw forward if pen is down|
| bk {num} or back     | bk(num) or back      | draw backward if pen is down|
| lt {degree} or left  | lt(degree) or left   | make (degree) left turn|
| rt {degree} or right | rt(degree) or right  | make (degree) right turn|
|                      |up(num)              | draw upward if pen is down|
|                      | dn(num) or down      | draw downward if pen is down|
|                      | rot(degree) or rotation| rotate turtle to absolute degree|
| pendown              | pd() or pendown      | pen down|
| penup                | pu() or penup        | pen up|
| setpencolor {num}    | sp(num) or setpen    | set the pen color|
|                      | push()               | push current tutle position into the stack|
|                      | pop()                | pop the poistion from the stack and set turtle into that position|
| sum                  | +                    |   |
| difference           | -                    |   |
| product              | \*                   |   |
| quotient             | /                    |   |
| modulo               | %                    |   |
| round {num}          | round(num)           | nearest integer|
| sqrt {num}           | sqrt(num)            | square root|
| power {num}          | power(num)           | power  |
| exp {num}            | exp(num)             | e (2.718281828+)|
| log10 {num}          | log10(num)           | common logarithm|
| ln {num}             | ln(num)              | natural logarithm|
| sin, cos, tan, arctan {num}| sin(num), cos(num), tan(num), arctan(num)| triangular function|
| random start, end    | random(start, end)   | return a random number between 0 (inclusive) and 1 (exclusive)|
|                      | floor                | rounds a number DOWNWARDS to the nearest integer|
|                      | ceil                 | rounds a number UPWARDS to the nearest integer|
| <, >, <=, >=, ==     | <, >, <=, >=, ==     |   less than, greater than, less than equal, greater than equal, equal|
| BITAND, BITOR, BITNOT, ASHIFT, LSHIFT|  &, \|, !, », « |   |
| AND, OR, NOT   | &&, \|\|, !=         |   |
{:.mbtablestyle}

## [](#header-2)Examples

```js
// Pyramid
function sq(len) {
  for (var i = 0; i < 4; ++i) {
    fd(len-1); rt(90);
  }
}

sp(21); rot(0);

for (var i = 18; i >= 0; i-=2) {
 pd(); sq(i); pu();

  up(1);fd(1);rt(90);fd(1);lt(90);pd();
}
```

```js
// Simple circle
var circle = function() {
    for (var i = 0; i < 90; ++i) {
          fd(1);
          rt(4);
    }
}

sp(4); rot(0);
circle();
```
## [](#header-2)Execution Model

Applications written in _ALC_ run on a web browser or node.js.
Since there is a single thread of execution, an _ALC_ function continues executing until it exits.  _ALC_ functions can't be interruted by other _ALC_ code.

## [](#header-2)Libraries

Followings are built-in libraries:

* Event loop and handler callback
* 3D graphics
* Networking
* Voxel handling
* User controls and related GUI
* DOM and CSS handling
* Package and plugin management
* Debugging and logging
* Cloud based data saving and loading
* Monetization
* Test automation


For further details, please refer to wiki sidemenu.
