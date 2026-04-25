# Frontend Mentor - Recipe page solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### Screenshot

![](./screenshot.jpg)

### Links

- Solution URL: [Github Project](https://github.com/GuilleMiranda/frontendmentor_recipe-page-main)
- Live Site URL: [Live Site URL](https://guillemiranda.github.io/frontendmentor_recipe-page-main/)

## My process

### Built with

- Semantic HTML5 markup (header, aside, main, section)
- CSS custom properties (variables for colors and consistent styling)
- Mobile-first workflow
- Responsive design with media queries
- CSS Grid for page layout
- HTML definition lists (dl, dt, dd) for structured content

### What I learned

**Planning HTML structure before CSS is crucial:** I learned that taking time to think through the HTML structure from the start saves time later. Instead of using divs for everything, I chose semantic elements based on their meaning: `<header>` for introductory content, `<aside>` for supplementary information (preparation time), `<main>` for primary content, and `<section>` for content grouping. This foundational decision made CSS styling more intuitive and the code more maintainable.

**Semantic vs. layout purposes in HTML:** A key insight was understanding that HTML serves two purposes:

- **Semantic:** Using `<dl>` for definitions, `<time>` for time values, `<h1>` for main heading—these convey meaning to browsers, screen readers, and other tools
- **Layout:** Using flexbox, grid, padding, and margins in CSS to arrange elements visually

For example, I used `<aside>` for the preparation time not because it visually floats to the side (that's CSS's job), but because the content is supplementary to the main recipe. This separation of concerns makes code cleaner and more professional.

**CSS best practices I applied:**

- **Use CSS custom properties (variables)** for colors and repeated values—makes design systems maintainable
- **Use flexbox/grid for layout** instead of floats or absolute positioning—cleaner and more responsive
- **Mobile-first approach** with base styles for mobile and media queries only for desktop changes—easier to maintain
- **Avoid putting presentation in HTML**—let CSS handle spacing, alignment, and styling completely
- **Target specific elements precisely** (like `header > h1`) rather than overly broad selectors—prevents unexpected style conflicts

**CSS pseudo-elements (::after, ::before, ::marker):** I discovered how powerful pseudo-elements are for adding content and styling without cluttering HTML. I used them throughout this project to:

- Add separators and formatting with `::after` (e.g., adding ": " after definition terms)
- Style bullet points with `::marker` to change color and size of list markers
- Create visual separators between table rows

```css
dt::after {
  content: ": "; /* Adds colon after each term */
}

dt::marker {
  color: var(--rose-800); /* Styles the bullet point */
  font-size: 0.75rem;
}

dd::after {
  content: "\A"; /* Adds line break */
  white-space: pre;
}
```

**Definition lists (<dl>) for semantic structure:** I learned that `<dl>` elements are perfect for structured key-value data like preparation times and nutrition facts. Using `<dt>` for terms, `<dd>` for descriptions, and styling them properly with CSS is much better than divs or other generic elements.

**box-sizing: border-box is essential:** Understanding `box-sizing: border-box` changed how I think about layouts. It ensures that padding and borders are included in the element's total width and height, making calculations predictable and preventing unwanted overflow:

```css
* {
  box-sizing: border-box; /* Width includes padding + border */
}
```

Without this, adding padding to a 100% width element would break layouts. With it, everything stays where it should be.

**CSS custom properties (variables) for consistency:** Using CSS variables like `--brown-800` and `--rose-800` made it easy to apply the same colors throughout and maintain a consistent design system.

### Continued development

- Explore CSS Grid more deeply for complex layouts
- Practice accessibility features like focus states and color contrast
- Learn how to implement animations and transitions
- Work with more advanced responsive design patterns

### AI Collaboration

I used GitHub Copilot throughout this project. It helped me:

- Clarify semantic HTML structure decisions
- Troubleshoot responsive design challenges
- Think through CSS approach alternatives
- Validate my solutions and suggest improvements

The AI was especially helpful in guiding my thinking rather than just giving me answers—it asked clarifying questions that helped me understand _why_ certain approaches work better than others.

## Author

- Frontend Mentor - [@GuilleMiranda](https://www.frontendmentor.io/profile/GuilleMiranda)
- GitHub - [Guille Miranda](https://www.github.com/GuilleMiranda)
