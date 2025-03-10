# SynthMind

## Overview
This AI-powered SaaS application leverages **Next.js, Node.js, PostgreSQL, LangChain, and OpenAI API** to provide AI-driven responses while supporting user authentication and backend logic.

## Features
- **User Authentication**: Secure registration and login using bcrypt and JWT.
- **AI Integration**: Uses LangChain and OpenAI API for AI-driven responses.
- **PostgreSQL Database**: Stores user data securely.
- **RESTful API**: Node.js backend with Express for handling AI queries and authentication.

## Tech Stack
- **Frontend**: Next.js (React framework)
- **Backend**: Node.js with Express
- **Database**: PostgreSQL
- **AI Model**: OpenAI API with LangChain
- **Authentication**: JWT & bcrypt

## Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/)
- [PostgreSQL](https://www.postgresql.org/download/)

## Setup & Installation

### 1. Clone the Repository
```sh
git clone https://github.com/harsh16629/SynthMind.git
cd SynthMind
```
### 2. Backend Setup
``` sh
mkdir server
cd server
npm init -y
```
### 3. Install Dependencies
``` sh
npm install express cors dotenv pg bcrypt jsonwebtoken langchain openai
```
### 4. Configure Environment Variables
- Create a .env file in the server/ directory and add:
  ``` sh
  DATABASE_URL=postgres://yourusername:yourpassword@localhost:5432/yourdatabase
  OPENAI_API_KEY=your-openai-api-key
  JWT_SECRET=your-jwt-secret
  PORT=5000
  ```
  Replace placeholders with actual values.
### 5. Set Up PostgreSQL Database
``` sh
psql -U yourusername -d postgres
CREATE DATABASE yourdatabase;
```
### 6. Start the Server
``` sh
node index.js
```
Server will run at ```http://localhost:5000```

## API Endpoints
### 1. User Authentication
- Register User
  Endpoint: ```POST /api/register```
  ```json
  {
  "email": "test@example.com",
  "password": "password123"
  }
  ```
### 2. Login User
- Endpoint: POST /api/login
  ```json
  {
  "email": "test@example.com",
  "password": "password123"
  }
  ```
- Response:
  ```json
  {
  "token": "your-jwt-token"
  }
  ```
## AI Interaction
### 1. AI Query
- Endpoint: POST /api/ai
  ```json
  {
  "prompt": "Tell me a joke"
  }
  ```
- Response:
  ```json
  {
  "response": "Sure! Here's a joke..."
  }
  ```

## License
This project is licensed under the MIT [Lcense](License).
