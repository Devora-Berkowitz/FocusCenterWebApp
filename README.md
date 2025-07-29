
# 🌐 FocusCenterWebApp

A full-stack web application for managing therapy appointments – built with React, .NET Core, SQL Server, and Tailwind CSS.

---

## 📖 Overview

**FocusCenterWebApp** is a digital scheduling platform tailored for therapy centers. It allows clients to explore therapists by specialization, view availability, and book appointments – all through a responsive and clean user interface.

---

## 🚀 Features

- 🔍 Search therapists by specialization  
- 🕒 View working hours and availability per therapist  
- 📅 Book appointments with a calendar-based UI  
- 🔐 User authentication with JWT & refresh tokens  
- 💡 Smart calendar: shows only available days & hours  
- 📱 Responsive design using Tailwind CSS  
- 🧾 Admin-friendly backend with .NET Core APIs  
- 🗄️ SQL Server database with seeded working hours & availability  

---

## 🛠️ Tech Stack

| Layer      | Technology             |
|------------|------------------------|
| Frontend   | React + TypeScript     |
| Styling    | Tailwind CSS           |
| Backend    | ASP.NET Core Web API   |
| Database   | SQL Server             |
| State Mgmt | Redux Toolkit          |
| Auth       | JWT + Refresh Tokens   |
| Calendar   | Custom calendar logic  |

---

## 🧪 Local Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/your-username/FocusCenterWebApp.git
cd FocusCenterWebApp
```

### 2. Frontend (React)
```bash
cd keshev-focus-hub
npm install
npm run dev
```

### 3. Backend (.NET Core)
- Open the solution in **Visual Studio** or **VS Code**
- Configure the database connection string in `appsettings.json`
- Apply EF Core migrations (if not seeded):
```bash
dotnet ef database update
```
- Run the backend:
```bash
dotnet run
```

---

## 🧾 Database Setup

- Use **SQL Server 2019 or higher**
- Recommended tables:
  - `Therapists`
  - `Specializations`
  - `TherapistHours`
  - `Appointments`
  - `AvailableAppointments`
- Optional seed scripts available in `/server/Data/Seed`

---

## 📂 Project Structure

```
FocusCenterWebApp/
│
├── client/                # React frontend
│   ├── components/        # Reusable components
│   ├── pages/             # Route-based pages
│   ├── store/             # Redux slices
│   ├── api/               # Axios and API logic
│   └── App.tsx            # Root app component
│
├── server/                # .NET Core backend
│   ├── Controllers/       # API endpoints
│   ├── Models/            # EF Core models
│   ├── Data/              # DbContext & seeders
│   ├── Services/          # Business logic
│   └── Program.cs         # Entry point
│
└── README.md
```

---

## 🔒 Authentication Flow

- Login issues **JWT** + **refresh token**
- Tokens sent via `Authorization: Bearer`
- Role-based access handled in API
- Protected routes on frontend verify session status
- Non-authenticated users are redirected to login

---

## 📆 Appointment Logic

- Working hours per therapist are preloaded from DB
- Calendar dynamically shows only valid dates
- Time slots are calculated based on therapist's treatment length and availability
- Admins can manage availability through backend

---

## 🎯 Future Improvements

- Admin dashboard (manage therapists/specializations)
- Email/SMS appointment reminders
- Multi-language support (Hebrew, English)
- Google Calendar sync
- PDF receipts for booked sessions

---

## 🤝 Contributing

Pull requests are welcome!  
For major changes, please open an issue first to discuss what you'd like to change.

---

## 👤 Author

**Devora Berkowitz**  
Fullstack Developer – React, .NET, SQL, Tailwind  
