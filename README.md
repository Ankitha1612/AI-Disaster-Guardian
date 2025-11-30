🛡️ AI Disaster Guardian
Multi-Agent Crisis Response & Misinformation Verification System

AI Disaster Guardian is a multi-agent emergency assistance system that helps people during disasters such as fires, floods, earthquakes, chemical leaks, and extreme weather events.

It verifies user-reported information, filters misinformation, and provides clear, safe, step-by-step emergency instructions using a Planner → Workers → Evaluator workflow.

This system was developed for the Google Kaggle AI Agents Challenge – Agents for Good Track.

🚨 Key Features
✔️ Disaster Detection

Understands natural-language messages and identifies the type of emergency (fire, flood, collapse, toxic gas, etc.).

✔️ Misinformation Verification

Checks rumors, unverifiable claims, and uncertainty using:

rule-based verification

confidence scoring

simple retrieval signals (RAG-lite)

✔️ Safety Instruction Generator

Returns structured, actionable safety steps based on verified information.

✔️ Session Memory

Stores conversation state:

detected intent

emergency type

verified claims

previous messages

safety steps

✔️ Multi-Agent Architecture

Includes:

Planner Agent – decides workflow

Verification Worker – checks claims & rumors

Safety Worker – generates emergency steps

Communication Worker – formats responses

Evaluator Agent – ensures safety & correctness

🧠 Multi-Agent Architecture 


                          ┌────────────────────────┐
                          │      User Message      │
                          └────────────┬───────────┘
                                       │
                                       ▼
                          ┌────────────────────────┐
                          │     🧭 Planner Agent    │
                          │ - Understands input     │
                          │ - Detects emergency     │
                          │ - Creates task plan     │
                          └────────────┬───────────┘
                                       │
                     ┌─────────────────┼─────────────────┐
                     │                 │                 │
                     ▼                 ▼                 ▼
         ┌──────────────────┐  ┌──────────────────┐  ┌────────────────────┐
         │ 🔍 Verification   │  │ 🛟 Safety        │  │ 💬 Communication    │
         │     Worker       │  │     Worker       │  │      Worker         │
         │ - Checks rumors  │  │ - Generates      │  │ - Formats response  │
         │ - Evidence RAG   │  │   safety steps   │  │ - Ensures clarity   │
         └─────────┬────────┘  └────────┬─────────┘  └──────────┬─────────┘
                   │                    │                       │
                   └──────────┬─────────┴─────────┬─────────────┘
                              ▼                   ▼
                     ┌────────────────────────────────────────┐
                     │         🛡 Evaluator Agent              │
                     │ - Safety rules check                   │
                     │ - Consistency check                    │
                     │ - Approve / Escalate                   │
                     └───────────────────┬────────────────────┘
                                         │
                                         ▼
                          ┌────────────────────────┐
                          │  ✅ Final Safe Output   │
                          │ (Safety steps, verified │
                          │  info, formatted text)  │
                          └────────────────────────┘

🧪 Example Outputs
🔥 Fire Scenario
Input: "There is smoke and fire in my building!"
Output:
Safety steps:
- Leave the building immediately.
- Do not use elevators.
- Cover your mouth with cloth.
- Call emergency services.

🌊 Flood Scenario
Input: "Water is rising near my house."
Output:
- Move to higher ground immediately.
- Do not walk or drive through flood water.
- Turn off electricity if safe.

❗ Rumor Verification
Input: "Someone told me Shelter A is closed, is that true?"
Output:
This claim cannot be verified. Please check official alerts or emergency helplines.

🏗️ Tech Stack

Python
Google Colab
Rule-based agents
Lightweight multi-agent architecture
Session memory (JSON)


🚀 How to Run (Google Colab)

Open the notebook
Click Runtime → Run All

Test with:
run_agent("There is smoke and fire in my building!")

👩‍💻 Developer
Chitiki Ankitha
B.Tech Cyber Security (2026)
AI & Cybersecurity Enthusiast
