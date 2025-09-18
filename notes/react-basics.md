# ⚛️ React Basics Notes

React is a **JavaScript library** for building user interfaces. It focuses on reusable UI components.

---

## 🔑 Core Concepts

### 1. Components
- Building blocks of React apps.
- Two types: **function components** and **class components**.
```jsx
function Welcome(props) {
  return <h1>Hello, {props.name}!</h1>;
}
```

### 2. JSX (JavaScript XML)
- Looks like HTML, but inside JavaScript.
- JSX compiles into `React.createElement()`.
```jsx
const element = <h1>Hello, world!</h1>;
```

### 3. Props
- Data passed from parent → child components.
- **Read-only**.
```jsx
function Greeting({ name }) {
  return <p>Hello, {name}!</p>;
}
```

### 4. State
- Local, changeable data inside a component.
- Updates trigger re-render.
```jsx
import { useState } from "react";

function Counter() {
  const [count, setCount] = useState(0);
  return (
    <button onClick={() => setCount(count + 1)}>
      Clicked {count} times
    </button>
  );
}
```

### 5. Events
- Handled with camelCase attributes.
```jsx
<button onClick={handleClick}>Click Me</button>
```

### 6. Conditional Rendering
```jsx
{isLoggedIn ? <Dashboard /> : <Login />}
```

### 7. Lists & Keys
```jsx
const items = ["A", "B", "C"];
<ul>
  {items.map((item, index) => (
    <li key={index}>{item}</li>
  ))}
</ul>
```

### 8. Hooks
- Add features to function components.
- Common ones:
  - `useState` → state
  - `useEffect` → side effects (fetching, subscriptions)
  - `useContext` → context

---

## 🛠 Example: Simple App
```jsx
import React, { useState } from "react";

function App() {
  const [name, setName] = useState("");

  return (
    <div>
      <h1>Hello, {name || "Guest"}!</h1>
      <input
        type="text"
        placeholder="Enter your name"
        onChange={(e) => setName(e.target.value)}
      />
    </div>
  );
}

export default App;
```

---

## 📚 References
- [React Official Docs](https://react.dev/)
- [Vite Documentation](https://vitejs.dev/)
- [Create React App Guide](https://create-react-app.dev/)
