# Background Meteors

Dimension is so important to a beautiful website application. This project enhances the visual appeal of web applications by integrating a dynamic and colorful background beam animation. 

[Aceternity](https://ui.aceternity.com/) is similar to [Framer Motion](https://www.framer.com/motion/) (which is still an amazing animation library) but better. Instead of needing to install an entire package to utilize every animation component, Aceternity allows for full customization of components that are open source.

## Features

- **Dynamic Beams**: The beams are animated to create a vibrant and engaging background.
- **Enhanced Visibility**: The beams are more visible and bolder, ensuring they stand out and catch the eye.
- **Extended Length**: The beams are longer, adding a dramatic effect to the background.
- **Colorful Animation**: A spectrum of colors is used in the beams to create a lively and colorful animation.

## Installation

To install and integrate the background beams into your project, follow these steps:

Integrating into your web project:

```
npm i framer-motion clsx tailwind-merge
```

Add to your Tailwind CSS plugin for variable classes, a utils file, a standalone file for the BackgroundBeams, and then calling it in your Hero or any other section as background!

```Typescript
"use client";
import React from "react";
import { BackgroundBeams } from "../ui/background-beams";

export function BackgroundBeamsDemo() {
  return (
    <div className="h-[40rem] w-full rounded-md bg-neutral-950 relative flex flex-col items-center justify-center antialiased">
      <BackgroundBeams />
    </div>
  );
}
```


## Customization
You can customize the beams by adjusting the following CSS variables:

**Beam Color:** Beam Color: Change the colors of the beams to fit your theme by modifying the stopColor properties in the motion.linearGradient components.
```javascript
<motion.linearGradient
  ...
>
  <stop stopColor="#18CCFC" stopOpacity="0"></stop>
  <stop stopColor="#18CCFC"></stop>
  <stop offset="32.5%" stopColor="#6344F5"></stop>
  <stop offset="100%" stopColor="#AE48FF" stopOpacity="0"></stop>
</motion.linearGradient>
```

**Beam Width:** Adjust the width of the beams by changing the strokeWidth property in the motion.path components.
```typescript
<motion.path
  ...
  strokeWidth="0.5"
></motion.path>
```

**Beam Speed:** Control the animation speed of the beams by modifying the duration and delay properties in the motion.linearGradient transition settings.
```javascript
<motion.linearGradient
  ...
  transition={{
    duration: Math.random() * 10 + 10,
    ease: "easeInOut",
    repeat: Infinity,
    delay: Math.random() * 10,
  }}
>
```


### Enjoy the dynamic and colorful background beams, and happy coding!
