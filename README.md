# GRAPHML David Agudelo 2026

This repository contains Assignment 2 of a graph-based architectural analysis workflow.
The project uses TopologicPy in Jupyter Notebook to convert 3D OBJ geometry into spatial graphs and metric tables.

## Project Goal

The goal is to analyze spatial organization in an architectural model using graph methods.
The notebook computes centrality, shortest paths, bottlenecks, and communities, then exports results for reports and presentations.

## Main Notebook

- `Assignment_02_David_Agudelo_v3.ipynb`: complete Assignment 2 workflow.

## Input Files

- `Aranjuez_Test_05_Rooms.obj`: room geometry.
- `Aranjuez_Test_02_Doors.obj`: door geometry.
- `Aranjuez_Test_02_Windows.obj`: window geometry.

## Output Folder

- `Assignment_02_Outputs/`: all exported Assignment 2 results.

Main output files include:

- `A2_room_graph_metrics.csv`
- `A2_access_graph_metrics.csv`
- `A2_shortest_paths.csv`
- `A2_street_door_shortest_paths.csv`
- `A2_bottlenecks.csv`
- `A2_bridge_edges.csv`
- `A2_cut_vertices.csv`
- `A2_global_summary.csv`
- `A2_access_graph.json`
- `A2_access_graph.gexf`
- `A2_short_report.md`

## Workflow Summary

1. Load room, door, and window OBJ files.
2. Rebuild rooms as topological cells.
3. Detect room-aperture relations.
4. Build two graphs:
	- room adjacency graph (room-to-room through doors)
	- access graph (rooms, doors, and windows)
5. Compute metrics:
	- Degree Centrality
	- Closeness Centrality
	- Betweenness Centrality
	- Shortest Paths
	- Bridges, Cut Vertices, and Communities
6. Export tables and graph files for analysis and visualization.

## Tools

- Python 3
- Jupyter Notebook
- TopologicPy

## Notes

- The shortest-path analysis in this notebook uses proxy routes in the graph.
- These results support spatial analysis and design interpretation, but they are not a formal egress code certification.

## Author

Arq. David Agudelo  
2026
