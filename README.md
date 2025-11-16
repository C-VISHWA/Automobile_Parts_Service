# Automobile Parts Service (Streamlit)

A simple Streamlit app for managing automobile parts and services. This repository contains the Streamlit app (`app.py`) and the SQL schema (`project.sql`).

**Purpose:**
- Provide an interface for interacting with the parts/service database.

**Repository contents:**
- `app.py` — Streamlit application entry point.
- `project.sql` — SQL schema / seed data (run this first in your database).

**Prerequisites**
- Python 3.8 or newer
- A running database (PostgreSQL, MySQL, SQLite, etc.)
- `pip` for installing Python packages

Setup
1. Run the database schema

   Use your database client to run `project.sql` so the database tables and sample data are created. Example command:

   - MySQL:

     ```powershell
     mysql -u <user> -p <dbname> < project.sql
     ```

   Replace `<user>` and `<dbname>` with your database user and name.

2. Configure secrets

   Create a Streamlit secrets file at `.streamlit/secrets.toml` and fill in your database credentials.

3. Install Python dependencies

   ```powershell
   pip install -r requirements.txt
   ```

4. Run the Streamlit app

   ```powershell
   streamlit run app.py
   ```

Repository / Git

If you want to create a git repository locally and make the initial commit, run:

```powershell
git init
git add .
git commit -m "Initial commit: add app and setup files"
```

Security notes
- Never commit `.streamlit/secrets.toml` or any file containing plaintext credentials.
- The provided `.streamlit/secrets.toml.example` is for reference only.

Troubleshooting
- If the app cannot connect to the database, verify `project.sql` was applied and credentials in `.streamlit/secrets.toml` are correct.
- For DB-specific driver errors, install the appropriate driver (e.g., `psycopg2-binary` for PostgreSQL or `mysql-connector-python` for MySQL).

Contact / Next steps
- If you'd like, I can add a `Makefile`/scripts to automate these steps, or detect missing dependencies on startup. Tell me which DB you primarily target and I can further tailor instructions.
