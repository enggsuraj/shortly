## Shortly - URL shortner

Get short URL instant, use shortly shorten and replace long URL to short link.

## Table of contents

- [Shortly - URL shortner](#shortly---url-shortner)
- [Table of contents](#table-of-contents)
- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- Shorten any valid URL
- See a list of their shortened links, even after refreshing the browser
- Copy the shortened link to their clipboard in a single click
- Receive an error message when the `form` is submitted if:
  - The `input` field is empty

### Screenshot

![shortly-URL-Shortner](https://user-images.githubusercontent.com/6918020/209463823-3c6feab4-db1c-4657-a0e2-b9b8203468ce.png)

### Links

- Live Site URL: [shortly](https://shortly.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Vanilla JavaScript
- REST API

Fetching URL Code snippets, see below:

```js
const getShortURL = async (url) => {
  const response = await fetch(`https://api.shrtco.de/v2/shorten?url=${url}`);
  const data = await response.json();
  return data;
};
```

QRCode.js

```js
<div id="qrcode"></div>
<script type="text/javascript">
new QRCode(document.getElementById("qrcode"), "http://jindo.dev.naver.com/collie");
</script>
```

### Continued development

Areas that I want to continue focus through this project is production
build ready code, connecting to kanban for issue tracking.

### Useful resources

- [Clean JavaScript Code](https://dev.to/deepaksisodiya/5-best-practices-for-clean-coding-in-javascript-26am) - This is an amazing article which helped me finally understand writing clean javascript code. I'd recommend it to anyone still learning this concept.

## Author

- Website - [blogtheorem](https://blogtheorem.com)
- Frontend Mentor - [@enggsuraj](https://www.frontendmentor.io/profile/enggsuraj)
- Twitter - [blogtheorem](https://www.twitter.com/blogtheorem)
