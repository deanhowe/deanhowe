---
title: 'css'
description: 'Cascading Style Sheets - what happens between the sheets?'
view: homepage
title-url: '/languages/css'
title-class: 'font-semibold text-snow-100 hover:text-snow-500 dark:text-white'
title-style: 'text-shadow: 0px 0px 7px black;'
icon: 'o-rocket-launch'
-icon-class: ''
-link-url: '/languages/css'
-link-title: 'css'
-link-icon: 's-arrow-small-right'
-content: '/languages/css.md'
-figure-background: 'images/thumbs/moof-digital.png'
-figure-alt: 'css'
-figure-link: '/languages/css'
article:modified_time: '2019-10-31T15:39:36+00:00'
og:title: 'css'
og:image: '/images/moof_logo.jpg'
og:image:width: '1921'
og:image:height: '1920'
og:image:type: 'image/jpeg'
---

# What happens between the sheets?


<summary></summary>

https://developer.mozilla.org/en-US/play

https://developer.mozilla.org/en-US/docs/Web/HTML/Element/dialog

https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors

https:// gist.github.com/gokulkrishh/242e68d1ee94ad05f488

https://developer.mozilla.org/en-US/docs/Web/CSS/gradient/radial-gradient

https://codepen.io/jh3y/pen/poxVPqo

```css

a {
  color: blue;
}

/* Internal links, beginning with "#" */
a[href^="#"] {
  background-color: gold;
}

/* Links with "example" anywhere in the URL */
a[href*="example"] {
  background-color: silver;
}

/* Links with "insensitive" anywhere in the URL,
   regardless of capitalization */
a[href*="insensitive" i] {
  color: cyan;
}

/* Links with "cAsE" anywhere in the URL,
with matching capitalization */
a[href*="cAsE" s] {
  color: pink;
}

/* Links that end in ".org" */
a[href$=".org"] {
  color: red;
}

/* Links that start with "https://" and end in ".org" */
a[href^="https://"][href$=".org"]
{
  color: green;
}


```

https://codepen.io/jh3y/pen/poxVPqo


<select name="style" id="style">
  <option value="choose">Shimmer Style</option>
  <option value="container">Container</option>
  <option value="flip">Flip</option>
  <option value="lazy">Lazy</option>
  <option value="in-n-out">In and Out</option>
</select>
<label for="secret">Show Trick</label>
<input type="checkbox" id="secret">
<button>
  <span class="spark__container">
    <span class="spark"></span>  
  </span>
  <span class="backdrop"></span>
  <span class="text">
    Shim Shimmer
  </span>
</button>

 > Waste no more time arguing what a good man should be, be one. - Marcus Aurelius

[PHP](/2024/PHP), [Markdown](/2024/markdown).

https:// gist.github.com/gokulkrishh/242e68d1ee94ad05f488

[^1]: This text is inside a footnote.
[^Markdown]: What is [Markdown](/2024/markdown).
[^PHP]: Is [PHP](/2024/PHP) dead?.
[^Laravel]: Read my [Laravel 11](/2014/laravel-11) review [here](/2014/laravel-11).
