# 🔗 URL Shortener Microservice

This project is part of the freeCodeCamp Back End Development and APIs Certification.

## 📌 Overview

The URL Shortener Microservice allows users to input a valid URL and receive a shortened version. When the shortened URL is visited, it redirects the user to the original URL. The backend uses Node.js, Express, and MongoDB to store and retrieve the URLs.

## 🔍 Features

- Accepts a valid URL and returns a shortened numeric code.
- Validates the URL using DNS lookup.
- Redirects users when they visit the shortened URL.
- Uses MongoDB to store original and shortened URL mappings.

## 📡 API Endpoints

### `POST /api/shorturl`

Submit a URL to shorten.

**Request body:**
{
  "url": "https://www.example.com"
}

**Response:**
{
  "original_url": "https://www.example.com",
  "short_url": 1
}

If the URL is invalid:
{
  "error": "Invalid URL"
}

### `GET /api/shorturl/:short_url`

Redirects to the original URL associated with `short_url`.

**Example:**  
Request: `GET /api/shorturl/1`  
Redirects to: `https://www.example.com`

## ⚙️ Technologies Used

- Node.js
- Express.js
- MongoDB
- DNS module for URL validation

## 🛠️ Getting Started Locally

1. **Clone the repository**:
 ```bash
git clone https://github.com/giannis07/fcc_url_shortener_microservice.git
cd fcc_url_shortener_microservice
```

2. **Install dependencies**:
 ```bash
npm install
```

3. **Set up environment variables**:

Create a `.env` file in the root directory and add:
 ```bash
MONGO_URI=your-mongodb-connection-string
```

4. **Start the server**:
 ```bash
npm start
```

The server will be running on `http://localhost:3000` 

5. Use a tool like Postman or your browser to test:
 ```
- POST http://localhost:3000/api/shorturl  
- GET http://localhost:3000/api/shorturl/1
```


## 💻 Source Code

🔗 https://github.com/giannis07/fcc_url_shortener_microservice
