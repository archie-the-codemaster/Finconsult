# Finconsult prototype

## Project structure

- `html/index.html` — page structure and content
- `css/styles.css` — visual styling and responsive layout
- `js/app.js` — application behaviour and AI-provider integrations
- `assets/finconsult-logo.png` — application logo

## Run locally

From the `Finconsult` project directory, start a local static server:

```sh
python -m http.server 8000
```

Then open <http://localhost:8000/html/> in your browser. The HTML page loads its stylesheet, JavaScript, and logo from the sibling `css`, `js`, and `assets` directories.

Some browser configurations restrict API requests from pages opened directly with `file://`, so using the local server is recommended.

## AI configuration and security

Choose Ollama, Google Gemini, or an OpenAI-compatible provider in the app settings. API keys are held in browser memory rather than saved in local storage, but a front-end demo cannot keep keys secret: browser users and network requests can expose them. Use a backend proxy for any public deployment, and avoid entering real personal or financial information during testing.
