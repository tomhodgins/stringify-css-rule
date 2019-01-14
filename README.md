# stringify-css-rule

Convert a CSS rule object to a string of text with JavaScript in the browser environment.

## about

When working in the browser environment with HTML and XML, the DOM can be stringified into text using things like [`innerHTML`](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML), [`outerHTML`](https://developer.mozilla.org/en-US/docs/Web/API/Element/outerHTML), and [`XMLSerializer`](https://developer.mozilla.org/en-US/docs/Web/API/XMLSerializer), but no equivalent functions exist for converting a CSS rule found in CSSOM into a string. That's what this module provides, and it only works in the browser environment.

## usage

This software is distributed as an ES module and should work in all modern browsers (including Chrome/Safari/Edge/Firefox).

```html
<style>a { --b: c; }</style>

<script type=module>
  import stringifyRule from 'https://unpkg.com/stringify-css-stylesheet/index.js'

  // Log the stringified CSSStyleRule object to the console
  console.log(
    stringifyRule(document.styleSheets[0].cssRules[0])
  )
</script>
```