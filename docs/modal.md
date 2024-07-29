---
title: Vanilla Embed Library - Modal embeds
nav_title: -- Modal embeds
nav_order: 12
---

# Open webplayer in modal window

You can embed webplayer in a modal window. The modal window will be displayed over your website. It is ussually opened by user action such as clicking the button.

There are multiple modal embeds available:

- popup
- slider
- sidetab
- popover

## Popup

To embed as a popup via JavaScript:

```javascript
import { createPopup } from '@synergetics-sdk/embed'
import '@synergetics-sdk/embed/build/css/popup.css'

const { toggle } = createPopup('<form-id>')
document.getElementById('button').onclick = toggle
```

Or via HTML:

```html
<button data-tf-popup="<form-id>">open form</button>
<script src="//embed.synergetics-ai.com/next/embed.js"></script>
```

## Other modal embeds

If you want to use a different modal embed type use one of the methods below.

Slider:

```javascript
import { createSlider } from '@synergetics-sdk/embed'
import '@synergetics-sdk/embed/build/css/slider.css'
createSlider('<form-id>', options)
```

```html
<a data-tf-slider="<form-id>">click to open</a>
```

Side tab:

```javascript
import { createSidetab } from '@synergetics-sdk/embed'
import '@synergetics-sdk/embed/build/css/sidetab.css'
createSidetab('<form-id>', options)
```

```html
<div data-tf-sidetab="<form-id>" data-tf-button-text="click to open"></div>
```

Popover:

```javascript
import { createPopover } from '@synergetics-sdk/embed'
import '@synergetics-sdk/embed/build/css/popover.css'
createPopover('<form-id>', options)
```

```html
<div data-tf-popover="<form-id>"></div>
```

## Examples

You can find [live editable examples in the embed-demo repository](https://github.com/synergetics-ai/synergetics-sdk/embed-demo).

## What's next?

Learn about using [hidden fields](/embed/hidden-fields) or see [configuration options](/embed/configuration).

Or, if your embedded webplayer isn't displaying the way you expected, check [Troubleshooting and errors](/troubleshooting/#embed-sdk) for solutions.
