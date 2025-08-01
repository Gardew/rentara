# Rentara - Real Estate Management

A real estate management application built with React and Node.js.

## Local Development

1. Clone the repository
2. Install dependencies
```bash
npm install
```
3. Create a postgres database, either locally or using a cloud service (e.g. Neon)
4. Create a `.env` file in the root directory and add the following environment variables:
```env
VITE_PUBLIC_URL=http://localhost:5173
VITE_API_URL=http://localhost:3000
DATABASE_URL=postgresql://neondb_owner:npg_5ynWzRT8ZlfK@ep-twilight-pond-a2vms51s-pooler.eu-central-1.aws.neon.tech/neondb?sslmode=require&channel_binding=require
PORT=3000
SECRET_KEY=123
REFRESH_TOKEN_SECRET=321
ACCESS_TOKEN_EXPIRES_IN=15m
REFRESH_TOKEN_EXPIRES_IN=7d
```
5. Start the development servers
```bash
npm run dev
cd server && npm start
```
6. Open the app in your browser at `http://localhost:5173`

## Deployment

### Frontend (Vercel)
- Framework: Vite + React
- Build Command: `npm run build`
- Output Directory: `dist`
- Environment Variables:
  - `VITE_API_URL`: Backend API URL
  - `VITE_PUBLIC_URL`: Frontend URL

### Backend (Render)
- Framework: Express.js
- Build Command: `cd server && npm install`
- Start Command: `cd server && npm start`
- Environment Variables:
  - `DATABASE_URL`: PostgreSQL connection string
  - `JWT_SECRET`: JWT secret key
  - `NODE_ENV`: production