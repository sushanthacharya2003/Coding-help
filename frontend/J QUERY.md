J QUERY

setup

Alright bro, let’s get you set up **clean and fast** — no over-engineering, no drama.
Here’s the **ultimate beginner-friendly setup guide** for both **jQuery** and **SCSS**.

---

# ✅ **1. jQuery Setup (Two Ways)**

## **A. Quickest Way — CDN (just copy-paste)**

Drop this inside your `<head>` OR before `</body>`:

```html
<script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
```

Boom. jQuery is ready.
Use it like:

```js
$(document).ready(function() {
  console.log("jQuery loaded!");
});
```

### When to use CDN?

✔ Small projects
✔ Learning
✔ No build tools
✔ Works instantly

---

## **B. Local File (Offline)**

1. Go to jQuery download page
2. Download **minified** version
3. Put it in your project folder
4. Link it:

```html
<script src="./js/jquery.min.js"></script>
```

### Folder structure:

```
project/
 ├─ index.html
 ├─ js/
 │   └─ jquery.min.js
```

---

## **C. Using jQuery with Node + bundlers (Optional)**

If you ever use Webpack/Vite:

```
npm install jquery
```

Then in JS:

```js
import $ from "jquery";

$(function() {
  console.log('jQuery ready');
});
```

---
---

# ⭐ **1. Selecting Elements**

### jQuery

```js
$('.item')
$('#id')
$('div ul li')
```

### Vanilla JS

```js
document.querySelectorAll('.item')
document.getElementById('id')
document.querySelector('div ul li')
```

✔ **Shortcut:** `$()` is basically a global querySelector on steroids.

---

# ⭐ **2. Ready Function**

### jQuery

```js
$(function() {
    // DOM loaded
});
```

### Vanilla JS

```js
document.addEventListener('DOMContentLoaded', () => {
    // DOM loaded
});
```

✔ **Shortcut:** No verbose event listener. Super handy.

---

# ⭐ **3. Quick Show/Hide/Toggle**

### jQuery

```js
$('.box').show();
$('.box').hide();
$('.box').toggle();
```

### Vanilla JS

```js
document.querySelector('.box').style.display = 'block';
document.querySelector('.box').style.display = 'none';
element.style.display = element.style.display === 'none' ? 'block' : 'none';
```

✔ **Shortcut:** Built-in animations + less code.

---

# ⭐ **4. Add / Remove Classes**

### jQuery

```js
$('p').addClass('active');
$('p').removeClass('active');
$('p').toggleClass('active');
```

### Vanilla JS

```js
document.querySelector('p').classList.add('active');
document.querySelector('p').classList.remove('active');
document.querySelector('p').classList.toggle('active');
```

✔ Vanilla JS caught up here — but jQuery is still cleaner and supports older browsers.

---

# ⭐ **5. GET / POST Requests**

### jQuery

```js
$.get('/api/data', function(res) {
    console.log(res);
});

$.post('/send', {name: "Sush"}, function(res){
    console.log(res);
});
```

### Vanilla JS

```js
fetch('/api/data')
  .then(res => res.json())
  .then(data => console.log(data));

fetch('/send', {
    method: 'POST',
    body: JSON.stringify({name: "Sush"}),
    headers: {'Content-Type': 'application/json'}
})
.then(res => res.json())
.then(data => console.log(data));
```

✔ jQuery is **way shorter** for AJAX.

---

# ⭐ **6. Animate Anything Easily**

### jQuery

```js
$('.box').fadeIn();
$('.box').fadeOut();
$('.box').slideUp();
$('.box').slideDown();
```

### Vanilla JS

You’d need CSS + JS combinations — no simple one-liner.

✔ Animation helpers = one of the biggest reasons jQuery stayed popular.

---

# ⭐ **7. Event Binding**

### jQuery

```js
$('button').click(function() {});
$('.item').on('mouseenter', function() {});
```

### Vanilla JS

```js
document.querySelector('button').addEventListener('click', () => {});
document.querySelector('.item').addEventListener('mouseenter', () => {});
```

✔ Cleaner syntax + supports live event binding.

---

# ⭐ **8. Looping Over Elements**

### jQuery

```js
$('li').each(function() {
    console.log($(this).text());
});
```

### Vanilla JS

```js
document.querySelectorAll('li').forEach(li =>
    console.log(li.textContent)
);
```

✔ Again, smaller syntax + consistent across browsers.

---

# ⭐ Bonus: **Chaining**

jQuery:

```js
$('.box')
  .addClass('active')
  .fadeIn()
  .slideUp()
  .fadeOut();
```

Vanilla JS:
lol, good luck writing chainable animation libraries by hand.

---

# 🔥 So can jQuery replace plain JS?

**No. Plain JS has caught up.

