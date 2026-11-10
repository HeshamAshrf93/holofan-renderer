# holofan-renderer

Turn images, videos and 3D models into frames for an LED hologram fan (a spinning LED strip, also called a POV display).

> Status: early development.

## How it works

A hologram fan draws a picture by spinning a strip of LEDs very fast and changing their colours at exactly the right moment. To show an image, it has to be converted from normal x/y pixels into polar coordinates: for every angle of the blade, which colour each LED should show.

## Planned features

- [ ] Image to polar frames, configurable LED count and angular resolution
- [ ] Video to frame sequence
- [ ] Render a rotating 3D model (glTF) to frames
- [ ] Black-background handling so the content looks like it floats in the air
- [ ] Gamma and brightness correction for LEDs
- [ ] Export formats: binary frame files and C headers for microcontrollers (ESP32 / Arduino)
- [ ] Simulator that previews what the fan will show
- [ ] Command-line tool and Python API
- [ ] Automated tests for the coordinate maths

## Planned usage

```bash
holofan convert logo.png --leds 64 --angles 360 -o logo.bin
holofan preview logo.bin
```

## Roadmap

1. Project setup: packaging, CLI, tests, CI
2. Image to polar conversion
3. Preview simulator
4. Video support
5. 3D model rendering
6. LED correction
7. Microcontroller export
8. Docs and examples

## License

MIT, see [LICENSE](LICENSE).

---
Built by [Hesham Ashraf](https://www.linkedin.com/in/hesham-ashrf)
