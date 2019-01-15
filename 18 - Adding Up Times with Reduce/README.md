#Adding up Time with `Reduce`

Add up total min and hours in total and on the and Console log it.
We will pull the data out of the DOM and convert them in to a min and hours.

We are going to use `reduce`.

1. We will see the `map` and `reduce`.
2. And just `reduce`.

First like always select the nodes

```javascript
const timeNodes = document.querySelectorAll("[data-time]");
```

Now you need to convert this from NodeList to actual array of actual time string. You have 2 ways to do it.

```javascript
(...document.querySelectorAll("[data-time]"))
```

```javascript
Array.from(document.querySelectorAll("[data-time]"));
```

This code here will convert NodeList in to an Array

```javascript
 .map(node => node.dataset.time)
```

This code here will turn in to just seconds

```javascript
.map(timeCode => {
   const [mins, secs] = timeCode.split(':').map(parseFloat);
```

Mora da koristime `.map(parseFloat)` za da konventira `strings` to `numbers`
