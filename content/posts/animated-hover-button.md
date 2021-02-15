---
title: ":star2: A Quick Hover Button"
summary: How to create a magic hover effect on buttons!
date: "2021-02-04"
draft: false
slug: hover-button
tags:
- css
---

I’ve always been fascinated by random animations and effects that spice up the user experience. I recently stumbled across a button on a webpage that had a hover effect that caught my eye. As I scrolled down the page, the button seemed pretty normal and bland at first glance. However when you hover, a small animation transforms it into something fun.

<GIF>

 Although small and ultimately meaningless I find it cool and interesting so here's my attempt at recreating it...

Start of with the basics. A **simple** html button with no styles

```html
<button class="btn">Hover Me!</button>
```

Let’s style the button and not make it look so lame.

```css
.btn {
  display: inline-block;
  background: transparent;
  font-size: 2em;
  font-weight: 700;
  letter-spacing: 0.3px;
  padding: 1em;
  cursor: pointer;
  color: rgb(255, 255, 255);
  position: relative;
  border: none;
}
```

Now let’s add some sizzle. CSS transitions make this pretty easy to do with the use of the `:hover` pseudo selector.

```css
...

.btn:hover .border__left, .btn:hover .border__right {
  height: 0%;
}

.btn:hover .border__top, .btn:hover .border__bottom {
  width: 0%;
}

.btn:hover .border__extra {
  width: 100%;
}
```
Viola! A fun, animated button to add to your next web project. Be warned don’t got crazy with making all buttons animated but this is perfect example for calm to action or even playful buttons to sprinkle into your web apps. 