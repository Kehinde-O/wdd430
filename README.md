# React Todo List Application

A fully functional to-do list application built with React, demonstrating modern React concepts including hooks, components, and local storage persistence.

## Features

- ✅ **Add new to-do items** - Enter a task and click "Add" to create new items
- ✅ **Mark items as complete** - Click the checkbox to toggle completion status
- ✅ **Delete items** - Remove unwanted tasks with the delete button
- ✅ **Data persistence** - Tasks are saved to local storage and persist between sessions
- ✅ **Empty state** - Shows "No To-Do's" when the list is empty
- ✅ **Responsive design** - Works on desktop and mobile devices

## Components

The application is built with reusable React components:

- **`App.jsx`** - Main application component that manages state and renders other components
- **`NewTodoForm.jsx`** - Form component for adding new todo items
- **`TodoList.jsx`** - List component that renders all todo items
- **`TodoItem.jsx`** - Individual todo item component with checkbox and delete functionality

## Technologies Used

- **React** - JavaScript library for building user interfaces
- **Vite** - Build tool for modern web development
- **CSS** - Custom styling for a clean, modern interface
- **Local Storage** - Browser storage for data persistence

## Getting Started

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start the development server:**
   ```bash
   npm run dev
   ```

3. **Open your browser** and navigate to `http://localhost:5173`

## React Concepts Demonstrated

- **Functional Components** - All components are written as functions
- **Hooks** - Uses `useState` for state management and `useEffect` for side effects
- **Props** - Data is passed between components using props
- **Event Handling** - Form submission, checkbox changes, and button clicks
- **Conditional Rendering** - Shows different UI based on application state
- **List Rendering** - Dynamically renders todo items using `.map()`
- **Key Props** - Proper key assignment for list items
- **State Immutability** - State is never mutated directly
- **Local Storage** - Persists data between browser sessions

## Project Structure

```
src/
├── App.jsx           # Main application component
├── NewTodoForm.jsx   # Form for adding new todos
├── TodoList.jsx      # List container component
├── TodoItem.jsx      # Individual todo item component
├── main.jsx          # Application entry point
└── styles.css        # Application styles
```

## How It Works

1. **State Management**: The main App component manages the todo list state using `useState`
2. **Data Persistence**: `useEffect` automatically saves todos to localStorage whenever the state changes
3. **Component Communication**: Parent components pass data and functions to child components via props
4. **Event Handling**: Form submissions and user interactions are handled through event handlers
5. **Conditional Rendering**: The UI adapts based on whether there are todos or not

## Key Features Implementation

### Adding Todos
- Form prevents submission of empty items
- New todos get unique IDs using `crypto.randomUUID()`
- Input field clears after successful submission

### Toggling Completion
- Checkbox state is controlled by the todo's `completed` property
- State is updated immutably using the spread operator

### Deleting Todos
- Items are removed using the `filter()` method
- State updates trigger automatic localStorage saves

### Data Persistence
- Initial state is loaded from localStorage on component mount
- All state changes are automatically saved to localStorage
- Data persists across browser sessions and page refreshes

This application serves as an excellent example of modern React development practices and can be extended with additional features like editing todos, filtering, or categories.
