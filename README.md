# BMW 3D Showroom: interactive car experiences

This is a multi-car 3D showroom built with [three.js](https://threejs.org/). The start screen shows the dealer's lineup, and each car opens an interactive experience. It is a concept demo and is not affiliated with BMW AG. The figures shown are indicative.

**Cars:** BMW M4 Competition and BMW X5 xDrive40i. You can add more; see "Add a car" below.

## Features on each car
- A real 3D model split into parts, shown in a dark studio with paints, a turntable and a light sweep.
- The bonnet or tailgate opens on its hinge. On the M4, hotspots mark the S58 engine, turbos, intake, cooling, strut brace and fluids.
- Click a part to lift it out of the car to centre stage. Drag to rotate it. Its info card has a real photo, what the part does, what it is made of, and figures.
- The brake system is shown side by side: tyre, wheel, disc and caliper.
- The car can be taken apart (button, or by scrolling) and put back together.
- Step inside: the door opens, you can look around, and there is a live instrument cluster and a working in-car screen.
- Drive on a night highway with gear shifts, a head-up display and a synthesised engine sound.
- A configurator for paint, seat colour and caliper colour, where the camera flies to the part you are changing.
- Full technical data.
- A test-drive / sales-advisor request form. Requests are emailed through FormSubmit.

## Modes
- `index.html` shows the lineup, then the chosen car.
- `index.html?car=x5` goes straight to one car.
- `index.html?kiosk` is the showroom touchscreen mode. It has a fullscreen button and bigger buttons. After 60 s with no touches it resets and plays an attract loop (spin, take apart, reassemble), and after 3 minutes it returns to the lineup. The form becomes "Talk to a sales advisor".

## Set it up for a dealer
Edit `dealer.js` with the name, city, phone, address, and the email address that should receive leads. The first request triggers a one-time confirmation email from FormSubmit; click it to start receiving requests. Opened from disk (`file://`), the form only shows the confirmation screen and sends nothing.

## Add a car
Create `cars/<id>/` containing:
- `car.js`: texts, paints, parts, camera points, gearbox and sound
- `model.glb.js`: the embedded split model
- `images/`: photos with credits
- `thumb.jpg`

Then add the car to `cars/lineup.js`. The tools and a step-by-step checklist are in the `car-website` skill:
- `split_parts.mjs` for Sketchfab-style models
- `rca_to_parts.mjs` for BMW's official Ramses projects

## Credits
- **M4 model:** ["BMW M4 Competition M Package"](https://sketchfab.com/3d-models/bmw-m4-competition-m-package-5c0a2dafb1ad408d9fc9eeef9aee531b) by [SRT Performance](https://sketchfab.com/TheRealSRT), [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/).
- **X5 model:** ["BMW X5 (G05)"](https://github.com/bmwcarit/digital-car-3d) by BMW Car IT GmbH, [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/). It was assembled from the Ramses Composer project and split into parts.
- **Photos:** Wikimedia Commons. Each card shows its photographer and licence, and full details are in `cars/*/images/credits.json`.
- **Libraries and fonts:** three.js (MIT); Archivo and Inter (OFL).
