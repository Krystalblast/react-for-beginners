# ⚛️ React Setup & First Project

This note explains how to set up a React environment and build your first simple project.

---

## 1. Install Node.js
- Download from [nodejs.org](https://nodejs.org)  
- Install the **LTS version** (recommended for stability).  
- Verify installation:
```bash
node -v
npm -v
```

---

## 2. Create a React Project

### Using Vite (modern & fast)
```bash
npm create vite@latest my-first-react-app
cd my-first-react-app
npm install
npm run dev
```

- Open browser → visit `http://localhost:5173`  
- You should see the default React + Vite page.

---

## 3. Project Structure (basic)
```
my-first-react-app/
 ├── node_modules/   # Dependencies
 ├── public/         # Static assets
 ├── src/            # Your React code
 │    ├── App.jsx    # Main component
 │    └── main.jsx   # Entry point
 ├── package.json    # Dependencies & scripts
 └── README.md
```

---

## 4. First Project: Hello React 🚀

Edit `src/App.jsx`:
```jsx
function App() {
  return <h1>Hello React 🚀</h1>;
}

export default App;
```

---

## 5. Run the App
Start the development server:
```bash
npm run dev
```
- Open the link in your terminal (usually `http://localhost:5173`)  
- You’ll see **Hello React 🚀** on the screen 🎉  

---

## 6. Build for Production
```bash
npm run build
```
- Vite creates a **`dist/`** folder with static files (HTML, CSS, JS).  
- You can host this on **Netlify, Vercel, or GitHub Pages** — or serve it locally with:
```bash
npm install -g serve
serve -s dist
```

---

## 📚 References
- [React Official Docs](https://react.dev/)
- [Vite Documentation](https://vitejs.dev/)
- [Create React App Guide](https://create-react-app.dev/)
