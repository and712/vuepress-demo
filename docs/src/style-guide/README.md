---
sidebar: auto
---

# Style Guide



## Theme colors

We use a subset of all colors to create a smaller color palette for generating color schemes, also available as Sass variables and a Sass map in Bootstrap's `scss/_variables.scss` file.


## All colors

All Bootstrap colors are available as Sass variables and a Sass map in `scss/_variables.scss` file. To avoid increased file sizes, we don't create text or background color classes for each of these variables. Instead, we choose a subset of these colors for a [theme palette](#theme-colors).

Be sure to monitor contrast ratios as you customize colors. As shown below, we've added three contrast ratios to each of the main colors—one for the swatch's current colors, one for against white, and one for against black.



## Core concepts

- **Breakpoints are the building blocks of responsive design.** Use them to control when your layout can be adapted at a particular viewport or device size.

- **Use media queries to architect your CSS by breakpoint.** Media queries are a feature of CSS that allow you to conditionally apply styles based on a set of browser and operating system parameters. We most commonly use `min-width` in our media queries.

- **Mobile first, responsive design is the goal.** Bootstrap's CSS aims to apply the bare minimum of styles to make a layout work at the smallest breakpoint, and then layers on styles to adjust that design for larger devices. This optimizes your CSS, improves rendering time, and provides a great experience for your visitors.

## Available breakpoints

Bootstrap includes six default breakpoints, sometimes referred to as _grid tiers_, for building responsively. These breakpoints can be customized if you're using our source Sass files.



### Min-width

Bootstrap primarily uses the following media query ranges—or breakpoints—in our source Sass files for our layout, grid system, and components.

```scss
// Source mixins

// No media query necessary for xs breakpoint as it's effectively `@media (min-width: 0) { ... }`

// Usage

// Example: Hide starting at `min-width: 0`, and then show at the `sm` breakpoint

```

These Sass mixins translate in our compiled CSS using the values declared in our Sass variables. For example:

```scss
// X-Small devices (portrait phones, less than 576px)
// No media query for `xs` since this is the default in Bootstrap

// Small devices (landscape phones, 576px and up)

```

### Max-width

We occasionally use media queries that go in the other direction (the given screen size *or smaller*):

```scss
// No media query necessary for xs breakpoint as it's effectively `@media (max-width: 0) { ... }`

```

These mixins take those declared breakpoints, subtract `.02px` from them, and use them as our `max-width` values. For example:

```scss
// `xs` returns only a ruleset and no media query
// ... { ... }

// `sm` applies to x-small devices (portrait phones, less than 576px)

```

