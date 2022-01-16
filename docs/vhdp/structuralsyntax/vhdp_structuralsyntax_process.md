---
id: process
title: Process
sidebar_label:  Process
---

## Definition

In Process, you write your code. This code gets executed every CLK cycle.

A name can be assigned to a process.
In the brackets, variables can be declared that can be assigned and read only in this process (they can be declared in
the brace too).
In the brace, the code can be written. Only If, Else, Elsif, Case, When and For should be used in the brace.
See Thread for the other operations.

## Example
```vhdp
Process <Name> --(optional)
(
    VARIABLE var : NATURAL range 0 to 3 := 0;
)
{
    If (…)
    {
        …
    }
}
```

## Use different CLK
If you want to use a different CLK, surround your code with `If(rising_edge(YOURCLOCK)) { … }.`

```vhdp
Process <Name> --(optional)
(
    ...
)
{
    If(rising_edge(YOURCLOCK))
    {
        ...
    }
}
```

With If(null) you can use no clock for a process

```vhdp
Process <Name> --(optional)
(
    ...
)
{
    If(null)
    {
        ...
    }
}
```

<div class="fluidMedia"><iframe id="ytplayer" type="text/html" width="100%" src="https://www.youtube.com/embed/8wJt7V7Gpb4?autoplay=0&origin=http://vhdplus.com" frameborder="0" allowFullScreen></iframe></div>