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
````md
📂 3D-Periodic-Table
│── 📄 index.html # Login page with Google authentication
│── 📄 periodictable.html # Main 3D visualization page
│── 📄 style.css # Styling for the login page
│── 📄 periodictable.css # Styling for the 3D periodic table UI
│── 📂 assets/ # Folder containing CSS and image assets
│── 📂 scripts/ # JavaScript files (if separated)
│── 📄 README.md # Project documentation (this file)

````

---

## Getting Started  

### Clone the Repository  
```sh
git clone https://github.com/YOUR_GITHUB_USERNAME/3D-Periodic-Table.git
cd 3D-Periodic-Table
```
---

## Set Up Google Authentication  
To enable Google Login authentication for this project, follow these steps:

### 1. Create a Google OAuth Client ID  
1. Go to the **[Google Cloud Console](https://console.cloud.google.com/)**.  
2. Navigate to **APIs & Services > Credentials**.  
3. Click **Create Credentials** → **OAuth Client ID**.  
4. Select **Web Application** as the application type.  
5. Under **Authorized JavaScript origins**, add: (Your webpage URL) e.g. (https://meeeehe.github.io)
6. Under **Authorized redirect URIs**, add: (Your webpage URL) e.g. (https://meeeehe.github.io/oauth2callback)
7. Click **Create**, then copy the **Client ID**.

### 2. Update the Google Client ID in `index.html`  
Replace `"YOUR_GOOGLE_CLIENT_ID"` with the actual **Client ID** you copied:

```html
<div id="g_id_onload"
  data-client_id="YOUR_GOOGLE_CLIENT_ID"
  data-callback="handleCredentialResponse">
</div>
```
### 3. Save and Test
- Open `index.html` in a browser.
- If everything is set up correctly, you should see a **Google Sign-In** button.
- Sign in with your **Google Account**, and it will redirect to `periodictable.html`.


