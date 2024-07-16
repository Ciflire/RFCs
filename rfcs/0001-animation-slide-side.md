---
feature: changing slide side animation
start-date: 2024-06-16
author: Ciflire
---

# Summary

This RFC aims to agree on a rule for forced side option of the slide animation style

# Motivation

The way the animation `slide` is used feels inconsistent in two ways at the moment i'm writing this:
- First, it describes a side that can be the side by which the animation starts as well as its end. For example the keyword `bottom` used for animation `windowsIn` will move the window **from** the bottom to the desired position and for the animation `windowsOut` the window will be slided to the bottom of the screen
- Secondly, following that logic, the keyword `bottom` would be used to make the window pop from the bottom and close sliding to the bottom. The same keyword is then used for two different visual results.
This RFC will allow to write the documentation as clear as possible without having to detail each case, or by try and fail by the user

# Detailed design

The new design for the forced side

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
counterintuitive to me Having to change the actual implementation

# Alternatives

Keeping the way it is

# Prior art

This is already impleted

# Unresolved questions

Still no community feedback so I use this dedicated space to have some

# Future work

Feel free to criticize it, sorry for my English as well i'm not native, also
first time doing an RFC
