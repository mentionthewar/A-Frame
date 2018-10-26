# Recovering lost Tudor Treasures with A-frame @ MozFest </h1>

<h3> Environment </h3>

1. Download vr-test1.htm and open it in your browser in another tab. Take a look at the 20 lines of code used to produce the rather dark and menacing landscape you will see. <a href="https://cdn.aframe.io/a-painter/images/sky.jpg">Here is one of the two images making up the scene</a>. What do you notice about it?

2. Download vr-test2.htm and open it in your browser. This is a little sunnier. Instead of using images we are now using an <a href="https://github.com/feiss/aframe-environment-component">extra piece of Javascript</a> (written by <a href="https://github.com/feiss">Diego Goberna</a>) to provide a lot of environmental details quickly. In A-frame these are called <strong>components</strong>.

3. Look at this code. You will see a line which reads:
```
<a-scene environment="preset: default">
```

The package contains many other options. In Notepad or similar replace the word default with one of:

<table>
<tr>
  <td> forest </td>
  <td> arches </td>
  <td> checkerboard </td>
  <td> contact </td>
  </tr>
<tr>
  <td> dream </td>
  <td> egypt </td>
  <td> goaland </td>
  <td> goldmine </td>
  </tr>
<tr>
  <td> japan </td>
  <td> osiris </td>
  <td> poison </td>
  <td> starry </td>
  </tr>
<tr>
  <td> threetowers </td>
  <td> tron </td>
  <td> volcano </td>
  <td> yavapai </td>
</table>

4. Save vr-test2.htm and refresh (F5) the page in the browser. Maybe try a few of these until you find one you like.

<h3> Adding objects </h3>

1. Below the empty assets tags, add a line of code:
```
<a-box position="-1 0.5 -3" rotation="0 45 0" color="#FFFFFF"></a-box>
```

2. Now we have a box which we can position and rotate in 3 dimensions. The three values of the position attribute control left to right, up and down and further/nearer in the scene respectively. (i.e. if we want objects on the ground, the middle number should be 0)

<h2> Useful A-frame tutorials and resources </h2>
<ul>
<li> Some stuff to watch out for - https://codeburst.io/a-frame-vr-pitfalls-tips-and-tricks-4829aa3cbc22
<li> Fun tutorial on A-frame physics - https://hacks.mozilla.org/2017/05/having-fun-with-physics-and-a-frame/
</ul>
