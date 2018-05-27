# Magnifx JS

Magnifx JS is a simple, lightweight JS plugin that adds a magnifying glass style zoom functionality to images. It is a useful feature to have for product images on ecommerce websites, or if you just want people to be able to zoom into an image without spawning additional overlays or popup windows that may cover your content. Magnifx JS is based on vanilla JS version of [Magnify JS](https://github.com/TrySound/magnify).

## Getting Started

### Step 1: Link the required files

```html
<link rel="stylesheet" href="/css/magnifx.css">
<script src="/js/magnifx.js"></script>
```

You have complete control over the style and size of the lens by modifying `magnifx.css`. It is recommended to load the JavaScript file at the bottom just before the closing `</body>` tag if possible.

### Step 2: Specify the large image

The URI to the large image can be placed in the `data-magnifx-src` attribute (as shown below) or passed as the `src` option when calling the `.magnifx()` function.

```html
<img src="/images/product.jpg" data-magnifx-src="/images/product-large.jpg">
```

If the `data-magnifx-src` attribute or `src` option is not used, then Magnifx JS will try to grab the large image from the parent `<a>` tag, e.g.:

```html
<a href="/images/product-large.jpg">
  <img src="/images/product.jpg">
</a>
```

### Step 3: Call the magnifx() function

Make sure this comes after the required JavaScript file from Step 1 is loaded.

```html
<script>
magnifx('img')
</script>
```

Calling the `magnifx()` function with options:

```html
<script>
magnifx('img', {
  speed: 200,
  src: '/images/product-large.jpg'
})
</script>
```

## Options

Options can be set using data attributes or passed in an `options` JavaScript object when calling `magnifx()`. For data attributes, append the option name to "data-magnifx-" (e.g., `data-magnifx-src="..."`).

Name    | Type    | Default | Description
--------| ------- | ------- | -----------
`debug` | boolean | false   | Toggle activity logging in the console.
`speed` | number  | 100     | The fade-in/out animation speed in ms when the lens moves on/off the image.
`src`   | string  | ''      | The URI of the large image that will be shown in the magnifying lens.

## Installation

Choose from one of the following methods:

- `git clone https://github.com/pemre/magnifx.git`
- `npm install magnifx`
