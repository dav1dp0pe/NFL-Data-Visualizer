Dockerfile: Container instructions (installs Nodes, copies code, runs npm run dev)

pyproject.toml: List of backend dependencies

.env: Backend secrets (DB URL, CORS settings)

/app/:
    main.py: FastAPI entrypoint (creates app, sets up routes, middleware)
    db.py: Database connection logic (SQLAlchemy + Postgres)
    models.py: Database schemas (SQLAlchemy ORM models)
    routers/: Organize API Routes:
        players.py -> /players endpoints
        stats.py -> /stats endpoints
    etl/: Data loading/cleaning scripts:
        ingest.py -> pulls Bengals data via nfl_data_py, writes to Postgres
    utils/: Helper functions (validation, caching, formatting)