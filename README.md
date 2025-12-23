# NodeFlow
NodeFlow – Visual Pipeline Builder
Contents

Introduction

Run Locally

Features

Tech Stacks & Libraries

Backend APIs

References

Introduction

NodeFlow is a visual pipeline builder that allows users to create workflows using a drag-and-drop, node-based interface.
The application enables users to connect different types of nodes such as input, text processing, LLM, and output nodes to form structured pipelines.

The system also integrates backend validation to analyze the pipeline by counting the number of nodes and edges and verifying whether the pipeline forms a Directed Acyclic Graph (DAG).
This helps ensure logical correctness and prevents invalid cyclic workflows.

NodeFlow is designed as a simple and intuitive tool to experiment with graph-based workflows and pipeline structures.

Run Locally

Clone the repository and run the frontend and backend using the following commands.

Frontend Setup
git clone https://github.com/your-username/nodeflow-visual-pipeline.git
cd nodeflow-visual-pipeline/frontend
npm install
npm start


The frontend will run at:

http://localhost:3000

Backend Setup (with Virtual Environment)
cd nodeflow-visual-pipeline/backend
python -m venv venv
source venv/bin/activate
pip install fastapi uvicorn
uvicorn main:app --reload


The backend will run at:

http://127.0.0.1:8000


API documentation is available at:

http://127.0.0.1:8000/docs

Features

Drag-and-drop node-based workflow editor

Reusable node abstraction for easy extensibility

Dynamic Text node that creates input handles from {{variables}}

Visual connections between nodes using edges

Backend validation to:

Count number of nodes

Count number of edges

Check whether the pipeline is a DAG

Simple and professional user interface

Tech Stacks & Libraries
Frontend

React

JavaScript

React Flow

Zustand

HTML

CSS

Backend

Python

FastAPI

Uvicorn

Backend APIs
POST /pipelines/parse

Description:
Analyzes the pipeline structure sent from the frontend.

Request Body:

{
  "nodes": [],
  "edges": []
}


Response:

{
  "num_nodes": 4,
  "num_edges": 3,
  "is_dag": true
}

References

React Flow Documentation
https://reactflow.dev

FastAPI Documentation
https://fastapi.tiangolo.com
