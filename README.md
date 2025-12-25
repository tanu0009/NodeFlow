# NodeFlow

# 🚀 NodeFlow – Visual Pipeline Builder

## 📑 Contents
- Introduction  
- Key Highlights  
- Pipeline Builder  
- Text Node Logic  
- Backend Validation  
- Tech Stacks  
- Tools Used  
- How to Run the Project  
- License  
- References  

---

## 🧩 Introduction

NodeFlow is a **visual, node-based pipeline builder** that allows users to create workflows using an intuitive **drag-and-drop interface**.  
The platform enables users to connect different nodes such as **Input, Text Processing, LLM, and Output nodes** to form structured and logical pipelines.

The application integrates **backend validation** to analyze pipeline structure by:
- Counting nodes and edges  
- Verifying whether the pipeline forms a **Directed Acyclic Graph (DAG)**  

This ensures logical correctness and prevents invalid cyclic workflows.

---

## ✨ Key Highlights

- 🖱️ **Drag-and-Drop Workflow** – Build pipelines visually using nodes and connections  
- 🔁 **Reusable Node Architecture** – Easily extend and add new node types  
- 🧠 **Dynamic Text Logic** – Automatically generates input handles from `{{variables}}`  
- ✅ **Backend Validation** – Counts nodes, edges, and checks DAG correctness  
- 🎨 **Clean UI** – Simple, professional, and user-friendly interface  

---

## 🛠️ Pipeline Builder

- Visual canvas to place and connect nodes  
- Supports multiple node types:
  - Input  
  - Text  
  - LLM  
  - Output  
- Connections between nodes represent **data flow** within the pipeline  

---

## 📝 Text Node Logic

- Automatically resizes as text content increases  
- Detects variables written inside `{{ }}`  
- Dynamically creates **input handles** for each detected variable  
- Enables flexible data injection into text-based nodes  

---

## 🔍 Backend Validation

- Receives pipeline structure from the frontend  
- Calculates:
  - Total number of nodes  
  - Total number of edges  
  - Whether the pipeline forms a **DAG**  
- Returns validation results to the frontend for display  

---

## ⚙️ Tech Stacks

### Frontend
- React  
- JavaScript  
- React Flow  
- Zustand  
- HTML  
- CSS  

### Backend
- Python  
- FastAPI  
- Uvicorn  

### IDE
- VS Code  

---

## 🧰 Tools Used

| Resource | Specifications | Purpose |
|--------|----------------|---------|
| Laptop | macOS, 8GB RAM | Development |
| VS Code | Latest Version | Code Editing |
| Node.js | v18+ | Frontend Runtime |
| Python | 3.x | Backend Development |

---

## ▶️ How to Run the Project

### 🔹 Frontend Setup

```bash
git clone <repository-url>
cd nodeflow-visual-pipeline/frontend
npm install
npm start

