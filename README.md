# Copilot Studio Budgetary Cost Estimator

This repository hosts a **published GitHub Pages application**.

Source files are not distributed for reuse.

➡️ **Live estimator:**  
https://bradlaw76.github.io/CopilotStudioBedgetaryCostEstimator/

---

## Overview

**Copilot Studio Agent Cost Calculator v1.3.3.1** is a professional-grade financial forecasting tool designed to estimate **consumption-based costs** for Microsoft Copilot Studio agent deployments.

The application models budgetary requirements using the **Microsoft Copilot Credit billing model** (January 2026 baseline) and is intended for:

- Architectural planning  
- Budgetary funding requests  
- ROI and scale analysis  

It enables stakeholders to clearly distinguish between **standard generative agents** and **high-intensity autonomous agents**.

---

## Why This Tool Exists

Microsoft Copilot Studio has transitioned from a *message-based* billing model to a **credit-based consumption model**. Estimating costs manually is complex due to:

- **Variable burn rates** across retrieval, generation, and reasoning
- **Linear scale dynamics** tied to agent count and conversation volume
- **Enterprise baselines** that typically assume a 22-day business month (not calendar days)

This tool consolidates those variables into a single, funding-ready interface.

---

## How It Works

### 1. Mode Selection

The estimator supports two distinct execution models:

- **Standard Agents**  
  Focused on tenant knowledge retrieval (Graph Grounding) and generative answers.

- **Autonomous Agents**  
  Advanced agents utilizing logic triggers, deep reasoning steps (o1), and Power Automate flow actions.

Each mode uses a dedicated calculation path.

---

### 2. Input Synchronization

Inputs can be adjusted using:

- **Range sliders** for rapid what-if modeling  
- **Numeric input fields** for precision planning  

All calculations update in real time across summary panels.

---

### 3. Calculation Methodology

The math follows a strict, sequential rollup validated against enterprise financial templates:

1. **Daily Credit Burn per Agent**  
   Session credit cost × daily conversation volume

2. **Monthly Rollup**  
   Daily credits × business days per month (default: 22)

3. **Monthly Financials**  
   Monthly credits × credit unit price (default: $0.01)

4. **Annual Projection**  
   Monthly total × 12

---

## Consumption Parameters (Defaults)

| Parameter | Credit Burn | Description |
|--------|-------------|------------|
| Tenant Graph Grounding | 10 | Knowledge retrieval from SharePoint / OneDrive via Graph |
| Generative AI Answers | 2 | Standard generative output |
| Autonomous Triggers | 7 | Initiation of autonomous logic loops |
| Deep Reasoning (o1) | 10 | Complex orchestration or multi-step reasoning |
| Agent Flow Actions | 0.13 | Execution of individual Power Automate cloud flows |

---

## Key Features

### Persistence
The application uses browser **localStorage** (`copilot_rates_v4`) to persist configuration changes.  
Custom burn rates and business-day assumptions remain saved between sessions on the same device.

---

### Outlook Integration
The **Generate Funding Draft** button automatically creates a customer-ready Outlook email containing:

- A professional financial summary  
- Annual and monthly projections  
- A hidden *technical audit block* appended below the fold for traceability  

---

### Security & Integrity Controls

To reduce accidental source reuse during demos and reviews, version **1.3.3.1** includes:

- Context menu blocking (right-click)
- Keyboard intercepts for Ctrl+S (Save) and Ctrl+U (View Source)

These measures are **deterrents**, not security controls.

---

## Important Funding Disclaimer

- **Non-binding:** All values are estimates provided for planning and funding purposes only  
- **Variable consumption:** Actual billing will vary based on agent configuration and runtime behavior  
- **Pricing subject to change:** Always validate credit rates against official Microsoft documentation  

---

## Technical Stack

- **HTML5 / CSS3** – Responsive layout  
- **Tailwind CSS** – Utility-first styling  
- **Vanilla JavaScript** – High-performance calculation engine  
- **Web Storage API** – Local persistence  

---

## Version Information

- **Version:** 1.3.3.1  
- **Baseline:** January 2026 Microsoft Copilot Studio Consumption Model  
- **Status:** Locked budgetary estimator baseline
