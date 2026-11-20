# Second Brain

A local career assistant for maintaining profile evidence, tracking jobs, and drafting
grounded CVs. It stores data locally and uses Ollama for text generation.

## Windows setup

```powershell
cd "D:\DEPI\second brain"
py -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python second_brain.py
```

Ollama must be running and accessible at `http://127.0.0.1:11434`. The app defaults
to `llama3.2:3b`, which is already installed.

To use another installed model:

```powershell
$env:BRAIN_MODEL = "llama3.2:3b"
python second_brain.py
```

Profile data is stored at `%USERPROFILE%\.career-brain\career.sqlite3`.

## Commands

- `file`: import TXT, Markdown, PDF, or DOCX content.
- `note`: add a personal update or career preference.
- `github`: import public repositories for a GitHub username.
- `profile`: review extracted evidence and exclude false or shared-work entries.
- `job`: add a job URL and description manually.
- `greenhouse`: import openings from a Greenhouse company board.
- `match`: evaluate unreviewed jobs, with a 75% minimum score.
- `tracker`: list saved applications.
- `applied`: record that an approved application was submitted manually.
- `quit`: exit.
