# 🚲 Tandem — A Collaborative App for Two

**Tandem** is a modern, privacy-focused web application designed for two people — partners, roommates, or close friends — to manage their **tasks**, **calendar**, and **shared expenses** in one place.

---

## ✨ Features

### ✅ Task Management
- Shared and personal to-do lists
- Tasks include: title, description, due date, priority, tags
- Recurring tasks (e.g. weekly, monthly)
- Drag & drop task ordering
- Mobile gestures (swipe to complete)
- Notes and comments on tasks

### 📅 Calendar Integration
- Calendar view (Month / Week / Day)
- Sync with Google Calendar (OAuth2) or CalDAV
- Due-dated tasks appear in calendar
- Create events directly in-app
- Link tasks to calendar events
- Color-coded views (per person or list)

### 💰 Shared Expense Tracking
- Add expenses with:
  - Title, amount, category, payer, date
  - Custom or 50/50 split between users
- Balance tracking: "You owe Alex 42 CHF"
- Record repayments and settlements
- Filters by category, user, time range
- Grouping by month or context/project (e.g. "Road Trip")
- Exportable expense history (CSV / optional PDF)

### 👥 Designed for Two
- Real-time updates via WebSocket or Firebase
- Shared ownership of tasks, calendars, expenses
- Activity feed: "Anna completed ‘Buy groceries’"
- User settings: time zones, dark mode, notifications

### 🧪 Optional Features (v2)
- Offline support (IndexedDB)
- End-to-end encryption for tasks & expenses
- Push notifications or email reminders
- Voice input for tasks (mobile)
- OCR support for expense receipts

---

## 🧱 Tech Stack

### Frontend
- [Vue 3](https://vuejs.org/) + [Vite](https://vitejs.dev/)
- [Pinia](https://pinia.vuejs.org/) for state management
- [Vue Router](https://router.vuejs.org/) for routing
- [Tailwind CSS](https://tailwindcss.com/) for styling
- [FullCalendar](https://fullcalendar.io/) for calendar UI
- [date-fns](https://date-fns.org/) for date handling

### Backend
- [Node.js](https://nodejs.org/) + [Express](https://expressjs.com/)
- [PostgreSQL](https://www.postgresql.org/) with [Prisma](https://www.prisma.io/)
- Auth: JWT (access + refresh tokens)
- Google Calendar integration (OAuth2)
- Realtime via [Socket.IO](https://socket.io/) or Firebase

### DevOps & Deployment
- Dockerized services
- CI/CD pipelines via GitHub Actions
- Deployable to Railway, Fly.io, Vercel, Render or other platforms

---

## 📁 Example Project Structure (Frontend)

```bash
/src
  /components
    TaskList.vue
    TaskItem.vue
    TaskDetailModal.vue
    CalendarView.vue
    ExpenseList.vue
    ExpenseForm.vue
    BalanceWidget.vue
  /pages
    Dashboard.vue
    Login.vue
    Register.vue
  /store
    useUserStore.ts
    useTaskStore.ts
    useCalendarStore.ts
    useExpenseStore.ts
  /api
    tasks.ts
    calendar.ts
    expenses.ts
````

---

## 📃 License

MIT License — Open for contributions!

```