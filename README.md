# Lisper - Random Secrets App

Lisper is a simple web application that fetches and displays random secrets using the **Secrets API**. Built with **Express.js**, it uses **EJS** for dynamic templates and **Axios** for API requests.

---

## Features
- Fetches random secrets from the [Secrets API](https://secrets-api.appbrewery.com/random).
- Renders secrets and usernames dynamically on the homepage.
- Serves static files from the `public` directory.

---

## How It Works
1. **Server**:
   - The app runs an Express server listening on port `3000`.
   - The server handles a `GET` request to the `/` route:
     - It fetches a random secret from the Secrets API using Axios.
     - The secret and username are passed to the `index.ejs` template.

2. **Frontend**:
   - The `index.ejs` file dynamically renders:
     - A secret in a styled card.
     - The username below the secret.
     ![HomePage Screenshot](public/images/demo1.PNG)
     - To view the secret hover over the card with the image.
     ![Secret display Screenshot](public/images/demo2.PNG)

3. **Static Files**:
   - CSS and other assets are served from the `public` folder.

---


---

## Prerequisites
- [Node.js](https://nodejs.org/) (v14+)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/JemoGithirwa4/Lisper.git
   cd lisper
2. Install dependencies:
   ```bash
   npm install

## Usage

1. Start the server:
   ```bash
   node app.js

2. Open your browser and go to:
   `http://localhost:3000`

## API Usage
**Secrets API**
- The app fetches data from the Secrets API.
- **Endpoint:** https://secrets-api.appbrewery.com/random
- **Example Response:**
- {
  "id": "12345",
  "secret": "This is a random secret.",
  "username": "anonymous_user",
  "date": "2025-01-01T00:00:00Z"
}

## Dependencies
- **Express:** Web framework for server-side functionality.
- **Axios:** HTTP client for API calls.
- **EJS:** Templating engine for dynamic page rendering.