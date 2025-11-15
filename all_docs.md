# Repository Catalog - All Documentation

**Purpose**: This file serves as the main entry point for the AI agent. It contains a concise list of all repositories with short descriptions to help the agent determine which repos to explore in detail.

**Last Updated**: 2025-11-15

---

## 📋 Quick Reference

| Repository | Domain | Description | Documentation File |
|-----------|--------|-------------|-------------------|
| `wmd06/CarAccidentPredictor` | Machine Learning | Predicts car accident likelihood using ML models | `docs/CarAccidentPredictor.md` |
| `mahdi-al-hakim/cme_workshop` | Web Application | Workshop application with Python backend | `docs/cme_workshop.md` |
| `mahdi-al-hakim/edgar_play` | Data Science | SEC Edgar data analysis and processing | `docs/edgar_play.md` |
| `mahdi-al-hakim/ProductService` | Backend Service | Product management service | `docs/ProductService.md` |
| `mahdi-al-hakim/SpotFix-BE` | Backend Service | SpotFix backend service | `docs/SpotFix-BE.md` |
| `mahdi-al-hakim/SpotFixBE` | Backend Service | SpotFix backend service (alternate) | `docs/SpotFixBE.md` |
| `mahdi-al-hakim/SpotFixFE` | Frontend | SpotFix frontend application | `docs/SpotFixFE.md` |
| `mahdi-al-hakim/docs_hub` | Documentation | Central documentation repository | `docs/docs_hub.md` |

---

## 🔍 Detailed Repository Descriptions

### Machine Learning / Data Science

#### `wmd06/CarAccidentPredictor`
- **Owner**: wmd06 (Contributor: mahdi-al-hakim)
- **Language**: Python
- **Status**: Development
- **Key Features**:
  - Machine learning models for accident prediction
  - Data preprocessing and feature engineering
  - Model training and evaluation
  - Prediction API/interface
- **Tech Stack**: Python, scikit-learn, pandas, numpy
- **Documentation**: `docs/CarAccidentPredictor.md`

#### `mahdi-al-hakim/edgar_play`
- **Owner**: mahdi-al-hakim
- **Languages**: Python, TeX
- **Status**: Development
- **Key Features**:
  - SEC Edgar data retrieval and analysis
  - Financial document processing
  - Data extraction and transformation
- **Tech Stack**: Python, TeX
- **Documentation**: `docs/edgar_play.md`

### Web Applications

#### `mahdi-al-hakim/cme_workshop`
- **Owner**: mahdi-al-hakim
- **Languages**: Python, HTML, JavaScript, CSS
- **Status**: Development
- **Key Features**:
  - Workshop/training application
  - Interactive web interface
  - Python backend processing
- **Tech Stack**: Python, HTML, JavaScript, CSS
- **Documentation**: `docs/cme_workshop.md`

#### `mahdi-al-hakim/SpotFixFE`
- **Owner**: mahdi-al-hakim
- **Languages**: TypeScript, CSS, JavaScript, HTML
- **Status**: Development
- **Key Features**:
  - Frontend for SpotFix application
  - Modern TypeScript-based UI
  - Responsive web interface
- **Tech Stack**: TypeScript, CSS, JavaScript, HTML
- **Documentation**: `docs/SpotFixFE.md`

### Backend Services

#### `mahdi-al-hakim/ProductService`
- **Owner**: mahdi-al-hakim
- **Languages**: Not specified
- **Status**: Development
- **Key Features**:
  - Product management and catalog
  - Service-oriented architecture
- **Tech Stack**: To be documented
- **Documentation**: `docs/ProductService.md`

#### `mahdi-al-hakim/SpotFix-BE`
- **Owner**: mahdi-al-hakim
- **Languages**: TypeScript, JavaScript
- **Status**: Development
- **Key Features**:
  - Backend API for SpotFix application
  - RESTful services
  - Data persistence
- **Tech Stack**: TypeScript, JavaScript
- **Documentation**: `docs/SpotFix-BE.md`

#### `mahdi-al-hakim/SpotFixBE`
- **Owner**: mahdi-al-hakim
- **Languages**: TypeScript, JavaScript
- **Status**: Development
- **Key Features**:
  - Backend API for SpotFix application (alternate implementation)
  - Service layer architecture
- **Tech Stack**: TypeScript, JavaScript
- **Documentation**: `docs/SpotFixBE.md`

### Documentation & Infrastructure

#### `mahdi-al-hakim/docs_hub`
- **Owner**: mahdi-al-hakim
- **Languages**: Markdown
- **Status**: Active
- **Key Features**:
  - Central documentation repository
  - Catalog for all repositories
  - AI agent integration point
- **Tech Stack**: Markdown, Git
- **Documentation**: `docs/docs_hub.md`

---

## 🏗️ Architecture Overview

```
Current Projects:
┌────────────────────────────────────────────────┐
│              Machine Learning                   │
│  - CarAccidentPredictor                        │
│  - edgar_play                                  │
└────────────────────────────────────────────────┘
┌────────────────────────────────────────────────┐
│            Web Applications                     │
│  - cme_workshop                                │
│  - SpotFixFE                                   │
└────────────────────────────────────────────────┘
┌────────────────────────────────────────────────┐
│           Backend Services                      │
│  - ProductService                              │
│  - SpotFix-BE                                  │
│  - SpotFixBE                                   │
└────────────────────────────────────────────────┘
┌────────────────────────────────────────────────┐
│     Documentation & Infrastructure             │
│  - docs_hub                                    │
└────────────────────────────────────────────────┘
```

---

## 📊 Repository Metadata Summary

### By Language
- **Python**: 3 repos (CarAccidentPredictor, edgar_play, cme_workshop)
- **TypeScript/JavaScript**: 4 repos (SpotFixFE, SpotFix-BE, SpotFixBE, cme_workshop)
- **HTML/CSS**: 2 repos (cme_workshop, SpotFixFE)
- **TeX**: 1 repo (edgar_play)
- **Markdown**: 1 repo (docs_hub)

### By Status
- **Development**: 7 repos
- **Active**: 1 repo (docs_hub)
- **Production**: 0 repos

### By Domain
- **Machine Learning/Data Science**: 2 repos
- **Web Applications**: 2 repos
- **Backend Services**: 3 repos
- **Documentation**: 1 repo

---

## 🎯 How to Use This Catalog

### For AI Agents:
1. **Start here**: Read this file to get an overview of all repositories
2. **Identify relevant repos**: Based on the user's requirement, determine which repositories are involved
3. **Read detailed docs**: Use `catalog_get_repo` to read the full documentation for each relevant repo (e.g., `docs/CarAccidentPredictor.md`)
4. **Check code if needed**: If catalog information is insufficient, use `repo_open` to peek at actual code files
5. **Create tickets**: Generate Jira tickets based on the analysis

### For Humans:
- This file provides a quick reference to find the right repository for a feature or bug fix
- Each repo's detailed documentation contains architecture, dependencies, testing strategies, and more

---

## 🔐 Security & Access

- All repositories require GitHub authentication
- CarAccidentPredictor: Contributor access (read/write)
- New repositories will be added as they are created/contributed to

---

## 📝 Maintenance

- **Last Updated**: 2025-11-15
- **Update Frequency**: Weekly or when new repos are added
- **Owner**: Mahdi Al-Hakim
- **Contact**: mahdi.a.alhakim@gmail.com

---

## ⚡ Quick Links

### Machine Learning / Data Science
- [CarAccidentPredictor Repository](https://github.com/wmd06/CarAccidentPredictor)
- [edgar_play Repository](https://github.com/mahdi-al-hakim/edgar_play)

### Web Applications
- [cme_workshop Repository](https://github.com/mahdi-al-hakim/cme_workshop)
- [SpotFixFE Repository](https://github.com/mahdi-al-hakim/SpotFixFE)

### Backend Services
- [ProductService Repository](https://github.com/mahdi-al-hakim/ProductService)
- [SpotFix-BE Repository](https://github.com/mahdi-al-hakim/SpotFix-BE)
- [SpotFixBE Repository](https://github.com/mahdi-al-hakim/SpotFixBE)

### Documentation
- [docs_hub Repository](https://github.com/mahdi-al-hakim/docs_hub)
- [Add New Repository Documentation](./docs/)

---

## 📌 Notes for Project Managers

When creating tickets:
- Reference this catalog to determine which repos are affected
- Include repo names in Jira labels
- Consult detailed documentation for acceptance criteria
- For new features requiring new repositories, document them here first

---

## 🆕 Adding New Repositories

When you create or gain access to new repositories:

1. **Add entry to Quick Reference table** (above)
2. **Add detailed description** in appropriate domain section
3. **Create documentation file** in `docs/` directory using template
4. **Update metadata summary** (language, status, domain counts)
5. **Commit and push changes**

Template available at: `../Jira_MCP/templates/repo_docs_template.md`

---

**End of Catalog Overview**
