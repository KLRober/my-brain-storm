# Astraly – Core Architecture

## Architecture

Astraly uses a **Bridge architecture** implemented with FastAPI that acts as a middleware between the Frontend (React + Tailwind) and the Backend (Python). The Bridge coordinates file operations, processing requests and data flow between UI and system-level services.

```
┌─────────────────┐     ┌─────────────────┐     ┌─────────────────┐
│    Frontend     │────▶│     Bridge      │────▶│    Backend      │
│ React + Tailwind│◀────│    (FastAPI)    │◀────│    (Python)     │
└─────────────────┘     └─────────────────┘     └─────────────────┘
```

## Data Management

Astraly follows a **local-first approach** for file handling. It uses Python libraries such as `shutil`, `os` and `pathlib` to perform real-time filesystem operations including:

- Moving files
- Organizing directories
- Renaming files
- Transforming file formats

All operations are performed directly on the user's machine without cloud dependencies.
