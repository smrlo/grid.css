# Grid.css

<a href="https://github.com/smrlo/grid.css/"><img src="https://badgen.net/badgesize/gzip/smrlo/grid.css/master/grid.min.css" /></a>

Grid.css is a ultra-lightweight and responsive CSS grid.

The goal of the project is to create a universal and easy-to-use responsive grid, with no-frills, that adds no unnecessary styles and with the mimimun footprint as possible - so as to be the base for any project.

Highlights:
- Ultra-lightweight (~0.6KB gzipped)
- No-frills, no unnecessary styles
- Very flexible and easy to use
- Responsive, mobile-first, flexbox based
- 12-column layout, with default and full-page width


## Installation

Include grid.css in your website's &lt;head&gt; before any other stylesheet:

```html
<link rel="stylesheet" href="grid.min.css">
```


## Setup

Grid.css has a responsive and mobile-first `12-column` layout, that can be set up with a default width or a full page width (see maximum width at the various breakpoint in the table below).

To set up the layout you first define the container, then within the container add the rows, and finally within each row add and define the columns.


#### 1. Start by adding the container

```html
<!-- default width -->
<div class="container">
  ...
</div>

<!-- full page width -->
<div class="container-full">
  ...
</div>
```


#### 2. Add as many rows as you need

```html
<div class="container">
  <div class="row">
    ...
  </div>
</div>
```


#### 3. Finally add and define the columns

To set up a column add the class `col` and then define the various column's size at the different breakpoints with `c-*`, `s-*`, `m-*`, `l-*`, `xl-*`, `xxl-*`.
Replace `*` with a number between `1-12` to define a specific column's width (e.g. c-2); use `0` to hide the column (i.e. c-0); or use `fx` for a flexible column (i.e. c-fx). The default size `c-*` must always be defined.

*Example: using `c-2` instructs the column to span for a width of 2 spaces; `c-5` instructs the column to span for a width of 5 spaces; `xl-2` instructs the column to span for a width of 2 spaces when the screen size is ≥1200px; using `xl-2 xxl-4` instructs the column to span for a width of 2 spaces when the screen size is ≥1200px, then 4 spaces when the screen size is ≥ 1400px.*

```html
<div class="container">
  <div class="row">
    <div class="col c-12 s-6 m-6 l-4 xl-4 xxl-6"> ... </div>
    <div class="col c-0 s-6 m-3 l-4 xl-4 xxl-6"> ... </div>
    <div class="col c-0 s-0 m-3 l-4 xl-4 xxl-0"> ... </div>
  </div>
</div>
```


## Breakpoints


#### Container max-width

|                   | <576px   | ≥576px   | ≥768px   | ≥992px   | ≥1200px  | ≥1400px  |
|-------------------|:--------:|:--------:|:--------:|:--------:|:--------:|:--------:|
| `container`       | 100%     | 540px    | 720px    | 960px    | 1140px   | 1320px   |
| `container-full`  | 100%     | 100%     | 100%     | 100%     | 100%     | 100%     |


#### Columns

| Column          | Screen size       |
| --------------- | :---------------: |
| `c-*`           | default           |
| `c-*`           | <576px            |
| `s-*`           | ≥576px            |
| `m-*`           | ≥768px            |
| `l-*`           | ≥992px            |
| `xl-*`          | ≥1200px           |
| `xxl-*`         | ≥1400px           |


## Contributing

Contributing guideline: be kind, be helpful.

Found a bug or have any suggestions? Please [open a new issue](https://github.com/smrlo/grid.css/issues).


## License

Released under the [MIT License](https://github.com/smrlo/grid.css/blob/main/LICENSE).
