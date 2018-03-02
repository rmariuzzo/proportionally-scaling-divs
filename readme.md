# Proportionally Scaling Divs with CSS

## Proportionally Scaling by Width

By declaring its width to be proportional to the window's width, and giving it a bottom padding that's also sized proportionally to the window's width, the div's width and calculated height (the latter created by the bottom padding) will both resize and maintain relative proportions to each other in sync with changes to the window's width.

### DEMO: http://codepen.io/jtheletter/pen/cFBLG

```
.proportional {
  background-color: yellow;

  padding-bottom: 25%;
  /* Can be any %, 0–∞. */
  /* Percentage is relative to container or window width. */
  /* Increase for a taller div. */
  /* Match width above for a square. */

  position: absolute;
  /* Can be absolute, fixed, or relative. */

  width: 25%;
  /* Can be any %, 0–∞. */
  /* Percentage is relative to container or window width. */
}

<div class="proportional"><div>
```

## Proportionally Scaling by Height

The child element's width and height are set to `1em`. The size of one em is then defined in the parent element as `font-size`, and the height of the parent is defined to match.

This assures that the child div will retain its proportions as it expands to fill the height of the parent div.

### DEMO: http://codepen.io/jtheletter/pen/jbNWqE

```
.wrap {
  background-color: yellow;
  font-size: 250px;
  height: 250px;
}
.circle {
  background-color: gray;
  border-radius: 50%;
  height: 1em;
  width: 1em;
}

<div class="wrap">
  <div class="circle"></div>
</div>

```
