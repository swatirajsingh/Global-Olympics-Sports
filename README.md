# Global Olympics Sports

A lightweight Flask app that hosts a Tableau Public dashboard and story for the Global Olympics Sports dataset. The app presents a clean landing page with tabs to switch between the dashboard and story view, making it easy to share and embed a public analytics experience.

## Overview

This project is designed to:

- serve a simple web page using Flask
- embed a Tableau Public dashboard and story in the browser
- allow quick switching between dashboard and story views from a single page
- deploy easily to Render using the included Procfile

## Tech Stack

- Python 3.12
- Flask 3.x
- Gunicorn
- Tableau Public embed links

## Project Structure

```text
.
├── app.py               # Flask app entry point
├── Procfile             # Render startup command
├── requirements.txt     # Python dependencies
├── runtime.txt          # Python runtime version
├── templates/
│   └── index.html       # Dashboard/story UI and embedded Tableau content
└── README.md            # Project documentation
```

## Features

- Single-page dashboard experience
- Toggle between "Dashboard" and "Story" views
- Direct links to the published Tableau workbooks
- Responsive layout for desktop and smaller screens
- Ready for deployment on Render

## Local Setup

1. Clone the repository:

```bash
git clone https://github.com/swatirajsingh/Global-Olympics-Sports.git
cd Global-Olympics-Sports
```

2. Create and activate a virtual environment:

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Run the app locally:

```bash
python app.py
```

The application will start on the default Flask port, which is typically `5000`.

## Run with Flask Development Server

If you prefer the Flask development server:

```bash
set FLASK_APP=app.py
flask run
```

## Deployment on Render

This project includes the required Render configuration:

- `Procfile` runs the app with Gunicorn
- `runtime.txt` pins the Python version

To deploy on Render:

1. Create a new Web Service in Render
2. Connect the repository
3. Use the default build and start commands from the project configuration
4. Render will use the `Procfile` to start the app automatically

## Notes

- The embedded Tableau views are hosted through Tableau Public.
- If the workbook is changed or made private, the page may stop displaying the embedded content.
- The live links in the template point to the published Tableau workbook for the Global Olympics Sports project.

## License

No explicit license file is included in this repository. If you plan to share or reuse this project publicly, consider adding an appropriate open-source license.
