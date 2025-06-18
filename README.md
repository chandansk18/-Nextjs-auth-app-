🛡️ Next.js Firebase Auth App with Token-Based Backend
A full-stack authentication system built with Next.js, Firebase Authentication, and a custom token-based backend API. Designed with a clean and modern UI resembling a payment gateway login flow, this project implements secure login using Google OAuth, access tokens, and refresh tokens stored in cookies.

🚀 Features
🔐 Google Sign-In with Firebase Authentication

🍪 Access & Refresh Token management using HTTP-only cookies

♻️ Token refresh system to keep users logged in securely

🔄 Redux Toolkit for global auth state management

🎨 Responsive UI inspired by payment gateways (like Razorpay, Stripe, etc.)

🧭 Protected routes with session verification

🌐 Built with Next.js App Router (13+)

🧱 Tech Stack
Frontend: Next.js (App Router), Tailwind CSS, Redux Toolkit

Authentication: Firebase Auth (Google Sign-In)

Backend: Custom REST API for token validation & refresh

Storage: Cookies (HTTP-only for secure tokens)

Tools: ESLint, Prettier, GitHub

📁 Project Structure
bash
Copy
Edit
.
├── app/
│   ├── login/
│   ├── dashboard/
│   └── layout.js
├── components/
│   ├── AuthForm.jsx
│   └── Sidebar.jsx
├── redux/
│   └── authSlice.js
├── utils/
│   └── verifyToken.js
├── pages/
│   └── api/
│       ├── login.js
│       └── refresh.js
├── .env.local
└── README.md
🔧 How It Works
User logs in with Google (via Firebase)

Firebase issues an ID token

The token is sent to a custom backend API (/api/login)

Backend issues:

Access Token (short-lived) stored in cookie

Refresh Token (long-lived) stored in cookie

Auth state is managed with Redux

On session expiration, /api/refresh is used to renew tokens silently

