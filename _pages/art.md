---
layout: archive
title: "Art / Image Processing"
permalink: /art/
author_profile: true
---

<style>
  .small-break {
    display: block;
    height: 1px; /* Adjust the height as needed */
  }
</style>
<div class="small-break"></div>

Using the image processing techniques that I developed to extract the micro-scale textural features of stromatolites, I created a method for analyzing and manipulating image properties to create moving images.

Here is an overview of the process: First, I apply a convolution to the original image. After applying the convolution, I measure vertical transects for each column of pixels spanning the laminae and take the mean of pixel intensities from each column. Then, I shift the corresponding row of pixels left or right by the difference of the mean value of the transect relative to the average pixel intensity for the whole image. The greater the difference in intensity from the threshold, the faster the row shifts. The direction of the shift is determined by whether the value is above or below the threshold. Lastly, I manipulate the color for each pixel according to its difference from a global threshold. I perform this process iteratively, with a convolution occurring at each step in the animation. The examples below each have a different convolution denominator, pixel threshold values, shift speed, and/or pixel color manipulation.

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
</div>