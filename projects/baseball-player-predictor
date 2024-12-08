# Player Performance Prediction Project

Welcome to the Player Performance Prediction project! This repository contains a complete workflow for predicting baseball player statistics such as Wins Above Replacement (WAR), Hits, Home Runs (HR), and Stolen Bases (SB) using historical data.

The project includes:

- Data preprocessing and analysis
- Model training and evaluation
- A Flask web application for interactive predictions

## Table of Contents

- [Overview](#overview)
- [Project Files](#project-files)
- [Data Analysis](#data-analysis)
- [Modeling](#modeling)
- [Web Application](#web-application)
- [Installation](#installation)
- [Usage](#usage)
- [Future Work](#future-work)

---

## Overview

The objective of this project is to forecast future baseball player performance metrics using machine learning models. A Flask web app provides an intuitive interface to select players and view predictions into the future.

Key features:

- Analysis of historical player performance data
- Predictions using multiple linear regression models
- Interactive web-based interface

---

## Project Files

- **notebooks/**
  - `Mini_Project_2.ipynb`: The main notebook containing data exploration, modeling, and Flask app setup.
- **data/**
  - `Player_Offense_by_Season.xlsx`: The dataset used for training and testing.
- **models/**
  - `WAR_model.pkl`, `H_model.pkl`, `HR_model.pkl`, `SB_model.pkl`: Pre-trained models for forecasting.
- **app/**
  - `app.py`: Flask application code.
  - `templates/`: HTML templates for the Flask app.
- **README.md**: This documentation.

---

## Data Analysis

The dataset includes player statistics across seasons, such as:

- **WAR**: Wins Above Replacement
- **Hits**, **Home Runs (HR)**, **Stolen Bases (SB)**
- Additional performance metrics: Plate Appearances (PA), At Bats (AB), Games Played (G), Slugging Percentage (SLG), On-base Percentage (OBP)

### Insights

- Linear regression was used to model relationships between player statistics and future performance.
- Exploratory analysis revealed trends and correlations among variables.

---

## Modeling

Four machine learning models were trained to predict:

1. **WAR**
2. **Hits**
3. **Home Runs (HR)**
4. **Stolen Bases (SB)**

### Model Performance

- **WAR Model**: R²: 0.8774, MSE: 0.6255
- **Hits Model**: R²: 0.9768, MSE: 57.0402
- **HR Model**: R²: 0.9013, MSE: 18.2825
- **SB Model**: R²: 0.4450, MSE: 69.7393

---

## Web Application

A Flask web application provides:

1. **Player Selection**: Users can select a player from a dropdown.
2. **Future Forecasts**: Predictions for up to 5 future seasons.
3. **Interactive Interface**: Results displayed in a user-friendly table format.

### Routes

- `/`: Home page with player selection.
- `/predict`: Displays forecast results.

---

## Installation

### Prerequisites

Ensure the following are installed:

- Python 3.x
- Flask
- Pandas
- Scikit-learn

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/chadb12/player-performance-prediction.git
   cd player-performance-prediction
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the Flask application:
   ```bash
   python app.py
   ```
4. Open the app in your browser:
   ```
   http://127.0.0.1:5000
   ```

---

## Usage

1. Launch the Flask app.
2. Select a player from the dropdown menu.
3. View forecasts for WAR, Hits, HR, and SB for the next few seasons.

---

## Future Work

- Incorporate additional metrics for richer predictions.
- Add clustering techniques to group players by performance.
- Enhance the web interface for better user experience.
- Transition to a production-grade deployment using services like AWS Elastic Beanstalk.

---

## Acknowledgments

- Data sourced from StatHead.com



