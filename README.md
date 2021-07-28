# Frontend Mentor - Profile card component solution

This is a solution to the [Profile card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/profile-card-component-cfArpWshJ). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)

## Overview

### The challenge

- Build out the project to the designs provided

### Screenshot

![](screenshot.png)

### Links

- Live Site URL: [https://joffenhopland.github.io/profile-card-component-main/](https://joffenhopland.github.io/profile-card-component-main/)

### Built with

- Semantic HTML5 markup
- CSS
- Flexbox
- CSS Animations

### What I learned

The biggest challenges I faced when working on this project were how to position the profile image, how to make the image a circle and how to layer and position the background images.
- To position the profile image I relalized I could just use margin. This was my solution to the problem: margin: -50px auto 30px auto;
- To make the profile image a circle I used border, border-radius and overflow. My complete HTML and CSS for the image looks like this

```html
<div class="img-holder">
          <img src="images/image-victor.jpg" alt="">
        </div>
```
```css
.img-holder {
    width: 100px;
    height: 100px;
    border: 4px solid white;
    border-radius: 50%;
    overflow: hidden;
    margin: -50px auto 30px auto;
}

.img-holder img {
    width: 100%;
    height: auto;
    display: block;
}
```
- This is how I positioned and layered the background images. In addition to that I created a fade in animation of the background images on page load. It was my first time using animation is CSS so that was a cool to learn:
```html
<div class="circles">
      <div class="c1"><img src="images/bg-pattern-top.svg" alt=""></div>
      <div class="c2"><img src="images/bg-pattern-bottom.svg" alt="" class="c2"></div>
    </div>
```
```css
.circles{
    position: absolute;
    z-index: -1;
-webkit-animation: fadein 2s; /* Safari, Chrome and Opera > 12.1 */
-moz-animation: fadein 2s; /* Firefox < 16 */
 -ms-animation: fadein 2s; /* Internet Explorer */
  -o-animation: fadein 2s; /* Opera < 12.1 */
     animation: fadein 2s;
}

.c1{
    position: relative;
    top: 100px;
    left: -500px;
}

.c2{
    position: relative;
    bottom: -20px;
    right: -200px;
}

@keyframes fadein {
    from { opacity: 0; }
    to   { opacity: 1; }
}

/* Firefox < 16 */
@-moz-keyframes fadein {
    from { opacity: 0; }
    to   { opacity: 1; }
}

/* Safari, Chrome and Opera > 12.1 */
@-webkit-keyframes fadein {
    from { opacity: 0; }
    to   { opacity: 1; }
}

/* Internet Explorer */
@-ms-keyframes fadein {
    from { opacity: 0; }
    to   { opacity: 1; }
}
```
### Continued development

I want to keep getting better at positioning, flexbox and animations.

## Author

- Frontend Mentor - [@Joffenhopland](https://www.frontendmentor.io/profile/Joffenhopland)

