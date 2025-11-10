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

Using the image processing techniques I developed to analyze the micro-scale textural features of stromatolites, I designed a method to create moving images by manipulating image properties.

Here is an overview of the process: First, I apply a convolution to the original image using a kernel with weights that are normalized according to a specified pattern (e.g., decreasing with each iteration). After performing the convolution, I calculate the mean pixel intensity value for a vertical transect taken from the middle column of the image. I expand and normalize this transect to match the dimensions of the whole image. Then, I multiply the convolved image by the expanded transect. For each row of the resulting image, I calculate the mean pixel intensity and compare it to the mean intensity of the vertical transect. Based on this difference, I shift the corresponding row of pixels left or right. The speed of the shift is proportional to the difference, and the direction is determined by whether the row's intensity is above or below the mean. Lastly, I adjust the color of each pixel exceeding a predefined intensity threshold. I repeat this process iteratively, performing a convolution with a kernel whose weights are normalized by the pattern specified for each frame. The examples below each use a different starting kernel, kernel normalization pattern, kernel update rate, pixel threshold value, shift speed, and/or pixel color manipulation.

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