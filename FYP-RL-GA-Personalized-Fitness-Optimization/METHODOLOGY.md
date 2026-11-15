# FITGENIX — Methodology Overview

This document summarizes the stages described in the public project notebook. It does not replace the private implementation.

## 1. Activity-data preparation

The notebook references daily activity, hourly calories, and hourly steps CSV files. Its workflow includes loading the records, converting activity timestamps, and ordering records chronologically.

## 2. Feature engineering

The project notebook describes derived activity features:

- **ActiveMinutes / TotalActiveMinutes:** user's activity duration.
- **StepCalorieRatio:** relationship between step count and calorie values.
- **IntensityScore:** derived activity-intensity representation.

## 3. Normalization

Selected numerical activity variables are scaled to a 0–1 range. The notebook describes normalization as a way to keep features on comparable scales for modelling.

## 4. Predictive baseline

Linear Regression and Ridge Regression are referenced as baseline methods for predicting a normalized calorie target from normalized activity-related inputs.

## 5. Genetic Algorithm

The notebook outlines a Genetic Algorithm for optimizing a linear model's parameters. The described stages include fitness evaluation, parent selection, crossover, and mutation. The full operators and optimization loop are not included in this public version.

## 6. Reinforcement Learning

The notebook describes a fitness-related environment and a Q-learning agent. Its conceptual elements include states, actions, rewards, state transitions, and a learned policy. The environment implementation and training updates are intentionally withheld.

## Reproducibility note

This is a methodology summary only. The public notebook contains placeholders in implementation-critical cells, so it cannot reproduce the complete experiments. Add only verified metrics and figures, with experiment settings and data-source attribution, if they are approved for public release.
