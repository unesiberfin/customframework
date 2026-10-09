# Custom Framework

A lightweight custom CSS framework built with Sass. It provides a consistent visual theme for common HTML elements and reusable utility classes for spacing, typography, color, and borders.

## Features

- Custom styling for standard HTML elements
- Reusable utility classes
- Sass variables for customization
- Modular Sass partial structure
- Styled buttons, forms, tables, typography, and lists
- Compiled CSS for easy use

## Project Structure

```text
_variables.scss
_base.scss
_typography.scss
_buttons.scss
_forms.scss
_tables.scss
_utilities.scss
main.scss
main.css
main.css.map
index.html
README.md
```

## Installation

Download or clone the repository.

To customize and compile the Sass source, install Dart Sass:

```bash
npm install --global sass
```

Include the compiled CSS file inside the `<head>` section of your HTML file:

```html
<link rel="stylesheet" href="main.css">
```

The browser only needs the compiled `main.css` file to use the framework.

## Usage

The framework automatically styles standard HTML elements such as headings, paragraphs, links, lists, buttons, forms, inputs, and tables.

For example:

```html
<h1>Page Title</h1>

<p>This is a paragraph using the custom framework.</p>

<button>Default Button</button>

<input type="text" placeholder="Enter your name">
```

The framework also includes additional button styles:

```html
<button class="btn-secondary">
  Secondary Button
</button>

<button class="btn-outline">
  Outline Button
</button>
```

Utility classes can be combined with HTML elements for additional styling:

```html
<p class="text-primary fw-bold">
  Primary bold text
</p>

<div class="p-2 m-2 border rounded">
  Utility class example
</div>
```

## Utility Classes

### Text Colors

- `.text-primary`
- `.text-secondary`
- `.text-dark`
- `.text-light`

### Background Colors

- `.bg-primary`
- `.bg-secondary`
- `.bg-light`
- `.bg-white`

### Font Weight

- `.fw-light`
- `.fw-normal`
- `.fw-medium`
- `.fw-bold`

### Font Size

- `.fs-small`
- `.fs-base`
- `.fs-large`

### Margin

- `.m-0`
- `.m-1`
- `.m-2`
- `.m-3`
- `.mt-1`
- `.mt-2`
- `.mt-3`
- `.mb-1`
- `.mb-2`
- `.mb-3`

### Padding

- `.p-0`
- `.p-1`
- `.p-2`
- `.p-3`
- `.pt-1`
- `.pt-2`
- `.pt-3`
- `.pb-1`
- `.pb-2`
- `.pb-3`

### Borders

- `.border`
- `.border-0`
- `.rounded`

## Customization

The framework can be customized by editing the Sass variables inside `_variables.scss`.

Available variables include colors, typography, spacing, and border settings.

Example:

```scss
// Colors
$primary-color: #4f46e5;
$secondary-color: #6b7280;
$text-color: #222222;
$background-color: #ffffff;
$light-color: #f3f4f6;
$border-color: #d1d5db;

// Typography
$font-family: Arial, sans-serif;

$font-size-small: 0.875rem;
$font-size-base: 1rem;
$font-size-large: 1.25rem;

// Spacing
$spacing-1: 0.5rem;
$spacing-2: 1rem;
$spacing-3: 1.5rem;

// Borders
$border-radius: 0.5rem;
$border-width: 1px;
```

For example, changing:

```scss
$primary-color: #4f46e5;
```

to:

```scss
$primary-color: #008000;
```

will update the primary color used throughout the framework after Sass is compiled again.

## Sass Structure

The framework is organized into Sass partials and combined through `main.scss`.

- `_variables.scss` — global Sass variables
- `_base.scss` — base styles and layout
- `_typography.scss` — headings, paragraphs, and lists
- `_buttons.scss` — buttons and button variations
- `_forms.scss` — form controls and form elements
- `_tables.scss` — table styles
- `_utilities.scss` — reusable utility classes
- `main.scss` — imports all Sass partials

The `main.scss` file includes:

```scss
@import "variables";
@import "base";
@import "typography";
@import "buttons";
@import "forms";
@import "tables";
@import "utilities";
```

After changing the Sass files, compile `main.scss` to generate an updated `main.css`:

```bash
sass main.scss main.css
```

During development, Sass can automatically recompile whenever a source file changes:

```bash
sass --watch main.scss:main.css
```

## Compiled CSS

A compiled version of the framework is included as:

```text
main.css
```

This allows the framework to be used directly in HTML without requiring Sass.

## Demo

Open `index.html` in a browser to view examples of:

- Typography
- Buttons
- Forms
- Tables
- Text and background colors
- Font weights and font sizes
- Margin and padding utilities
- Border utilities