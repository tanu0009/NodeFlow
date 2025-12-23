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

NodeFlow is a visual pipeline builder that enables users to design workflows using a drag-and-drop, node-based interface.
The application allows users to connect different processing nodes such as input, text, LLM, and output nodes to form structured pipelines.

The system integrates backend validation to analyze the pipeline structure by counting the number of nodes and edges and verifying whether the workflow forms a Directed Acyclic Graph (DAG).
This ensures logical correctness and prevents invalid cyclic dependencies.

NodeFlow simplifies experimentation with graph-based workflows and provides a clean interface for building and validating pipelines efficiently.

Run Locally

Clone the repository in a virtual environment and run the frontend and backend using the following commands:

Frontend
git clone https://github.com/your-username/nodeflow-visual-pipeline.git
cd nodeflow-visual-pipeline/frontend
npm install
npm start


The frontend will run at:

http://localhost:3000

Backend
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

Reusable node abstraction for creating new nodes easily

Dynamic Text node that generates input handles from {{variables}}

Visual connections between nodes using edges

Backend validation to:

Count number of nodes

Count number of edges

Check whether the pipeline forms a DAG

Simple and professional user interface

Tech Stacks & Libraries
Frontend

ReactJS

Hyper Text Markup Language (HTML)

Cascading Style Sheets (CSS)

JavaScript

React Flow

Zustand

Backend

Python

FastAPI

Uvicorn

Backend APIs
/pipelines/parse

This API receives pipeline node and edge data from the frontend and returns analysis results including node count, edge count, and DAG validation.

References

https://reactflow.dev

https://fastapi.tiangolo.com
