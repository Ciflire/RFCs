---
feature: changing slide side animation
start-date: 2024-06-16
author: Ciflire
---

# Summary

Trying to normalize the side parameter given to animation

# Motivation

I felt like the animation side is not consistent. To give an example I will be
using my configuration file:

```
animation=windowsIn, 1,2,windowIn, slide bottom
animation=windowsOut,1,2,windowOut, slide bottom
```

These two animation have the same side given, but one gives an animation that
slides **from** bottom **to** the center and the other gives an animation that
slides **from** center **to** bottom

This bothered me, so I decided i would make an RFC to get feedback on that, to
know if I am the only thinking that or not as I could get no feedback in the
discord.

# Detailed design

The other conception of it would be to think of a vector which to me feels more
intuitive when thinking of animation, and movement. Instead of thinking of a
fixed size.

# Examples and Interactions

The previous configuration would be rewritten into

```
animation=windowsIn, 1,2,windowIn, slide top
animation=windowsOut,1,2,windowOut, slide bottom
```

Where `top` and `bottom` give the direction of the window when going in or out.

# Drawbacks

People would have to change this in their entire config, could also be
counterintuitive to other people just as the way it is designed today is
counterintuitive to me
Having to change the actual implementation

# Alternatives

Keeping the way it is

# Prior art

This is already impleted

# Unresolved questions

Still no community feedback so I use this dedicated space to have some

# Future work

Feel free to criticize it, sorry for my English as well i'm not native, also
first time doing an RFC
