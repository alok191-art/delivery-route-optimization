# Delivery Route Optimization
## Overview
This project develops a delivery route optimization workflow for a central warehouse serving multiple customer locations.

The objective is to construct feasible delivery routes while considering customer demand and vehicle capacity, then improve the routes to reduce total travel distance.

## Objectives
- Generate and analyze customer delivery locations
- Divide customers into geographic zones using SQL
- Calculate distances between delivery locations
- Construct capacity-constrained delivery routes
- Compare optimized routes with a baseline route
- Improve routes using the 2-opt algorithm
- Visualize optimized routes on an interactive map

## Tools & Technologies
- Python
- Pandas
- NumPy
- SQLite / SQL
- Faker
- Folium

## Project Workflow
Customer Data Generation → SQL Zoning → Distance Matrix → Baseline Route → Capacity-Constrained Route Construction → 2-opt Improvement → Route Comparison → Interactive Map

## Methodology
### 1. Customer Data Generation
Generated 50 customer locations around a central warehouse using latitude, longitude, and delivery demand.

### 2. Geographic Zoning
Used SQLite and the SQL `NTILE()` window function to divide customers into five geographic zones.

### 3. Distance Calculation
Calculated pairwise distances between the warehouse and customer locations using the Haversine formula.

### 4. Route Construction
Constructed delivery routes using a Nearest Neighbor approach while respecting a vehicle capacity of 40 demand units.

### 5. Route Improvement
Applied the 2-opt algorithm to improve the generated routes and reduce travel distance.

### 6. Visualization
Created an interactive Folium map showing the central warehouse, customer locations, and optimized delivery routes.

## Key Output
- Baseline route distance
- Optimized route distance
- Distance saved
- Percentage reduction in travel distance
- Vehicle-wise route assignments and loads

## Repository Contents
- `Delivery_Route_Optimisation.ipynb` — Complete route optimization workflow

## Note
The customer dataset is synthetically generated for analytical and algorithmic demonstration. The calculated distances represent geographic straight-line distances and do not account for actual road networks or traffic conditions.
