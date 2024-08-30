# Maintaining *GITADORA FUZZ-UP*

We are currently focused on maining the *DrumMania* half of *Fuzz-Up*.

## Game Setup

We follow the instructions at [this Emulink post](https://www.emuline.org/topic/3757-arcade-pc-gitadora-collection-original-overdrive-tri-boost-reevolve-matixx-exchain-nexage-high-voltage-fuzz-up-konami/).

## E-Amusement Server

We incorporate [an ongoing fork](https://github.com/wz18207/bemaniutils-gfdm) (as of M08 30 2024) of [`bemaniutils`](https://github.com/DragonMinded/bemaniutils) that supports *Fuzz-Up* into [our own fork](https://github.com/rg-mit/bemaniutils/tree/wz18207-trunk).
If `bemaniutils-gfdm` gets updated, merge the changes from their `trunk` branch into our `wz18207-trunk` branch, and then merge `wz18207-trunk` into `rg-mit`.

For the `server.yaml`, make sure that `support.gitadora` is a truth value, i.e.:
```yaml
support:
  gitadora: true
```

Once the server is running, you'll need to add an arcade machine to the database. You can do that by navigating to the "Arcades" page in the admin dashboard.
Make sure the name of the shop in the admin dashboard is the same as inputted in the debug options.

## E-Kit

Kyle (@supersonichub1) bought a used [Alesis DM5 Kit](https://www.alesis.com/products/view/dm5-kit) off Craigslist for the installation.
The [drum module](https://www.alesis.com/products/view/dm5-drum-module) outputs MIDI.
With a DIN-to-USB adapter (to be purchased) and spice2x's support for MIDI controllers, we'll use the e-kit as a controller.
