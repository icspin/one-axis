# One Axis

An equatorial telescope mount can only do one thing: turn one axis at one
constant speed. That is enough to track the entire sky, but only if you live
on a rotating sphere. This tool puts the same mount in both worlds, side by
side, and lets you drive the comparison live.

Live at https://icspin.github.io/one-axis/

## What it argues

- The polar axis tilt equals your latitude, everywhere, and flips to a second
  celestial pole south of the equator. A flat plane has one center and no
  second pole.
- One motor with three constant switch positions (15.041, 15.000, 14.492
  arcsec per second) tracks stars, Sun, and Moon. The gaps between those
  numbers are the year and the month.
- Long exposures: clean circles about the pole at altitude = latitude on the
  globe; distorted, non-closing sweeps around a misplaced hub over a plane.
- An alt-az mount needs two continuously varying rates and the eyepiece field
  still twists. All rates on screen are computed from the live geometry.

## Running

Single file, entirely client side. Three.js is pinned from a CDN, so it needs
a network connection. Serve the repo root with any static server:

    python -m http.server 8000

Keys: 1 to 6 run the demonstrations, space pauses, R resets, arrows nudge
latitude. Drag rotates both views together.

The build number lives in the footer. It increments on every deploy; if the
footer disagrees with what you expect, you are looking at a cached copy.
