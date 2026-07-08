# Sportz - Real-time Sports Events Platform

A full-stack web application for live sports event coverage with real-time updates using WebSockets.

## 📦 Project Structure

```
.
├── sportz-frontend-main/     # React + Vite frontend
├── sportz-websockets-main/   # Node.js + Express backend
└── README.md
```

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- PostgreSQL database (local or cloud)

### Setup

1. **Clone the repository**
```bash
git clone https://github.com/anandpakharia/sportz.git
cd sportz
```

2. **Backend Setup**
```bash
cd sportz-websockets-main
npm install

# Create .env file with your database URL
# DATABASE_URL=postgresql://user:password@host/database
# See README in sportz-websockets-main for full configuration

npm run db:migrate
npm run seed
npm run dev
```

3. **Frontend Setup**
```bash
cd sportz-frontend-main
npm install
npm run dev
```

Visit `http://localhost:5173` in your browser!

## 🏗️ Tech Stack

**Frontend:**
- React 19
- TypeScript
- Vite
- WebSockets

**Backend:**
- Node.js
- Express 5
- PostgreSQL
- Drizzle ORM
- WebSockets (ws library)
- Zod (validation)

## 📚 Documentation

- [Frontend README](./sportz-frontend-main/README.md)
- [Backend README](./sportz-websockets-main/README.md)

## 🔌 API & WebSocket

### REST Endpoints
- `GET /matches?limit=50` - List all matches
- `POST /matches` - Create new match
- `GET /matches/:id/commentary?limit=100` - List commentary for a match
- `POST /matches/:id/commentary` - Create commentary

### WebSocket
- Connect: `ws://localhost:8000/ws`
- Subscribe to match: `{ "type": "subscribe", "matchId": 123 }`
- Real-time updates: `{ "type": "commentary", "data": {...} }`

See backend README for detailed protocol documentation.

## 🎯 Features

✅ Real-time match updates via WebSockets  
✅ Live commentary feeds  
✅ Match score tracking  
✅ Rate limiting & security  
✅ Responsive UI  
✅ Developer-friendly APIs  

## 📝 License

ISC

## 👤 Author

Anand Pakharia
