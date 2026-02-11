# IVSG Table of Contents

<!---
ivsg-psu/ivsg-psu is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

Welcome to the Intelligent Vehicles and Systems Group (IVSG) wiki, the core codes used by Prof. Sean Brennan (sbrennan AT psu DOT edu) within the Mechanical Engineering department at Penn State University, University Park campus. This page is basically a launch site toward other repos, to organize activities within the team and provide a hub where people can see how and where their project fits in.

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

## [Vehicle Simulations](https://github.com/ivsg-psu/vehicleSimulations)

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


## [Position Postings!](https://github.com/ivsg-psu/PositionPostings)

Position postings for the lab. We are regularly in search of:

* Volunteers who want to learn new skills (design, build, experimentation, coding, automation)
* Hourly wage undergrads who can offer specific skills (CAD, machining, programming, etc.)
* Grad students with scholarships, assistancships, or similar self-funding 
* Highly qualified grad students for specific projects

Specific sub-projects include:\

### Hardware Development to Support Connected Vehicle-to-X (CV2X) Systems
Requirement: need to have valid Drivers License and ability to get to mapping van located at the Transportation Research Building south of BJC

Project Goal: Restore wheel encoder functionality on the mapping vehicle through systematic inspection, repair, documentation, testing, and (if necessary) redesign of the encoder mounting and integration. 

Subtasks include:

1. Finish construction of electronics that go into data collection boxes (6 of them) at the Penn State test track
    * Soldering the Arduino board and make it weather-proof
    * Mount the soldered board into the cabinets
    * Keep Track Boxes repo updated with hardware purchases, changes, edits, photos, etc.
    * Update the pole status diagram (power status and device status)
    * Create wiring diagram for device connection within the cabinets
    * Track the conduit installation process at the track
2. Get communication of data working from boxes to cloud services
3. Collect on-vehicle connectivity data using specially-wired systems installed in our mapping van
    * Test the Radar power and the ROS 1 code Yao has
    * Need to update Radar driver to make it compatible with ROS 2
    * Collect baseline GNSS-only runs (no V2X fusion) for different lane centerlines
    * Collect multi-vehicle runs with BSM exchange enabled
    * Log raw GNSS, IMU, and BSM data with time separately and jointly within ROS
4. Collect roadside sensor data that tracks vehicles going by
    * Record baseline LiDAR-only detection and tracking runs
    * Collect data with V2V communication enabled
    * Capture occlusion-heavy scenarios (curves, intersections, cut-ins)
    * Log vehicles entering and exiting LiDAR field of view


### Wheel Encoder Repair, Redesign, and Validation
Requirement: need to have valid Drivers License and ability to get to mapping van located at the Transportation Research Building south of BJC

Project Goal: Restore wheel encoder functionality on the mapping vehicle through systematic inspection, repair, documentation, testing, and (if necessary) redesign of the encoder mounting and integration. 

Subtasks
1. Component Identification and Procurement (Buy a new cable) Estimated time: 1 to 2 days
    * Identify the exact model and key specifications of the existing wheel encoder, along with all associated cabling.
    * Determine the correct replacement cable and connector types if the current ones are damaged or incompatible.
    * Share part numbers, vendor links, estimated costs, and availability with Dr. B and Aneesh for approval before purchase.
2. Documentation of Existing Encoder System (Make lists and photos of parts) Estimated time: 1 to 2 days
    * Create a complete parts list for the current encoder system, including the encoder, cables, connectors, mounting brackets, fasteners, and any protective components.
    * Take clear photographs and write short explanations showing how the encoder is mounted and how the cable is routed on the vehicle.
    * Organize and upload this documentation to the relevant GitHub repository so it is easy for others to follow later.
3. Initial Repair and Short-Term Restoration Investigation (Guess next repair) Estimated time: 1 to 2 days
    * Inspect the encoder, cabling, and mounting hardware to identify likely points of failure.
    * Decide which components can be repaired versus which ones need replacement in order to restore basic encoder functionality as quickly as possible.
4. Mechanical Mounting and Design Investigation (Find what other people do) Estimated time: 1 to 2 days
    * Evaluate whether the current encoder mounting approach is appropriate for the operating conditions of the mapping vehicle.
    * Identify alternative mounting concepts or commercial solutions that may improve reliability.
5. CAD Updates (Update our drawings) Estimated time: 1 to 2 days
    * Update existing CAD models of the encoder mounting assembly and create new ones if documentation is missing (should not be).
    * If modifications are required, generate revised CAD drawings and updated part lists. (again, not expecting this to be needed)
    * If new mounting concepts are identified, create preliminary CAD designs and supporting documentation for review.
6. Fabrication and Repair Execution (Build) Estimated time: 1 to 2 weeks
    * Perform mechanical repairs or modifications to the encoder mounting assembly.
    * Fabricate new parts as required using available machine shop resources or external vendors.
    * Track costs and fabrication feasibility for proposed solutions.
7. Encoder Assembly and Vehicle Installation (Install) Estimated time: 1 to 2 days
    * Assemble the encoder system, including mounting hardware and cabling.
    * Install the encoder assembly on the mapping vehicle.
8. Testing and Validation (Drive and test) Estimated time: 1 to 2 days
    * Perform low-speed functional tests in a parking lot to confirm basic operation.
    * Conduct medium-speed testing at the test track after successful low-speed validation.
    * Perform highway-speed testing once prior tests confirm reliable operation.
    * Verify encoder performance across all operating conditions and document results.
9. Documentation and Reporting (write it down) Estimated time: 1 to 2 days
    * Document all repairs, design changes, test procedures, and test results.
    * Update repository documentation to reflect the final configuration and lessons learned.
    * If alternative designs were explored, include design summaries, part lists, vendor information, and cost estimates for future consideration.

Final Expected Outcome
A fully documented, tested, and operational wheel encoder system suitable for reliable use on the mapping vehicle, with clear records enabling future maintenance, redesign, or replication.


### Mapping Vehicle Operations, Sensor Installation, and Field Support

Project Goal: Support safe, reliable operation of the mapping vehicle through sensor installation and testing, vehicle readiness checks, field experiment support, and documentation during data collection activities.

Subtasks
1. Mapping Vehicle Familiarization and Safety Preparation
    * Become familiar with the mapping vehicle layout, onboard systems, and safety procedures.
    * Review vehicle operation guidelines, lab safety protocols, and field testing expectations.
    * Assist with pre-drive safety and readiness checklists prior to any data collection activity.
2. Sensor Installation and Physical Integration
    * Assist with the physical installation of onboard sensors, including Ouster LiDAR, wheel encoders, and supporting hardware.
    * Support mounting, alignment, fastening, and cable routing to ensure secure and repeatable installations.
    * Verify that sensor installations meet basic mechanical stability and safety requirements.
3. Sensor Testing and Verification
    * Assist with initial power-on checks and basic functional verification of installed sensors.
    * Support test procedures to confirm sensor outputs are being generated correctly prior to field operation.
    * Help identify and report issues related to mounting stability, cabling, or sensor performance.
4. Mapping Vehicle Operation and Driving Support
    * Support driving of the mapping vehicle during approved data collection runs (Driver’s license required).
    * Support safe operation of the vehicle during low-speed, test-track, and on-road data collection.
5. Field Experiment Support
    * Assist during field experiments by helping set up equipment, monitor sensors, and track experiment progress.
    * Support real-time checks of sensor status during data collection.
    * Assist with troubleshooting simple issues encountered during field operations.
6. Documentation and Reporting
    * Document sensor installation procedures, vehicle configurations, and field-testing setups.
    * Record issues encountered during field operations and the steps taken to resolve them.
    * Update repository or shared documentation with notes, photographs, and procedural updates to support repeatability.

Expected Outcome
A mapping vehicle that is consistently prepared for data collection, with properly installed and tested sensors, safe and efficient field operations, and clear documentation enabling repeatable experiments and smooth onboarding of new team members.


### Data Pipeline Testing, Debugging, and Documentation

Project Goal: Support the verification, testing, debugging, and documentation of the existing data pipeline used to convert raw sensor data into clean, time-aligned, and analysis-ready datasets.

Subtasks

1. Pipeline Familiarization and Conceptual Understanding
    * Study the existing data pipeline architecture and processing flow.
    * Understand the role of each major stage in the pipeline (raw data ingestion, cleaning, time alignment, merging).
    * Review existing code, documentation, and diagrams to develop a conceptual understanding of the system.
2. Pipeline Debugging and Incremental Improvement
    * Assist with debugging issues discovered during testing.
    * Modify or extend existing code under guidance to improve robustness or clarity.
    * Ensure changes do not break existing functionality.
3. Documentation and Knowledge Transfer
    * Document the full data pipeline step-by-step, aligned with the actual code behavior.
    * Create clear explanations of each processing stage, including inputs, outputs, and assumptions.
    * Update repository documentation with diagrams, flowcharts, and usage notes.
    * Record known limitations, edge cases, and troubleshooting tips.


Expected Outcome

A well-tested and well-documented data pipeline, with clearly explained processing stages, verified behavior on real datasets.


### GPS Base Station Setup, Integration, and Documentation

Project Goal: Assist with the setup, configuration, testing, and documentation of a GPS base station used to support high-accuracy positioning for mapping experiments.

Subtasks

1. System Familiarization and Background Study
    * Learn the purpose and role of a GPS base station in high-accuracy positioning and mapping.
    * Review existing documentation, diagrams, and code related to the current base station setup.
    * Become familiar with key components, including the Raspberry Pi, RTK Express unit, antennas, and network interfaces.
2. Physical Assembly of the Base Station
    * Assist with the physical assembly of the existing GPS base station hardware.
    * Verify that hardware components are securely installed and ready for operation
3. Raspberry Pi and Hardware Configuration
    * Assist with configuring the Raspberry Pi used in the base station.
    * Verify communication between the Raspberry Pi and the RTK Express unit.
4. ROS Setup and Software Integration
    * Learn and assist with setting up ROS nodes related to GPS data handling.
    * Help configure ROS launch files, parameters, and logging settings for the base station.
    * Verify that GPS data is correctly published and accessible within the ROS environment.
    * Assist with troubleshooting ROS-related configuration or communication issues.
5. Base Station Initialization and Testing
    * Assist with initializing the GPS base station and verifying correct operation.
    * Help confirm that correction data is being generated and transmitted as expected.
6. Deployment of a New GPS Base Station
    * Assist with setting up a new GPS base station at a designated location.
    * Assist with diagnosing hardware, software, or communication issues encountered during setup or testing.
7. Documentation and Knowledge Transfer
    * Document the full base station setup process step-by-step.
    * Create clear assembly instructions, configuration notes, and troubleshooting guides.
    * Update repository documentation with photographs, diagrams, and usage instructions.

Expected Outcome
A functional and well-documented GPS base station system, with clear setup procedures, verified operation, and documentation that enables future students to deploy, maintain, and troubleshoot the system efficiently.


### MATLAB Code Cleanup, Data Processing, Visualization, and Documentation

Project Goal: Support the maintenance, cleanup, debugging, and documentation of existing MATLAB code repositories used for data processing, analysis, and visualization in mapping and vehicle research.

Subtasks
1. Repository Familiarization
    * Review existing MATLAB repositories to understand their structure, purpose, and workflows.
    * Learn how data flows through the code, from raw inputs to processed outputs.
2. Code Cleanup and Organization
    * Improve code readability by organizing scripts and functions.
    * Standardize variable naming, comments, and formatting where appropriate.
    * Remove unused or deprecated code under guidance.
    * Ensure scripts and functions follow consistent structure and conventions.
3. Visualization and Plotting
    * Improve existing plotting scripts for clarity and usability.
    * Assist with creating new visualizations for debugging, validation, or presentation purposes.
    * Ensure plots are well-labeled and suitable for documentation or reports.
4. Debugging and Testing
5. Documentation and README Updates
    * Update README files with clear usage instructions and examples.
    * Document key functions, inputs, outputs, and assumptions.
    * Add inline comments where clarity is needed.
    * Create simple workflow guides to help new users understand how to run the code.

Expected Outcome
Cleaner, more robust, and better-documented MATLAB code repositories, with improved visualization tools and clearer workflows that support ongoing research and onboarding of new students.