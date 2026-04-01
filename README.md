# Serverless Dynamic Portfolio & Admin Dashboard 🚀

A fully dynamic, responsive, and serverless personal portfolio template. It comes with a built-in Admin Dashboard, allowing you to manage projects, services, resume timelines, skills, and client reviews without writing a single line of backend code.

## ✨ Features
- **Zero Backend Needed**: Powered entirely by Firebase Firestore.
- **Built-in Admin Panel**: Easily add, edit, delete, and reorder your content on the fly.
- **Bilingual Support**: Seamlessly toggle between English (LTR) and Arabic (RTL) without reloading.
- **Dark & Light Mode**: Modern UI with a smooth theme toggle and preference saving.
- **Direct Telegram Leads**: Contact form is integrated with Telegram via Cloudflare Workers to send requests directly to your phone.
- **Live Chat Ready**: Pre-configured placeholder for the Tawk.to live chat widget.
- **100% Free to Host**: Deploy easily on GitHub Pages, Firebase Hosting, Vercel, or Netlify.

## 🛠️ Tech Stack
- **Frontend:** HTML5, CSS3 (Vanilla), JavaScript (ES6+ Modules)
- **Database:** Firebase Firestore (NoSQL)
- **APIs:** Telegram API via Cloudflare Workers

## 🚀 Getting Started

Follow these steps to get your portfolio up and running:

### 1. Database Setup (Firebase)
1. Go to the [Firebase Console](https://console.firebase.google.com/) and create a new project.
2. Navigate to **Firestore Database** and click **Create database** (Start in **Test Mode** for initial setup).
3. Go to **Project Settings** > **General** > **Your apps** and add a Web App `</>`.
4. Copy your Firebase Config object.
5. Open `index.html` and `admin.html`, locate `const firebaseConfig = {...}`, and replace the placeholder keys with your actual Firebase keys.

### 2. Contact Form Setup (Telegram via Cloudflare Workers)
To receive client messages directly to your Telegram:
1. Create a Telegram Bot using `@BotFather` on Telegram and save the **Bot Token**.
2. Get your **Chat ID** by messaging `@userinfobot`.
3. Create a Cloudflare Worker that accepts `POST` requests and forwards them to the Telegram API.
4. Open `index.html`, locate the `fetch` call inside the `clientRequestForm` submit event, and replace `https://YOUR_CLOUDFLARE_WORKER_URL.workers.dev` with your worker's URL.

### 3. Live Chat Setup (Tawk.to)
1. Create a free account on [Tawk.to](https://www.tawk.to/).
2. Get your Property ID and Widget ID from the dashboard.
3. Open `index.html`, locate the Tawk.to script near the bottom, and replace `YOUR_PROPERTY_ID/YOUR_WIDGET_ID`.

### 4. Admin Dashboard Usage
- Navigate to `/admin.html` on your local server or deployed site.
- Use the sidebar to manage your General Settings, Projects, Services, and more.
- **Security Note:** In a production environment, you must secure your `admin.html` route and update your Firestore Security Rules to only allow authenticated access to write data.

## 📦 Deployment
Since this is a static, frontend-only application, you can host it anywhere for free:
- [Firebase Hosting](https://firebase.google.com/docs/hosting) (Recommended)
- [GitHub Pages](https://pages.github.com/)
- [Vercel](https://vercel.com/)

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page if you want to contribute.

## 📝 License
This project is open-source and available under the [MIT License](LICENSE). Feel free to fork, customize, and use it to land your next big client!