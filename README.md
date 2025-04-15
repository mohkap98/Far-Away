# Far Away - Travel Essentials App

A simple and elegant React app for managing your travel packing checklist. "Far Away" allows users to add, remove, check, and uncheck travel-related items to help ensure they never forget the essentials again.

---

## 🧠 Project Overview

"Far Away" is built with the goal of providing an intuitive user interface to manage travel items efficiently. The application helps users:

- ✅ Add essential items
- ❌ Remove unwanted items
- 🔄 Toggle items as packed/unpacked
- 📊 View total stats about packing progress

---

## 🏗️ Block Diagram

```
+---------------------------+
|         App.jsx          |
|---------------------------|
|  - Holds state of items   |
|  - Renders all components |
+---------------------------+
             |
             v
+---------------------------+
|        Logo.jsx           |
|---------------------------|
| - Static component        |
| - Displays app title/logo|
+---------------------------+
             |
             v
+---------------------------+
|      Form.jsx             |
|---------------------------|
| - Handles input           |
| - Adds new item to list   |
+---------------------------+
             |
             v
+---------------------------+
|   PackingList.jsx         |
|---------------------------|
| - Maps through items      |
| - Renders each Item       |
| - Allows remove/toggle    |
+---------------------------+
             |
             v
+---------------------------+
|       Item.jsx            |
|---------------------------|
| - Displays item info      |
| - Button to delete        |
| - Checkbox to mark packed |
+---------------------------+
             |
             v
+---------------------------+
|        Stats.jsx          |
|---------------------------|
| - Shows number of items   |
| - Shows % packed          |
+---------------------------+
```

---

## 🛠️ Implementation Details

### 1. **State Management**
- The main `App.jsx` component uses `useState` to store an array of item objects:
  ```js
  const [items, setItems] = useState([]);
  ```
  Each item object has:
  ```js
  {
    id: Number,
    description: String,
    quantity: Number,
    packed: Boolean
  }
  ```

### 2. **Adding Items (Form.jsx)**
- User enters item description and quantity.
- On submit, the new item is added to state with a unique ID and `packed: false`.

### 3. **Displaying Items (PackingList.jsx & Item.jsx)**
- `PackingList.jsx` maps through all `items` and renders each one using the `Item.jsx` component.
- `Item.jsx` shows the description and has:
  - a checkbox to toggle `packed`
  - a delete button to remove the item

### 4. **Removing Items**
- Clicking delete calls a function that filters out the item from the state array in `App.jsx`.

### 5. **Toggling Packed Status**
- Checkbox click triggers an update that toggles the `packed` field for the clicked item.

### 6. **Statistics (Stats.jsx)**
- Shows total number of items and how many are packed.
- Also shows a percentage of items packed out of total.

---

## 💡 Technologies Used
- React (functional components)
- JavaScript (ES6+)
- CSS (custom styling or Tailwind)

---

## 📁 Folder Structure
```
src/
|-- components/
|   |-- Logo.jsx
|   |-- Form.jsx
|   |-- PackingList.jsx
|   |-- Item.jsx
|   |-- Stats.jsx
|
|-- App.jsx
|-- index.js
```

---

## 🚀 Future Enhancements
- Persistent local storage support
- Drag and drop sorting
- Categorized items (clothes, documents, etc.)
- Dark/light theme toggle

---

## 🧳 Live Demo / Screenshots
_Include link if hosted or attach screenshots here_

---

## 🙌 Mohak Kapoor
Built with ❤️ using React.

---

