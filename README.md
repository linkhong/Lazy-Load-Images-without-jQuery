# About

Lazy load your images without the overhead of a framework. Optionally, send mobile-optimized images to smaller screens. Tested on IE7+, Firefox, Chrome, Safari, iOS.

Based on code from [Mike Pulaski](http://www.mikepulaski.com/code/2012/06/29/lazy-load-images-without-external-libraries/).

# Usage

1) Include `lazyload.js` or inline it or import or require it.

2) Add `.lazy-load` and `data-src` to each of your `<img>` tags. Optionally add `data-src-mobile`, a placeholder src, and a fallback image.

```html
<img class="lazy-load" data-src="lazy.jpg" data-src-mobile="lazy-small.jpg" src="blank.gif" />
<noscript><img src="lazy.jpg" /></noscript>
```

3) Add CSS3 magic for an animated fade-in:

```css
.lazy-load, .lazy-loaded {
  -webkit-transition: opacity 0.3s;
  -moz-transition: opacity 0.3s;
  -ms-transition: opacity 0.3s;
  -o-transition: opacity 0.3s;
  transition: opacity 0.3s;
  opacity: 0;
}

.lazy-loaded { opacity: 1; }
```

4) Manually run the plugin. If there is any new images you justed appended into the DOM, just run again.

```
    lazyload.run();
```
# Demo

http://kaizau.github.com/Lazy-Load-Images-without-jQuery/
