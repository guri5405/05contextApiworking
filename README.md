# 🧠 Mini Context App (React)

A simple React application demonstrating **global state management using Context API**.
This project shows how to share user data (like login info) across components without prop drilling.

---

## 🚀 Features

* 🔐 Simple Login functionality (username & password)
* 🌐 Global state management using **React Context API**
* 🔄 Real-time state updates across components
* 👤 Profile page displaying logged-in user
* ⚛️ Clean and beginner-friendly React structure

---

## 🏗️ Project Structure

```
src/
│
├── context/
│   ├── UserContext.js          # Context creation
│   └── UserContextProvider.js # Global state provider
│
├── component/
│   ├── Login.js               # Login form component
│   └── Profile.js             # Profile display component
│
├── App.js                     # Root component
└── App.css
```

---

## 🧩 How It Works

### 1. Context Creation

* `UserContext.js` creates a global store using:

```js
const UserContext = React.createContext();
```

---

### 2. Provider Setup

* `UserContextProvider.js` wraps the app and provides state:

```js
<UserContext.Provider value={{ user, setUser }}>
  {children}
</UserContext.Provider>
```

---

### 3. Updating State (Login)

* `Login.js` uses `useContext` to update global state:

```js
const { setUser } = useContext(UserContext);
setUser({ username, password });
```

---

### 4. Consuming State (Profile)

* `Profile.js` reads user data:

```js
const { user } = useContext(UserContext);
```

* Displays:

  * "Please login.." if no user
  * "Welcome {username}" after login

---

## 🛠️ Tech Stack

* ⚛️ React (Functional Components)
* 🪝 React Hooks (`useState`, `useContext`)
* 📦 Context API

---

## ▶️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/guri5405/minicontext.git
```

### 2. Navigate to project

```bash
cd minicontext
```

### 3. Install dependencies

```bash
npm install
```

### 4. Run the app

```bash
npm start
```

---

## 🎯 Learning Outcomes

* Understanding **Context API**
* Avoiding **prop drilling**
* Using **useContext hook**
* Managing **global state in React**

---

## 💡 Future Enhancements

* 🔒 Add authentication validation
* 💾 Persist user data using localStorage
* 🎨 Improve UI with Tailwind CSS
* 🔐 Add logout functionality
* 🌍 Add routing using React Router

---

## 📌 Conclusion

This project is a great starting point for learning how React handles **shared state** using Context API.
It builds a strong foundation before moving to advanced state management tools like Redux or Zustand.

---

## 👨‍💻 Author

Made with ❤️ while learning React.
