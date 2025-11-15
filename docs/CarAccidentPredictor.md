---
repo: CarAccidentPredictor
owner: wmd06
org: wmd06
language: python
tier: normal
domains:
  - machine-learning
  - data-science
  - prediction

entrypoints:
  - "app.py"
  - "notebook.ipynb"

key_files:
  - "README.md"
  - "notebook.ipynb"
  - "app.py"
  - "requirements.txt"
  - "random_forest_model.pkl"

interfaces:
  http:
    - path: "/"
      method: "GET"
      auth: "none"
      description: "Web interface for car accident prediction"
    - path: "/predict"
      method: "POST"
      auth: "none"
      description: "API endpoint for making predictions"

dependencies:
  internal: []
  external:
    - scikit-learn
    - pandas
    - numpy
    - Flask (if web app)
    - jupyter

risks:
  - "Model accuracy depends on training data quality"
  - "Pickle file security - ensure model file is not tampered with"
  - "Input validation required for prediction endpoint"
  - "Model may need retraining with new data periodically"

non_goals:
  - "This is NOT a real-time accident prevention system"
  - "Does NOT collect or store user data"
  - "Does NOT provide legal or insurance advice"

jira_labels:
  - "ml"
  - "data-science"
  - "python"
  - "prediction"

acceptance_hints:
  - "Model predictions should be tested with diverse input data"
  - "Web interface should handle invalid inputs gracefully"
  - "Changes to model should include accuracy metrics comparison"
  - "New features should not degrade model performance"
  - "Unit tests required for data preprocessing functions"

updated_from:
  repo_ref: "https://github.com/wmd06/CarAccidentPredictor"
  commit: "latest"
  refreshed_at: "2025-11-15T19:30:00Z"
---

# Car Accident Predictor

## Summary

The Car Accident Predictor is a machine learning project that predicts the likelihood of car accidents based on various input features. The project includes a trained Random Forest model, a Jupyter notebook for exploration/training, and a web application (app.py) for making predictions.

**Key Capabilities**:
- Predicts car accident risk using machine learning
- Web interface for easy predictions
- Jupyter notebook for model development and analysis
- Pre-trained Random Forest model (random_forest_model.pkl)

## Architecture

### System Design

```
┌─────────────┐         ┌──────────────────┐         ┌─────────────────┐
│   User      │────────▶│  Web App (Flask) │────────▶│  ML Model       │
│  (Browser)  │◀────────│  app.py          │◀────────│  (Random Forest)│
└─────────────┘         └──────────────────┘         └─────────────────┘
                                                               │
                                                      ┌────────▼────────┐
                                                      │  Trained Model  │
                                                      │  (.pkl file)    │
                                                      └─────────────────┘
```

### Tech Stack
- **Language**: Python
- **Framework**: Flask (likely)
- **ML Library**: scikit-learn
- **Data Processing**: pandas, numpy
- **Model**: Random Forest Classifier
- **Development**: Jupyter Notebook

### Project Structure

```
CarAccidentPredictor/
├── README.md                    # Project documentation
├── app.py                       # Web application
├── notebook.ipynb               # Jupyter notebook for model development
├── random_forest_model.pkl      # Pre-trained model
├── requirements.txt             # Python dependencies
└── templates/                   # HTML templates for web interface
    └── (HTML files)
```

## APIs

### Web Application Endpoints

#### GET /
**Description**: Home page with prediction form.

**Response**: HTML page with input form for accident prediction.

#### POST /predict
**Description**: Make accident prediction based on input features.

**Request** (form data or JSON):
```json
{
  "feature1": "value1",
  "feature2": "value2",
  "feature3": "value3"
  // ... (features depend on model training)
}
```

**Response**:
```json
{
  "prediction": "high_risk | low_risk",
  "probability": 0.75,
  "confidence": "75%"
}
```

## Functionalities

### Core Features

1. **Accident Risk Prediction**
   - Input: Various features (road conditions, weather, driver info, etc.)
   - Output: Risk level (high/low) with probability
   - Model: Random Forest Classifier
   - Format: Web form or API

2. **Model Training** (notebook.ipynb)
   - Data loading and exploration
   - Feature engineering
   - Model training with scikit-learn
   - Model evaluation and metrics
   - Model export to pickle file

3. **Web Interface** (app.py)
   - User-friendly form for inputs
   - Real-time predictions
   - Results visualization
   - Responsive design

## Data & Model

### Input Features (Typical)
- Weather conditions (clear, rain, snow, fog)
- Road type (highway, urban, rural)
- Time of day
- Traffic density
- Driver experience
- Vehicle type
- Speed limit
- Other contextual features

### Model Details
- **Algorithm**: Random Forest
- **Saved as**: random_forest_model.pkl
- **Training**: See notebook.ipynb for details
- **Performance**: (Add metrics after reviewing notebook)

## Operational Constraints

### Model Considerations
- **Retraining**: Model may need periodic retraining with new data
- **Input validation**: All inputs must be validated before prediction
- **Error handling**: Handle missing or invalid features gracefully

### Security
- **Model file**: Verify integrity of pickle file (prevent tampering)
- **Input sanitization**: Prevent injection attacks via form inputs
- **Data privacy**: Do not log sensitive user information

### Performance
- **Prediction latency**: < 100ms per prediction (in-memory model)
- **Concurrent users**: Depends on server capacity
- **Model size**: ~few MB (Random Forest pickle file)

## Testing Strategy

### Unit Tests
- **Coverage Target**: > 80%
- **Framework**: pytest
- **Focus**:
  - Feature preprocessing
  - Input validation
  - Model loading
  - Prediction pipeline

### Integration Tests
- **Framework**: pytest + Flask testing
- **Focus**:
  - End-to-end prediction flow
  - Web form submission
  - API endpoints
  - Error handling

### Model Tests
- **Framework**: pytest + sklearn
- **Focus**:
  - Model accuracy on test set
  - Prediction consistency
  - Feature importance validation

### Manual Tests
- Test with various input combinations
- Verify predictions make sense
- Check UI/UX

## Development Setup

### Prerequisites
```bash
# Python 3.7+
python --version

# Install dependencies
pip install -r requirements.txt
```

### Running the Application
```bash
# Run web app
python app.py

# Open browser
# Navigate to http://localhost:5000
```

### Running Jupyter Notebook
```bash
# Start Jupyter
jupyter notebook

# Open notebook.ipynb
```

## Ticketing Guidance

### Good Subticket Patterns

When breaking down work for this project:

1. **Add New Feature to Model** (e.g., "Add weather severity feature"):
   - Subtask 1: Update dataset with new feature
   - Subtask 2: Retrain model with new feature
   - Subtask 3: Update web form to accept new input
   - Subtask 4: Update prediction pipeline
   - Subtask 5: Test and compare accuracy

2. **Improve Model Accuracy** (e.g., "Improve prediction accuracy"):
   - Subtask 1: Analyze current model performance
   - Subtask 2: Try different algorithms (XGBoost, etc.)
   - Subtask 3: Tune hyperparameters
   - Subtask 4: Evaluate and select best model
   - Subtask 5: Deploy new model

3. **Add New UI Feature** (e.g., "Add visualization of results"):
   - Subtask 1: Design visualization mockup
   - Subtask 2: Implement frontend chart library
   - Subtask 3: Update backend to return visualization data
   - Subtask 4: Style and responsive design
   - Subtask 5: Test across browsers

### Pitfalls to Avoid

1. **Don't modify model without versioning**
   - Always save old models before creating new ones
   - Track model versions and performance metrics

2. **Don't skip data validation**
   - Validate all inputs before feeding to model
   - Handle missing values gracefully

3. **Don't ignore model bias**
   - Check for bias in predictions
   - Ensure training data is representative

4. **Don't hardcode model path**
   - Use configuration for model file path
   - Make it easy to swap models

### Typical Story Sizes

- **Small (1-2 days)**: UI tweaks, add simple feature to form, bug fixes
- **Medium (3-5 days)**: Add new model feature, improve UI significantly, refactor code
- **Large (1-2 weeks)**: Retrain model with new data, migrate to new algorithm, add API

### Acceptance Criteria Checklist

For any ticket on this project, ensure acceptance criteria includes:

- [ ] Code changes don't break existing predictions
- [ ] Unit tests added/updated (>80% coverage)
- [ ] Model accuracy not degraded (if model changes)
- [ ] Web interface tested manually
- [ ] README updated if new features added
- [ ] Requirements.txt updated if new dependencies
- [ ] Model versioning maintained
- [ ] Input validation implemented
- [ ] Error handling added
- [ ] Performance not degraded

---

## Contact & Ownership

- **Repository**: https://github.com/wmd06/CarAccidentPredictor
- **Owner**: wmd06
- **Contributor**: mahdi-al-hakim
- **Language**: Python (Jupyter Notebook)
- **Created**: 2024-12-10
- **Last Updated**: 2024-12-20

---

## Future Enhancements

Potential improvements for Jira tickets:

1. **API Development**:
   - Create RESTful API for predictions
   - Add API documentation (Swagger/OpenAPI)
   - Implement API authentication

2. **Model Improvements**:
   - Try ensemble methods (XGBoost, LightGBM)
   - Add explainability (SHAP values)
   - Implement online learning

3. **Data Pipeline**:
   - Automate data collection
   - Build data preprocessing pipeline
   - Add data versioning (DVC)

4. **Deployment**:
   - Containerize with Docker
   - Deploy to cloud (Heroku, AWS, Azure)
   - Add CI/CD pipeline

5. **Monitoring**:
   - Add prediction logging
   - Monitor model drift
   - Track API usage

---

**Last Updated**: 2025-11-15

**Note**: This documentation should be updated as the project evolves. When making significant changes to the model or architecture, update this file accordingly.
