# Quiz

Prototype of a quiz game in [p5.js](https://p5js.org/), with a planned integration with the Firebase Realtime Database. The project is incomplete: right now there is only a single hard-coded question (a riddle) rendered on screen along with the name/answer fields, but the "Enviar" (Submit) button doesn't process the answer (the logic is commented out in the code) and the `Contestant` class is still empty.

## Technologies

- p5.js and p5.dom (via CDN) for drawing and UI elements
- p5.play.js included in the repository
- Firebase (app + realtime-database, via CDN) configured in `index.html`, but with the initialization partially commented out

## Structure

- `sketch.js` — p5.js `setup()`/`draw()`, creates the canvas and instantiates `Quiz`
- `js/Quiz.js` — class that starts displaying the question
- `js/Question.js` — creates the DOM elements for the question, options and answer form
- `js/Contestant.js` — empty class (skeleton not yet implemented)
- `p5.play.js` — p5 sprite library

## How to run

Open `index.html` directly in the browser or serve the folder with a static server (e.g. `npx serve .`). There is no build step or `package.json` — all dependencies are loaded via `<script>` tags in the HTML.
