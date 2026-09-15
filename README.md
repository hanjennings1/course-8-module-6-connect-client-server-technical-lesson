# Flask + Frontend Starter Project
**Completed Sept 15, 2026**

---

## Objectives Learned:

- Serve an HTML page using Flask
- Create a Flask API route that returns JSON
- Connect frontend JavaScript to backend Flask using fetch()
- Structure a full-stack project with clear separation between client and server


## Project Structure

```
.
├── client/
│   ├── index.html
│   ├── styles.css
│   └── script.js
├── server/
│   ├── app.py
│   ├── store.py
│   └── __init__.py
├── tests/
│   └── test_app.py
├── Pipfile / Pipfile.lock
└── README.md
```

---

## How to Start

1. Install dependencies:

**Using Pipenv:**
```bash
pipenv install
pipenv shell
```

**Using pip and venv:**
```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

2. Run the server (from the `server/` directory):
```bash
cd server
python app.py
```

3. Open your browser and go to:
```
http://localhost:5000/
```

You should see "Hello from the client!" along with a "Fetch Data" button. Clicking it calls the `/api/data` endpoint and displays the JSON response on the page.

---

## Running the Tests

All tests in `tests/test_app.py` pass:

```bash
pytest
```

Tests verify:
- `GET /` returns a `200` status and valid HTML
- `GET /api/data` returns a `200` status with JSON content
- The JSON response includes a `message` and a `status` of `"success"`
- Both `message` and `status` are strings

---

## Summary

This lesson connected a Flask backend to a static frontend:

1. Flask serves `index.html` as a static file from the `client` folder.
2. A dedicated API route (`/api/data`) returns JSON data sourced from `store.py`.
3. Client-side JavaScript uses `fetch()` to call that API route and dynamically updates the page without a reload.
4. Automated tests confirm both routes behave as expected.

