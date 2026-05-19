
# Assignment 2 Short Report - Graph Analysis of Aranjuez Model

## Method
The architectural model was represented as two related TopologicPy graphs. The room adjacency graph uses rooms as nodes and door-mediated room-to-room relationships as edges. The access graph uses rooms, doors, and windows as nodes; edges connect each aperture to the room or rooms detected around its centroid. Edges are treated as unweighted for centrality and as centroid-distance weighted for the shortest-path proxy.

## Key Results
- Most directly connected space: **Circulation_011** with degree centrality **0.125**.
- Most globally accessible space: **Circulation_008** with closeness centrality **1.0**.
- Strongest bottleneck / connector: **Circulation_011** with betweenness centrality **0.598224**.
- Longest proxy route to an exterior aperture starts at **Parking_31** and reaches **Window_033** in **59.295304** model units.
- Detected community labels: **0, 1, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 2, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 3, 30, 4, 5, 6, 7, 8, 9**.

## Interpretation
High degree centrality identifies spaces that work as local distributors because they connect to many neighboring rooms through doors. High closeness centrality identifies spaces that are topologically near the rest of the building, which usually indicates strong accessibility and a likely role in circulation. High betweenness centrality marks rooms or apertures that many shortest routes depend on; these elements behave as critical connectors or bottlenecks.

## Spatial Organization
The graph reveals how circulation is structured by the relationship between rooms and apertures rather than by geometry alone. Central rooms and circulation spaces organize movement, while doors with high betweenness indicate thresholds where multiple routes converge. Communities suggest functional or spatial zones, such as clusters of storage rooms, circulation cores, service areas, or repeated room groups. Shortest paths to exterior aperture proxies provide an accessibility reading, not a code-compliant egress certification.

## Why Graph Analysis Is Useful
Graph analysis translates architectural geometry into relational evidence. It helps identify hierarchy, accessibility, connectivity, bottlenecks, and zones that can be hard to compare visually in a complex model. The metrics should be read together with drawings, dimensions, program, and design intent.
