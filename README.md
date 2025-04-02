# README.md

## SevaVerse: Connecting Hearts, Empowering Communities

Welcome to **SevaVerse**, a centralized platform designed to connect NGOs, orphanages, well-wishers, and volunteers to foster collaboration and enhance child welfare. This project was developed during the **Women Techies'25 Hackathon** organized by Google Developers Student Club (GDSC), VIT Vellore.


---

## Team
- Aditya Vardhan Kochar
- Adith Manikonda
- Arikta Das

---

## Problem Statement

There is a pressing need for a user-friendly platform that bridges the gap between NGOs, orphanages, volunteers, and well-wishers. The challenges include:
- Limited visibility and outreach for NGOs and orphanages.
- Inefficient resource mobilization and donation management.
- Difficulty in volunteer recruitment and onboarding.
- Lack of transparency and accountability among stakeholders.

**SevaVerse** addresses these issues by providing tools for:
- Streamlined volunteer management.
- Enhanced collaboration and networking.
- Robust tracking and reporting mechanisms.

---

## Features

### For NGOs/Organizations
1. **Sign-Up/Login**: Secure authentication for organizations.
2. **Task Creation**: Post volunteer opportunities with details like location, description, time, and required team size.
3. **Volunteer Management**: View registered volunteers for tasks.
4. **Dashboard**: Manage tasks and track progress.

### For Volunteers
1. **Sign-Up/Login**: Register as a volunteer with personal details.
2. **Browse Tasks**: Explore available tasks filtered by location, date, or category.
3. **Register for Tasks**: Express interest in tasks posted by organizations.
4. **Dashboard**: View registered tasks and manage participation.

### General Features
- JWT-based authentication for security.
- Role-based access control (NGO vs Volunteer).
- Responsive UI with Tailwind CSS for an enhanced user experience.
- SQLite database integration via Prisma ORM.

---

## Tech Stack

### Frontend
- HTML, CSS, JavaScript
- Tailwind CSS

### Backend
- Node.js with Express.js
- Prisma ORM

### Database
- SQLite (development)
- Firebase/Supabase (future scope)

---

## Installation

### Prerequisites
Ensure you have the following installed:
- Node.js
- npm or yarn
- SQLite database (or Prisma-supported database)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/sevaverse.git
   cd sevaverse
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Set up environment variables:
   Create a `.env` file in the root directory with the following:
   ```
   DATABASE_URL="file:./dev.db"
   JWT_ORG="your_jwt_secret_for_organizations"
   JWT_VOL="your_jwt_secret_for_volunteers"
   ```

4. Initialize the database:
   ```bash
   npx prisma migrate dev --name init
   ```

5. Start the server:
   ```bash
   npm start
   ```
   The application will run on `http://localhost:3000`.

---

## Usage

### NGO Workflow:
1. Sign up or log in as an organization.
2. Create tasks specifying details like description, location, time range, etc.
3. Monitor volunteer registrations via the dashboard.

### Volunteer Workflow:
1. Sign up or log in as a volunteer.
2. Browse available tasks based on filters such as location or category.
3. Register for tasks of interest and view them on your dashboard.

---

## Database Schema

The platform uses Prisma ORM for database management:

### Models:
1. **Volunteer**
    - Attributes: `id`, `name`, `dob`, `age`, `gender`, `mobileNo`, `emailId`, `city`, `tasks[]`
2. **Organization**
    - Attributes: `id`, `name`, `mobileNo`, `emailId`, `tasks[]`
3. **Task**
    - Attributes: `id`, `orgId`, `title`, `description`, `fromTime`, `toTime`, `location`, `size`, `volunteers[]`
4. **Reviews**
    - Attributes: `id`, `review`, `volunteerId`, `orgId`

---

## Roadmap

### MVP Features Completed:
- Core task creation and registration workflows.
- Volunteer dashboard to browse tasks.
- Organization dashboard to manage tasks.

### Future Enhancements:
1. Map Integration:
    - Display task locations on a map using Google Maps API.
2. Advanced Filtering & Sorting:
    - Filter tasks by skills or categories.
3. Notifications:
    - Email notifications for task updates or registrations.
4. Mobile App Development:
    - Extend functionality to Android/iOS platforms.


