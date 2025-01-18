# Dark Mode Toggle

This project implements a simple Dark Mode Toggle using React and CSS. It provides an elegant way for users to switch between light and dark themes, with the chosen preference saved in the browser's `localStorage` for persistence across sessions.

## Features

- **Dark Mode Toggle**: Allows users to switch between light and dark themes.
- **Persistence**: The selected theme is saved in `localStorage`, so it remains consistent even after the page is reloaded.
- **Smooth Transitions**: CSS transitions ensure a visually pleasing experience when switching themes.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/tahaesii/dark-mode-toggle.git
   ```

2. Navigate to the project directory:

   ```bash
   cd dark-mode-toggle
   ```

3. Install dependencies (if needed):

   ```bash
   npm install
   ```

## Usage

1. Include the `DarkModeToggle` component in your React application:

   ```javascript
   import { DarkModeToggle as Control } from "./controls/darkModeRadioBtn/DarkModeToggle";

   function App() {
     return (
       <div>
         <Control />
       </div>
     );
   }

   export default App;
   ```

2. Customize styles by modifying the `styles.css` file.

3. Run your application:

   ```bash
   npm start
   ```

## Code Overview

### Component

The `DarkModeToggle` component uses the following key functionalities:

- **useEffect**: Ensures the dark mode class is applied on the initial render if it exists in `localStorage`.
- **handleToggled**: Toggles the `dark` class on the `body` element and updates the `localStorage` with the current theme.

### CSS

- Variables `--color-dark` and `--color-light` are used to define the primary colors for dark and light themes.
- Transitions are implemented to create a smooth switch effect.

## CSS Classes

- **`:root`**: Declares theme variables.
- **`body`**: Sets the default background color and applies transitions.
- **`body.dark`**: Defines the dark mode styles.
- **`.switch`**: Styles the toggle switch container.
- **`.handle`**: Styles the toggle switch handle with smooth animations.
