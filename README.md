# FastAPI + Jinja2 Full Stack Starter

A lightweight, full-stack web application template using **FastAPI** for the backend and **Jinja2** for server-side rendering. This project uses **uv** for blazing-fast dependency management.

## 🚀 Tech Stack

- **Python 3.12+**
- **FastAPI** (Web Framework)
- **Jinja2** (Templating Engine)
- **Uvicorn** (ASGI Server)
- **uv** (Package Manager)

## 📂 Project Structure

```text
.
├── main.py               # Application entry point & routes
├── pyproject.toml        # Dependency configuration (managed by uv)
├── uv.lock               # Lock file for reproducible builds
├── static/               # CSS, JavaScript, Images
│   └── styles.css
└── templates/            # HTML files
    ├── base.html         # Layout template
    └── index.html        # Page template
```

## 📦 Installation & Setup

Follow the steps below to get the project up and running.

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/fastapi-jinja2-starter.git
cd fastapi-jinja2-starter
```

### 2. Install `uv`

`uv` is a super-fast Python package manager and workflow tool.

#### 🐧 macOS / Linux

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

#### 🪟 Windows (PowerShell)

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

#### Alternative: Install via pip

```bash
pip install uv
```

### 3. Install Dependencies

Since dependencies are managed by `uv`, simply run:

```bash
uv sync
```

This installs all required packages based on `pyproject.toml` and `uv.lock`.

### 4. Run the Application

Use `uvicorn` (installed automatically via `uv`) to start the server.

```bash
uv run uvicorn main:app --reload
```

The app will now be available at:

```
http://127.0.0.1:8000
```

## 🔧 Development Notes

- Modify HTML templates inside the `templates/` directory.
- Add static files (CSS/JS/images) under `static/`.
- Expand routes and logic in `main.py`.
- Use `uv add <package>` to install new dependencies.

## 🛠 Build & Deployment

For production deployments, run Uvicorn without `--reload`:

```bash
uv run uvicorn main:app --host 0.0.0.0 --port 8000
```

You may also use production-grade ASGI servers like **Gunicorn** with **Uvicorn workers**.

## 📄 License

This project is open-source and available under the MIT License.

---

Happy coding! 🚀
