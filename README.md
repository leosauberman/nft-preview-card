# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Links

- Solution URL: [Solution URL](https://github.com/leosauberman/nft-preview-card.git)
- Live Site URL: [Live site](https://leosauberman.github.io/nft-preview-card/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

During this project, I learned an important lesson about CSS transitions and animations. Initially, I tried using the `visibility` property for showing/hiding elements with transitions, but discovered it doesn't work well since `visibility` is a discrete property that can't be gradually animated. Instead, using `opacity` proved to be a much better solution as it supports smooth transitions between values. Here's an example of the improved implementation:
```css
.card__overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 255, 247, 0.5);
  pointer-events: none;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.card:hover .card__overlay {
  opacity: 1;
  pointer-events: auto;
}
```
