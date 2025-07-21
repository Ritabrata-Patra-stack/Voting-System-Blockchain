Voting System with Facial Recognition and Blockchain
Overview
This project is a secure electronic voting system that uses facial recognition for voter authentication and blockchain technology to ensure vote integrity. The system provides a user-friendly web interface for registration, authentication, voting, and viewing live results.

Features
Facial recognition-based voter authentication using OpenCV and KNN

Blockchain-backed vote recording for tamper resistance and transparency

Voter registration (with facial data capture)

Secure vote casting; prevents double voting

Live results dashboard

Web frontend built with Flask and HTML

Directory Structure
File/Folders	Purpose
client.py	Frontend Flask server for user interactions
voting_server.py	Backend server: facial recognition & blockchain logic
facial_module.py	Handles facial recognition, registration, and voting logic
templates/	HTML templates (index.html, register.html, results.html)
data/	Stores registered face and voter data (pickles)
Votes.csv	Tracks who has voted
Requirements
Python 3.x

Flask

OpenCV

scikit-learn

Requests

NumPy

Install dependencies:

bash
pip install flask opencv-python scikit-learn requests numpy
Usage
Start the backend server:

bash
python voting_server.py
Start the frontend server:

bash
python client.py
Open your browser:
Go to http://127.0.0.1:5000/

Typical Workflow:

Register: Click “Register”, enter voter ID, and let webcam capture facial data.

Authenticate and Vote: On home page, start face verification, select a candidate, and cast vote.

View Results: Click “View Live Results” to monitor current standings.

Security
One vote per person: Enforced by unique voter ID and face recognition.

Tamper-evident log: The blockchain backend ensures recorded votes are immutable and verifiable.

Vote privacy: Only vote choices are stored on blockchain (not face data).

Notes
Ensure you have a webcam connected for facial verification.

For demonstration, both servers run locally on different ports (5000 for frontend, 5001 for backend).

For production, securely handle face data and harden network security.
