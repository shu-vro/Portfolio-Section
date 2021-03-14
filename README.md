# PORTFOLIO-SECTION
PORTFOLIO SECTION &lt;HTML> {CSS} (JavaScript)

This Reposiory is created with the help of 2 library which runs by [jQuery](https://jquery.com/). 

They are:

- [Swiper js](https://swiperjs.com)
- [MixItUp](https://www.kunkalabs.com/mixitup/)


## Swiper Js

Swiper is the most modern free mobile touch slider with hardware accelerated transitions and amazing native behavior. It is intended to be used in mobile websites, mobile web apps, and mobile native/hybrid apps.

Swiper is not compatible with all platforms, **it is a modern touch slider which is focused only on modern apps/platforms to bring the best experience and simplicity.**

Swiper, along with other great components, is a part of Framework7 - a fully-featured framework for building iOS & Android apps. Swiper is also a default slider component in the Ionic Framework.

### Installation

``` html 
<link rel="stylesheet" href="https://unpkg.com/swiper/swiper-bundle.min.css" />
<div class="swiper-container">
  <!-- Additional required wrapper -->
  <div class="swiper-wrapper">
    <!-- Slides -->
    <div class="swiper-slide">Slide 1</div>
    <div class="swiper-slide">Slide 2</div>
    <div class="swiper-slide">Slide 3</div>
    ...
  </div>
  <!-- If we need pagination -->
  <div class="swiper-pagination"></div>

  <!-- If we need navigation buttons -->
  <div class="swiper-button-prev"></div>
  <div class="swiper-button-next"></div>

  <!-- If we need scrollbar -->
  <div class="swiper-scrollbar"></div>
</div>
<script src="https://unpkg.com/swiper/swiper-bundle.min.js"></script>
```

In StyleSheet, 

```css
.swiper-container {
  width: 600px;
  height: 300px;
}
```

In JavaScript,

```js
const swiper = new Swiper('.swiper-container', {
  // Optional parameters
  direction: 'vertical',
  loop: true,

  // If we need pagination
  pagination: {
    el: '.swiper-pagination',
  },

  // Navigation arrows
  navigation: {
    nextEl: '.swiper-button-next',
    prevEl: '.swiper-button-prev',
  },

  // And if we need scrollbar
  scrollbar: {
    el: '.swiper-scrollbar',
  },
});
```
For more information, goto [swiper js](https://swiperjs.com/demos)

## MixItUp

MixItUp is a high-performance, dependency-free library for animated filtering, sorting, insertion, removal and more. MixItUp gives you beautiful animated DOM manipulation on top of native CSS layout. For more info, goto [mixitup official page](https://www.kunkalabs.com/mixitup/)

## Starter Template

In HTML 

```html
<nav class="about_nav padding_top">
    <ul>
        <li>
            <!-- Mandatory data-filter attribute which contains the class name of the respective box. -->
            <a class="filter active" href="#" data-filter="all">All</a>
        </li>
        <li>
            <a class="filter" href="#" data-filter=".w1">W1</a>
        </li>
        <li>
            <a class="filter" href="#" data-filter=".w2">W2</a>
        </li>
        <li>
            <a class="filter" href="#" data-filter=".w3">W3</a>
        </li>
    </ul>
</nav>
<div class="mymixcont">
    <div class="mix w1"></div>
    <div class="mix w2"></div>
    <div class="mix w3"></div>
    <div class="mix w1"></div>
    <div class="mix w2"></div>
    <div class="mix w3"></div>
    <div class="mix w1"></div>
    <div class="mix w2"></div>
    <div class="mix w3"></div>
    <div class="mix w1"></div>
    <div class="mix w2"></div>
    <div class="mix w3"></div>
</div>

<!-- Linking jQuery and mixitup cdn -->
<script src="https://cdn.jsdelivr.net/npm/jquery@3.6.0/dist/jquery.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/mixitup@3.3.1/dist/mixitup.min.js"></script>
<script src="src/index.js"></script>
<script>
    // Get the container
    let config = document.querySelector(".mymixcont");
    var mixer = mixitup(config);
</script>
```

In CSS

```css
html {
    scroll-behavior: smooth;
}

body {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Montserrat", "Gill Sans", "Gill Sans MT", Calibri,
        "Trebuchet MS", sans-serif;
}

/* Selecting every box */
.mix {
    position: relative;
    width: 20%;
    height: 100px;
    background: #000;
    margin: 10px;
    display: inline-block;
}

.w1 {
    background: dodgerblue;
}

.w2 {
    background: orangered;
}

.w3 {
    background: indigo;
}

.mixBtns {
    width: 100%;
    margin: 20px;
    text-align: center;
}

.mixBtns a {
    display: inline-block;
    text-decoration: none;
    margin: 10px;
    font-weight: bold;
    color: dodgerblue;
    text-align: center;
}

```

For more details, goto [MixItUp](https://www.kunkalabs.com/mixitup/docs/configuration-object/)
