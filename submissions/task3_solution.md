# Intern Workflow Management System — Task 3 Solution

## Project Summary
This submission implements a full-stack MERN application for managing intern records across their lifecycle. The solution provides centralized intern data management with CRUD operations, search, filtering, pagination, input validation, and operational error handling.

## Project Outcome
Key outcomes delivered:
- Centralized storage of intern records in MongoDB.
- RESTful API for intern data management.
- Responsive React dashboard for intern workflows.
- Full CRUD support (create, read, update, delete).
- Efficient data navigation through search, filters, and pagination.
- Validation and error handling to preserve data integrity.

## System Architecture
The application follows a standard MERN architecture:

1. **Client Layer (React)**
   - Dashboard UI for intern list and lifecycle actions.
2. **Application Layer (Node.js + Express)**
   - REST endpoints for CRUD and query operations.
3. **Data Layer (MongoDB + Mongoose)**
   - Schema-based persistence and validation.

Flow:
React client -> Express API -> Mongoose model -> MongoDB

## Data Model (Intern Collection)
- `name`: String, required, minimum length validation.
- `email`: String, required, unique, email format validation.
- `role`: Enum (`Frontend`, `Backend`, `Fullstack`).
- `status`: Enum (`Applied`, `Interviewing`, `Hired`, `Rejected`).
- `score`: Number, constrained to 0-100.
- `createdAt`: Date timestamp.
- `updatedAt`: Date timestamp.

## Backend Implementation

### API Endpoints
- `POST /api/interns`: Create intern record.
- `GET /api/interns`: Retrieve interns with pagination, search, and filters.
- `GET /api/interns/:id`: Retrieve a single intern by id.
- `PATCH /api/interns/:id`: Update intern details.
- `DELETE /api/interns/:id`: Delete intern record.

### Backend Capabilities
- Schema-level validation through Mongoose.
- Consistent HTTP status and structured error responses.
- Query-based search by name/email.
- Filtering by role and status.
- Pagination support for large lists.
- Centralized error handling middleware for validation, duplicate key, and invalid ObjectId cases.

## Frontend Implementation

### Intern Dashboard
- Tabular intern list (name, email, role, status, score, created date).
- Search input for name/email.
- Role and status filters.
- Pagination controls for list navigation.

### Intern Management
- Add intern form with client-side validation.
- Edit intern flow using modal or inline form.
- Delete intern with confirmation prompt.

### User Experience
- Loading indicators during asynchronous API operations.
- API error messages displayed in the UI.
- Clear feedback on create/update/delete actions.

## Technology Stack
- **Frontend**: React, Axios, CSS/basic UI components.
- **Backend**: Node.js, Express.js, MongoDB, Mongoose.
- **Tools**: Git, GitHub, Postman.

## Setup and Run

### Backend
```bash
cd server
npm install
```
Create `.env`:
```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
```
Run backend:
```bash
npm run dev
```

### Frontend
```bash
cd client
npm install
npm start
```

Default URLs:
- Frontend: `http://localhost:3000`
- Backend: `http://localhost:5000`

## Screenshots / Demo
Include screenshots or demo links for:
- Dashboard view
- Add intern form
- Edit intern flow
- Delete confirmation

## Future Improvements
- Authentication and role-based authorization.
- Advanced analytics for intern pipeline metrics.
- Export options for intern reports.
- Integrations with external recruitment platforms.

## Author
Developed as part of a MERN stack engineering assignment focused on full-stack CRUD system implementation.
