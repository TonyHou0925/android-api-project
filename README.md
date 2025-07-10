# Project 4: Cloud-Based Unemployment Rate Search Platform

This project was completed as part of **95-702 Distributed Systems (Spring 2025)** at Carnegie Mellon University. It demonstrates a fully integrated cloud-native system consisting of an Android mobile app, a Java servlet-based web API, a MongoDB backend, and a web-based analytics dashboard.

## Project Summary

This system enables users to search historical U.S. unemployment rates by month and year via a mobile app. The application makes real-time API requests to the U.S. Bureau of Labor Statistics (BLS), logs requests/responses, and displays analytics via a dashboard.

### Components

#### 1. Native Android Application (Client)

- Built with native Android SDK
- Includes user input fields (`EditText`), trigger button (`Button`), and output display (`TextView`)
- Sends HTTP requests to the backend servlet
- Parses JSON responses from the servlet and displays unemployment rate
- Repeatable and robust user experience

#### 2. Java Servlet Web Service (API Layer)

- Receives HTTP requests from Android app at path `/employment`
- Fetches JSON data from the BLS API
- Extracts and processes unemployment data
- Responds to Android app with a custom JSON payload
- Logs requests and responses with metadata

#### 3. MongoDB Integration (Logging & Analytics)

- Logs each user request into MongoDB with fields:
  - Timestamp
  - Month and year
  - Full request and response payloads
  - Parsed unemployment rate
  - Parsing success status
- Enables data aggregation for analytics

#### 4. Web Dashboard (Operational Analytics)

- Web interface hosted on GitHub Codespaces
- Publicly accessible dashboard displays:
  - Average unemployment rate
  - API response success rate
  - Timeline chart of queried unemployment rates
  - Full formatted logs

### Cloud Deployment

- Backend deployed using **GitHub Codespaces**
- Servlet container (Catalina) configured on port `8080`
- ROOT.war uploaded and deployed using Maven build flow
- Endpoint made **public** to support unauthenticated access by Android clients
- MongoDB Atlas used as a managed cloud database

## Technologies Used

- Android SDK
- Java Servlet API (Tomcat Catalina)
- MongoDB Atlas
- GitHub Codespaces
- BLS Public API
- JSON parsing
- REST API design

## Deliverables

- Native Android application (APK or source)
- Java web service (`ROOT.war`)
- MongoDB-backed logging system
- Live dashboard showing analytics and logs
- Screenshots of deployment and functionality

## Course Information

- Course: 95-702 Distributed Systems
- Semester: Spring 2025
- Instructor: Marty Barrett and Michael McCarthy
- Institution: Carnegie Mellon University
