# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- Image should be brought to the same color variation as it is on the challenge

### Screenshot

![Design screenshot](https://github.com/TheCoder-Rahul/fontend_mentor_stats_preview_card/blob/main/project_screenshot.png)

### Links

- 👉 [Solution URL](https://github.com/TheCoder-Rahul/fontend_mentor_stats_preview_card.git)
- 👉 [Live Site URL](https://thecoder-rahul.github.io/fontend_mentor_stats_preview_card/)

## My process

### Built with

- 👉 **Markup:** Semantic HTML5 for better accessibility and SEO.
- 👉 **Styling:** CSS3 with Custom Properties (variables) for a maintainable color scheme, font-properties, and different sizes.
- 👉 **Layout:** CSS Grid (Grid Template Areas) for the main layout and Flexbox for internal component alignment.
- 👉 **Workflow:** Mobile-first approach and Responsive Design using Media Queries.

### What I learned

Check my code snippets below:

```html
<article class="insight_summary__card">
  <section class="insight_summary__card_img">
    <img class="mob_img" src="images/image-header-mobile.jpg" alt="Project Discussion for Business Growth" loading="lazy">
    <img class="dsk_img" src="images/image-header-desktop.jpg" alt="Project Discussion for Business Growth" loading="lazy">
  </section>
  <section class="insight_summary__card_cont">
    <h1 class="insight_summary__card_title">Get <span>insights</span> that help your business grow.</h1>
    <p class="insight_summary__card_details">Discover the benefits of data analytics and make better decisions regarding revenue, customer experience, and overall efficiency.</p>
    <section class="insight_summary__card_metrics">
      <div class="insight_summary__card_companies">
        <h2 class="insight_summary__card_metrics__number">10k+</h2>
        <p class="insight_summary__card_metrics__context">companies</p>
      </div>
      <div class="insight_summary__card_templates">
        <h2 class="insight_summary__card_metrics__number">314</h2>
        <p class="insight_summary__card_metrics__context">templates</p>
      </div>
      <div class="insight_summary__card_queries">
        <h2 class="insight_summary__card_metrics__number">12M+</h2>
        <p class="insight_summary__card_metrics__context">queries</p>
      </div>
    </section>
  </section>
</article>
```
```css
@import url('https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,100..900&family=Lexend+Deca&display=swap');
:root {
  --navy-950: hsl(233, 47%, 7%);
  --pure-white: hsl(0, 0%, 100%);
  --blue-950: hsl(244, 37%, 16%);
  --purple-500: hsl(277, 64%, 61%);
  --light-white: hsla(0, 0%, 100%, 0.6);
  --para-white: hsla(0, 0%, 100%, 0.75);
  --para-font: "Inter", sans-serif;
  --heading-font: "Lexend Deca", sans-serif;
}
*, *::before, *::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-size: 0.9375rem;
  color: var(--light-white);
  font-family: var(--para-font);
  background-color: var(--navy-950);
}
main {
  display: flex;
  min-height: 100dvh;
  align-items: center;
  justify-content: center;
}
img {
  width: 100%;
  height: auto;
  display: block;
}
.insight_summary__card {
  overflow: hidden;
  border-radius: 0.5rem;
  width: min(70rem, 85%);
  background-color: var(--blue-950);
}
.insight_summary__card_img {
  position: relative;
  background-color: var(--purple-500);
}
.insight_summary__card_img img {
  opacity: 0.8;
  mix-blend-mode: multiply;
}
.insight_summary__card_img .dsk_img {
  display: none;
}
.insight_summary__card_cont {
  padding: 2rem;
  text-align: center;
}
.insight_summary__card_cont :is(h1, h2) {
  color: var(--pure-white);
}
.insight_summary__card_title {
  line-height: 1.2;
  margin-bottom: 1.5rem;
  font-family: var(--heading-font);
  font-size: clamp(1.5rem, calc(2vw + 1.125rem), 2.25rem);
}
.insight_summary__card_title span {
  color: var(--purple-500);
}
.insight_summary__card_details, .insight_summary__card_metrics__context {
  line-height: 1.5;
  margin-bottom: 2rem;
  color: var(--light-white);
}
.insight_summary__card_metrics__context {
  margin-bottom: 0;
  letter-spacing: 1px;
  font-size: 0.75rem;
  text-transform: uppercase;
  font-family: var(--heading-font);
}
.insight_summary__card_metrics {
  gap: 2rem;
  display: flex;
  align-items: center;
  flex-direction: column;
}
.insight_summary__card_metrics__number {
  margin-bottom: 0.5rem;
}
.attribution { font-size: 0.6875rem; text-align: center; position: absolute; inset: auto 0 0; }
.attribution a { color: hsl(228, 45%, 44%); }

@media (min-width: 768px) {
  .insight_summary__card {
    display: flex;
  }
  .insight_summary__card_cont, .insight_summary__card_img {
    flex: 1 1 50%;
  }
  .insight_summary__card_img {
    order: 2;
  }
  .insight_summary__card_img .mob_img {
    display: none;
  }
  .insight_summary__card_img .dsk_img {
    display: block;
  }
  .insight_summary__card_cont {
    display: flex;
    text-align: left;
    flex-direction: column;
    justify-content: center;
    padding: 2rem 6rem 2rem 5rem;
  }
  .insight_summary__card_metrics {
    gap: 4rem;
    margin-top: 2rem;
    flex-direction: row;
  }
}
```

## Author

- 👉 GitHub - [TheCoder-Rahul](https://github.com/TheCoder-Rahul)
- 👉 Frontend Mentor - [@TheCoder-Rahul](https://www.frontendmentor.io/profile/TheCoder-Rahul)
- 👉 LinkedIn - [@Rahul Kumar](https://www.linkedin.com/in/rahul-the-developer/)