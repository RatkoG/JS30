# Sega za sega treba da naprajme 3 raboti:

1.  Get our elements
2.  Build out functions
3.  Hook up the event listeners

### Ova e da funkcijata

```javascript
function togglePlay() {
  if (video.paused) {
    video.play();
  } else {
    video.pause();
  }
}
```

### Use ternary operator

```javascript
function togglePlay() {
  const method = video.paused ? "play" : "pause";
  video[method]();
}
```

Ova e da go pretvori vo cel broj. Zosto ke dobijash String.

```javascript
parseFloat(this.dataset.skip);
```

#CHALLENGE
Add a button for full screen. And when it gets clicked make it full screen.
