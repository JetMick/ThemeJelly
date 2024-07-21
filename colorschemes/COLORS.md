# Color schemes

Inspired by the [Zorin OS](https://zorin.com/os/) [color schemes](https://github.com/ZorinOS/zorin-desktop-themes)

---

**Template Colors:**

<img src="./../images/colorschemes/electric-cyan.png" alt="default" width="40%"/>

<img src="./../images/colorschemes/blue.png" alt="blue" width="40%"/>

<img src="./../images/colorschemes/coral.png" alt="coral" width="40%"/>

<img src="./../images/colorschemes/gray.png" alt="gray" width="40%"/>

<img src="./../images/colorschemes/green.png" alt="green" width="40%"/>

<img src="./../images/colorschemes/purple.png" alt="purple" width="40%"/>

<img src="./../images/colorschemes/red.png" alt="red" width="40%"/>

<img src="./../images/colorschemes/yellow.png" alt="yellow" width="40%"/>

---

### Custom colors

To add the theme to Jellyfin, copy the following line to Dashboard > General > Custom CSS:

`@import url('https://cdn.jsdelivr.net/gh/stpnwf/ZestyTheme@latest/theme.css');`

**If** you didn't like any of the presets and would like to have custom colors, replace the R, G, B values and paste it **underneath** the theme's `@import...` line:

```
:root {--accent: R, G, B;}
:root {--accent-off: R, G, B;}
:root {--dark: R, G, B;}
:root {--darkest: R, G, B;}
:root {--dark-highlight: R, G, B;}
:root {--dark-apparent: R, G, B;}
```

**Then** use a color picker on the *background color* anywhere in Settings or Dashboard, set `--dark-apparent` to that value, and save it. **Now you are done.**

If you don't do this, the backdrop gradient will not blend perfectly into the background on *mobile*. The background color is affected by the `--accent` color, so `--dark apparent` needs to be calculated for every color combination, hence why I made the presets...

If you'd like to make your own custom login wallpaper to match it, in line with the ones I made, follow the instructions in `images/colorschemes/base.svg` and add this following line as well:

`#loginPage {background: url(link-to-your-image-goes-here) !important;}`


---

Notes: 

 Check `theme.css` to see what each color does.
 
 Lighter `--accent` colors work better, as colorful colors will make the background color look very saturated, since the accent color is overlayed on top of the background.
 
