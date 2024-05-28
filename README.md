# Project Overview

This README outlines a project focusing on graph data analysis across various sectors, with a special emphasis on the film and finance industries. The project utilizes the graph database Neo4j and GPT-3 (Generative Pre-trained Transformer) to analyze and interpret complex network data, assisting decision-makers in optimizing workflows and detecting irregular activities.

## Project Structure

The project is divided into several directories, each focusing on a specific industry or type of analysis. Below is an overview of these directories and the notebooks they contain.

### Film Industry Analysis

This directory contains notebooks that apply graph data analysis to optimize film production schedules and test various scenarios using GPT models. The main logic is to understand graph data from the film industry and find an optimal path using MST (Minimal Spanning Tree), which represents an optimal shooting schedule.

#### Notebooks:

- **GPT Transfer**
  - **Description**: Test whether GPT-3 can recognize optimal shooting schedules with the given prompt and convert complex network data into understandable language to aid decision-makers in planning film production schedules.

- **Filmproduction Scenes Management Schedule 1**
  - **Description**: Demonstrates the use of a Neo4j database to manage film production scenes, including the creation of scenes, relations, and weightings based on shared resources. It generates a Minimal Weight Spanning Tree (MWST) and the Traversals to identify scenes that can be shot simultaneously and concludes with producing an optimal shooting schedule. This approach optimizes resource allocation and maximizes efficiency in the shooting process.

- **Filmproduction Scenes Management Schedule 2**
  - **Description**: This notebook follows the same methodology as Schedule 1, using a Neo4j database to manage film production scenes with shared resources. It generates a Minimal Spanning Tree (MWST) starting from a different node to explore alternative shooting schedules. This variation allows for examining the impact of different starting points on the optimality and feasibility of the production schedule, using the same set of scenes as in Schedule 1.

- **Testdate Generation**
  - **Description**: Defines and generates test data pairs for various requirements to ensure a diverse set of test data is available for analysis.
    
- **Testing**
  - **Description**: Conducts tests to ensure that all functionalities meet the specified requirements.
 
- **Heatmap for Actors/Equipment/Location Tests**
  - **Description**: Generates heatmaps to visualize the testing results.

### Finance Industry Analysis

This directory applies the same principles used in the film industry to detect potential money laundering cases in the financial sector, translating findings from Neo4j Pathfinding algorithm into understandable language for decision-makers.

#### Notebooks:

- **MWST and GPT**
  - **Description**: Adapts the principles used in the film industry to the financial sector, focusing on detecting anomalies that could indicate money laundering.

### Network Graph Analysis

This directory explores various network graph analysis techniques using Neo4j libraries and passes the results to GPT for interpretation.

#### Notebooks:

- **Centrality Metrics GPT**
- **Community Detection GPT**
- **Connected Components**
- **Pathfinding Algorithms GPT**
- **Similarity Algorithm GPT**

### First Trials

Initial experiments in graph analysis using Neo4j Cypher Queries and algorithms, followed by processing with GPT through the RAG framework.

#### Notebooks:

- **RAG Example**
- **Talk to Graph**

## Installation


### Setting Up Neo4j Graph Database

To fully utilize the functionalities of this project, you need to set up a Neo4j graph database using the Neo4j Desktop application.

#### Install Neo4j Desktop
- **Download and install** the Neo4j Desktop application from [Neo4j's official website](https://neo4j.com/download/).

#### Create a New Project
- **Open Neo4j Desktop** and create a new project.

#### Generate Two Different DBMS
- **Within the project**, generate two different DBMS instances for Schedule Plan 1 and Schedule Plan 2. For each of the instances, you must install the GDS (Graph Data Science) and APOC (Awesome Procedures On Cypher) libraries:
  - For each DBMS, click 'Plugins' and install both 'APOC' and 'GDS' from the available options.

#### Start the Graph Database
- **Start one of the graph databases** and set the password, which will be used to connect from the notebooks.

#### Connect from Notebooks
- **Once the graph database is running**, you can establish a connection using the specified password in your notebooks. This connection will allow you to access the database and perform data analyses and algorithm implementations.

#### Neo4j Browser
- **You can track data analyses and algorithms** directly in the Neo4j Browser, which provides a visual interface to interact with your graph data.



### Setting up the project environment

Install all necessary Python packages using the following command:

```bash
pip install -r requirements.txt
