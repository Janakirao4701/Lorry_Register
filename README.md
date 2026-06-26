# 🚛 Lorry Trips Register — Adding Value Transport

An offline-first, client-side daily entry sheet designed for transport operators to manage lorry trips, track tonnage records, compute billing, and share data securely—all without external databases, servers, or internet dependencies.

This application runs natively in modern web browsers and can be deployed directly to static hosting services like **GitHub Pages**.

---

## 🚀 Live Deployment
The project is hosted live on GitHub Pages:
**[https://janakirao4701.github.io/Lorry_Register/](https://janakirao4701.github.io/Lorry_Register/)**

---

## 🎨 Key Features

### 1. Offline-First & Safe Storage
* **Auto-Save**: All vehicle entries are automatically saved to your browser cache (`localStorage`) as you type.
* **Dual-Write Backup**: Writes data to a primary key (`lorry_register_v3`) and a backup key (`lorry_register_v3_bak`) to protect your records from unexpected cache corruption.

### 2. Real-Time Calculator (₹130/Ton)
* **Automatic Billing**: Enter the tonnage for any trip, and the row instantly calculates the billing amount (`Tonnage * 130`).
* **Dynamic Aggregates**: Recalculates total trips, total tonnage, and total billing amounts in real time for:
  - Each individual vehicle card header badge.
  - Each individual vehicle table footer.
  - The top dashboard stats panel.
  - The bottom floating Grand Bar.

### 3. Serverless State Sharing (URL-Based)
* **No Database Sharing**: Click **Share Link** to compress your entire active sheet into a short, Base64-encoded text payload attached to the URL hash (e.g., `#share=eyJ2...`).
* **Delimited Compression**: Uses a custom pipe-and-semicolon formatting algorithm that compresses the sharing link by **over 50%**, keeping links extremely short and compatible with chat tools like WhatsApp or Email.
* **Consent Gate**: When opening a shared link, the app shows a warning modal prompting for confirmation before loading the data, preventing you from accidentally overwriting your own local entries.

### 4. CSV Import & Export Compatibility
* **Backup Exports**: Export your sheet as a formatted CSV file detailing vehicle numbers, dates, invoice numbers, tonnages, row totals, and grand totals.
* **locale-Safe Importing**: Import CSV files back into the register. The import parser automatically detects date formats (`DD/MM/YYYY`, `MM/DD/YYYY`, and `YYYY-MM-DD`) and normalizes them. The parser ignores the Amount column on import and recalculates amounts dynamically to guarantee mathematical correctness.

### 5. Premium UI & Mobile Optimization
* **Aesthetics**: Sleek interface built with modern typography (`Inter` & `JetBrains Mono`), glassmorphism overlays, and smooth transition animations (250ms cubic-bezier).
* **Auto Date Picker**: Click anywhere in a row's Date cell to programmatically trigger the browser's calendar dropdown, resolving the default behavior where you had to hit the tiny right-side edge icon.
* **Dark Mode**: Features a native dark theme synced automatically with your OS preference, complete with a manual theme toggle.
* **Mobile Breakpoints**:
  - **Stats Cards Grid**: Metrics display in a compact 2x2 CSS Grid instead of a vertical list.
  - **Horizontal Grand Bar**: Grand totals remain on a single horizontal row, wrapping only action buttons below them.
  - **Toolbar Auto-Wrap**: Toolbar action buttons arrange in a 2x2 grid to prevent layout overflow and keep tap targets large.
  - **Table Swiping**: Tables allow smooth horizontal scroll-swiping inside cards to prevent scaling distortions.

### 6. Print-Ready Styling
* Press `Ctrl+P` or click **Print** to open the print dialog. 
* Interactive components (theme toggles, buttons, search bars, inputs) are automatically hidden on printouts.
* Table borders and colors are optimized for high-contrast ink-saving black & white prints.

---

## 🛠️ File Structure

```text
├── index.html        # Monolithic self-contained app (HTML, CSS Variables, and JS modules)
├── lorry_logo.svg    # High-resolution standalone logo asset
├── README.md         # This documentation file
└── .gitignore        # Standard Git exclusions (ignoring local resume docs/temp backups)
```

---

## ⚙️ How to Run Locally

### Prerequisites
The app runs natively in any modern web browser. No compilation, node modules, or server setup is required.

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/Janakirao4701/Lorry_Register.git
   ```
2. Open the directory:
   ```bash
   cd Lorry_Register
   ```
3. Open `index.html` directly in your browser. Alternatively, run a local web server:
   * **Python**: `python -m http.server 8000`
   * **Node.js**: `npx serve`

---

## ⚠️ Data Safety Warning
> [!IMPORTANT]
> Because this application stores data directly in your browser cache (`localStorage`), **clearing your browser history or site data will delete your records**.
> Please use the **Export CSV** button regularly to back up your entries.
