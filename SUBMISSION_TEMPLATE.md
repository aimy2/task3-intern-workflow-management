# Candidate Submission Template

## Candidate Information
- Full Name: Aiman
- Email: [Add your email]
- GitHub Profile Link: [Add your GitHub profile URL]
- Demo Link (if deployed): [Add demo URL if available]
- Submission Date: March 17, 2026

## Backend (Node + Express)

### API Endpoints Implemented:
1. **POST /api/interns**:
   - [x] Created intern functionality.
2. **GET /api/interns**:
   - [x] Search/filter/pagination functionality.
3. **GET /api/interns/:id**:
   - [x] Fetch single intern.
4. **PATCH /api/interns/:id**:
   - [x] Update intern.
5. **DELETE /api/interns/:id**:
   - [x] Delete intern.

### Error Handling
- [x] Centralized error middleware implemented.
- [x] Handled validation errors, duplicate email, invalid MongoDB ObjectId errors.

## Frontend (React)

### Features Implemented:
1. **Intern List Page**:
   - [x] Table with intern data (name, email, role, status, score).
   - [x] Search and filter functionality.
   - [x] Pagination.
2. **Add Intern Form**:
   - [x] Form with validation.
   - [x] Successful creation adds intern to list.
3. **Edit Intern Form**:
   - [x] Inline modal or form for editing.
   - [x] Updates refresh the list.
4. **Delete Intern**:
   - [x] Confirmation dialog for delete.
   - [x] Successful delete removes intern from list.

### UX Features:
- [x] Loading indicators for API calls.
- [x] Error messages from API shown to users.

## Assumptions
- [x] Email is unique per intern and enforced at schema level.
- [x] Score range is validated between 0 and 100.
- [x] Role values are restricted to Frontend, Backend, Fullstack.
- [x] Status values are restricted to Applied, Interviewing, Hired, Rejected.

## Setup Instructions
- [x] Backend setup:
  1. `cd server`
  2. `npm install`
  3. Create `.env` with `PORT=5000` and `MONGO_URI=<your_connection_string>`
  4. `npm run dev`
- [x] Frontend setup:
  1. `cd client`
  2. `npm install`
  3. `npm start`

Additional details and architecture notes are provided in `README.md` and `submissions/task3_solution.md`.
