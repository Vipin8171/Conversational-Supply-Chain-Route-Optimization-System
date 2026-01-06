# Conversational Supply Chain Route Optimization System

## 📌 Overview
This project implements an end-to-end **supply chain decision support system** using real-world shipment data.  
It transforms historical logistics records into optimization-ready inputs, solves a cost-based routing problem under capacity constraints, and provides **explainable decisions** through a conversational AI layer.

The system is designed to reflect **real industrial supply chain workflows** and is implemented entirely in a **Jupyter Notebook**.

---

## 🎯 Objectives
- Process and clean real-world shipment data  
- Estimate shipment demand using historical quantities and weights  
- Optimize freight routing while respecting vehicle capacity constraints  
- Minimize overall transportation cost  
- Generate business-friendly explanations of routing decisions  

---

## 🗂 Dataset
- **Source:** Public Supply Chain Shipment Dataset (Kaggle)  
- **Records:** ~10,000 shipment entries  
- **Key Fields Used:**
  - Country  
  - Manufacturing Site  
  - Line Item Quantity  
  - Weight (Kilograms)  
  - Freight Cost (USD)  

> **Note:**  
> The dataset is not included in this repository due to licensing constraints.  
> Please download it manually and update the dataset path in the notebook before execution.

---

## 🧠 Methodology

### 1. Data Cleaning & Preparation
- Converted numeric fields stored as text into proper numerical formats  
- Removed incomplete and inconsistent shipment records  
- Aggregated shipment statistics at the destination (country) level  

### 2. Demand Estimation
- Estimated shipment demand using a weighted combination of historical shipment quantity and weight  
- Scaled demand values to ensure feasibility across available vehicles  

### 3. Optimization Modeling
- Formulated a **cost-based Vehicle Routing Problem (VRP)** using freight cost as the routing objective  
- Applied **Google OR-Tools** to minimize total transportation cost  
- Enforced vehicle capacity constraints derived from real shipment data  

### 4. Conversational Layer
- Simulated intent and entity extraction (Rasa-style) from natural language logistics queries  
- Interpreted optimization constraints using an open-source LLM (Llama-3)  
- Generated clear, business-oriented explanations of routing decisions  

### 5. Evaluation & Analysis
- Validated feasibility using total demand vs total capacity checks  
- Analyzed cost and load distribution across vehicles  
- Visualized cost allocation to support decision transparency  

---

## 📊 Results & Insights
- Optimized routing across **30+ destination countries** using **4 vehicles**  
- Handled **310,235 units of estimated shipment demand** within **372,280 units of total vehicle capacity**  
- Achieved a total estimated freight cost of **$14,509**  
- Balanced shipment loads and transportation cost across all vehicles  

---

## 🛠 Technologies Used
- **Programming Language:** Python  
- **Data Processing:** Pandas, NumPy  
- **Optimization:** Google OR-Tools  
- **Conversational AI:** Rasa-style NLU (simulated)  
- **LLM:** Llama-3 (constraint interpretation & explanation)  
- **Environment:** Jupyter Notebook  

---

## ▶️ How to Run
1. Download the dataset from Kaggle  
2. Place the CSV file in a local directory  
3. Update the dataset path in the notebook  
4. Run all cells sequentially from top to bottom  

---

## 🚀 Future Enhancements
- Anomaly detection for abnormal shipment cost or weight patterns  
- Multi-objective optimization (cost vs delivery time)  
- Deployment of the conversational layer as a real-time chatbot  

---

## 👤 Author
**Vipin Tomer**  
B.Tech – Artificial Intelligence & Data Science  
IIITDM Kurnool  

---

## 📄 License
This project is intended for educational and internship demonstration purposes.
