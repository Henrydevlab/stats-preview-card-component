# Stats preview card component

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![](./screenshot.png)

### Links

- Solution URL: [https://github.com/henrydevlab/stats-preview-card-component](https://github.com/henrydevlab/stats-preview-card-component)
- Live Site URL: [https://henrydevlab.github.io/stats-preview-card-component/](https://henrydevlab.github.io/stats-preview-card-component/)

## My process

### Built with

- Semantic HTML5 markup (including description lists for structured data mapping)
- CSS custom properties (Variables)
- CSS Flexbox (for overall page centering and card data distribution)
- Mobile-first workflow
- BEM (Block-Element-Modifier) Architecture for modular CSS structure

### What I learned

During this project, I strengthened my understanding of responsive design flow and image handling. Instead of manipulating complex background rules or adding unsemantic elements to implement color overlays, I learned to use `mix-blend-mode` combined with an explicit element background color. This mirrors professional Figma design specifications cleanly.

Here is the CSS rule implementation I used to achieve the exact overlay tint effect:

```css
.stats-card__image-wrapper {
  background-color: var(--clr-accent);
  position: relative;
}

.stats-card__image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  mix-blend-mode: multiply;
  opacity: 0.75;
}
```

I also learned how to implement a semantic description list `<dl>, <dt>, <dd>` rather than standard generic blocks to manage structured data metrics safely for screen readers and search engines:

```html
<dl class="stats-card__list">
  <div class="stats-card__stat-group">
    <dt class="stats-card__stat-value">10k+</dt>
    <dd class="stats-card__stat-label">companies</dd>
  </div>
</dl>
```

### Useful resources

- [MDN Web Docs - Description List Element](https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Elements/dl) - This reference page explains the exact semantic properties of `<dl>, <dt>, and <dd>`, which helped me build an accessible layout structure for data metrics.
- [MDN Web Docs - mix-blend-mode](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/Properties/mix-blend-mode) - A clear guide on applying blend modes to HTML elements, which helped me avoid using heavy, complex multi-layered background styles.

## Author

- Frontend Mentor - [@henrydevlab](https://www.frontendmentor.io/profile/henrydevlab)
- Twitter - [@henrydevlab](https://www.twitter.com/henrydevlab)