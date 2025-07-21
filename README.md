# Blockchain-based Face Recognition Voting System

## Overview

This project is a **secure, blockchain-powered online voting system** that integrates **facial recognition authentication** to uphold election integrity. The platform ensures that only registered users can vote, prevents double voting, and guarantees that all votes are transparently recorded on an immutable blockchain ledger.

## Features

- **User Registration**
  - Voters register using a unique Voter ID and **facial data** for biometric authentication.
  - Registration is handled via a frontend form, with facial data captured, encoded, and stored locally for privacy and verification[2][6].

- **Facial Authentication**
  - Uses computer vision with OpenCV and a K-Nearest Neighbors (KNN) classifier to recognize faces during login and voting, ensuring a single person can only vote once[2][6].

- **Voting Process**
  - Authenticated users select their candidate.
  - Vote transactions are validated and incorporated into a custom **blockchain**, securing vote history from tampering or duplication[6].

- **Blockchain Ledger**
  - Custom blockchain implementation with proof-of-work mining to validate and link blocks containing vote records[6].
  - Chain integrity can be checked, and any tampering is immediately detected and flagged by the backend[6].

- **Results**
  - Voting results are aggregated live from the blockchain and presented in the UI for transparency[5][6].

- **Web Application**
  - User-friendly web interface built with Flask and HTML templates, covering registration, voting, and result viewing[1][3][4][5].
  
- **API Endpoints**
  - `/register`: Face-based voter registration
  - `/recognize`: Facial recognition and authentication
  - `/vote`: Cast vote (ensures no double voting)
  - `/results`: View live election results from the blockchain
  - Blockchain validation and test endpoints[6]

## Technology Stack

- **Python 3**
- **Flask** (Backend & Frontend serving)
- **OpenCV, numpy** (Facial recognition)
- **scikit-learn** (KNN classifier)
- **HTML/CSS** (Web templates)
- **Custom Blockchain** (Python-based)

## How It Works

1. **Registration**: Voter submits Voter ID and facial data at `/register`[2][6].
2. **Authentication**: Before voting, user verifies identity by face at `/recognize`[2][6].
3. **Voting**: Authenticated user selects a candidate; backend ensures they haven't voted before and appends their vote in a new blockchain block[6].
4. **Results**: Votes counted live from blockchain data, displayed on `/results`[5][6].


## Setup & Usage

1. **Installation:**
     pip install flask opencv-python numpy scikit-learn requests

2. **Start the Blockchain Voting Server:**
    python voting_server.py

3. **Start the Flask Web Client:**
    python client.py

4. Open [http://localhost:5000](http://localhost:5000) to use the application.
