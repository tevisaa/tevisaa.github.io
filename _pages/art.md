---
layout: archive
title: "Art / Image Processing"
permalink: /art/
author_profile: true
---

<style>
  .small-break {
    margin-top: 0.25px; /* Adjust the value as needed */
  }
</style>

<br class="small-break">

Using the image processing techniques that I have developed to analyze the micro-scale textural features of stromatolites, I created a method for analyzing and manipulating image properties to create moving images.

Here is an overview of the process: First, I apply a convolution to the original image. After applying the convolution, I measure vertical transects for each column of pixels spanning the laminae and take the mean of pixel intensities from each individual column of pixels. After calculating the mean for each column, I shift each corresponding row of pixels by the difference of the mean intensity value of the transect relative to a pre-defined intensity threshold, where the greater the difference in intensity from the threshold, the faster the row shifts. Lastly, I check individual pixel intensity values against a global threshold and manipulate the color for each pixel according to its difference from this threshold. I perform this process iteratively, with a convolution occurring at each step in the animation for a set number of iterations, each with a different denominator for the convulation. Each example below has a different convolution denominator, pixel threshold value, shift speed, and/or pixel color manipulation.

The image used in these examples is a photomicrograph of a polished slab of stromatolite laminations from Suarez-Gonzalez et al., 2014.

<div class="art-grid">
  <div class="art-item">
    <a href="{{ site.baseurl }}/images/IMG_1070.GIF" data-lightbox="art-gallery" data-title="Art 1">
      <img src="{{ site.baseurl }}/images/IMG_1070.GIF" alt="Art 1">
    </a>
  </div>
  <br>
  <div class="art-item">
    <a href="{{ site.baseurl }}/images/IMG_1067.GIF" data-lightbox="art-gallery" data-title="Art 1">
      <img src="{{ site.baseurl }}/images/IMG_1067.GIF" alt="Art 1">
    </a>
  </div>
  <br>
  <div class="art-item">
    <a href="{{ site.baseurl }}/images/IMG_1066.GIF" data-lightbox="art-gallery" data-title="Art 1">
      <img src="{{ site.baseurl }}/images/IMG_1066.GIF" alt="Art 1">
    </a>
</div>