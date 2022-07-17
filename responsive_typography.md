# Modern CSS techniques for responsive typography

```css
:root {
	/* Similar numbering convetion as font-weight */
	--fs-xl: 5rem;
	--fs-600: 2rem;
	--fs-500: 1.25rem;
	/* fs-400 is the regular (or normal) font */
	--fs-400: 1rem;
}

@media (min-width: 40em) {
	:root {
		--fs-xl: 7rem;
		--fs-600: 3rem;
		--fs-400: 1.125rem;
	}
}
```

## Setting font size using _vw_ can be a mistake

```css
:root {
	--fs-xl: 15vw;
	/* Problem: In small screen size it's going to be really small and for ultra wide monitor, the font size will be extremely large */
	--fs-400: 2vw;
	/* Another problem is you can't zoom in or out */
	/* The texts set with vw doesn't change while zooming in or out */
}
```

## Solution using **clamp()** function

```css
:root {
	--fs-xl: clamp(3.5rem, 12vw + 1rem, 12rem);
}
```
