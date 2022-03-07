---
layout: page
title: Overlay CSS guide
permalink: /overlay/
---

The overlay is built up with flexbox in this simple structure and these generic classes

```css
.overlay
  .overlay__item
    .overlay__label
    .overlay__value
  .overlay__item
    .overlay__label
    .overlay__value
```

Each `overlay__item` also contains a unique class for each supported data set.

- `.overlay__loggingToggle`
- `.overlay__sessionTime`
- `.overlay__huntingSet`
- `.overlay__killCount`
- `.overlay__totalLoot`
- `.overlay__totalSpend`
- `.overlay__returnTotal`
- `.overlay__returnPercent`
- `.overlay__numGlobals`
- `.overlay__numHofs`
- `.overlay__evadePercent`

### Special cases
`.overlay__sessionTime`
- Includes a `.overlay__sessionTimeToggle` inside the `.overlay__value` for starting/stopping the logger

`.overlay__huntingSet`
- Includes a `select` inside the `.overlay__value` for weapon selection

## Super basic examples which may help you get started

Want to learn more about CSS? [W3 Schools](https://www.w3schools.com/css/default.asp)

**Increase label text size and make it bold.**

```css
.overlay__label {
  font-size: 20px;
  font-weight: bold;
}
```

**Increase value text size**

```css
.overlay__value {
  font-size: 20px;
}
```

**Increase both label and value text size**

```css
.overlay__label,
.overlay__value {
  font-size: 20px;
}
```

**Make value text color green** ([Need help with hex colors?](https://www.w3schools.com/colors/colors_hexadecimal.asp))

```css
.overlay__label {
  color: #00ff00;
}
```

**Make background color red** ([Need help with hex colors?](https://www.w3schools.com/colors/colors_hexadecimal.asp))

```css
body {
  background-color: #ff0000;
}
```

**Make the label be on top**

```css
.overlay__label {
  flex: 1;
  order: 1;
}

.overlay__value {
  flex: 0;
}
```

**Custom order** (you need to specify order for EACH value available)

```css
.overlay__killCount {
  order: 1;
}

.overlay__sessionTime {
  order: 2;
}
```
