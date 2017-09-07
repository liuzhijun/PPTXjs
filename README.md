PPTXjs
==========
[![MIT License][license-image]][license-url]

[license-image]: http://img.shields.io/badge/license-MIT-blue.svg?style=flat
[license-url]: LICENSE
 
### jQuery plugin for convertation pptx to html using pure javascript.
### Demo: https://meshesha.github.io/pptxjs/

# Version: 
### 1.0.6
# environment
### browsers:
- IE > 10
- Edge
- FireFox
Support:
----
* Text
  * Font size
  * Font family
  * Font style: blod, italic, underline, stok
  * Color
  * hyperlink
  * bullets (include numeric)
* Text block (convert to Div)
  * Align (Horizontal and Vertical)
  * Background color (single color)
  * Border (borderColor, borderWidth, borderType, strokeDasharray)
* Shapes (not all types, yet)
  * Background color (single color, gradient colors)
  * Background image
  * Rotations
  * Align
  * Border
* Custom shape
* Media
  * Picture (jpg/jpeg,png,gif,svg)
  * Video (html5 video player: mp4,wmv,ogg)
  * Audio (html5 audio player:mp3,wma,wav,ogg)
* Graph
  * Bar chart
  * Line chart
  * Pie chart
  * Scatter chart
* SmartArt diagrams
* Custom table
* Theme table
* Theme
  * Background color
  * Background image
* and more ... see demo

###  usage:
----
 include necessary css files:
 ```
<link rel="stylesheet" href="./css/pptxjs.css">
<link rel="stylesheet" href="./css/nv.d3.min.css"> <!-- for charts graphs -->
```
 include necessary css files:
 ```
<script type="text/javascript" src="./js/jquery-1.11.3.min.js"></script>
<script type="text/javascript" src="./js/jszip.min.js"></script> <!-- v2.. , no v.3.. -->
<script type="text/javascript" src="./js/d3.min.js"></script> <!-- for charts graphs -->
<script type="text/javascript" src="./js/nv.d3.min.js"></script> <!-- for charts graphs -->
<script type="text/javascript" src="./js/pptxjs.js"></script>
<script type="text/javascript" src="./js/divs2slides.js"></script> <!-- for slide show -->
 ```
 html body :
 ```
 ...
   <div id="your_div_id_result"></div>
   optional:
   <input id="upload_pptx_fiile" type="file" />
 ...
 ```
 add javascript:
 ```
<script type="text/javascript">
 $("#your_div_id_result").pptxToHtml({
   pptxFileUrl: "path/to/yore_pptx_file.pptx", 
   fileInputId: "upload_pptx_fiile",
   slideMode: false,
   keyBoardShortCut: false,
   mediaProcess: true, /** true,false: if true then process video and audio files */
   slideModeConfig: {  //on slide mode (slideMode: true)
     first: 1,
     nav: false, /** true,false : show or not nav buttons*/
     navTxtColor: "white", /** color */
     navNextTxt:"&#8250;", //">"
     navPrevTxt: "&#8249;", //"<"
     showPlayPauseBtn: false,/** true,false */
     keyBoardShortCut: false, /** true,false */
     showSlideNum: false, /** true,false */
     showTotalSlideNum: false, /** true,false */
     autoSlide: false, /** false or seconds (the pause time between slides) , F8 to active(keyBoardShortCut: true) */
     randomAutoSlide: false, /** true,false ,autoSlide:true */ 
     loop: false,  /** true,false */
     background: "black", /** false or color*/
     transition: "default", /** transition type: "slid","fade","default","random" , to show transition efects :transitionTime > 0.5 */
     transitionTime: 1 /** transition time in seconds */           
   }
 });
</script>
 ``` 
# License
- Copyright © 2017 Meshesha
- MIT
