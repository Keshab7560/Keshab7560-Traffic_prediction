# TrafficVision AI - Traffic Prediction System

## Project Overview
TrafficVision AI is a machine learning-powered web application that predicts traffic conditions based on vehicle counts and time parameters. The application uses a trained Random Forest model to classify traffic situations as low, normal, high, or heavy.

## Current State
✅ **FULLY FUNCTIONAL** - The application is running successfully on Replit with all features working.

## Recent Changes (September 19, 2025)
- Imported from GitHub repository
- Set up Python 3.11 environment with required dependencies
- Configured Flask development server to run on 0.0.0.0:5000 for Replit compatibility
- Created workflow for automatic application startup
- Configured deployment settings for production using Gunicorn
- Verified prediction API functionality and web interface

## Project Architecture

### Backend (Flask)
- **Framework**: Flask 3.0.3
- **Main App**: `app.py` - Contains prediction logic and API endpoints
- **ML Components**: 
  - `traffic_prediction_model.joblib` - Trained Random Forest classifier
  - `scaler.joblib` - Feature scaler for preprocessing
  - `label_encoders.joblib` - Label encoders for categorical variables
- **API Endpoints**:
  - `GET /` - Main web interface
  - `POST /predict` - Traffic prediction API

### Frontend 
- **Template**: `templates/index.html` - Modern, responsive single-page application
- **Styling**: Bootstrap 5.3.0 with custom CSS variables and animations
- **Features**:
  - Dark/light theme toggle
  - Interactive traffic light animation
  - Vehicle count input forms (cars, bikes, buses, trucks)
  - Time parameter controls (hour, minute, day of week)
  - Real-time prediction results with probability charts
  - Responsive design for mobile and desktop

### Dependencies
- Flask==3.0.3 (web framework)
- numpy==1.26.4 (numerical computations)
- scikit-learn==1.3.2 (machine learning models)
- joblib==1.3.2 (model serialization)
- gunicorn==22.0.0 (production WSGI server)

## Configuration

### Development
- **Workflow**: Flask App (`python app.py`)
- **Port**: 5000 (configured for Replit)
- **Host**: 0.0.0.0 (allows external access)

### Production Deployment
- **Target**: Autoscale (stateless web application)
- **Command**: `gunicorn --bind=0.0.0.0:5000 --reuse-port app:app`
- **Ready for deployment** with optimized production server

## Features
1. **Traffic Prediction**: Uses ML model to predict traffic conditions
2. **Real-time Processing**: Immediate predictions based on user input
3. **Visual Interface**: Modern UI with traffic light animations
4. **Multiple Themes**: Dark and light theme support
5. **Mobile Responsive**: Works on all device sizes
6. **Probability Visualization**: Shows prediction confidence levels

## User Preferences
- No specific user preferences documented yet
- Uses modern web technologies and responsive design principles
- Follows accessibility best practices with proper contrast and typography