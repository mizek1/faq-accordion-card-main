# Frontend Mentor - 3-column preview card component solution

This is a solution to the [FAQ accordion card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/faq-accordion-card-XlyjD0Oam).

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

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- See hover states for all interactive elements on the page
- Hide/Show the answer to a question when the question is clicked

### Screenshot

<center>

![Screenshot-1](./images/screenshot-1.png)
<br/>
Desktop design

![Screenshot-2](./images/screenshot-2.png)
<br/>
Mobile design

</center>

### Links

- Solution URL: [Here!](https://github.com/mizek1/faq-accordion-card-main)
- Live Site URL: [Here!](https://mizek1.github.io/faq-accordion-card-main/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Responsive design with media query
- Mobile first

### What I learned

Not very satisfied with this one, but I will try to improve it ASAP. I'm happy that I didn't have to use Javascript to do the accordions!

Some snippets:

> I used `details` and `summary` to do the accordion without Javascript:

```html
<details class="card__collapse">
    <summary class="card__question">
        How many team members can I invite?
    </summary>
    <div class="card__answer">
        You can invite up to 2 additional users on the Free plan. There is
        no limit on team members for the Premium plan.
    </div>
</details>
```

> This CSS part was very cool to do:

```css
  &__collapse {
    width: 100%;
    color: var(--very-dark-grayish-blue);
    padding-bottom: 1.5em;
    border-bottom: 1px solid var(--light-grayish-blue);
    
    &:not(:first-child) {
      padding-top: 1.5em;
    }

    &:last-child {
      margin-bottom: 1.5em;
    }
    
    &[open] {
      transition: all 1.5s ease-in-out;
      .card__question {
        font-weight: 700;
        color: var(--dark-blue);
      }
    }
  }
  
  &__question {
    font-size: 1.15em;
    cursor: pointer;
    position: relative;

    &:hover {
      color: var(--soft-red);
    }

    &::after {
      content: url(images/icon-arrow-down.svg);
      position: absolute;
      right: 0;
    }
  }
```

### Continued development

Need to learn to use images in a best way.

## Author

- Website - [Danilo Alves](https://github.com/mizek1)
- Frontend Mentor - [@mizek1](https://www.frontendmentor.io/profile/mizek1)
