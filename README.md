## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# AI ChatBot Component

This AI-powered ChatBot is a fully functional component built using React and OpenAI's GPT models (GPT-3.5 as the default). It includes features such as message history, typing indicators, copy-to-clipboard, and a notification system. Easily customizable, it can be integrated into your React project for a wide range of use cases, including personal assistants, customer support, or creative projects.

## Features
- Integrates with OpenAI GPT API (default is GPT-3.5, but any GPT model can be used).
- Message history tracking for user and assistant conversations.
- Typing indicators to simulate a real-time chat experience.
- Copy-to-clipboard functionality for convenient message sharing.
- Notification system for alerts and prompts.
- Responsive design using Tailwind CSS.

## Built With

This project uses the following frameworks, styles, and languages:

[![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![Vite](https://img.shields.io/badge/Vite-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
[![PostCSS](https://img.shields.io/badge/PostCSS-DD3A0A?logo=postcss&logoColor=white)](https://postcss.org/)
[![OpenAI](https://img.shields.io/badge/OpenAI-412991?logo=openai&logoColor=white)](https://beta.openai.com/)

## Installation

To install and run the ChatBot component in your React project, follow the steps below:

### Part 1: Clone or Download the Files
Unzip the downloaded ChatBot package and copy the `ChatBot.jsx` component from the `src` folder into your React project.

### Part 2: Install Necessary Dependencies
Ensure that you have **Node.js** and **npm** installed on your machine. Then, run the following commands to install the required dependencies:

```bash
# Initialize your React project (if you haven't already)
npm create vite@latest my-app -- --template react

# Change directory to your project
cd my-app

# Install required dependencies
npm install react-icons tailwindcss postcss autoprefixer
```

### Part 3: Install and Configure Tailwind CSS
Tailwind CSS is used for styling the ChatBot component. Follow these steps to install and configure it:

Step 1: Install **Tailwind CSS** and **PostCSS**:
```bash
npm install -D tailwindcss postcss autoprefixer
```

Step 2: Generate the **Tailwind configuration** files:
```bash
npx tailwindcss init -p
```

Step 3: Open your `tailwind.config.js` file and replace its content with:
```javascript
module.exports = {
  content: [
    "./src/**/*.{js,jsx,ts,tsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

Step 4: In your `src/index.css` file, include the following Tailwind imports:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Part 4: Set Up Environment Variables

The ChatBot uses the OpenAI API for GPT-3.5 by default, but you can use any GPT model available in OpenAI. You need to create an environment variable for your OpenAI API key.

Step 1: Create a `.env` file in the root of your project (if it doesn’t exist).

Step 2: Add the following environment variable:
```bash
VITE_OPENAI_API_KEY=your_openai_api_key
```

Replace `your_openai_api_key` with your actual OpenAI API key, which you can get from [OpenAI's API website](https://beta.openai.com/).

You can update the model in the API call by modifying the model parameter to use any GPT model:
```javascript
body: JSON.stringify({
    model: 'gpt-4',  // Example for switching to GPT-4
    messages: [
      {
        role: 'system',
        content: "Your system prompt here..."
      },
      {
        role: 'user',
        content: message,
      },
    ],
}),
```

### Part 5: Import and Use the ChatBot

Step 1: Import the ChatBot component into your React app:
```jsx
import ChatBot from './path-to-your-file/ChatBot';
```

Step 2: Customize any props or design elements to match your project.

---
For support or inquiries, contact: keanudatatech@gmail.com or https://www.linkedin.com/in/keanugms.