# IVSG Table of Contents

<!---
ivsg-psu/ivsg-psu is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

Welcome to the Intelligent Vehicles and Systems Group (IVSG) wiki, the core codes used by Prof. Sean Brennan (sbrennan AT psu DOT edu) within the Mechanical Engineering department at Penn State University, University Park campus. This page is basically a launch site toward other repos, to organize activities within the team and provide a hub where people can see how and where their project fits in.

## [Position Postings!](https://github.com/ivsg-psu/PositionPostings)

Position postings for the lab. We are regularly in search of:

* Volunteers who want to learn new skills (design, build, experimentation, coding, automation)
* Hourly wage undergrads who can offer specific skills (CAD, machining, programming, etc.)
* Grad students with scholarships, assistancships, or similar self-funding 
* Highly qualified grad students for specific projects

***

The technical sub-topics are organized as follows:
![Main_Page_Bubble_Diagram](https://github.com/ivsg-psu/ivsg_master/blob/master/Main_Page_Bubble_Diagram.gif)

## [Field Data Collection](https://github.com/ivsg-psu/FieldDataCollection)

Field Data Collection includes repositories and procedures focused on acquiring, organizing, and validating field data from physical vehicles and external data sources. These include:

* Vehicle and platform safety procedures for autonomous field testing
* Field data visualization tools for quick inspection and validation (geoplots, animations)
* GPS infrastructure setup, including base stations, CORS servers, and time synchronization
* Road network data ingestion and handling from OSM, RoadXML, and OpenDRIVE formats
* Operational procedures for field platforms (mapping van, P1 racecar, tractor-trailer, Husky robot, autonomous wheelchair)
* Standardized hardware configurations for field deployments (power systems, grounding, cabling, time sync)
* Typical software deployments for field data collection (ROS1/ROS2 systems and configurations)
* ROS-based data collection pipelines, diagnostics, logging, parsing, and database integration

## [Feature Extraction](https://github.com/ivsg-psu/FeatureExtraction)

This includes algorithms primarily, with specific focus on how to process large data sets and extract features from this. These include:

* Processing GPS data to remove data drops
* Kalman Filtering examples
* Data clustering algorithms
* Path extraction from trajectories
* Road edge extraction from LIDAR data

## [Path Planning and Geometric Tools for Maps](https://github.com/ivsg-psu/PathPlanning)

Path Planning and Geometric Tools for Maps includes algorithms to extract paths from traces of cleaned GPS data, plan paths through obstacle fields and in network graphs, tools to generate random maps, and geometric tools. Specific subsections include:

* Averaging methods for repeated traversals of the same lanes
* Extraction of individual lanes for multi-lane roads with lane-changes
* Determination of decision points given trajectories
* Geometric calculation of visibility graph methods

## [Databases of Vehicle and Road Measurements](https://github.com/ivsg-psu/ivsg_master/wiki/Databases)

Databases of Vehicle and Road Measurement repos deal with the process of storing and retrieving data from databases. They include:

* Setting up database access (PostGres) within MATLAB
* Schema used to store road information within databases
* Pulling data out of databases for use in simulations

## [Traffic Simulators](https://github.com/ivsg-psu/ivsg_master/wiki/Traffic-Simulators)

Traffic Simulator repos include algorithms and codes that enable simulation of large numbers of vehicles on road networks, e.g. traffic simulations. Codes include:

* Comparisons of different traffic simulations tools - e.g. why we chose AIMSUN
* Getting started with AIMSUN
* Interacting with AIMSUN via ROS in non-real-time modes
* Real-time interaction with AIMSUN
* Import of real-world road information into AIMSUN
* Calibration of model parameters

## [Vehicle and Sensing Hardware](https://github.com/ivsg-psu/Hardware)

Vehicle and Sensing Hardware repos include codes, diagrams, and CAD models for our vehicles, including:

* Mapping van
* P1 - the by-wire racecar
* The steer-by-wire tractor trailer
* The wheelchair
* The RC car builds
* Simulator hardware builds

## [Vehicle Simulations](https://github.com/ivsg-psu/ivsg_master/wiki/Vehicle-Simulations)

Vehicle Simulation repos include simulation tools for vehicle behaviors including:

* Vehicle chassis models
* Powertrain models
* Driver models
* Friction estimators
* State estimators

## [Driving Simulators](https://github.com/ivsg-psu/ivsg_master/wiki/Driving-Simulators)

Driving Simulator repos include code for interacting with a driving simulator including:

* Choosing a simulation environment for visualization (what is out there?)
* Setting up Blender and Unity for visualization
* Automated road generation in Blender
* Importing real-world geometric information
* Hardware interfaces to the driving simulator

## [Publications](https://github.com/ivsg-psu/Publications)

Repos for code sets to suport publications. These include:

* Theses
* Journals
* Conferences
* Reports

## [Classes](https://github.com/ivsg-psu/Classes)

Repos for Dr. Brennan's course offerings. These include:

* Automatic grading tools
* ME 452 - Vehicle Dynamics

## [Errata](https://github.com/ivsg-psu/Errata)

Odds and Ends repos include codes and items that just don't really fit anywhere else. These include:

* Planned publications (scratch area)
* The group webpage repo
* Tutorials
* Games and challenges for coding practice within the team
* Copy and paste items
* [Errata_Private](https://github.com/ivsg-psu/Errata_Private): This is a private repository for Errata. It contains private information, such as GitHub IDs of IVSG team.
