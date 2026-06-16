# Professional Resume Builder

A premium, modern, and modular web-based resume builder designed to help engineers and professionals create, manage, preview, and export print-perfect resumes. 

The interface features a sleek, dark-mode design system with an instant, interactive side-by-side preview pane.

---

## 🚀 Live Demo & Deployment
This project is fully static and runs natively in the browser. You can deploy it to any static hosting provider (e.g., Cloudflare Pages, Vercel, Netlify, or GitHub Pages) by deploying the root folder contents.

---

## 🎨 Key Features

- **Modular Architecture**: Clean separation of concerns with dedicated files for layout (`index.html`), styling (`style.css`), and functionality (`app.js`).
- **Multi-Profile Management**: Support for creating, duplicating, renaming, and deleting multiple profile configurations.
- **Backup & Migration**: One-click import and export of JSON profile data to easily back up or transfer configurations.
- **Dynamic Live Preview**: Instant side-by-side preview with automatic multi-page pagination.
- **Dual Export Options**:
  - **Download PDF**: Standardized PDF printing layout via the browser's native print API.
  - **Download DOCX**: Direct compilation into high-quality, ATS-friendly Word documents (DOCX) using native document specifications.
- **Sleek Dark Mode**: Responsive glassmorphism interface with intuitive detail drawers for personal information, education, and certifications.
- **Interactive Parsing**: Clipboard text capture, drag-and-drop text file imports, and automated section detection.

---

## 🛠️ File Structure

```text
├── index.html       # Clean HTML5 structure containing UI panels and details drawers
├── style.css        # Premium dark mode theme styles, layout, and print styles
└── app.js           # Core application controller, DOM handlers, state management, and exports
```

---

## ⚙️ Getting Started

### Prerequisites
No compilation or server setup is required. The project runs natively in modern web browsers.

### Running Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/Janakirao4701/Professional_Resume_Builder.git
   ```
2. Open the directory:
   ```bash
   cd Professional_Resume_Builder
   ```
3. Open `index.html` directly in any web browser, or serve it using a local HTTP server:
   * **Python**: `python -m http.server 8000`
   * **Node.js**: `npx serve`
   * **VS Code**: Use the "Live Server" extension.

---

## 📦 Third-Party Libraries

To keep the codebase lightweight and maintainable, dependencies are loaded dynamically via high-performance CDNs:
- **[docx.js](https://cdn.jsdelivr.net/npm/docx@7.3.0/)**: Used for client-side ATS-compliant DOCX document packaging.
- **Google Fonts**: Loading modern typography faces including *Plus Jakarta Sans*, *Outfit*, and *Inter*.

---

## 📄 License
This project is open-source. Feel free to customize it to fit your professional needs.
