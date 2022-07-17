# min(), max() and clamp() functions

Website for [Moderen CSS Solutions](https://moderncss.dev/).  
Website for [Utopia Fluid Type Scale](https://utopia.fyi/). This website has type scale calculator.

## min() function

### Widths with **min()**

```css
.container {
	/* Choose smaller of the two options. */
	/* When it gets smaller, it follows the 90% but when we reach the max size, it locks in at 1000px */
	/* Chooses the smaller between 90% of the parent, or viewport, and 1000px */
	width: min(90%, 1000px);

	/* margin-inline sets the left and the right margin only and not the top and the bottom margin. */
	/* Here, auto puts auto margin on the left and right which centers the div */
	margin-inline: auto;
}
```

## max() function

### Margin and padding with **max()**

```css
.background {
	/* Chooses the bigger value of the two options. */
	/* Increasing the viewport height will increase the margin as 3vh will be greater the 1rem */
	/* At somepoint, 1rem becomes greater thann 3vh as the viewport height decreases which will then lock the padding to 1rem */
	/* The padding will stop shrinking after it locks to 1rem */
	/* The 2nd value in padding, 1.5rem, sets the left and the right margin to 1.5rem */
	padding: max(3vh, 1rem) 1.5rem;

	/* Similar with the margin bottom */
	margin-bottom: max(5vh, 2rem);
}
```

## clamp() function

### Typography with **clamp()**

```css
h2 {
	/* Min size is set as 3rem, max size is 5rem, and the ideal size 10vw + 1rem will increase or decrease the font size */
	font-size: clamp(3rem, 10vw + 1rem, 5rem);
}
```
