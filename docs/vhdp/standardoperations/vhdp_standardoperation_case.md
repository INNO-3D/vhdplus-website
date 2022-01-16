---
id: case
title: Case and When
sidebar_label:  Case and When
---

## Definition

Executes an operation if the signal of case has the value of when.
All possible numbers defined by range must have one when, but you can add When (others) { null; }.

## Examples

```vhdp
Case (a) 
{ 
	When (0)           --a = 0
	{ 
		a := 1; 
	} 
	When (1 to 3)      --a = 1, 2, 3
	{ 
		a := a + 1; 
	} 
	When (4 | 6 | 8)   --a = 4, 6, 8
	{ 
		a := 0; 
	} 
	When (others)      --a = 5, 7, 9, ...
	{ 
		a := 0; 
	} 
}
```

<div class="fluidMedia"><iframe id="ytplayer" type="text/html" width="100%" src="https://www.youtube.com/embed/8wJt7V7Gpb4?autoplay=0&origin=http://vhdplus.com" frameborder="0" allowFullScreen></iframe></div>