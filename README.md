# UPLB Soil Test Kit Companion

An Android-based digital companion for the UPLB Soil Test Kit (STK), developed to guide users through soil testing, assist in interpreting test results, and generate STK-based fertilizer and lime recommendations.

## Overview

The UPLB Soil Test Kit Companion is an Android application designed to digitize and simplify the workflow of the UPLB Soil Test Kit.

The application guides users through soil pH, nitrogen, phosphorus, potassium, and lime requirement testing. For color-based tests, it uses guided image capture and digital color analysis to assist with result interpretation.

The system also provides crop-specific fertilizer and lime recommendations based on UPLB Soil Test Kit reference tables, stores soil test records locally for offline access, and supports optional cloud synchronization when an internet connection is available.

A web-based administrative dashboard was also developed for authorized users to view, monitor, search, filter, and export synchronized soil test records.

## Key Features

### Soil Testing
- Guided soil testing workflow
- Individual and complete soil test workflows
- Soil pH interpretation
- Nitrogen interpretation
- Phosphorus interpretation
- Manual potassium turbidity confirmation
- Buffer pH interpretation for lime requirement testing
- Test-specific instructions and timers

### Camera & Color Interpretation
- Guided camera capture
- Image quality checking for brightness, darkness, and blur
- Placement confirmation
- Manual reference selection fallback
- Average RGB color extraction
- RGB to CIELAB conversion
- ΔE2000 color difference matching

### Recommendations
- Crop-specific fertilizer recommendations
- Lime requirement recommendations
- Fertilizer rate selection based on STK reference ranges
- Fertilizer material computations
- Household measurement conversions based on STK references

### Data Management
- Offline result storage using Hive
- Saved soil test history
- Optional Cloud Firestore synchronization
- User authentication
- Online backup and retrieval of synchronized records

### Administrative Dashboard
- Administrator authentication
- View registered user information
- View synchronized soil test records
- Search and filter records
- Export soil test records as CSV

## Tech Stack

### Mobile Application
- Flutter
- Dart
- Hive
- Firebase Authentication
- Cloud Firestore
- Camera and image processing packages

### Web Admin Dashboard
- React
- JavaScript
- Vite
- Tailwind CSS
- Firebase Authentication
- Cloud Firestore
- Firebase JavaScript SDK
- Vercel

## Color Interpretation

For color-based Soil Test Kit procedures, the application captures the test tube solution together with the corresponding physical STK reference chart or strip.

The system extracts average RGB values from the test solution and reference swatches and converts them from:

`RGB → CIELAB`

It then computes the CIEDE2000 (ΔE2000) color difference between the test solution and the captured reference swatches.

The reference swatch with the lowest ΔE2000 value is selected as the closest match and is used to determine the corresponding STK interpretation.

This process is used for:

- Soil pH
- Nitrogen
- Phosphorus
- Buffer pH

Potassium is handled separately through manual confirmation because the UPLB STK potassium test is based on the presence or absence of a cloudy layer rather than color matching.

## System Architecture

The system follows a hybrid offline-online architecture.

Core soil testing, color interpretation, recommendation generation, and saved-result viewing can operate locally using Hive.

When an internet connection is available, saved results may be synchronized to Cloud Firestore. The web administrative dashboard accesses these synchronized records through the same Firebase project.

`Mobile App → Hive Local Storage → Cloud Firestore → Admin Dashboard`

## Development

Sole Developer | Undergraduate Special Problem | 2026

This project was developed as my undergraduate Special Problem for the BS Computer Science program at the University of the Philippines Los Baños.

I designed and implemented the system, including:

- Android mobile application
- Mobile UI and soil testing workflow
- Guided camera capture
- Image quality validation
- Color extraction and interpretation pipeline
- CIELAB and ΔE2000 color comparison
- Fertilizer recommendation logic
- Lime requirement computation
- Offline data storage
- Firebase authentication and synchronization
- Web-based administrative dashboard
- CSV export
- Functional testing and usability evaluation

## Evaluation

The system was evaluated through:

- System Usability Scale (SUS)
- Expert/staff functional testing
- Controlled STK-based soil testing
- Recommendation and computation checking
- Administrative dashboard checking

The mobile application achieved an overall SUS score of approximately 87.75, indicating strong perceived usability during evaluation.

Controlled testing also showed that the evaluated application-generated interpretations were consistent with the expected UPLB STK-based interpretations used in the study.


## Project Scope

This application is a companion tool for the UPLB Soil Test Kit.

It does not replace the physical Soil Test Kit, modify its chemical testing procedures, or replace laboratory soil analysis. Users must still perform the required STK procedures using the appropriate soil samples, reagents, test tubes, and physical reference charts.

## Source Code

The source code for this project is private.

This repository serves as a public project showcase containing project information, screenshots, system architecture, and selected technical documentation.