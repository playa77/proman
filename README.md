# ProMan: Prompt Manager for Firefox

🚀 **ProMan is an intelligent and seamless prompt management tool, designed as a Firefox browser extension to enhance your workflow with AI, especially Gemini.**

It provides a central library for all your prompts, accessible from any input field on the web. With ProMan, you can save, manage, and deploy your most effective prompts with a simple `/p` trigger, a keyboard shortcut, or a right-click.

Built with React and modern web technologies, ProMan is designed to be fast, intuitive, and entirely local—your data never leaves your machine.

---

## ✨ Features

ProMan is more than just a clipboard; it's a complete system for prompt engineering, designed to feel like a native part of your browser.

*   **📝 Prompt Library**: A clean, searchable interface to create, edit, and organize all your prompts.
*   **⚡ Universal Trigger**: Type `/p` in any text field (`<input>`, `<textarea>`, or `contenteditable` divs) to instantly open a prompt selector overlay.
*   **⌨️ Keyboard Shortcuts**:
    *   `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac) to open the prompt selector anytime.
    *   `Ctrl+Shift+S` (or `Cmd+Shift+S` on Mac) to quickly save any selected text as a new prompt.
*   **🖱️ Context Menu Integration**: Right-click on any selected text and choose "Save as Prompt" to add it to your library effortlessly.
*   **🏷️ Tagging & Searching**: Organize your prompts with tags. The powerful search function filters by title, content, or tags in real-time.
*   **💾 Import & Export**: Easily back up your entire prompt library to a JSON file or import prompts from another machine. You can choose to merge or replace existing data.
*   **🌗 Light & Dark Mode**: The interface automatically adapts to your system's theme for a comfortable viewing experience, day or night.
*   **💎 Gemini-Optimized**: Special care has been taken to ensure flawless operation within Google Gemini's main chat and system instruction inputs.
*   **🔒 100% Private**: All your data is stored locally using the `browser.storage.local` API. There are no external servers, no tracking, and no network requests (except to the Firefox Add-ons store for updates).

## 🖼️ Screenshots

*(Placeholder: Add screenshots of the popup, the /p trigger overlay, and the context menu here once the UI is complete.)*

**Main Popup View (Dark Mode)**
`[Image of the main prompt list with search and add buttons]`

**Prompt Selector Overlay in Action**
`[GIF showing a user typing /p in a textarea and the overlay appearing]`

**Quick Save with Context Menu**
`[Image of a user right-clicking selected text on a webpage]`

## 📦 Installation

There are two ways to install ProMan.

### 1. From the Firefox Add-ons Store (Recommended)

Once the extension is approved, you will be able to install it directly from the official Firefox Add-ons website.

*   **(Link will be here)**

### 2. From Source (For Developers)

If you want to run the latest development version or contribute to the project, you can install it from the source code.

1.  **Clone the repository**:
    ```bash
    git clone https://github.com/your-username/proman.git
    cd proman
    ```

2.  **Install dependencies**:
    ```bash
    npm install
    ```

3.  **Build the extension**:
    ```bash
    npm run build
    ```
    This will create a `dist` folder with the bundled extension files.

4.  **Load the extension in Firefox**:
    *   Open Firefox and navigate to `about:debugging`.
    *   Click on "This Firefox".
    *   Click "Load Temporary Add-on...".
    *   Select any file inside the `dist` directory.

## 🚀 Usage Guide

Here’s how to get the most out of ProMan.

### Creating a Prompt

1.  Click the ProMan icon in your Firefox toolbar to open the popup.
2.  Click the "Add Prompt" button.
3.  Fill in the title, the content of your prompt, and any comma-separated tags.
4.  Click "Save".

### Using a Prompt

There are three ways to insert a prompt:

1.  **The `/p` Trigger**: In any input field, type `/p`. An overlay will appear. Start typing to search for your prompt, use the arrow keys to navigate, and press `Enter` to insert the selected prompt's content. Press `Esc` to close the overlay.
2.  **Keyboard Shortcut**: Press `Ctrl+Shift+P` to bring up the same overlay, no matter where you are on the page.
3.  **From the Popup**: Open the main popup, find the prompt you want, and click the "Copy" button to copy its content to your clipboard.

### Saving Selected Text

Highlight any text on a webpage. You can either:
*   **Right-click** and select "Save as Prompt".
*   Press the `Ctrl+Shift+S` shortcut.

A small dialog will appear, pre-filled with the selected content, allowing you to add a title and tags before saving.

## 🛠️ Technology Stack

ProMan is built with a modern, robust, and efficient technology stack.

*   **Core Technologies**:
    *   **React 18**: For building a dynamic and responsive user interface.
    *   **WebExtension API (Manifest V3)**: The standard for creating secure and performant Firefox extensions.
    *   **CSS Modules / Tailwind CSS**: For scoped, maintainable, and utility-first styling.
*   **Build Tools**:
    *   **Vite / Webpack**: For bundling the React code and assets into an optimized package.
    *   **Node.js & npm**: For package management and running scripts.
*   **Development Tools**:
    *   **ESLint**: To ensure high-quality, consistent code.
    *   **web-ext**: The official tool for developing and testing Firefox extensions.

## 💻 Development & Contributing

Contributions are welcome! Whether you're fixing a bug, adding a feature, or improving documentation, your help is appreciated.

### Setup for Local Development

1.  Follow the installation steps in the "From Source" section.
2.  To start the development server with auto-reloading, run:
    ```bash
    npm run dev
    ```
    This command will watch for file changes and automatically rebuild the extension. You can then use `web-ext run` in another terminal or reload the temporary add-on in `about:debugging` to see your changes.

### Project Structure

The project follows a logical structure to keep code organized and maintainable.

```
proman/
├── dist/                   # Bundled output for the extension
├── public/                 # Static assets (icons, etc.)
├── src/
│   ├── background/         # Background service worker
│   ├── content/            # Content script and styles
│   ├── popup/              # Main popup UI components
│   │   ├── components/     # Reusable React components
│   │   └── Popup.jsx
│   └── utils/              # Helper functions (storage, etc.)
├── manifest.json           # Extension configuration
├── package.json
└── webpack.config.js       # Build configuration
```

### Git Workflow

1.  Fork the repository.
2.  Create a new branch for your feature (`git checkout -b feature/your-feature-name`).
3.  Make your changes and commit them daily with clear messages.
4.  Push to your branch (`git push origin feature/your-feature-name`).
5.  Open a pull request with a detailed description of your changes.

## 🔒 Privacy Policy

Your privacy is paramount. ProMan is designed with a privacy-first approach.

*   **Local Storage**: All of your prompt data is stored exclusively on your local computer using the `browser.storage.local` API. This data is not synced to any cloud and is not accessible by the developer or any third party.
*   **No Tracking**: The extension does not include any analytics, tracking pixels, or telemetry.
*   **Minimal Permissions**: ProMan only requests the permissions necessary for its core functionality:
    *   `storage`: To save your prompts locally.
    *   `activeTab`: To insert prompts into input fields.
    *   `contextMenus`: To enable the "Save as Prompt" right-click feature.

## 📄 License

This project is open source and available under the **MIT License**. See the [LICENSE](LICENSE) file for more details.
