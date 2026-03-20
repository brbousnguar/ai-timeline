# AI History Timeline Project

A comprehensive, interactive web application showcasing the milestones of Artificial Intelligence, from historical breakthroughs to future planned events.

## Project Overview

-   **Purpose:** To provide a visual and filterable timeline of significant AI events.
-   **Architecture:** A single-page application (SPA) built with vanilla HTML, CSS, and JavaScript.
-   **Key Features:**
    -   Interactive timeline with scroll animations.
    -   Filtering by company, year, and search terms.
    -   Support for "Major" vs "Minor" events.
    -   Dedicated section for "Future & Planned Events".
    -   Dark/Light theme support.
    -   Detailed modal views for each event.
-   **Technologies:**
    -   Frontend: HTML5, CSS3 (Modern features like CSS Variables, Grid, and Flexbox), Vanilla JavaScript.
    -   Data: Embedded directly in `script.js` for fast loading and simple deployment.
    -   Assets: SVG icons and PNG logos for AI companies.
    -   Scripts: Python for automated data enhancement (link addition).

## Project Structure

-   `index.html`: The main entry point and UI structure.
-   `script.js`: Contains both the application logic (filtering, rendering, theme management) and the event dataset.
-   `styles.css`: Comprehensive styling, including theme-specific variables and responsive design.
-   `add_links.py`: A Python utility script to automatically map official announcement links to events in `script.js`.
-   `assets/logos/`: Contains brand assets for major AI companies (OpenAI, Google, Meta, etc.).

## Getting Started

### Running the Application
Since this is a static site, you can run it by opening `index.html` in any modern web browser. No build step or local server is strictly required, though using a simple server like `live-server` or VS Code's "Live Server" extension is recommended for development.

### Updating Event Links
To update the event links in `script.js` using the data defined in `add_links.py`:
1.  Ensure Python 3 is installed.
2.  Run the script:
    ```bash
    python add_links.py
    ```

## Development Conventions

-   **Adding Events:** New events should be added to the `timelineEvents` array in `script.js`.
-   **Event Properties:**
    -   `date`: String (e.g., "October 2025", "Q2 2027 (Planned)").
    -   `title`: Clear, concise event name.
    -   `company`: The organization responsible (e.g., "OpenAI", "Google").
    -   `description`: A detailed explanation of the event.
    -   `impact`: A brief note on why the event is significant.
    -   `link`: (Optional) URL to an official announcement.
    -   `eventType`: (Optional) Set to `"major"` for highlighted events or `"planned"` for future entries.
-   **Styling & UI Aesthetics:** 
    -   Maintain the premium, modern aesthetic established in the UI.
    -   Use CSS variables defined in `:root` for consistency across themes (including `var(--glass-bg)` and `var(--glass-border)`).
    -   Use the `Outfit` font for titles and headers, and `Inter` for standard body text.
    -   Apply glassmorphism (`backdrop-filter: blur(...)`) and rich visual effects like dynamic backgrounds, hover 3D tilts, and glows for any new UI components.
-   **Icons:** Use inline SVGs for UI elements to ensure they scale and respond to theme changes.
-   **Logos:** Company logos are automatically matched by name. Ensure new logos are added to `assets/logos/` with names matching the `company` field (converted to lowercase).
