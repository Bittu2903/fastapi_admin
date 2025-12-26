# fastapi-project

A simple FastAPI project scaffolder. After installation, run `fastapi-admin start <project_name>` to generate a ready-to-run FastAPI app with:

- `main.py` including CORS and router inclusion
- Versioned API with `/health` endpoint
- `modules/example` with basic router, schema, service, and model stub
- Postgres configuration with sync and async SQLAlchemy sessions loaded from `.env`

## Install

```
pip install fastapi-project
```

On macOS with externally managed Python:

```
python3 -m pip install fastapi-project --user --break-system-packages
export PATH="$(python3 -m site --user-base)/bin:$PATH"
```

## Usage

```
fastapi-admin start my_project
cd my_project
uvicorn main:app --reload
```

Create `.env` in the project root:

```
DATABASE_URL_SYNC=postgresql://user:password@localhost:5432/db
DATABASE_URL_ASYNC=postgresql+asyncpg://user:password@localhost:5432/db
```

## Development

```
pip install -r requirements.txt
python3 -m pip install -e .
fastapi_admin start dev_project
```