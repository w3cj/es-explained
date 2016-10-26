
#### To view this as a slide deck:

`npm install -g reveal-md`

`npm start`

---

# [es-explained]()

## ECMAScript, TC39 and The Future of JavaScript

#### hello@cjr.co.de
#### CJ on Denver Devs

---

<!-- https://flixels.s3.amazonaws.com/flixel/de6w5hh1ijhzux3c3pah.webm -->

<!-- .slide: data-background-video="https://flixels.s3.amazonaws.com/flixel/ypy8bw9fgw1zv2b4htp2.webm" data-background-video-loop="loop" data-background-video-muted -->

## Agenda

* whoami
* The History of JavaScript
* TC39 Process
* `es-next`

---

<!-- .slide: data-background-video="https://flixels.s3.amazonaws.com/flixel/52vy4yxt8yw76d2u8dsm.webm" data-background-video-loop="loop" data-background-video-muted -->

# `whoami`

----

<!-- .slide: data-background="http://galvanize-wp.s3.amazonaws.com/wp-content/uploads/2016/09/14143218/Platte-Oct-2015-4593-min.jpg"  -->

<div style="background: rgba(0, 0, 0, 0.4);border-radius: 50px">
  <h1>CJ</h1>
  <h3>Instructor, Sr. Full Stack Developer</h3>
  <h2>at</h2>
  <img src="http://www.galvanize.com/wp-content/themes/galvanize/img/galvanize-logo.svg" style="height:100px;width:auto;border:none;background:rgba(0, 0, 0, 0)">
</div>

---

# The History of JavaScript

----

## 1995: JavaScript Beginngings

* May - [Brendan Eich](https://brendaneich.com/2008/04/popularity/) is recruited by Netscape to create "Scheme in the Browser"
  * Developed in 10 Days under the code name "Mocha"
* September - "LiveScript" ships with Netscape Navigator 2.0 beta
* December - Renamed to "JavaScript", ships with Netscape Navigator 2.0 beta 3

<img style="border:none;" src="https://upload.wikimedia.org/wikipedia/commons/6/69/Netscape_Navigator_2_Screenshot.png" />

----

## Java !== JavaScript

* Netscape partnered with Sun to ride the momentum of the Java language
  * [Press Release from December 4 1995](https://web.archive.org/web/20070916144913/http://wp.netscape.com/newsref/pr/newsrelease67.html)

![](https://coderanch.com/t/456377/a/401/javascript-java.jpg)

[Comic via coderanch.com](https://coderanch.com)

----

### Early Browser Wars

<img style="display:inline" src="http://www.guidebookgallery.org/pics/splashes/netscape/2.0.png"/>
#### vs
<img style="display:inline"  src="http://www.wincons.or.jp/view/vol25/data/ie3logo.gif"/>

----

### August 1996: Microsoft reverse engineers JavaScript for IE 3

* Named JScript to prevent lawsuit

<img style="border:none;" src="http://www.donmouth.co.uk/web_design/browsermuseum/images/ie3_screen.jpg" />

[via Wikipedia](https://en.wikipedia.org/wiki/JScript)

----

## Standardization: ECMA-262

* November 1996: Netscape delivers JavaScript to ECMA International for standardization
* June 1997: The first edition of ECMA-262 was adopted by the ECMA General Assembly
*  The name "ECMAScript" was a compromise, Brendan Eich says it "sounds like a skin disease"

[via Wikipedia](https://en.wikipedia.org/wiki/ECMAScript)

[ECMAScript 1st Edition PDF](http://www.ecma-international.org/publications/files/ECMA-ST-ARCH/ECMA-262,%201st%20edition,%20June%201997.pdf)

<img style="border:none;height:300px;width:auto;" src="http://i.imgur.com/Shf7ZbG.png" />

----

### JavaScript 1.1: Netscape Navigator 3.0

* Any JavaScript error would open a pop-up.
* The Number constructor would throw if the parameter could not be converted successfully

```js
Number('some string');
```

* If at least one of the operands of the equals operator was Boolean, undefined or Number it will then coerse both operands to Number.

```js
if(new Object() == false) {}
```

<img style="border:none;height:200px;" src="https://s3.amazonaws.com/media-p.slid.es/uploads/58780/images/2470478/object-is-not-a-number.png" />

----

### Continued: JavaScript 1.1: Netscape Navigator 3.0

* The reference to the value `undefined` was not present.

<img style="border:none;height:200px;" src="https://s3.amazonaws.com/media-p.slid.es/uploads/58780/images/2474697/undefined-is-not-defined.png" />

[undefined appeard in JS 1.3](https://developer.mozilla.org/en-US/docs/Web/JavaScript/New_in_JavaScript/1.3)

[undefined polyfill on github](https://github.com/a0viedo/undefined)

[Notes on explicit JavaScript versioning](https://developer.mozilla.org/en-US/docs/Web/JavaScript/New_in_JavaScript#JavaScript_versions)

----

### June 1998: ECMAScript 2nd Edition

Added 40 future reserved words (38 are also a Java keyword).

<table><tbody>
<tr>
<td>abstract</td>
<td>do</td>
<td>import</td>
<td>short</td>
</tr>
<tr>
<td>boolean</td>
<td>double</td>
<td>instanceof</td>
<td>static</td>
</tr>
<tr>
<td>byte</td>
<td>enum</td>
<td>int</td>
<td>super</td>
</tr>
<tr>
<td>case</td>
<td>export</td>
<td>interface</td>
<td>switch</td>
</tr>
<tr>
<td>catch</td>
<td>extends</td>
<td>long</td>
<td>synchronized</td>
</tr>
<tr>
<td>char</td>
<td>final</td>
<td>native</td>
<td>throw</td>
</tr>
<tr>
<td>class</td>
<td>finally</td>
<td>package</td>
<td>throws</td>
</tr>
<tr>
<td>const</td>
<td>float</td>
<td>private</td>
<td>transient</td>
</tr>
<tr>
<td>debugger</td>
<td>goto</td>
<td>protected</td>
<td>try</td>
</tr>
<tr>
<td>default</td>
<td>implements</td>
<td>public</td>
<td>volatile</td>
</tr>
</tbody></table>

----

### December 1999: ECMAScript 3rd Edition

Introduced:
* try/catch
* strict comparison
* instanceof
* fn.apply
* switch
* function expressions
* Array helpers (push, pop ,slice, concat, etc)
* Regular expressions

----

<!-- .slide: data-background="http://i.imgur.com/JWj54QI.jpg" -->

----

### OK.... 7 years later

----

### 2007: ECMAScript 4th Edition

* Abandoned in 2008

<img style="border:none;height:150px;" src="http://www.threadbombing.com/data/media/29/AbandonThread.gif"/>

* There were a lot of very strong opinions about how to move JavaScript forward, many of which were incompatible, some of which had mostly assembled what they thought would be the 4th edition before things fell apart

>"ES4 was so large and so innovative that there were doubts about whether it could be successfully specified and implemented." -Douglas Crockford

----

### August 2008: Brendan Eich proposes "Harmony" Process

<img style="border:none;background:none;height:100px;" src="http://sweetclipart.com/multisite/sweetclipart/files/nature_weather_rainbow_arc_2.png" />

1. Focus work on ES3.1 with full collaboration of all parties
2. Collaborate on the next step beyond ES3.1
3. Some ES4 proposals have been deemed unsound for the Web, and are off the table for good: packages, namespaces and early binding. This conclusion is key to Harmony.
4. Other goals and ideas from ES4 are being rephrased to keep  
consensus in the committee.

[Brendan Eich: ES Harmony](https://mail.mozilla.org/pipermail/es-discuss/2008-August/003400.html)

----

### December 2009: ECMAScript 5th Edition

* strict mode
* getters and setters
* Higher order array methods (forEach, map, reduce, etc)
* JSON
* Object.seal and Object.freeze
* immutable undefined

Before ES5:

```js
undefined=1;
alert(undefined == 1); // true
```

----

### June 2011: ECMAScript 5.1 edition

* A revision of 5.0 that corrects some errors in the document itself.

>The ISO edition of the ES5 specification incorporates a number of editorial and technical corrections including those listed in the current ES5 errata.

>It contains no new language or library features. TC39 is continuing its longer term work on “ECMAScript Harmony” which is intended to be the next version to include any new features.

[Announcing ECMAScript 5.1](http://www.wirfs-brock.com/allen/posts/39)

----

## June 2015: ECMAScript 2015 (6th Edition)

Official goals: a better language for
* applications
* libraries
* code generators

----

## June 2015: ECMAScript 2015 (6th Edition)

* Classes
* Arrow functions
* Iterators (and generators)
* Proxies
* Destructuring
* let and const
* and much much more

----

## June 2016: ECMAScript 2016 (7th Edition)

----

### ECMAScript at a glance

* June 1997 - ES1
* June 1998 - ES2
* December 1999 - ES3

10 Years Go By

* December 2009 - ES5
* December 2011 - ES5.1

4 Years Go By

* June 2015 - ES2015 (6)
* June 2016 - ES2016 (7)

---

# TC39

----

## Technical Committee 39

[https://github.com/hemanth/tc39-members](https://github.com/hemanth/tc39-members)

[TC39 Org on Github!](https://github.com/tc39)

[TC39 Meeting Notes](https://github.com/rwaldron/tc39-notes)

[ESDiscuss](https://esdiscuss.org/)

----

# The TC39 Process

----

>The Ecma TC39 committee is responsible for evolving the ECMAScript programming language and authoring the specification. The committee operates by consensus and has discretion to alter the specification as it sees fit. However, the general process for making changes to the specification is as follows.

[https://tc39.github.io/process-document/](https://tc39.github.io/process-document/)


----

## Stage 0: Strawman
## Stage 1: Proposal
## Stage 2: Draft
## Stage 3: Candidate
## Stage 4: Finished

[Stage 0 Proposals](https://github.com/tc39/proposals/blob/master/stage-0-proposals.md)

[Finished Proposals](https://github.com/tc39/proposals/blob/master/finished-proposals.md)

---

# [es-next](https://github.com/hemanth/es-next)

----

## You may be asking...

----

## How can I try these new features if browsers haven't implemented them yet??

----

# [Babel JS](https://babeljs.io/)

----

## [Kangax Compat Table](http://kangax.github.io/compat-table/es6/)

---

## Resources

* [Browser Museum](http://www.donmouth.co.uk/web_design/browsermuseum/browsermuseum.html)
* [Netscape Navigator on Wikipedia](https://en.wikipedia.org/wiki/Netscape_Navigator_2)
* [MDN: New in JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/New_in_JavaScript)
* [The A-Z of Programming Languages: JavaScript](http://www.computerworld.com.au/article/255293/a-z_programming_languages_javascript/)
* [Brendan Eich: JavaScript - The High Road, The Low Road](http://cdn.oreillystatic.com/en/assets/1/event/106/JavaScript_%20Taking%20both%20the%20High%20and%20the%20Low%20Roads%20Presentation%201.pdf)
* [What's going on with JavaScript versioning?](https://benmccormick.org/2015/09/14/es5-es6-es2016-es-next-whats-going-on-with-javascript-versioning/)

---

## Resources: Videos

* [Alejandro Oviedo - THE !FUTURE OF JAVASCRIPT](https://www.youtube.com/watch?v=n84fLyM_88w)
* [Nordic.js 2016 • Jem Young - Embracing The Future](https://www.youtube.com/watch?v=CRjGt0KfjzE)
* [JavaScript Air - The past, present and Future of Javascript](https://javascriptair.com/episodes/2015-12-09/)

---

# [es-explained]()

## ECMAScript, TC39 and The Future of JavaScript

#### hello@cjr.co.de
#### CJ on Denver Devs
