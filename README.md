# Docs-Hub Repository Setup

This directory contains the complete structure for your `docs_hub` repository.

## Quick Setup Instructions

### Option 1: Create Repository on GitHub (Recommended)

1. **Create the repository on GitHub**:
   ```bash
   # Go to https://github.com/new
   # Repository name: docs_hub
   # Description: Central documentation catalog for all repositories
   # Visibility: Public or Private (your choice)
   # Click "Create repository"
   ```

2. **Clone and populate**:
   ```bash
   # Clone your new repository
   git clone https://github.com/mahdi-al-hakim/docs_hub.git
   cd docs_hub

   # Copy files from this setup directory
   cp -r ../Jira_MCP/docs_hub_setup/* .

   # Commit and push
   git add .
   git commit -m "Initial docs-hub setup with catalog and examples"
   git push origin main
   ```

### Option 2: Use GitHub CLI

```bash
cd /c/Users/user
gh repo create mahdi-al-hakim/docs_hub --public --description "Documentation catalog for all repositories"
git clone https://github.com/mahdi-al-hakim/docs_hub.git
cd docs_hub
cp -r ../Jira_MCP/docs_hub_setup/* .
git add .
git commit -m "Initial setup"
git push origin main
```

## Repository Structure

```
docs_hub/
├── README.md                  # This file
├── all_docs.md                # Main catalog (REQUIRED)
├── docs/                      # Individual repository documentation
│   └── CarAccidentPredictor.md
└── .gitignore
```

## What to Do Next

1. **Create the repository** using one of the options above
2. **Edit all_docs.md** to list YOUR actual repositories
3. **Create a doc file for each repo** in the `docs/` directory
4. **Commit and push** to GitHub
5. **Run tests** from Jira_MCP: `python tests\test_connections.py`

## Template Files Included

- `all_docs.md` - Main catalog with example entry for CarAccidentPredictor
- `docs/CarAccidentPredictor.md` - Example documentation (customize this!)

## Need Help?

See the main project documentation:
- `Jira_MCP/DOCS_HUB_SETUP.md` - Detailed setup guide
- `Jira_MCP/templates/` - Additional templates
