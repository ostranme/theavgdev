---
title: ":space_invader: Mandalorian Character UI Cards"
summary: Create your own Mandalorian character cards
date: "2021-02-15"
draft: false
slug: mandolorian-character-cards
tags:
- css
- ui
---

Here's a quick tutorial on some Mandalorian character cards I created. Nothing special, just mainly playing around with UI cards.

## The Card

This character card is pretty pointless but I wanted to play around with creating a *somewhat* clean card and work on some flexbox skillz at the same time.

![Mando Card](/images/mando-card.png)

Please find the HTML and CSS code below the button.

### Card HTML

```html
<div class="card">
    <div class="card-inner">
        <div class="card-info">
            <h1 class="title">Mando</h1>
            <p class="sub-title">This is the Way</p>
        </div>
        <div class="card-media">
            <img src="https://res.cloudinary.com/dvdswa7zm/image/upload/v1575229407/codepen/mando_wfyrkw.png" class="card-img mando">
        </div>
    </div>
</div>
```

### Card CSS

```css
@import url('https://fonts.googleapis.com/css?family=Open+Sans|Rubik+Mono+One&display=swap');

html, body {
  font-family: 'Rubik Mono One', sans-serif;
}

.card {
  width: 425px;
  height: 200px;
  background: white;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 2px 2px 10px 2px rgba(153,153,153,1);
  border: 5px solid;
  border-image-source: linear-gradient(45deg, rgb(218,95,72), rgb(241,188,79));
  border-image-slice: 1;
  margin: 2rem;
}

.card-inner {
  width: 98%;
  height: 95%;
  background: rgb(34,31,34);
  background: linear-gradient(45deg, rgba(34,31,34,1) 36%, rgba(102,100,105,1) 100%);
  display: flex;
}

.card-info {
  padding: 25px;
  color: white;
}

.title {
  margin: 0;
  text-transform: uppercase;
  font-size: 1.8rem
}
.sub-title {
  margin-top: .2rem;
  font-family: 'Open Sans';
  font-style: italic;
}

.mando {
  position: relative;
  bottom: 75px;
  right: 57px;
  height: 275px;
}

.kuiil {
  position: relative;
  bottom: 75px;
  right: 66px;
  height: 275px;
}

.ig11 {
  position: relative;
  bottom: 75px;
  right: -9px;
  height: 275px;
}
```

There you go, a simple UI character card. Feel free to swap out and use different characters. Add a comment to what you come up with. Here's a link to the [repo](https://github.com/ostranme/mandalorian-cards) if you want the full code.