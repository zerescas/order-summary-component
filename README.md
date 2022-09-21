# Frontend Mentor - Order summary card solution

This is a solution to the [Order summary card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/order-summary-component-QlPmajDUj). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshots](#screenshots)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
    - [CSS Reset](#css-reset)
    - [border-radius vs. overflow: hidden](#border-radius-vs-overflow-hidden)
    - [100vh vs. 100% in html, body](#100vh-vs-100-in-html-body)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- See hover states for interactive elements

### Screenshots

![](/images/screenshots/desktop-screenshot.jpeg)<br>
<strong>Desktop</strong>

<br>

![](/images/screenshots/mobile-screenshot.png)<br>
<strong>Mobile</strong>

### Links

- Live Site URL: [https://zerescas.github.io/order-summary-component/](https://zerescas.github.io/order-summary-component/)

## My process

### Built with

- Semantic HTML5 markup
- CSS:
  - CSS Reset
  - Custom properties
  - Flexbox
  - Grid

### What I learned

#### CSS Reset

The original purpose to use "CSS Reset" is "reduce browser inconsistencies" seems is a little obsolete because a total domination of Google Chrome and death of all browser engines except of Blink(Chrome and Chromium based browsers), Webkit(Safari) and Quantum(Firefox with ~3% of the market share). Now the main purpose is to define global rules to get more logical and predictable behaviour of HTML elements.
<br>

#### border-radius vs. overflow: hidden

It turns out there's few ways to get a rounded container (all sides) and a rounded image (only top corners)<br>
![](/images/screenshots/border-radius-trouble.jpg)<br>

1. Setup an image and a container 
  ```css
  .image {
    /* top-left-corner and top-right-corner only */
    border-radius: 2em 2em 0 0;
  } 
  
  .container {
    /* all sides */
    border-radius: 2em;
  }
  ```

2. Setup a container only 
  ```css
  .container {
    border-radius: 0 0 0 0;
    overflow: hidden;
  }
  ```

<br>

#### 100vh vs. 100% in html, body

A goal - stretch <strong>body</strong> to full height of a browser window.<br>

1. Setup body only. 

```css
body {
  height: 100vh;
} 
```

This works fine only on desktop, but there's trouble on mobile (GUI of a browser overlaps of webpage)
![body-only-in-vh](/images/gif/body-only-in-vh.gif)

2. Setup <strong>html</strong> and <strong>body</strong>

```css
html,
body {
    height: 100%;
}
```

This still works on desktop and now on mobile we get real estate of a browser's viewport.
![html-and-body-in-percentages](/images/gif/html-and-body-in-percentages.gif)

### Useful resources

- [CSS Reset from meyerweb](https://meyerweb.com/eric/tools/css/reset/)
- [Custom CSS Reset from Joshua Comeau](https://www.joshwcomeau.com/css/custom-css-reset/)


## Author

- Twitter - [https://twitter.com/zerescas](https://twitter.com/zerescas)
- Telegram - [https://t.me/zerescas](https://t.me/zerescas)

## Acknowledgments

Thanks to [Aviral](https://www.frontendmentor.io/profile/Akunamo) for the [tip](https://www.frontendmentor.io/solutions/order-summary-component-with-flexbox-and-grid-XGlPOXPXuA#comment-632aa9ed037479dfd70fa4bb):
- Replace two <strong>div</strong> in <strong>footer</strong> content to ::before, ::after 

![](/images/screenshots/fix-before-after.png)