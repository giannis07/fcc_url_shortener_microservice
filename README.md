# 🔗 URL Shortener Microservice

This project is part of the [freeCodeCamp Back End Development and APIs Certification](https://www.freecodecamp.org/learn/back-end-development-and-apis/back-end-development-and-apis-projects/url-shortener-microservice).

## 📌 Overview

A simple API that allows users to shorten URLs. Given a valid URL, the service returns a short URL ID which can be used to redirect to the original link.

## 🔍 Features

- Accepts valid HTTP/HTTPS URLs via POST request  
- Stores and retrieves shortened URLs  
- Redirects to original URL using short ID  

## 📡 API Endpoints

### `POST /api/shorturl`

Send a URL to be shortened:

Request body:
{
  "url": "https://example.com"
}

Response:
{
  "original_url": "https://example.com",
  "short_url": 1
}

### `GET /api/shorturl/:short_url`

Redirects the user to the original URL associated with the short ID.

Example:  
GET /api/shorturl/1 → Redirects to https://example.com

## ⚙️ Technologies Used

- Node.js  
- Express.js  
- body-parser  

## 💻 Source Code

🔗 [GitHub Repository](https://github.com/giannis07/fcc_url_shortener_microservice)

## 🛠️ Getting Started Locally

1. Clone the repository:
 ```bash
git clone https://github.com/giannis07/fcc_url_shortener_microservice.git  
cd fcc_url_shortener_microservice
```

2. Install dependencies:
 ```bash
npm install
```

3. Start the server:
 ```bash
npm start
```

4. Use a tool like Postman or your browser to test:
 ```
- POST http://localhost:3000/api/shorturl  
- GET http://localhost:3000/api/shorturl/1
```

