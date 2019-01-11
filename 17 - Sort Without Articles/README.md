# We gonna be working with JS Arrays .sort method

We gonna be sorting this array. We have to sort them without **The**,**A**,**An**. Cause those are articles.

1.  We need to make `sortedBands` variable. We will take the bands and we are going to sort it. `.sort` will take a function where `(a,b)` will be the one who is sorting the list. Alphabetically or by size.

```javascript
const sortedBands = bands.sort(function(a, b) {
  //here will go the function
});
```

2. Now this will return the sorted list based on the starting letter.

````javascript
if (a > b) {
        return 1;
      } else {
        return -1;
      }```
````

3.  New function `strip` where with regular expression we can escape from **a**,**the**,**an**. `i` is where the case will be insensitive, regardless whether is capital or small letter and `.trim()` will make sure there is not any space after.
    `/^`_ means when its starts with_.

4.  This is the **Function where will be in short version**

```javascript
const sortedBands = bands.sort(function(a, b) {
  if (strip(a) > strip(b)) {
    return 1;
  } else {
    return -1;
  }
});
```

5. Put the list in to the DOM
   What this will do it takes the element it sets the `innerHTML` to be `sortedBands` but we want to `.map` trough each of those that will return Array so we want to `.join()` them.
