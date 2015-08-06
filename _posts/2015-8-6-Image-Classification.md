---
layout: page
title:  "It's a Bird, It's a Plane!"
subheadline:  "Introduction to image classification"
author: Trisha
teaser: "The first step in answering any question involves getting some data. In this case, that meant web scraping."
---

<script src="http://d3js.org/d3.v3.min.js"></script>
<script src="http://d3js.org/colorbrewer.v1.min.js"></script>
<script src="http://code.jquery.com/jquery-1.11.0.min.js"></script>
<script src="http://d3js.org/queue.v1.min.js"></script>
<!--<script src="https://github.com/turban/d3.slider/d3.slider.js"></script>
-->
<script src="../blog/heatmap.js"></script>
<link rel="stylesheet" href="../blog/heatmap.css" />

<!--<head>-->

<script>

$(document).ready(function() {
	
	heatmap_display("../blog/heatmaps/linsvc_lim=500_k=300.json", "#heatmap", "PuRd", 'linsvc');
});
</script>

<!--</head>

<body>-->

<div id="heatmap"></div>
<table style="height:80px; width:80%; text-align: center">
  <tr>
    <td>
    <table ><!--style="width:30%;">-->
        <tr>
         <p>
            <label for="lim" 
                style="display: inline-block; text-align: center">
            # Images:<span id="lim-value"></span>
            </label>
            <input type="range" min="1" max="510" id="lim" value="500">
        </p>
        </tr>
        <tr>
         <p>
            <label for="k" 
                style="display: inline-block; text-align: center">
            # Clusters:<span id="k-value"></span>
            </label>
            <input type="range" min="1" max="310" id="k" value="300">
        </p>
        </tr>
    </table>
    </td>
    <td>
    <table>
    <tr><!--
    Model:
    <select id="model">
    <option value="nomodel">----</option>
    <option value="mnb" selected>Multinomial Naive Bayes</option>
    <option value="gnb">Gaussian Naive Bayes</option>
    <option value="linsvc">Linear SVC</option>
    <option value="logreg">Logistic Regression</option>
    <option value="rf">Random Forrest</option>
    <option value="tree">Decision Tree</option>
    </select>-->
    </tr>
    <tr>
    <p>
      <label for="mname" 
         style="display: inline-block; text-align: center">
         Model Slider:<span id="mname-value"></span>
      </label>
      <input type="range" min="1" max="600" id="mname" value="600">
    </p>
    </tr>
    </table>
    </td>
  </tr>
  <!--<tr>
    <td>Eve</td>
    <td>Jackson</td> 
    <td>94</td>
  </tr>-->
</table>

<!--Palette:
<select id="palette">
  <option value="BuPu">BuPu</option>
  <option value="RdPu">RdPu</option>
  <option value="PuRd" selected>PuRd</option>
 <option value="RdGy">RdGy</option>
  <option value="PuBu">RdBu</option>
  <option value="PiYG">PiYG</option>
  <option value="PRGn">PRGn</option>
  <option value="BrBG">BrBG</option>
  <option value="PuOr">PuOr</option> 
</select>-->


