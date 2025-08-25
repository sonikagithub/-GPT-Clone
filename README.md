Chat-GPT Clone 

A full-stack Chat-GPT–style app built with React, Node.js, Express, Tailwind CSS, and the OpenAI API.

Table of Contents

Overview

Features

Tech Stack

Project Structure

Prerequisites

Getting Started

Configuration

Run the App

Usage

Troubleshooting

Contributing

License

Overview

Fenil-GPT is a lightweight Chat-GPT clone. The React client offers a responsive, friendly UI and streams responses; the Node/Express server securely proxies requests to the OpenAI API. Styling is done with Tailwind CSS.

Features

Interactive conversations with an OpenAI model

Real-time client ↔ server communication

Tailwind-powered modern UI

Environment-based configuration with .env

Dev-friendly with Vite (client) and Nodemon (server)

Tech Stack

Client: React, Vite, Tailwind CSS
Server: Node.js, Express, dotenv, cors, body-parser, node-fetch
Dev tools: Nodemon

Project Structure
.
├─ client/            # React + Vite app
│  ├─ src/
│  ├─ index.html
│  └─ tailwind.config.js
├─ server/            # Express API server
│  ├─ app.js
│  └─ .env            # OPENAI_API_KEY lives here (not committed)
└─ README.md

Prerequisites

Node.js (LTS recommended)

An OpenAI API key

Getting Started

Clone the repo

git clone https://github.com/sonikagithub/-GPT-clone.git
cd Chat-GPT-Clone


Install dependencies

Server

cd server
npm i express body-parser cors dotenv node-fetch
npm i -D nodemon


Client

cd ../client
npm i react react-dom
# Tailwind setup is required (see below)


Tailwind CSS (client)
Follow the official guide for Vite: https://tailwindcss.com/docs/guides/vite

(Initialize Tailwind, add the content paths, include @tailwind base; @tailwind components; @tailwind utilities; in your main CSS.)

Configuration

Create a .env file inside server/:

# server/.env
OPENAI_API_KEY=your_openai_api_key_here
PORT=5000


(Optional) If your client needs to know the API base URL at build time, create client/.env:

# client/.env
VITE_API_BASE_URL=http://localhost:5000


Keep .env files out of version control.

Run the App

Server

cd server
# package.json script example:
# "dev": "nodemon app.js"
npm run dev
# Expected: "Server is running..." on http://localhost:5000


Client

cd client
# package.json script example:
# "dev": "vite"
npm run dev
# Vite will print a local URL (e.g., http://localhost:5173)


You should see terminal outputs similar to:

Server


Client


Usage

Start server and client.

Open the client URL in your browser.

Enter a prompt and send—responses stream back in real time from the server via the OpenAI API.


Server is running on PORT you expect (5000 by default).

cors() middleware is enabled on the server.

Tailwind styles not applying

Confirm tailwind.config.js content paths include your index.html and all src/**/*.{js,ts,jsx,tsx} files.

Ensure Tailwind directives are imported in your main CSS.

Contributing

Contributions are welcome!

Fork the repo

Create a feature branch (feat/your-feature)

Commit, push, and open a PR

License

This project is open-source. If you add a specific license, include it here (e.g., MIT).
