# GRAPHML David Agudelo 2026

Spatial analysis and representation project focused on architectural relationships derived from 3D OBJ models. The work is developed in Jupyter Notebook with TopologicPy and converts architectural geometry into semantic structures, spatial graphs, and exportable metric tables.

The repository documents an applied workflow to identify spaces, doors, and windows, register apertures in an architectural model, build connectivity graphs, and produce outputs useful for analysis, teaching, and research.

![Architectural model](Apartment%20Model.png)

## Project Objective

This project aims to demonstrate how a geometric model can be transformed into an interpretable spatial model. Starting from OBJ files, the main notebook builds a `CellComplex`, transfers semantic attributes to architectural spaces, registers apertures, and generates graphs that describe relationships such as adjacency, access, and connections between rooms.

In simple terms, the project translates geometry into spatial information that can be used to:

- read the internal organization of a house or building
- study connectivity between rooms
- identify relationships among doors, windows, and spaces
- export metrics for later analysis or external visualization

## Repository Contents

### Main Notebook

- `Assigment 01_David_Agudelo.ipynb`: complete workflow for import, classification, spatial analysis, graph construction, and result export.

### Input Models

- `Test_05.obj`: main architectural model.
- `Test_05_Doors.obj`: door geometry used as apertures.
- `Test_05_Windows.obj`: window geometry used as apertures.

### Exported Results

- `rooms_summary.csv`: general summary of spaces.
- `rooms_metrics.csv`: spatial metrics for rooms.
- `rooms_schedule.csv`: room schedule table.
- `apertures_summary.csv`: summary of doors and windows.
- `global_counts.csv`: overall counts for the model and the graph.

## Methodology

The notebook workflow can be summarized as follows:

1. Import OBJ geometry and read its basic attributes.
2. Convert enclosed rooms into spatial cells.
3. Assign semantic dictionaries to spaces and internal selectors.
4. Build an architectural `CellComplex`.
5. Register doors and windows as apertures on the model faces.
6. Generate spatial graphs with `Graph.ByTopology`.
7. Extract room-to-room and door-to-room relationships.
8. Export metrics, tables, and counts to CSV.

## Main Tools

- Python 3
- Jupyter Notebook
- TopologicPy
- CSV export for results

## Type of Results Produced

The project does not stop at geometry visualization. It also generates structured information such as:

- spatial connectivity graphs
- identification of connections through shared apertures
- door and window tables with area, dimensions, and position
- room summaries with volume, dimensions, and aperture relationships
- global counts of spaces, apertures, vertices, and edges

### 1. Computational Spatial Analysis

Methodology for transforming geometric models into navigable spatial graphs. The contribution lies in the reproducible workflow: OBJ import, topological conversion, aperture registration, and extraction of spatial metrics.

Possible research question: how does the explicit incorporation of doors and windows influence the interpretation of connectivity and accessibility in an architectural floor plan?

## Author

Arq. David Agudelo  
2026
