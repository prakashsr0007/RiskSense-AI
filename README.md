# RiskSense AI

## Predicting Risk. Protecting Earnings

---

## The Story Behind RiskSense AI

Every day, delivery riders step out to earn their livelihood. Unlike traditional jobs, their income depends entirely on daily work. On normal days, they earn consistently. However, when conditions such as **heavy rain, extreme heat, or high pollution** occur, working becomes unsafe.

In these situations, riders are forced to stop working, which means their **income drops to zero**. At the same time, their essential expenses like **rent, food, and family responsibilities continue**.

This creates a real and urgent gap:
**there is no reliable system that protects their income during unavoidable disruptions.**

RiskSense AI is designed to solve this problem.

---

## What is RiskSense AI?

RiskSense AI is an **AI-powered income protection system** built for delivery workers.

It follows a simple idea:
**if a rider cannot work due to real-world risks, they should still receive financial support.**

Instead of manual claims, the system automatically detects risk conditions and triggers **instant payouts**. This removes delays, paperwork, and dependency on human approval.

---

## Core Problem

Delivery workers today face:

* **Income loss** during unsafe weather or environmental conditions
* **No real-time protection system**
* **Slow and complex insurance processes**
* **High dependency on manual claim verification**

---

## Solution Approach

RiskSense AI uses a **parametric protection model**.

This means payouts are not based on manual claims but on **predefined measurable conditions** such as weather and environmental data.

When these conditions are met, the system automatically processes the payout.
This ensures **speed, transparency, and reliability**.

---

## System Workflow

1. The user subscribes to a **weekly membership plan**

2. The system continuously monitors:

   * Weather conditions
   * Temperature levels
   * Air Quality Index

3. If risk thresholds are crossed:

   * User activity is evaluated

4. Based on verification:

   * **Payout is triggered** or
   * **Monitoring continues**

---

## Example Scenario :

Consider a delivery rider working in a city during **heavy rainfall**.

### System Observation

- The system detects **rainfall above defined threshold levels**  
- The rider’s activity shows **reduced or no movement**  
- GPS, sensor data, and environmental data are continuously validated  


### Case 1: Genuine User

- Movement patterns are **natural and consistent**  
- Location correctly matches **real weather conditions**  
- Risk score remains **low**

> **Payout is approved instantly**


### Case 2: Fake GPS Attempt

- GPS shows rider inside a **high-risk (flood) zone**  
- Sensor data indicates **no real physical movement**  
- LSTM detects **abnormal movement patterns**

> **Risk score increases and verification is triggered**


### Case 3: Coordinated Fraud

- Multiple users appear in the **same high-risk location**  
- Claims are made at **similar timestamps**  
- Behavior patterns show strong similarity  

> **System detects group fraud and blocks claims**

---

## Weekly Membership Model

RiskSense AI follows a **simple weekly subscription system**.

* Users pay a **small weekly premium**
* Pricing is based on **location risk and conditions**

### Why weekly?

* Matches the **earning pattern of gig workers**
* Keeps the system **affordable and flexible**
* Ensures **continuous protection without long-term commitment**

---

## Technology Stack

RiskSense AI is built using a combination of **scalable backend systems** and **intelligent AI models** to ensure reliability and performance.

### Core Technologies

- **Backend**: Python / Node.js for API handling and system processing  
- **Machine Learning**: LSTM (time-series model) for movement anomaly detection  
- **Data Processing**: Real-time streaming of GPS and sensor data  
- **APIs**: Weather API for environmental condition validation  
- **Database**: MongoDB / PostgreSQL for storing user and activity data  
- **Security**: JWT-based authentication and secure API communication  

-> This stack ensures the system is **scalable, reliable, and capable of real-time decision-making**.

---

## Important Reality Check

It is important to understand that:

* **GPS cannot be forced to stay ON at all times**
* Devices may disable location services to save battery
* Users can manually turn off permissions

Because of this, RiskSense AI does not rely only on GPS.
Instead, it uses a **multi-layer verification system** to ensure accuracy and trust.

---

## Multi-Layer Detection System

To prevent fraud and ensure fairness, RiskSense AI uses a **multi-layer detection approach**.
Each layer validates user behavior from a different perspective.

### 1. Device-Level Checks

The system checks device integrity by detecting:

* Fake GPS or mock location apps
* Developer mode usage
* Rooted or modified devices


### 2. Sensor Fusion

Instead of trusting GPS alone, the system compares:

* GPS location
* Physical movement (accelerometer)
* Device orientation (gyroscope)
* Network signals

Any mismatch between these signals indicates **suspicious behavior**.


### 3. Movement Pattern Analysis (LSTM Model)

The system uses an **LSTM-based time-series model** to understand user movement over time.

It learns normal behavior and detects:

* **Unrealistic location jumps**
* **Impossible speeds**
* **Artificial or repetitive movement patterns**

This produces an **anomaly score**, representing how unusual the behavior is.


### 4. Geo-Fencing and Weather Validation

The system verifies whether:

* The user is actually in the affected area
* The environmental condition is real

If the location does not match real-world data, it is flagged as **invalid**.


### 5. Group Fraud Detection

The system identifies coordinated fraud by analyzing:

* Multiple users at the same location
* Similar timing of claims
* Repeated patterns across users

This helps prevent **organized misuse of the system**.


### 6. Server-Side Security

All backend requests are protected using:

* Secure authentication
* Device binding
* Rate limiting
* Encrypted communication

This ensures that only **valid and trusted requests** are processed.

---

## AI Risk Scoring System

All detection signals are combined into a **single risk score** for each claim.

The score is calculated using:

* Device integrity results
* Sensor consistency
* LSTM anomaly detection
* Location and weather validation
* Group behavior analysis

### Decision Logic

* **Low Risk** → Claim approved
* **Medium Risk** → Verification required
* **High Risk** → Claim blocked

---

## Fairness and User Verification

To ensure genuine users are not affected:

Users with a **medium risk score** are given a chance to verify their claim by providing:

* Live photo proof
* Real-time location confirmation
* Activity validation

This ensures that **honest users are always protected**.

---

## Honor Score System (User Trust Model)

RiskSense AI maintains a long-term **Honor Score** for each user.

* Every user starts with a score of **100**
* The score reflects **overall behavior and trustworthiness**

### Score Decreases When:

* Fraud or spoofing is detected
* Suspicious activity is repeated
* Verification fails

### Score Increases When:

* The user behaves consistently
* Claims are verified successfully
* No suspicious activity is observed

### Impact of Honor Score:

* **95–100** → High trust, faster approvals
* **80–94** → Normal usage
* **60–79** → Increased verification
* **Below 60** → Restricted access

This system encourages **honest usage and long-term trust**.

---

## AI RISK SCORING SYSTEM

All checks are combined into a **Final Risk Score**:

```python
Final Risk Score = (Device Risk * 0.2)  +  (Sensor Mismatch * 0.2)  +  (LSTM Anomaly * 0.3) +  (Geo Validation * 0.1) +  (Group Fraud * 0.2)
```
---

## Implementation Insight :

The LSTM model is trained on **time-series movement data**, including:
- Latitude and longitude sequences  
- Speed and direction variations  
- Time intervals between movements  

### How It Works
- The system uses a **sliding window approach** to continuously analyze recent activity  
- Current movement is compared with **learned normal behavior patterns**  
- An **anomaly score** is generated to represent deviation.

This anomaly score is then combined with other signals inside the **AI Risk Scoring Engine** to make final decisions.

---

## System Architecture

```
User (Mobile App)
        │
        ▼
Data Collection Layer
(GPS, Sensors, Device Info)
        │
        ▼
Pre-Processing Layer
        │
        ▼
Multi-Layer Detection Engine
        │
        ▼
AI Risk Scoring Engine
        │
        ▼
Decision Engine
        │
        ▼
Honor Score System
        │
        ▼
Payout / Monitoring
```
<img width="1152" height="768" alt="architecture" src="https://github.com/user-attachments/assets/860b5587-29d8-45eb-9a62-4e56faddfd0c" />

---

## System Design Strength :

RiskSense AI follows a **multi-layered defense architecture**.

### Key Design Principles

- Each layer validates a **different aspect of user behavior**  
- There is **no single point of failure**  
- Detection operates in **real-time with adaptive learning**  

### Outcome

This design ensures the system is:
- **Resilient against simple spoofing attacks**  
- **Capable of detecting advanced and coordinated fraud**  
- **Reliable for real-world deployment scenarios**

---

## Key Innovation

RiskSense AI does not depend on a single data source.

It combines:

* **Behavioral AI (LSTM model)**
* **Sensor-based validation**
* **Device integrity checks**
* **Real-world data verification**

This enables **accurate and real-time fraud detection** while protecting genuine users.

---

## Final Message

RiskSense AI is not just a technical solution. It is a system designed to provide:

* **Financial security**
* **Confidence during uncertain conditions**
* **Reliable support for gig workers**

**Predicting risks early, protecting earnings always.**

---
## RISKSENSE AI's Goal

To build a system where: **no one delivery worker loses income due to conditions beyond their control.**

---
by **TEAM AI RUDHRA**
