# Using SVGs

Example:

```hbs
<span class="icon is-small is-svg is-dark-grey">
  {{inline-svg "icons/pro"}}
</span>
```

When adding new SVGs, make sure not to rely on stroked paths. If colour override classes are used (e.g. `is-light-purple`, `is-success`), all path strokes will be removed. Instead, use a filled path or polygon. See `core/_icon.scss` for the relevant rules.

Make sure that all new SVGs have a `viewbox`, and ensure that there's no `width` or `height` attribute. These settings are required for cross-browser compatibility. You can use [svgo](https://github.com/svg/svgo) to do this for you. 

`svgo --disable=removeViewBox ./icons/*.svg`
