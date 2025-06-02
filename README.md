# Media Dashboard

A personalized, client-side dashboard to monitor your media services like SABnzbd, Plex, and Sonarr all in one place. This dashboard is a single HTML file that runs directly in your browser and uses `localStorage` to save your settings.

## ✨ Features

* **Service Integration:**
    * **SABnzbd:**
        * View current download queue and history.
        * "Show More" functionality to load more download history.
        * In-app notification for newly completed downloads (if enabled).
    * **Plex:**
        * Link your Plex account via a PIN-based authentication flow.
        * Display "Continue Watching" items.
        * Display "Recently Added Movies" (toggleable in settings).
        * Display "Recently Added TV Shows" (toggleable in settings).
        * "Load All" option for Plex lists.
        * In-app notifications for new movies and TV shows/episodes added to Plex (if enabled).
    * **Sonarr:**
        * View upcoming TV show episodes from your calendar (next 7 days).
* **Customizable Dashboard:**
    * Configure URLs and API keys for SABnzbd and Sonarr.
    * Set custom titles for each service card on the dashboard.
    * Define the display order of service cards.
* **User-Friendly Interface:**
    * Clean, responsive design that works on desktop and mobile.
    * **Dashboard View:** Displays all configured service cards.
    * **Settings View:** Easy-to-use interface for all configurations.
    * **Floating Action Buttons:** Quick access to Settings, Notification History, and Scroll Page (Up/Down).
    * **Mobile Accordion:** On smaller screens, service cards collapse into an accordion style for better usability.
    * **Scroll Indicators:** Visual cues for scrollable content within cards on desktop.
    * Clear loading, success, and error messages.
* **Notifications:**
    * Toggleable in-app toast notifications for service updates.
    * A "Notification History" modal to review past notifications.
    * Option to clear notification history.
    * "Test Notification" button in settings.
* **Client-Side Operation:**
    * Runs entirely in your web browser.
    * All settings, including API keys and Plex tokens, are stored in your browser's `localStorage`. No backend server is required.
* **Auto-Refresh:**
    * Dashboard data automatically refreshes every 5 minutes.

## 🛠️ Tech Stack

* **Frontend:** HTML, CSS (Flexbox, Grid, Custom Properties), Vanilla JavaScript
* **APIs Consumed:**
    * SABnzbd API
    * Plex API (including Plex.tv PIN authentication)
    * Sonarr API (v3)
* **Storage:** Browser `localStorage`

## 🚀 Getting Started

### Prerequisites

* A modern web browser (e.g., Chrome, Firefox, Edge, Safari).
* Access to your SABnzbd, Plex, and Sonarr instances with their respective URLs and API keys.

### Installation

1.  **Download or Clone:**
    * Download the `md.html` file.
    * Or, clone the repository:
        ```bash
        git clone [https://github.com/davidsnyder-nc/mediadashboard.git](https://github.com/davidsnyder-nc/mediadashboard.git)
        ```
2.  **Open in Browser:**
    * Navigate to the directory where you saved/cloned the file.
    * Open the `md.html` file directly in your web browser.

### Initial Configuration

1.  When you first open the dashboard, you might see a message "Welcome! Please configure your services via the settings icon to see your media."
2.  Click the **Settings icon** (⚙️) in the floating action buttons (usually bottom-right).
3.  In the **Settings View**:
    * **SABnzbd Configuration:**
        * Enter your SABnzbd URL (e.g., `http://localhost:8080`).
        * Enter your SABnzbd API Key.
    * **Sonarr Configuration:**
        * Enter your Sonarr URL (e.g., `http://localhost:8989`).
        * Enter your Sonarr API Key.
    * **Plex Configuration:**
        * Enter your Plex Server URL (e.g., `http://localhost:32400`).
        * Click "Link Plex Account (Get Token)".
        * Follow the on-screen instructions: Go to `https://plex.tv/link` and enter the PIN displayed on the dashboard.
        * Wait for the linking process to complete. A success message will be shown.
        * Toggle "Enable Recently Added Movies" and "Enable Recently Added TV Shows" as desired.
    * **Card Titles:** Customize the titles for each service card (e.g., change "Downloads" to "My SABnzbd Downloads").
    * **Card Display Order:** Select which service card appears in which position (1st, 2nd, etc.). You can choose "None" to hide a position.
    * **Notification Settings:**
        * Check "Enable In-App Notifications" to receive toast messages for updates.
        * Click "Test Notification" to see an example.
4.  Click **"Save & View Dashboard"**. Your settings will be saved in `localStorage`, and you'll be taken to the main dashboard view.

## 📖 How to Use

* **Dashboard View:**
    * Displays cards for each configured and enabled service in the order you've set.
    * SABnzbd, Plex, and Sonarr sections will show relevant information.
    * Use "Show More" or "Load All" buttons within cards to see more items if available.
    * On mobile, tap a card's title to expand or collapse its content.
* **Settings View:**
    * Access by clicking the Settings icon (⚙️).
    * Modify any service URLs, API keys, card titles, card order, or notification preferences.
    * Re-link Plex if needed.
    * Remember to click "Save & View Dashboard" to apply changes.
* **Notification History:**
    * Click the Bell icon (🔔) in the floating action buttons to view recent in-app notifications.
    * Click "Clear" within the modal to remove all history.
* **Scroll Page Button:**
    * Click the Arrow icon (↕️) to scroll to the top or bottom of the page. The icon indicates the direction of scroll.

## 💡 Notes

* **Security:** Since API keys and tokens are stored in your browser's `localStorage`, be mindful of who has access to your computer and browser, especially if using a shared machine.
* **Local Network:** This dashboard is primarily designed for accessing services running on your local network. If your services are exposed externally, ensure they are secured appropriately.
* **API Limits:** There are no explicit rate limit handling mechanisms built into this dashboard. For typical home use, this should not be an issue.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Please feel free to check the [issues page](https://github.com/davidsnyder-nc/mediadashboard/issues) (if the repository is public and has issues enabled).

## 📝 License

This project is open-source. Please refer to the repository's license file for more details (e.g., MIT License, if you choose to add one).
