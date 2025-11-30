# 🛡️ AI Disaster Guardian  
### Multi-Agent Crisis Response & Misinformation Verification System

AI Disaster Guardian is a **multi-agent emergency assistance system** built to help people during disasters such as floods, fires, earthquakes, and chemical leaks.  
It verifies user-reported information, filters misinformation, and provides **clear, safe emergency instructions** using a Planner → Workers → Evaluator workflow.

This system was developed as part of the **Google Kaggle AI Agents Challenge (Agents for Good Track)**.

---

## 🚨 Key Features

### ✔️ **Disaster Detection**
Understands user messages and identifies the emergency type (fire, flood, earthquake, etc.).

### ✔️ **Misinformation Checker**
Verifies claims using retrieval, rules, and confidence scoring.

### ✔️ **Safety Instruction Generator**
Provides step-by-step emergency guidance based on verified data.

### ✔️ **Session Memory**
Stores context per conversation:
- user intent  
- disaster type  
- verified claims  
- safety instructions  

### ✔️ **Multi-Agent Architecture**
Uses:
- **Planner Agent** → decides which workers to call  
- **Workers** → verification, safety, routing, communication  
- **Evaluator** → checks safety, consistency & correctness  

---

## 🧠 Multi-Agent System Architecture

