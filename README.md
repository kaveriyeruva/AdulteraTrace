# AdulteraTrace
An ESP32-based tool that checks food sample sensor data against standard safety limits to detect adulteration.
# AdulteraTrace

An ESP32-based tool that checks food sample sensor data against standard safety limits to detect adulteration.

## Overview
This project is a hardware and software setup designed to test food samples for adulteration. It uses an ESP32 microcontroller paired with basic sensors (like pH and TDS meters) to measure physical and chemical properties. The backend script compares these readings against standard safe limits, calculates any deviations, and flags potential additives or dilution (such as added water in milk or syrup in honey).

## Project Structure
- `firmware/`: ESP32 C++ code for reading sensor inputs and sending data over Wi-Fi.
- `backend/`: Python FastAPI service that evaluates safety thresholds and returns warnings.

## Getting Started

### 1. Backend Setup
Navigate to the backend folder, install dependencies, and run the server:
```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload --host 0.0.0.0 --port 8000
