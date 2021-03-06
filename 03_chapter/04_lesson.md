**WDI Fundamentals Unit 3**
---

#Working With Images

Adding images to your website can help it come to life. To add images to your site, use the `img` tag with the **src** attribute. `src` stands for “Source” and tells the `img` tag where to find the image you want to include on your page. 


<div class="wistia_responsive_padding" style="padding:56.25% 0 0 0;position:relative;"><div class="wistia_responsive_wrapper" style="height:100%;left:0;position:absolute;top:0;width:100%;"><iframe src="//fast.wistia.net/embed/iframe/kn8gfpd9z9?seo=false&videoFoam=true" allowtransparency="true" frameborder="0" scrolling="no" class="wistia_embed" name="wistia_embed" allowfullscreen mozallowfullscreen webkitallowfullscreen oallowfullscreen msallowfullscreen width="100%" height="100%"></iframe></div></div>
<script src="//fast.wistia.net/assets/external/E-v1.js" async></script>

### Breaking Down the Image Tag

The `img` tag alone doesn't do much. It's like putting an empty `<a>` in your code. The most important thing to do is to tell the browser what image to show using helpful attributes. That's what the `src` attribute does. The `src` attribute for an `img` tag works just like the `href` attribute for a link: It tells a browser where to look for an image.

```html
<img src="">
```

The **image alternate attribute** is a text description of the image, and is read aloud to users with visual impairments. This description is especially important to include when there's text in an image.

```html
<img src="http://i.imgur.com/z9gGd0t.jpg" alt="grumpy cat">
```

The **title attribute** tells search engines what the image is depicting, which helps the page appear in Google Image Search.

```html
<img src="http://i.imgur.com/z9gGd0t.jpg" alt="grumpy cat" title="grumpy cat">
```


[On to the next lesson.](07_lesson.md)
