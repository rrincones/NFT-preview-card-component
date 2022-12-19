# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](images/screenshot.png)

### Links

- Solution URL: [Frontend Mentor](https://www.frontendmentor.io/solutions/nft-preview-card-component-bJf6zMFAkD)
- Live Site URL: [GitHub Pages Live Site](https://rrincones.github.io/NFT-preview-card-component/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

One thing I learned is to always include a height and width attribute in image tags as advised in the MDN documentation and elsewhere. Doing so prevents layout shifts when the page loads and thus contributes to a better user experience. I also learned to set the height to auto in my CSS in order to override the height attribute, which is in pixels, and make my image responsive. 

```html
<img class="avatar" width="132" height="132" src="images/image-avatar.png" alt="Jules Wyvern avatar">
```
```css
.avatar {
  width: 10%;
  height: auto;
  margin-right: 1rem;
  border: 1px solid white;
  border-radius: 50%;
  vertical-align: middle;
}
```
It took me a few hours of trial and error and research to also learn how to create the active state required for the main image. I ended up making a :hover pseudo class that, although applied to one element, triggers CSS changes to another once it's in the active state. You can see this below as the second ruleset applies to the .filter2 element, changing its opacity from 0 to 1 and the cursor to a pointer. 

```css
.filter2 {
  position: absolute;
  opacity: 0;
  background: hsl(178, 100%, 50%, 30%);
  width: 100%;
  height: 100%;
  border-radius: 1rem;
  transition-property: opacity;
  transition-duration: 0.2s;
  transition-timing-function: linear;
}

.filter:hover .filter2 {
  opacity: 1;
  cursor: pointer;
}
```

### Continued development

For future projects, I want to keep learning how to implement better solutions that lend to an optimal user experience. I also want to get better at thinking through all the technical details such as image optimization, SEO, and so on. But that'll come later. 

### Useful resources

- [Beginner's CSS Tutorial](https://www.youtube.com/watch?v=OXGznpKZ_sA) - Part 16 about images in this tutorial helped me during this project. 

## Author

- Frontend Mentor - [@rrincones](https://www.frontendmentor.io/profile/rrincones)

## Acknowledgments

Special thanks to [@Lixandro Beato](https://www.frontendmentor.io/profile/lixandro96), whose code I peeked at to figure out what I didn't know. 
