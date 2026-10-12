# blow-out-the-candles
An interactive birthday webpage featuring an animated cake, floating balloons, confetti and microphone-based candle blowing detection.

## About the Project

This project is a small birthday-themed web experience built with HTML, CSS and JavaScript. It combines animated decorations with a simple audio interaction to recreate the familiar tradition of blowing out birthday candles.

Press the microphone button, allow microphone access, and blow to extinguish the candle flame.

## Features

- **Interactive birthday cake:** A CSS-designed cake with multiple layers, icing, a plate and a candle.
- **Microphone-based interaction:** Uses the Web Audio API to analyse microphone input and detect sufficiently loud sounds.
- **Animated candle flame:** A flickering flame that disappears when the sound threshold is reached.
- **Floating balloons:** Colourful balloons with a continuous floating animation.
- **Falling confetti:** Automatically generated confetti with random positions, colours, sizes and animation speeds.
- **Custom styling:** A purple background, contrasting colours and Google Fonts typography.

## Technologies Used

- **HTML5** for the page structure.
- **CSS3** for styling, animations, and the cake design.
- **JavaScript** for microphone access, audio analysis and dynamic confetti generation.
- **Web Audio API** for processing microphone input.
- **MediaDevices API** for requesting microphone access.

## How to Run

1. Clone or download this repository.
2. Open `index.html` in a modern browser through a local development server.
3. Click the microphone button.
4. Grant microphone permission when prompted.
5. Blow towards your microphone and watch the candle flame disappear.

**Note:** Microphone access generally requires HTTPS or a trusted local development environment such as `localhost`. The browser must also support the required audio APIs.

## How It Works

When the user presses the button, the webpage requests microphone access and creates an audio analysis pipeline using the Web Audio API.

The JavaScript analyses incoming audio samples and calculates their average absolute deviation from the midpoint of the audio signal. When this value exceeds a predefined threshold, the cake receives a CSS class that hides the flame.

Meanwhile, CSS animations make the flame flicker and the balloons float. JavaScript generates the confetti elements when the page loads.

The sound detection is amplitude-based rather than a specialised blow-recognition system, so other sufficiently loud sounds may also extinguish the candle.

## Project Structure

```text
blow-out-the-candles/
└── index.html
```

The HTML file contains the page structure, CSS styles, and JavaScript functionality in a single file.

## Possible Improvements

- Add a replay button to relight the candle.
- Improve sound detection to reduce false triggers.
- Make the layout more responsive across mobile devices.
- Add personalised birthday messages and customisation options.

---

Created as a small creative project exploring interactive web development, CSS animations, and browser audio capabilities.
