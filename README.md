# SpriteSpreadr
## A tool, that helps you previewing your SVG icon sprites.



<img 
src="http://silkine.github.io/sprite-spreadr/images/pic-illustrator-canvas.png" width="150" alt="original illustrator file"> -> <img src="http://silkine.github.io/sprite-spreadr/images/pic-spritespreader-result.png" alt="spriteSpreaded icons" width="300">

<sub>Icons created by Sergey Demushkin from the Noun Project</sub>

This tool is designed for SVG icon sprites, that you created by stacking all icons over each other in order to use them in your html with the &lt;use&gt; tag for example. I found it hard to control how your icons might look on the website, when opening a SVG file directly in the browser, as browsers tend to open them in 100% width and height and sometimes you might need to change the white background in order to see transparency or white icons.

SpriteSpreadr will give you a structured overview by displaying your icons in a reasonable grid next to each other in their original size with the id names underneath them and offers you a possibility to change the background color in the browser.

For this it is important, that you give your icons id names. You can do this in Adobe Illustrator by naming your layers. This will turn out to be id attributes automatically with the export to SVG.

## So your workflow with Adobe Illustrator would be: 

1. Put all your SVG icons in groups or in 1 compound path per icon
2. Place them all over each other.
3. Make sure, they're all visible
4. Name each icon group or icon compound path
5. Export it to SVG
6. Upload the SVG on SpriteSpreadr
7. See how they will look 
8. Edit the background color, when needed

>  Please note that as for now (November 2015) the "Reload File" functionality and the background color chooser will only work in Chrome and Firefox.

>  Please note that css, js and html markdown are all merged into the html. This is not meant to be beautiful but could come in handy, as you could easily pass the html on or download it and open it offline on your browser without any hassle or additional files. The image folder contains the images of the help layer.

## Using one SVG file with the &lt;use&gt; tag and ID in HTML
1. Put your SVG code inline at the top of your &lt;body&gt; tag.
2. Insert a &lt;defs&gt; tag inside the &lt;svg&gt; thus wrapping all contents with it
  ```html
  <svg>
    <defs>
      <g id="icon-id1">
        <!-- paths, groups, circles, rects etc. -->
      <g>
      <g id="icon-id2">
        <!-- paths, groups, circles, rects etc. -->
      <g>
    </defs>
  </svg>
  ```

3. Reference the icons you need to use by ID in the &lt;use&gt; tag inside a &lt;svg&gt; tag :
&lt;use xlink:href="#id"&gt;:
  ```html
  <svg viewBox="0 0 32 32" class="icon-class">
    <use xlink:href="#icon-id1"></use>
  </svg>
  ```
  
Find more about this [on css tricks](https://css-tricks.com/svg-sprites-use-better-icon-fonts/) 
