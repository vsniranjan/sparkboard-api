
# Sparkboard API

A simple REST API for managing and sharing ideas. Built with Node.js, Express, and MongoDB.

## Features

- Create, read, update, and delete ideas
- Tag ideas for better organization
- Associate ideas with usernames
- MongoDB integration with Mongoose

## Installation

1. Clone the repository:
```bash
git clone https://github.com/vsniranjan/sparkboard-api.git
cd sparkboard-api
```

2. Install dependencies:
```bash
npm install
```

3. Create a `.env` file in the root directory:
```
MONGO_URI=your_mongodb_connection_string
PORT=5000
```

4. Start the server:
```bash
# Development mode with nodemon
npm run dev

# Production mode
npm start
```

The server will run on `http://localhost:5000`

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/ideas` | Get all ideas |
| GET | `/api/ideas/:id` | Get a specific idea |
| POST | `/api/ideas` | Create a new idea |
| PUT | `/api/ideas/:id` | Update an idea |
| DELETE | `/api/ideas/:id` | Delete an idea |

## Request Examples

### Create an idea
```bash
POST /api/ideas
Content-Type: application/json

{
  "text": "Build a mobile app for tracking habits",
  "tag": "productivity",
  "username": "john_doe"
}
```

### Update an idea
```bash
PUT /api/ideas/:id
Content-Type: application/json

{
  "text": "Updated idea text",
  "tag": "new-tag"
}
```

## Response Format

All responses follow this format:
```json
{
  "success": true,
  "data": { /* idea object or array */ }
}
```

Error responses:
```json
{
  "success": false,
  "error": "Error message"
}
```

## License

MIT

## Author

Niranjan V S
