# WorkForce HR Management System

A full-stack HR management system built with React, Node.js, Express, and PostgreSQL.

## Project Structure

- `backend/` - Express API server, PostgreSQL schema, authentication, employee and leave management
- `frontend/` - React app with routing, protected pages, dashboard, employees, leaves, departments, reports, and profile

## Backend Setup

1. Open a terminal in `backend/`
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file from `.env.example` and set your PostgreSQL `DATABASE_URL` and JWT secrets.
4. Initialize the database schema:
   - Run the SQL script in `backend/sql/init.sql` against your PostgreSQL database.
5. Start the server:
   ```bash
   npm start
   ```

The backend runs on `http://localhost:4000` by default.

## Frontend Setup

1. Open a terminal in `frontend/`
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the frontend:
   ```bash
   npm run dev
   ```

The frontend runs on `http://localhost:5173` by default.

## Environment Variables

Copy `backend/.env.example` to `backend/.env` and update:

- `PORT`
- `NODE_ENV`
- `DATABASE_URL`
- `JWT_SECRET`
- `REFRESH_SECRET`
- `CLIENT_URL`

## Demo Credentials

- Admin: `admin@company.com` / `admin123`
- HR: `hr@company.com` / `hr123`
- Manager: `manager@company.com` / `mgr123`
- Employee: `emp@company.com` / `emp123`

## API Docs

Swagger documentation is available at `http://localhost:4000/api-docs` once the backend is running.

## Notes

- File uploads are served from `backend/uploads/`
- Refresh tokens are stored in the database
- JWT access tokens are configured for 15 minutes, refresh tokens for 30 days
