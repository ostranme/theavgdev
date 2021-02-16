---
title: ":crystal_ball: A Quick Button Hover Effect"
summary: How to create a magic hover effect on buttons!
date: "2021-02-04"
draft: false
slug: hover-button
tags:
- css
- ui
---

I’ve always been fascinated by random animations and effects that spice up the user experience. I recently stumbled across a button on website that had a hover effect that caught my eye. I know there are countless tutorials on how to create stylish buttons, so here's another one to add to the mix. Although small and ultimately meaningless I found the button interesting so here's my attempt at recreating it.

If you're looking for something pointless, let's get started! I like simplicity, and this HTML and CSS button is exactly that. You'll see the button preview below, followed by the respective HTML and CSS code to make the button work on your own website or landing page. 

## The Button

So this button has a simple design it's a normal button with blue borders. On hover, the button transitions with borders sliding out of the way and underlining the text.

![Hover](/images/hover.gif)

Please find the HTML and CSS code below the button.

### Button HTML

```html
<button class="btn">
  <span class="border__top"></span> 
  <span class="border__bottom"></span>
  <span class="border__left"></span>
  <span class="border__right"></span>
  <span class="border__extra"></span>
  Hover Me!
</button>
```

### Button CSS

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

.border__top {
  border-top: 4px solid rgb(0, 107, 237);
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0px;
  left: 0px;
  transition: width .5s;
}

.border__bottom {
  border-bottom: 4px solid rgb(0, 107, 237);
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0px;
  right: 0px;
  transition: width .5s;
}
.border__left {
  border-left: 4px solid rgb(0,107,237);
  height: 100%;
  position: absolute;
  bottom: 0px;
  left: 0px;
  transition: height .5s;
}

.border__right {
  border-right: 4px solid rgb(0,107,237);
  height: 100%;
  position: absolute;
  top: 0px;
  right: 0px;
  transition: height .5s;
}

.border__extra {
  border-bottom: 4px solid rgb(0, 107, 237);
  width: 0%;
  height: 100%;
  position: absolute;
  top: 0px;
  left: 0px;
  transition: width 1s;
}
```

### Button Hover CSS

Now let’s add some sizzle. CSS transitions make this pretty easy to do with the use of the `:hover` pseudo selector.

```css
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

Viola! A fun, animated button to add to your next web project. Here's a link to the [repo](https://github.com/ostranme/hover-button) I created for reference. Be warned don’t go to crazy with making all buttons animated but this is perfect example for a call to action or even playful buttons to sprinkle into your web apps. 