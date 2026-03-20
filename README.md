# 🚀 RiskSense AI  
### Predicting Risk. Protecting Earnings.

---

## 🌍 THE STORY BEHIND RISKSENSE AI

Every day, delivery riders step out to earn their livelihood. Unlike traditional jobs, their income depends completely on daily work.

On a normal day, they earn steadily.  
But when conditions like heavy rain, extreme heat, or pollution occur, working becomes unsafe.

In such situations:
- They are forced to stop working  
- Their income drops to zero  

However, their expenses don’t stop:
- Rent  
- Food  
- Family responsibilities  

This creates a real problem:

> ❗ There is no system that protects their income during unavoidable disruptions.

**RiskSense AI is designed to solve this gap.**

---

## 💡 WHAT IS RISKSENSE AI?

RiskSense AI is an **AI-powered income protection system for delivery workers**.

It works on a simple principle:

> If a rider cannot work due to real-world risks, they should still receive financial support.

Instead of manual claims:
- The system automatically detects risk conditions  
- Provides **instant payouts**

---

## 👤 UNDERSTANDING THE USER

Consider a delivery rider:

- ✅ Normal days → steady income  
- ❌ Risky days → no income  

What they need is:
> A simple, reliable safety system — not complex insurance.

---

## ⚠️ CORE PROBLEM

Delivery workers face:

- Income loss due to weather and environmental conditions  
- Unsafe working situations  
- No real-time financial protection  
- Slow and impractical traditional insurance systems  

---

## 🛠️ SOLUTION APPROACH

RiskSense AI uses a **Parametric Protection Model**.

- No manual claim processing  
- No paperwork  
- No delays  

> When conditions are met → payout is triggered automatically

---

## ⚙️ SYSTEM WORKFLOW

1. User subscribes to a weekly membership  
2. System continuously monitors:
   - Weather conditions  
   - Temperature  
   - Air Quality Index  

3. If thresholds are crossed:
   - Rider activity is verified  

4. If impact is confirmed:
   - ✅ Instant payout  

5. Otherwise:
   - 🔄 Monitoring continues  

---

## 📊 PARAMETRIC TRIGGERS

Payouts are triggered based on:

- 🌧️ Heavy rainfall  
- 🌡️ Extreme temperature  
- 🌫️ High pollution (AQI)  

### Benefits:
- Fast decision-making  
- No human dependency  
- Transparent execution  

---

## 💳 WEEKLY MEMBERSHIP MODEL

- Users pay a small weekly premium  
- Premium varies based on location risk  

### Why weekly?
- Matches daily earning pattern  
- Affordable  
- Flexible  

---

## 🤖 ROLE OF AI

AI powers the intelligence of the system:

- Risk Prediction  
- Dynamic Pricing  
- Fraud Detection  
- Continuous Learning  

---

# 🔐 FRAUD DETECTION & SECURITY SYSTEM (NEW 🔥)

To ensure fairness, RiskSense AI uses a **Multi-Layer Fraud Detection System**.

> We don’t trust GPS alone.

---

## 🧠 MULTI-LAYER DETECTION SYSTEM

### 1. Device-Level Checks
- Detect mock GPS apps  
- Check developer options  
- Detect rooted devices  

👉 Output: Device Risk Score  

---

### 2. Sensor Fusion
Compare:
- GPS 📍  
- Accelerometer 🚶  
- Gyroscope 🧭  
- Network 📶  

👉 If mismatch → Suspicious  

---

### 3. Movement Pattern Analysis (LSTM Model) 🔥

We use an **LSTM (Long Short-Term Memory) time-series model**.

### What it does:
- Learns user movement over time  
- Understands normal behavior  

### Detects:
- ❌ Sudden jumps (fake teleportation)  
- ❌ Impossible speeds  
- ❌ Unrealistic paths  
- ❌ Repeated fake locations  

👉 Output: **Anomaly Score**

---

### 4. Geo-Fencing + Weather Validation
- Verify user is inside affected area  
- Match with real weather data  

👉 If mismatch → Fraud  

---

### 5. Group Fraud Detection
Detect:
- Multiple users in same fake location  
- Same claim timing  

👉 Prevents coordinated attacks  

---

### 6. Server-Side API Protection
- JWT authentication  
- Device binding  
- Rate limiting  
- Encrypted requests  

👉 Stops bots & hackers  

---

## ⚖️ AI RISK SCORING SYSTEM

All checks are combined into a **Final Risk Score**:

```python
Final Risk Score = (Device Risk * 0.2) + (Sensor Mismatch * 0.2) + (LSTM Anomaly * 0.3) + (Geo Validation * 0.1) + (Group Fraud * 0.2)
