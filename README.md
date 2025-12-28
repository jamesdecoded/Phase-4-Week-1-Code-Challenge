# Superheroes API (student-friendly)

This is a small Flask app for the Phase 4 Week 1 Code Challenge — it tracks heroes and their powers.

Quick setup

1. Make a virtual environment and activate it:

```bash
python3 -m venv venv
source venv/bin/activate
```

2. Install the packages:

```bash
pip install -r requirements.txt
```

3. Seed the database (this wipes and fills it with sample data):

```bash
python seed.py
```

4. Start the app:

```bash
python app.py
```

Open `http://127.0.0.1:5000` in your browser or use curl/Postman to try the endpoints.

Main endpoints (examples)

- `GET /heroes` — returns a list of heroes (id, name, super_name)
- `GET /heroes/1` — returns hero #1 and their `hero_powers` (with nested `power` info)
- `GET /powers` — returns a list of powers
- `GET /powers/1` — returns power #1
- `PATCH /powers/1` — update the description (must be at least 20 characters)
  - Example body: `{ "description": "A detailed description at least 20 chars long." }`
- `POST /hero_powers` — create a hero_power
  - Example body: `{ "strength": "Average", "power_id": 1, "hero_id": 3 }`

Notes and gotchas

- DB file: `superheroes.db` (SQLite) in the project root.
- Valid strengths: `Strong`, `Weak`, `Average`.
- When updating a power, `description` must be >= 20 chars.
- `seed.py` creates the sample data used in the challenge.

If you want, I can:
- Add migrations with Flask-Migrate,
- Add the Postman collection to the repo,
- Or run some quick sanity curl checks for you.

Have fun! If anything breaks when you run it, tell me what error you see and I’ll fix it.
