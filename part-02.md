# Part 02 — setTimeout & setInterval

## setTimeout() — run once after a delay

```js
setTimeout(function() {
  console.log("runs after 2 seconds")
}, 2000)
```

2000 = 2 seconds in milliseconds.

---

## setInterval() — run repeatedly

```js
setInterval(function() {
  console.log("runs every 2 seconds")
}, 2000)
```

Keeps running until stopped.

---

## clearTimeout() — cancel setTimeout

```js
let timer = setTimeout(function() {
  console.log("hello")
}, 2000)

clearTimeout(timer) // cancelled ✅
```

---

## clearInterval() — stop setInterval

```js
let interval = setInterval(function() {
  console.log("hello")
}, 2000)

clearInterval(interval) // stopped ✅
```

---

## Real World Examples

```js
// show popup after 3 seconds
setTimeout(function() {
  document.getElementById("popup").classList.add("show")
}, 3000)

// live clock — updates every second
setInterval(function() {
  let time = new Date().toLocaleTimeString()
  document.getElementById("clock").innerText = time
}, 1000)
```

---

## Quick Reference

| Method | Runs | Stop with |
|--------|------|-----------|
| setTimeout() | Once after delay | clearTimeout() |
| setInterval() | Repeatedly | clearInterval() |

> JavaScript Events Series
