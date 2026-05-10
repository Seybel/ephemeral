# Basic Web Dev Arena Template

A single-file HTML template for building interactive web applications using vanilla HTML, CSS, and JavaScript.

## Requirements

- Docker and Docker Compose installed on your machine

## Running the Project

### Option 1: Docker Compose (Recommended)

```bash
docker compose up
```

Then open [http://localhost:8080](http://localhost:8080) in your browser.

To stop the server, press `Ctrl+C` or run:

```bash
docker compose down
```

### Option 2: Docker CLI

```bash
docker build -t web-app .
docker run -p 8080:80 web-app
```

Then open [http://localhost:8080](http://localhost:8080) in your browser.

### Option 3: Without Docker

If you don't have Docker, you can open `index.html` directly in your browser, or use any local server:

```bash
# Python 3
python -m http.server 8080

# Node.js (if npx available)
npx serve .
```

## Project Structure

```
├── index.html          # All your code goes here (HTML + CSS + JS)
├── Dockerfile          # Container configuration
├── docker-compose.yml  # Easy container orchestration
└── README.md
```

## Adding Libraries

Since this project uses vanilla JS without npm, include libraries via CDN links directly in `index.html`:

```html
<!-- CSS libraries go in <head> -->
<script src="https://cdn.tailwindcss.com"></script>

<!-- JS libraries go before closing </body> -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
```

See the comments in `index.html` for more library examples.
