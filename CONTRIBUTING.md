# Contributing to Fenrir Saga Ragnarok Online Wiki

Thanks for helping improve the wiki! Keep it simple, accurate, and respectful.

## 1. Local Development Setup

To preview changes locally before submitting a PR:

### Prerequisites

1. **Install Python** (3.8 or higher)
   - **Windows**: Download from [python.org](https://www.python.org/downloads/)
     - During installation, check "Add Python to PATH"
   - **macOS/Linux**: Python is usually pre-installed, or use your package manager
   - Verify installation: `py --version` (Windows) or `python3 --version` (macOS/Linux)

2. **Install Git**
   - Download from [git-scm.com](https://git-scm.com/downloads)

### Setup Steps

1. **Fork and clone the repository**
   ```bash
   git clone https://github.com/<your-username>/fenrirsaga-wiki-public
   cd fenrirsaga-wiki-public
   ```

2. **Create a virtual environment**
   ```bash
   # Windows
   py -m venv venv
   
   # macOS/Linux
   python3 -m venv venv
   ```

3. **Activate the virtual environment**
   ```bash
   # Windows PowerShell
   .\venv\Scripts\Activate.ps1
   
   # Windows Command Prompt
   .\venv\Scripts\activate.bat
   
   # macOS/Linux
   source venv/bin/activate
   ```
   
   *Note: If you get a PowerShell execution policy error on Windows, run:*
   ```powershell
   Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
   ```

4. **Install dependencies**
   ```bash
   pip install mkdocs mkdocs-material
   ```

5. **Run the local server**
   ```bash
   mkdocs serve
   ```
   
   The wiki will be available at `http://127.0.0.1:8000/`

6. **Make your changes** and preview them in real-time in your browser

7. **Stop the server** when done by pressing `Ctrl+C`

## 2. Basic Flow

1. Fork the repo.
2. Clone your fork and set up local environment (see above).
3. Create a branch: `content/<topic>` or `fix/<short-description>`.
4. Make changes and test locally with `mkdocs serve`.
5. Commit and push.
6. Open a Pull Request (PR) to `main`.
7. I review and merge.

## 3. What to Add

Good:
- New or updated pages (classes, monsters, items, quests, maps).
- Fixes (typos, broken links, outdated info).
- Small structural/navigation improvements.
- Optimized images (PNG/WebP) with meaningful `alt` text.

Not good (without asking first):
- Huge redesigns.
- Bulk unverified data.
- Copyrighted material you don't own.

## 4. File & Folder Basics

Please follow the current organization methods.

## 5. Commit Style (Keep Short)

Format:
```
type(scope): short description
```
Types: `content`, `fix`, `feat`, `chore`, `docs`

Examples:
```
content(monsters): add doppelganger guide
fix(items): correct hydra card drop rate
```

## 6. Pull Request

Include:
- Short summary.
- Screenshot if layout changed.

Only the owner merges.

## 7. Review

I may request small changes. Inactive PRs (no response in ~2 weeks) can be closed.

## 8. Quick Example

```bash
git clone https://github.com/<you>/fenrirsaga-wiki-public
cd fenrirsaga-wiki-public

# Set up environment
py -m venv venv                    # Windows
.\venv\Scripts\Activate.ps1        # Windows PowerShell
pip install mkdocs mkdocs-material

# Start development server
mkdocs serve

# In another terminal, make your changes
git checkout -b content/doppelganger
# Edit or add files
git add docs/
git commit -m "content(monsters): add doppelganger guide"
git push origin content/doppelganger
# Open PR
```

Thanks for contributing!