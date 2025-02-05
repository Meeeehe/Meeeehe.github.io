# 3D Periodic Table Visualization

## Project Overview

This project was developed as part of an **assessment from Kasatria Technologies Sdn Bhd**. It is an interactive **3D periodic table** built using **Three.js**, dynamically fetching data from **Google Sheets** and rendering elements as 3D objects. Users can interact with the table and switch between multiple layouts, including table, sphere, helix, and grid views.

---

## Features

✅ Google Login authentication using OAuth 2.0  
✅ 3D visualization using Three.js  
✅ Dynamic data fetching from Google Sheets (CSV format)  
✅ Smooth animations and transitions using TWEEN.js  
✅ Multiple layout options: **table, sphere, helix, and grid**  
✅ Interactive camera controls (rotate, zoom, pan)  
✅ Responsive UI that adapts to different screen sizes

---

## Technologies Used

- **HTML5** – Structure
- **CSS3** – Styling
- **JavaScript (ES6+)** – Logic and rendering
- **Three.js** – 3D rendering library
- **Google Sheets API** – Data retrieval
- **Google OAuth 2.0** – Authentication
- **TWEEN.js** – Smooth animations

---

## Project Structure

```
📂 3D-Periodic-Table
│── 📄 index.html # Login page with Google authentication
│── 📄 periodictable.html # Main 3D visualization page
│── 📄 style.css # Styling for the login page
│── 📄 periodictable.css # Styling for the 3D periodic table UI
│── 📂 assets/ # Folder containing CSS and image assets
│── 📂 scripts/ # JavaScript files (if separated)
│── 📄 README.md # Project documentation (this file)
```

---

## Getting Started

### Clone the Repository

```sh
git clone https://github.com/Meeeehe/Meeeehe.github.io.git
cd Meeeehe.github.io
```

---

## Set Up Google Authentication

To enable Google Login authentication for this project, follow these steps:

### 1. Create a Google OAuth Client ID

1. Go to the **[Google Cloud Console](https://console.cloud.google.com/)**.
2. Navigate to **APIs & Services > Credentials**.
3. Click **Create Credentials** → **OAuth Client ID**.
4. Select **Web Application** as the application type.
5. Under **Authorized JavaScript origins**, add your webpage URL, e.g.: https://meeeehe.github.io
6. Under **Authorized redirect URIs**, add your webpage callback URL, e.g.: https://meeeehe.github.io/oauth2callback
7. Click **Create**, then copy the **Client ID**.

### 2. Update the Google Client ID in `index.html`

Replace `"YOUR_GOOGLE_CLIENT_ID"` with the actual **Client ID** you copied:

```html
<div
  id="g_id_onload"
  data-client_id="YOUR_GOOGLE_CLIENT_ID"
  data-callback="handleCredentialResponse"
></div>
```

### 3. Save and Test

- Open `index.html` in a browser.
- If everything is set up correctly, you should see a **Google Sign-In** button.
- Sign in with your **Google Account**, and it will redirect to `periodictable.html`.

## Update Google Sheets Data Source

To dynamically load data into the 3D Periodic Table, you need to set up a Google Sheet and configure it to be publicly accessible.

### 1. Create a Google Sheet

1. Open [Google Sheets](https://docs.google.com/spreadsheets/).
2. Create a new sheet and enter **six columns** in the first row:
   - `Name`
   - `Photo URL`
   - `Age`
   - `Country`
   - `Interest`
   - `Net Worth`

### 2. Publish the Google Sheet

1. Click **"File" → "Share"** and change the access to **"Anyone with the link"**.
2. Click **"File" → "Publish to the Web"**.
3. Under **"Link"**, select **Comma-separated values (.csv)**.
4. Click **"Publish"** and confirm.

### 3. Get the Public CSV Link

1. After publishing, copy the generated link.
2. The link should look something like this: https://docs.google.com/spreadsheets/d/e/EXAMPLE-ID/pub?output=csv

### 4. Update `periodictable.html`

Replace the `SHEET_URL` in `periodictable.html` with your Google Sheets **CSV link**:

```js
const SHEET_URL =
  "https://docs.google.com/spreadsheets/d/e/YOUR_SHEET_ID/pub?output=csv";
```

### 5. Save and Test

- Open `periodictable.html` in a browser.
- The data from your Google Sheet should now be loaded dynamically.

If you encounter issues, ensure that:

- ✅ The Google Sheet is set to **"Anyone with the link can view"**.
- ✅ The CSV format is selected in **"Publish to the Web"**.

## Usage Instructions

Once the project is set up, follow these steps to use it:

### 1. Open `index.html` and Sign In

- Navigate to the `index.html` file in your browser.
- Click the **Google Sign-In button** to authenticate.

### 2. Automatic Redirect to `periodictable.html`

- Upon successful login, the page will automatically redirect to `periodictable.html`.

### 3. Switch Between Views

Use the buttons at the bottom of the page to switch between different 3D layouts:

| Button     | Function                                          |
| ---------- | ------------------------------------------------- |
| **Table**  | Displays the elements in a periodic table layout. |
| **Sphere** | Arranges elements into a spherical shape.         |
| **Helix**  | Organizes elements into a double-helix pattern.   |
| **Grid**   | Arranges elements into a structured grid.         |

### 4. Camera Controls

- **Rotate:** Click and drag the mouse to rotate the view.
- **Zoom:** Use the scroll wheel to zoom in and out.
- **Pan:** Right-click and drag to move the view.

### 5. Interact with Elements

- Hover over an element to see a **highlight effect**.
- Click an element (if functionality is added) to trigger additional actions.

## Final Notes

This project was developed as part of an **assessment for Kasatria Technologies Sdn Bhd**. It explores the capabilities of **3D visualization using Three.js**, with a focus on interactivity and smooth user experience.
