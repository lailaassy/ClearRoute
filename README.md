# ClearRoute
### Accessible navigation for people with low vision

**C++ · OpenStreetMap · OpenMP · ECE297, University of Toronto**

Built by **Laila Assy, Prithika Paraneetharan, and Daisy Grachev**.

ClearRoute is a mapping project built around a simple question: how can navigation be easier to use for people with low vision? We focused on readable maps, forgiving search, spoken directions, and a less cluttered interface.

![ClearRoute map with floating search controls and navigation buttons](clearroute-interface.png)

## Designed around accessibility

### A clearer map
High-contrast map styling helps distinguish roads, water, buildings, and points of interest. Our design explores the Okabe–Ito palette and differences in brightness, rather than relying on colour alone.

![High-contrast map showing roads, buildings, water, and points of interest](high-contrast-map.png)

### Search that gives you some room
Partial street names, abbreviation expansion, word-order-independent matching, and fuzzy matching help users find a destination without needing to type an exact name. Text-to-speech provides an audio channel for map labels and navigation instructions.

![Search suggestions for a partially entered street name](search-autocomplete.png)

### One trip, multiple stops
Users can add, reorder, and remove stops in one workflow, with an organized overview and arrival cues along the route.

![ClearRoute interface for planning a trip with several stops](multiple-stops.png)

## Under the hood

- **Pathfinding:** Dijkstra’s algorithm and A* for finding routes through a road network.
- **Route optimization:** a greedy initial route followed by local improvements, including swaps, 2-opt, relocation, and double-bridge perturbations.
- **Parallel computation:** OpenMP splits repeated preprocessing work across threads.

## What we explored next

Our presentation also explores indoor navigation, streetlight information, and voice input. Incorporating lighting into route cost is a future direction; it is not presented here as a completed routing feature.

## About this repository

This repository is a visual overview of our ECE297 team project. The screenshots come from our final presentation. It contains project documentation rather than the course source code.

[Connect with Laila](https://www.linkedin.com/in/laila-assy/) · [Email](mailto:laila.assy@outlook.com)
