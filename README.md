# Prompt Manager

🚀 A powerful Firefox browser extension designed for seamless prompt management with universal input field support, empowering you to interact with Gemini AI like never before.

This extension allows you to save, manage, and quickly access your favorite prompts, injecting them into any text field with a simple trigger or keyboard shortcut. It's built with a modern tech stack including React and the latest WebExtension APIs, ensuring a smooth and responsive user experience.

!Screenshot](placeholder.png)

## ✨ Features

*   **📝 Prompt Management:** Easily create, edit, and delete prompts through a user-friendly interface.
*   **⚡ Universal Input Support:** Use the `/p` trigger in any input field or textarea to bring up your prompt library.
*   **⌨️ Keyboard Shortcuts:** Access your prompts instantly with customizable keyboard shortcuts (Ctrl+Shift+P and Ctrl+Shift+S).
*   **🖱️ Context Menu Integration:** Save selected text as a new prompt with a simple right-click.
*   **📂 Import/Export:** Backup and restore your prompts with JSON import and export functionality.
*   **🎨 Light/Dark Theme:** The extension automatically adapts to your system's theme for a comfortable viewing experience.
*   **🔒 Privacy-Focused:** All your data is stored locally in your browser, ensuring your prompts remain private.

## 📦 Installation

### From the Firefox Add-ons Store (Recommended)

1.  Visit the [AI Gateway page on the Firefox Add-ons store](https://addons.mozilla.org/).
2.  Click "Add to Firefox".
3.  Follow the on-screen instructions.

### From Source (for Developers)

1.  Clone this repository: `git clone https://github.com/your-username/ai-gateway.git`
2.  Navigate to the project directory: `cd ai-gateway`
3.  Install the dependencies: `npm install`
4.  Build the extension: `npm run build`
5.  Open Firefox and navigate to `about:debugging`.
6.  Click "This Firefox" and then "Load Temporary Add-on".
7.  Select the `manifest.json` file from the `dist` directory in the project folder.

## 🚀 Usage

### Creating a Prompt

1.  Click on the AI Gateway icon in your browser's toolbar.
2.  Click the "Add Prompt" button.
3.  Fill in the title, content, and any relevant tags for your prompt.
4.  Click "Save".

### Using a Prompt

*   **With the `/p` trigger:** In any text field, type `/p` to open the prompt selector overlay. Start typing to search for your prompt, use the arrow keys to navigate, and press Enter to insert the prompt's content.
*   **With Keyboard Shortcuts:**
    *   `Ctrl+Shift+P`: Opens the prompt selector overlay.
    *   `Ctrl+Shift+S`: Saves the currently selected text as a new prompt.
*   **From the Popup:**
    1.  Click the extension icon.
    2.  Find the prompt you want to use.
    3.  Click the "Copy" button to copy the prompt's content to your clipboard.

### Saving a Prompt from a Webpage

1.  Highlight any text on a webpage.
2.  Right-click and select "Save as Prompt".
3.  A dialog will appear with the selected text pre-filled as the content. Add a title and tags, then save.

## 🛠️ Tech Stack

*   **React 18:** For building the user interface.
*   **WebExtension API (Firefox Manifest V3):** The foundation of the browser extension.
*   **localStorage:** For local data persistence.
*   **CSS Modules / Tailwind CSS:** For styling the components.
*   **Webpack / Vite:** For bundling the assets.
*   **Node.js & npm:** For package management and scripting.
*   **web-ext:** For testing and development.
*   **ESLint:** For code quality.
*   **Git:** For version control.

## 🤝 Contributing

Contributions are welcome! If you have any ideas, suggestions, or bug reports, please open an issue or submit a pull request.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
