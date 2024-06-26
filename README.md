# Mobile IoT-Based Pothole Detection System

Welcome to the Mobile IoT-Based Pothole Detection System GitHub repository! This project aims to detect potholes on roads using a mobile device equipped with a camera and an AI algorithm. The detected pothole locations are then stored in a cloud database and displayed on a web application for public and government use.

## Table of Contents

1. [Introduction](#introduction)
2. [System Design](#system-design)
3. [Project Scope](#project-scope)
4. [Hardware Components](#hardware-components)
5. [AI Algorithm and Data Handling Scripts](#ai-algorithm-and-data-handling-scripts)
6. [GPS Module/Cloud Storage/Web App](#gps-module-cloud-storage-web-app)
7. [3D Printed Casing and Camera](#3d-printed-casing-and-camera)
8. [Limitations](#limitations)
9. [Conclusion](#conclusion)

## Introduction

Potholes pose significant hazards to public roads, causing vehicle damage and safety risks. This project addresses the issue by deploying a pothole detection system on mobile vehicles, capturing live video feeds, and processing the data with an AI algorithm to identify and record pothole locations. The collected data is shared on a public website and application for public and city use.

## System Design

The core of the system is the Raspberry Pi 4, which houses the camera, cellular connectivity module, and AI algorithm. The system architecture is visualized below:

![System Architecture](#)

## Project Scope

The project aims to assemble a prototype of a Mobile IoT-Based Pothole Detection System to provide pothole location information around New York City to government agencies and road users. The prototype uses a Raspberry Pi 4 Model B, Raspberry Pi Camera, GPS module with 4G technology, and a car charger for power supply.

## Hardware Components

- **Raspberry Pi 4 Model B**: Acts as the central processor, running the AI algorithm and connecting various modules.
- **GPS Module (SIM7600A-H)**: Provides precise pothole location using satellite positioning and LTE CAT4 for data transfer.
- **Raspberry Pi Camera**: Captures road images for the AI algorithm.
- **Power Supply**: Car charger with a USB port for powering the device.

## AI Algorithm and Data Handling Scripts

The project utilizes a Convolutional Neural Network (CNN), specifically MobileNetV2, to detect potholes in road images. The trained model processes images every 2 seconds and flags potholes, recording their coordinates using the GPS module. Detected pothole data is transmitted to a cloud database.

## GPS Module/Cloud Storage/Web App

The system uses a 4G/GNSS HAT for cellular connectivity and GNSS for location data. Data is sent to ThingSpeak using MQTT and retrieved via REST API. The web application, built with Python Flask and Folium, displays pothole locations to users.

## 3D Printed Casing and Camera

The project includes a custom-designed 3D-printed case to house the Raspberry Pi and modules, providing protection and ensuring proper camera placement.

## Limitations

- **Hardware**: The Raspberry Pi has limited RAM, which may affect processing speed. Fixed-focus lenses require careful case design.
- **AI/ML Algorithm**: The model has an accuracy of 82.13%, with a practical accuracy of 95.95% considering project objectives. False positives remain a challenge.
- **Communication and Web App**: GNSS performance can be affected by weather and time of day. The web app is locally hosted, limiting accessibility.

## Conclusion

The project successfully developed a functioning module for detecting potholes and transmitting data for visualization. Future steps involve scaling up the deployment in collaboration with the New York City government to create a comprehensive pothole database.

## System Architecture Drawing

![System Architecture Drawing](attachment-url-here)

---

Thank you for visiting our project repository. For more details, please refer to the [Final Report](attachment-url-here).

For any queries or contributions, feel free to open an issue or submit a pull request.
