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

2. Now we have a box which we can position and rotate in 3 dimensions. The three values of the position attribute control left to right, up and down and further/nearer in the scene respectively. (i.e. if we want objects on the ground, the middle number should be 0). 

Move things around a bit and when you're ready add other objects, e.g.:
```
<a-cylinder position="1 0 -3" radius="0.75" height="6" color="#FFC65D"></a-cylinder>
```
The basic shapes are listed <a href="https://aframe.io/docs/0.8.0/introduction/html-and-primitives.html">on this page</a>.

3. The camera can be repositioned in a similar way. Below the asset tags add:
```
<a-entity position="-12 0 -2">
  <a-camera></a-camera>
</a-entity>
```
4. This puts us in a position to view a very basic building we can add:
```
<a-box position="-2 0.5 -9" color="grey" depth="6" height="5" width="0.25"></a-box>
<a-box position="-5 0.5 -6" rotation="0 90 0" color="grey" depth="6" height="5" width="0.25"></a-box>
<a-box position="-5 0.5 -12" rotation="0 90 0" color="grey" depth="6" height="5" width="0.25"></a-box>
<a-box position="-8 0.5 -11" rotation="0 0 0" color="grey" depth="2" height="5" width="0.25"></a-box>
<a-box position="-8 0.5 -7" rotation="0 0 0" color="grey" depth="2" height="5" width="0.25"></a-box>
<a-box position="-5 3 -9" rotation="0 0 0" color="grey" depth="6" height="0.25" width="6"></a-box>
```
<h3> Calling other assets </h3>
1. Running on a local machine this makes A-Frame rather grumpy. But we can slap a mural on our building. Into the assets section, we can add an image from Wikimedia Commons:

```
<a-assets>
<img id="dali" src="https://upload.wikimedia.org/wikipedia/commons/f/fc/Street_Art_%284240649293%29.jpg">
</a-assets>
```

2. We then call this asset with our boxes and other objects:
```
<a-image position="-5 0.5 -5.8" rotation="0 0 0" src="#dali" height="5" width="6"></a-image>
```

<h3> Physics and importing 3D objects</h3>

This can be done through a properly configured localhost. Take a look, for instance, at https://github.com/donmccurdy/aframe-physics-system


<h2> Useful A-frame tutorials and resources </h2>
<ul>
<li> Some stuff to watch out for - https://codeburst.io/a-frame-vr-pitfalls-tips-and-tricks-4829aa3cbc22
<li> Geat walkthrough on a local system to produce a Pacman-like game - https://gamedevacademy.org/beginners-guide-to-a-frame-vr/
<li> Another good, simple tutorial mentioning quirks of the framework https://hacks.mozilla.org/2017/09/i-built-something-with-a-frame-in-2-days-and-you-can-too/
<li> Fun tutorial on A-frame physics - https://hacks.mozilla.org/2017/05/having-fun-with-physics-and-a-frame/
</ul>
