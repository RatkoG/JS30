# When you move your cursor on top of the window the shadow follows you around.

So for now we gonna listen for mouse move on `hero`, also we gonna grab the `text` that is inside of that `hero`.

```javascript
const hero = document.querySelector(".hero");
const text = hero.querySelector("h1");
```

## Function Shadow

```javascript
function shadow(e){
  TODO:Magic is here
}
```

To make the magic happen we need some specific data. We're going to need the width & height of the hero div along with the current location of the mouse.

```javascript
const { offsetWidth: width, offsetHeight: height } = hero;
let { offsetX: x, offsetY: y } = e;
```

There is some odd behaviour caused by the bubbling nature of JavaScript. When the mouse hovers over any children of the hero div the event fires as though the width & height of the child is the correct area. This is not what we want. Instead, we will normalize it so that it ignores mousemove events on children.

```javascript
if (this !== e.target) {
  x = x + e.target.offsetLeft;
  y = y + e.target.offsetTop;
}
```

Then in our shadow() function:

```javascript
//calculate the maximum movements that we want to happen (total set above)
const xMovement = (x / width) * movement - movement / 2;
const yMovement = (y / width) * movement - movement / 2;
```

Now we can use these values to style the text shadow:

```javascript
text.style.textShadow = `${xMovement}px ${yMovement}px 0 red`;
```

## What we need to listen for:

```javascript
hero.addEventListener("mousemove", shadow);
```
