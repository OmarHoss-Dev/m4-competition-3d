# M4 Competition: interactive 3D car experience

A single-page 3D car showcase built with [three.js](https://threejs.org/). This is a concept demo and is not affiliated with BMW AG. The figures on the page are indicative.

## What it does

- A real 3D car, pre-split into 70 parts, in a dark studio with a turntable, light sweep and 7 paints (with or without the M livery).
- The bonnet swings open on its hinge. Hotspots mark the S58 engine, twin turbos, intake, cooling pack, strut brace and fluids.
- Clicking a part lifts it out of the car. It flies to centre stage (drag to rotate) and an info card shows a real photo, what it does, what it is made of and its key figures.
- The brake system is shown side by side: tyre, forged wheel, carbon-ceramic disc and caliper.
- "Take it apart" (button, or scroll through Anatomy) explodes the car into its components with labels, then reassembles it.
- "Step inside" opens the door and moves the camera to the driver's seat, with free look, a live instrument cluster, cabin hotspots and an in-car screen (M Setup, live data, vehicle status).
- Drive mode takes the wheel on a night highway: throttle, brake, 8-speed shifts, a head-up display and shift lights.
- The engine sound is synthesised live with Web Audio: cold start, revs, limiter, gear-change cracks, turbo flutter and overrun crackle.
- The configurator covers paint, seat upholstery and caliper colour, and the camera flies to the part you are changing.
- A full technical data section.
- The test-drive booking form is front end only. Connect it to a form service before real use.

## Run it

Open `index.html` in a browser. It works straight from disk, because the model is embedded in `models/bmw_m4.glb.js`. An internet connection is needed for three.js and the fonts (both loaded from a CDN).

## Deploy

It is a static site with no build step. On Netlify, publish the repository root; `netlify.toml` is already set up.

## Credits

- **3D model:** ["BMW M4 Competition M Package"](https://sketchfab.com/3d-models/bmw-m4-competition-m-package-5c0a2dafb1ad408d9fc9eeef9aee531b) by [SRT Performance](https://sketchfab.com/TheRealSRT), licensed [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/). It was split into parts and compressed for this site.
- **Photos:** from Wikimedia Commons. Each photo's author and licence are shown on its card, and full details are in `images/credits.json`:
  Wikisympathisant (CC BY-SA 4.0), Tommi Nummelin (CC BY-SA 3.0), Liftarn (CC BY 3.0), Tokumeigakarinoaoshima (CC BY-SA 4.0), Julian Herzog (CC BY 4.0), Damian B Oh (CC BY-SA 4.0), LuvsMG481 (CC BY-SA 4.0), Duboyong (CC BY-SA 4.0), M3C30 (CC BY-SA 4.0).
- **Libraries and fonts:** three.js (MIT); Archivo and Inter from Google Fonts (OFL).

`source-assets/` (the original model, the uncompressed split and the earlier code-built version) is kept locally and is not published.
