# Multi-site Craft CMS

## Overview
This project was built using **Craft CMS** as the main content management system, with a local development environment set up using **Docker**, **DDEV**, and **Composer**. We used Twig templates for dynamic pages, implemented responsive layouts with CSS Grid and Flexbox, and added minimal JavaScript for interactive elements.

## What We Built
- **Content Management & CMS Setup**
  - Configured Craft CMS for content input and management.
  - Database snapshot automatically imported (see “Database” below).

- **Template Development**
  - Twig templates for the homepage, project pages, services, gallery, about page, and housing pages.
  - Grid layouts and a component-based structure using custom CSS classes (e.g. `.twige`, `.grid.cards`).
  - Global H2 style definitions and themes (mariahuis, sintcoleta, cultuurcolette).

- **Interaction & Responsiveness**
  - CSS media queries for mobile responsiveness.
  - Minimal JavaScript for menu toggles and other UI interactions.

- **Version Control & Dependencies**
  - Git for version control.
  - Composer for PHP packages and Craft CMS.

## Technologies Used
- **Craft CMS** – content management and dynamic pages.
- **Twig** – templating engine.
- **Docker** – containerization of the web server and database.
- **DDEV** – easy local setup and configuration for Craft CMS.
- **Composer** – dependency management.
- **HTML5 & CSS3** – structure and styling.
- **Flexbox & CSS Grid** – layout systems.
- **JavaScript** – interactive components.

## Installation & Usage (Visual Studio Code)

### 1. Requirements
- Docker installed and running.
- DDEV installed.
- Composer available.
- Visual Studio Code (or another IDE).

### 2. Configure the Project
```bash
git clone https://your-repo-url.git
cd project-2-werkstuk-akg
ddev config --project-type=craftcms --docroot=web --create-docroot
```

### 3. Start DDEV & Install Dependencies
```bash
ddev start
composer install
```

### 4. Database
- Place your database snapshot (e.g. `project-2-werkstuk-akg.sql.gz`) inside:
  ```
  .ddev/db_snapshots/
  ```

- DDEV automatically imports the snapshot when running:
  ```bash
  ddev start
  ```

- You can also import it manually:
  ```bash
  ddev import-db --src=.ddev/db_snapshots/project-2-werkstuk-akg.sql.gz
  ```

### 5. Access the Website
- **Mariahuis:** `https://project-2-werkstuk-akg.ddev.site/`
- **Sint-Coleta:** `https://project-2-werkstuk-akg.ddev.site/sint-coleta`
- **Cultuur-Colette:** `https://project-2-werkstuk-akg.ddev.site/cultuur-colette`
- **Admin URL:** `https://project-2-werkstuk-akg.ddev.site/admin`
