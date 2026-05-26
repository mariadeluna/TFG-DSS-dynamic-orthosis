# Decision Support System for Dynamic Orthoses

This repository contains the Python implementation of the Decision Support System (DSS) developed for my Final Project.

The aim of this tool is to support the conceptual design stage of dynamic orthoses manufactured by 3D printing when selecting a suitable motion transmission system.

The DSS is based on a questionnaire, a rule engine and a weighted ranking method.

## Project context

The project focuses on dynamic orthoses and motion transmission systems. The methodology considers different design requirements, such as:

- type of movement
- range of motion
- passive or active assistance
- need for force transmission
- distal mass
- adaptability
- precision
- complexity
- feasibility with PLA and 3D printing

Based on these inputs, the system filters and ranks different mechanical configurations.

## Files included

- `DSS_orthosis.ipynb`  
  Main Jupyter Notebook containing the complete DSS implementation.

- `PLA_filter.csv`  
  Matrix used to check the manufacturing feasibility of each configuration depending on the selected PLA integration level.

- `configurations_matrix.csv`  
  Matrix containing the mechanical configurations and their evaluation criteria.

- `requirements.txt`  
  List of Python libraries needed to run the notebook.

## How the DSS works

The notebook follows these main steps:

1. The required libraries and input files are loaded.
2. The user answers a design questionnaire.
3. A manufacturing filter removes configurations that are not compatible with the selected PLA manufacturing scenario.
4. A rule engine modifies the importance of the evaluation criteria according to the user inputs.
5. The weights are limited and normalised to avoid excessive influence from overlapping rules.
6. Each configuration is scored using a weighted ranking method.
7. The final output is a ranked list of suitable motion transmission systems.

## How to run the notebook

1. Download or clone this repository.

2. Install the required Python libraries:

```bash
pip install -r requirements.txt
