---
version: 2
project: 2
name: "Test example Project 2"
description: "Change this to name your audience and describe how your design should feel to them."
tokensFile: "tokens.css"
colors:
  defaultText: "var(--primary-text)"
  defaultBackground: "var(--primary-background)"
  action: "var(--action)"
  hover: "var(--action-hover)"
  buttonText: "var(--button-text)"
  alternateText: "var(--alternate-text)"
  alternateBackground: "var(--alternate-background)"
  alternateAction: "var(--alternate-action)"
  alternateHover: "var(--alternate-action-hover)"
  alternateButtonText: "var(--alternate-button-text)"
typography:
  rootSizeSource: "html font-size in tokens.css"
  bodyFamily: "var(--base-family)"
  headingFamily: "var(--headings-family)"
  bodySize: "var(--text-size-md)"
  smallSize: "var(--text-size-sm)"
  bodyLineHeight: "var(--line-height-base)"
  headingLineHeight: "var(--line-height-headings)"
textScale:
  xs: "var(--text-size-xs)"
  sm: "var(--text-size-sm)"
  md: "var(--text-size-md)"
  lg: "var(--text-size-lg)"
  xl: "var(--text-size-xl)"
  2xl: "var(--text-size-2xl)"
  3xl: "var(--text-size-3xl)"
headingSizes:
  h1: "var(--text-size-2xl)"
  h2: "var(--text-size-xl)"
  h3: "var(--text-size-lg)"
  h4: "var(--text-size-lg)"
  h5: "var(--text-size-md)"
  h6: "var(--text-size-md)"
spacing:
  base: "var(--space-unit)"
  space-1: "var(--space-1)"
  space-2: "var(--space-2)"
  space-3: "var(--space-3)"
  space-4: "var(--space-4)"
  space-6: "var(--space-6)"
  space-8: "var(--space-8)"
  space-12: "var(--space-12)"
  space-16: "var(--space-16)"
  space-24: "var(--space-24)"
  space-32: "var(--space-32)"
layout:
  pageWidth: "var(--page-width)"
  gridGap: "var(--grid-gap)"
  sectionSpacing: "var(--section-spacing)"
  contentPadding: "var(--content-padding)"
---

# Design system

## Overview

Change this to name your audience and describe how your design should feel to them.

This guide describes the choices in tokens.css. Use the CSS variables above rather than copying their values. Keep design.md and tokens.css in your project folder, and link tokens.css before your own stylesheet on every page. Add page-specific styling in your own stylesheet.

## Colors

Use `var(--primary-text)` on `var(--primary-background)` for the default palette. Add the alternate class to use `var(--alternate-text)` on `var(--alternate-background)`.

Default links and button backgrounds use `var(--action)` and `var(--action-hover)`; button text uses `var(--button-text)`. In alternate areas, use `var(--alternate-action)`, `var(--alternate-action-hover)`, and `var(--alternate-button-text)`. Keep links underlined.

### Contrast targets

Aim for WCAG AAA contrast for normal text; WCAG AA is the minimum. Check these text/background pairings, including hover states:

- `var(--primary-text)` on `var(--primary-background)`
- `var(--action)` on `var(--primary-background)`
- `var(--action-hover)` on `var(--primary-background)`
- `var(--button-text)` on `var(--action)`
- `var(--button-text)` on `var(--action-hover)`
- `var(--alternate-text)` on `var(--alternate-background)`
- `var(--alternate-action)` on `var(--alternate-background)`
- `var(--alternate-action-hover)` on `var(--alternate-background)`
- `var(--alternate-button-text)` on `var(--alternate-action)`
- `var(--alternate-button-text)` on `var(--alternate-action-hover)`

## Typography

Use `var(--base-family)` for body text and `var(--headings-family)` for headings. Body text uses `var(--text-size-md)`, small text uses `var(--text-size-sm)`, and each heading uses its selected variable in headingSizes above.

Use `var(--line-height-base)` for body line height and `var(--line-height-headings)` for heading line height. The html rule in tokens.css sets the root size; rem-based sizes scale from it. The form's xxl and xxxl labels correspond to --text-size-2xl and --text-size-3xl.

## Spacing and layout

Use the spacing variables listed above. Each --space-N token is a multiplier of `var(--space-unit)`.

- `var(--page-width)`: maximum page width.
- `var(--grid-gap)`: space between grid items, not around the grid.
- `var(--section-spacing)`: space between sections.
- `var(--content-padding)`: padding inside sections, outside a nested grid.

Read tokens.css to see which spacing step each layout variable uses. Text wraps within its containing element; there is no separate line-length variable.

## Do and Don't

### Do

- Use the same tokens.css on every page to keep the design consistent.
- Reuse the CSS variables for colors, typography, spacing, and layout.
- Use headings in order, beginning with one page-title h1.
- Keep underlined links and visible keyboard focus.

### Don't

- Add one-off design values when an existing variable fits.
- Rely on color alone to communicate meaning.
- Change a design choice in only one exported file. Update the form and export a fresh set of files when the design changes.
