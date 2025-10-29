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

Here is an overview of the process: First, I apply a convolution to the original image using a kernel with a specified denominator. After applying the convolution, I calculate the mean pixel intensity value for a vertical transect taken from the middle column of the image. I expand and normalize this transect to match the dimensions of the whole image. Then, I multiply the convolved image by the expanded transect. For each row of the resulting image, I calculate the mean pixel intensity and compare it to the mean intensity of the original transect. Based on this difference, I shift the corresponding row of pixels left or right. The magnitude of the shift is proportional to the difference, and the direction is determined by whether the row's intensity is above or below the mean. Lastly, I adjust the color of each pixel exceeding a predefined threshold. I repeat this process iteratively, applying a convolution with a decreasing kernel denominator at each frame. The examples below each have a different starting kernel denominator, kernel denominator step size, pixel threshold value, shift speed, and/or pixel color manipulation.

The image used in these examples is a photomicrograph of a polished slab of stromatolite laminations taken from Suarez-Gonzalez et al., 2014.

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