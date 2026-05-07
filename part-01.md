# Part 01 — Event Bubbling

## What is Event Bubbling?

When an event fires — it travels up through every parent element.

```html
<div id="parent">
  <button id="btn">Click me</button>
</div>
```

```js
document.getElementById("btn").addEventListener("click", function() {
  console.log("button clicked")
})

document.getElementById("parent").addEventListener("click", function() {
  console.log("parent clicked")
})

// Click the button — both run:
// button clicked
// parent clicked
```

---

## stopPropagation()

Stops the event from bubbling up.

```js
document.getElementById("btn").addEventListener("click", function(e) {
  e.stopPropagation()
  console.log("button clicked") // only this runs ✅
})
```

---

## Connection to Event Delegation

Bubbling is what makes Event Delegation possible.

```js
document.getElementById("parent").addEventListener("click", function(e) {
  console.log(e.target) // exact element clicked ✅
})
```

---

## Quick Reference

| | Behavior |
|---|---|
| Default | Event bubbles up to every parent |
| stopPropagation() | Stops event from going up |
| e.target | The exact element clicked |

> JavaScript Events Series
