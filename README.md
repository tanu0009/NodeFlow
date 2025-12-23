# NodeFlow

NodeFlow – Visual Pipeline Builder
Contents

Introduction

Key Highlights

Pipeline Builder

Text Node Logic

Backend Validation

Tech Stacks

Tools Used

How to Run the Project

License

References

Introduction

NodeFlow is a visual, node-based pipeline builder that allows users to design workflows using a drag-and-drop interface.
The project enables users to connect different nodes such as input, text processing, LLM, and output nodes to form structured pipelines.

The system integrates backend validation to analyze the pipeline structure by counting nodes and edges and checking whether the workflow forms a Directed Acyclic Graph (DAG).
This ensures logical correctness and prevents invalid cyclic dependencies.

Key Highlights

Drag-and-Drop Workflow: Create pipelines visually using nodes and connections.

Reusable Node Design: Easy to extend and add new node types.

Dynamic Text Handling: Generates input handles from {{variables}}.

Backend Validation: Verifies DAG structure and pipeline correctness.

Simple UI: Clean, professional, and user-friendly interface.

Pipeline Builder

Visual canvas for building pipelines.

Supports multiple node types such as Input, Text, LLM, and Output.

Connections represent data flow between nodes.

Text Node Logic

Automatically resizes based on input content.

Detects variables wrapped in {{ }}.

Creates dynamic input handles for each detected variable.

Enables flexible data injection into text-based workflows.

Backend Validation

Receives node and edge data from the frontend.

Calculates:

Number of nodes

Number of edges

DAG validity

Returns results to the frontend for user display.

Tech Stacks

Frontend: React, JavaScript, React Flow, Zustand, HTML, CSS

Backend: Python, FastAPI, Uvicorn

IDE: VSCode

Tools Used
Resource	Specifications	Quantity	Purpose
Laptop	macOS, 8GB RAM	1	Development & Testing
VSCode	Latest Version	1	Code Editing
Node.js	v18+	1	Frontend Runtime
Python	3.x	1	Backend Development
How to Run the Project

Clone the repository:

git clone <repository-url>


Navigate to the frontend folder and run:

cd frontend
npm install
npm start


Open a new terminal and navigate to the backend folder:

cd backend
python -m venv venv
source venv/bin/activate
pip install fastapi uvicorn
uvicorn main:app --reload


Open the application in the browser using:

http://localhost:3000

License

This project is licensed under the MIT License.

References

https://reactflow.dev

https://fastapi.tiangolo.com
