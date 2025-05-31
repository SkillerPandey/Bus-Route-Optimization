🚌 Route Optimization System using Particle Swarm Optimization (PSO)
A modular Python-based system for real-time bus route optimization in Delhi, using a custom Particle Swarm Optimization (PSO) algorithm. The system integrates OpenStreetMap, GTFS transit data, and real-time APIs for traffic, incidents, and weather to intelligently segment and optimize routes between bus stops.
🚀 Features

Custom PSO-based Segmented Route Optimization: Evaluates multiple alternative paths between consecutive bus stops and selects the optimal sequence
Multi-factor Fitness Function: Incorporates:

Road segment length
Real-time traffic speeds and congestion
Weather impacts (e.g. rain, wind, temperature)
Traffic incidents and road closures


Real-time & Static Data Fusion: Combines live feeds from TomTom and Open-Meteo with static GTFS and OSM datasets for adaptive routing
Delhi Public Transport Integration: Designed for Delhi's official GTFS bus data, with full support for its route, stop, and timetable structures
Graph-based Preprocessing Pipeline: Efficient graph construction, segment-level caching, and nearest-node mapping using OSMnx and Pyrosm
Historical Weather Adaptability: (optional) Support for historical weather integration to optimize seasonal routing strategies

📊 Data Sources
🔴 Real-time APIs

TomTom Traffic & Incident APIs → https://developer.tomtom.com

Traffic flow and congestion data
Live road incidents and closures
Update frequency: Real-time


Open-Meteo Weather API → https://open-meteo.com/

Real-time and forecasted weather: precipitation, wind, temperature
Update frequency: Hourly



🟡 Static Datasets

Open Transit Delhi – Static Bus Data → https://otd.delhi.gov.in/data/static/

Route shapes, stops, timetables
Format: GTFS
Size: ~25–40 MB


Open Transit Delhi – Real-time Bus Positions → https://otd.delhi.gov.in/data/realtime/

Live vehicle tracking
Used optionally for route validation
Size: ~50–100 MB


OpenStreetMap PBF Data

Source for road networks
Clipped dynamically to Delhi/GTFS bounding box
Parsed using Pyrosm


Open-Meteo Historical Weather Data (optional)

10 years of Delhi weather history
Used to analyze long-term weather influence on routing
Size: ~15–30 MB
