# Field Data Collection
<img src="https://github.com/ivsg-psu/ivsg_master/blob/master/images/FieldDataCollection_cropped.jpg" alt="Field Data Collection" width="1280" height="377">

***
Welcome to the group's repo hub for repos that detail data procedures and data processing codes for field data. Specifically, this repo includes information and codes related to the the collection of data, processing of data, and storage of data. If there is a PROCEDURE that relates to collecting data in the field, then this is the area where the repos of these procedures should be linked.

This is not the section to find information on particular hardware (e.g. the mapping van, P1, the Husky, etc.). Repos and details on the hardware itself can be found in the "Hardware" section. As well, this is not the section to find details or codes on specific data processing steps or the use of data, such as feature extraction, path planning, etc. There are entire sections of the team repo for these topics.

<!-- img src="https://github.com/ivsg-psu/ivsg_master/blob/master/images/PathPlanning_org.png" alt="Field Data Collection Org chart" width="1280" height="150" -->

<!-- TABLE OF CONTENTS -->
# Table of Contents
<details open>
  <summary> Click to see/unsee </summary>

  <ol>
    <li>
      <a href="#safety-procedures">Safety Procedures</a> 
      THese are repos for key safety procedures in common use in the team: testing procedures for autonomous vehicles, checkout procedures for vehicles, etc.
    </li>
    <li>
      <a href="#visualizing-field-data">Visualizing Field Data</a> 
      This includes techniques to plot data using geoplot, animating data, etc.
    </li>
    <li>
      <a href="#gps-related-codes">GPS Related Codes</a> 
      This includes how to set up a GPS base station, setting up the GPS CORS server, etc.
    </li>
    <li>
      <a href="#road-segment-codes">Road Segment Codes</a> 
      This includes examples of importing road networks from OSM / RoadXML / OpenDRIVE;  the RoadSegment library; plotting road segments; etc.
    </li>
    <li>
      <a href="#equipment-operational-procedures">Equipment Operational Procedures</a> 
      Operation and maintenance procedures for: Mapping van, tractor-trailer (VNL300), steer-by-wire racecar (P1), autonomous wheelchair, Husky robot.
    </li>
    <li>
      <a href="#typical-hardware-setups">Typical Hardware Setups</a> 
      Power system setup for shore power functionality, avoiding ground loops, time synchronization methods and codes, real-time computing platforms and the Audesse setup, cabling and connector standards.
    </li>
    <li>
      <a href="#typical-software-setups">Typical Software Setups</a> 
      Typical software systems and deployments used on field data collection. This includes repos for ROS1 deployments, ROS2 deployments, etc.
    </li>
    <li>
      <a href="#data-collection-procedures">Data Collection Procedures</a> 
      ROS setup and introduction, ROS diagnostic interface setup, ROS data recording methods, Raw data parsing, Pushing/pulling data from ROS into databases, Bridging ROS live into MATLAB/Simulink via UDP and SLRT, CANOpen blocksets for Simulink.
    </li>
  </ol>
</details>

<a href="#field-data-collection">Back to top</a>

***

# Safety Procedures

<!-- SAFETY PROCEDURES -->
<details closed> 
  <summary> Click to see/unsee </summary>
  <ul>
    <li> <h2> Lab Safety </h2>
      <a href="https://ehs.psu.edu/sites/ehs/files/psu_lab_electrical_safety_for_modified_or_lab-made_equipment_final_11_18_22.docx">
      Penn State's policy for modified electrical equipment.
      </a>
      <br>
      This EHS document lists policies for using and maintaining electrical equipment with focus on high-voltage safety. Some notes:
      <ul>
          <li> No live electrical work 50 volts or higher is permitted in labs </li>
          <li> 120 volt cords must be disconnected for all electrical servicing. </li>
          <li> Lab personnel are not allowed to handle any physical infrastructure related to building electrical systems, such as fuse boxes. </li>
      </ul>
    </li>
    <li> <h2> Autonomous Vehicle Testing Safety </h2>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_SafetyProcedures_AutonomousRobotTestingProcedureOrdering/wiki">
      FieldDataCollection_SafetyProcedures_AutonomousRobotTestingProcedureOrdering
      </a>
      <br>
      This repo lists safety procedures and test ordering related to the start-up operation of an autonomous vehicle.
    </li>
  </ul>
</details>

<a href="#field-data-collection">Back to top</a>

***

# Visualizing Field Data

<!-- VISUALIZING FIELD DATA -->
<details closed> 
  <summary> Click to see/unsee </summary>
  <ul>
      <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_PlotRoad">
      FieldDataCollection_VisualizingFieldData_PlotRoad
      </a>
      <br>
      Main plotting library supporting core MATLAB functions to plot XY, XYZ, LLA data, including color mapping.
    </li>
      <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_PlotCV2X">
      FieldDataCollection_VisualizingFieldData_PlotCV2X
      </a>
      <br>
      MATLAB tools for plotting CV2X data
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_MapPanAndZoom/wiki">
      FieldDataCollection_VisualizingFieldData_MapPanAndZoom
      <br>      
      <img src="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_MapPanAndZoom/blob/master/MapPanAndZoom_Satellite.png" height="100"   
       width="150" >
      <img src="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_MapPanAndZoom/blob/master/MapPanAndZoom_OSM.png" height="100" 
      width="150" >
      <img src="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_MapPanAndZoom/blob/master/MapPanAndZoom_Streets.png" height="100"       
      width="150" >
      <img src="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_MapPanAndZoom/blob/master/MapPanAndZoom_StreetsDark.png" 
      height="100" width="150" >
      <img src="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_MapPanAndZoom/blob/master/MapPanAndZoom_Landcover.png" height="100" 
      width="150" >
      <img src="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_MapPanAndZoom/blob/master/MapPanAndZoom_Topographic.png" 
       height="100" width="150" >
      </a>
      <br>
      This is code demonstrating MATLAB map plotting, as well as an ability to do synchronized pan and zoom across the figures.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_AnimatedGeoplot/wiki">
      FieldDataCollection_VisualizingFieldData_AnimatedGeoplot
      <br>
      <img 
            src="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_MapPanAndZoom/blob/master/MapPanAndZoom_Satellite.png" 
            height="100"   
            width="150" 
      >      
      </a>
      <br>
      A simple example showing animation of a geoplot in MATLAB, wherein a point on the test track is moved North and the map moves underneath it where 
      point remains centered and seems unmoving. 
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_testTrackImageFromGoogle">      
         FieldDataCollection_VisualizingFieldData_testTrackImageFromGoogle
      </a>
      <br>
      This code produces a VERY high resolution image of the test track by tiling high resolution images obtained by Google Maps API. 
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_VisualizingHighDensityData">      
         FieldDataCollection_VisualizingFieldData_VisualizingHighDensityData
      </a>
      <br>
      This details the code to visualize 2-D high density data.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_StitchingImgFromSmallToBig">   
         FieldDataCollection_VisualizingFieldData_StitchingImgFromSmallToBig
      </a>
      <br>
      This details the code to stitch data of small images into a large image.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_pixels2LLA">   
         FieldDataCollection_VisualizingFieldData_pixels2LLA
      </a>
      <br>
      This details the code to find the coordinate of the brighest point on the geoplot and covert it to LLA coordinate.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_PlotWorkZone">   
         FieldDataCollection_VisualizingFieldData_PlotWorkZone
      </a>
      <br>
      Functions to plot common work zone objects in 2D.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_VisualizingFieldData_LoadWorkZone">   
         FieldDataCollection_VisualizingFieldData_LoadWorkZone
      </a>
      <br>
      This is the repo that loads Work Zone scenario data for the ADS demonstrator project.
    </li>
  </ul>
</details>

<a href="#field-data-collection">Back to top</a>


***


# GPS Related Codes

<!-- GPS RELATED CODES -->
<details closed> 
  <summary> Click to see/unsee </summary>
  <ul>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_GPSRelatedCodes_GPSClass">
      FieldDataCollection_GPSRelatedCodes_GPSClass
      </a>
      <br>
      This is the class library, including both MATLAB and Python codes, to convert from LLA to ENU, ENU to LLA given a specific base station point.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/ivsg_master/wiki/GPS-Base-Station-Calibration">
      GPS Base Station Calibration
      </a>
      <br>
      Information and resources for setting up a GPS Base Station for use in a base/rover setup with Real Time Kinematic (RTK) positioning for 
      centimeter-level accuracy.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_GPSRelatedCodes_GPSBaseServer/wiki">
      FieldDataCollection_GPSRelatedCodes_GPSBaseServer
      </a>
      <br>
      Instructions for setting up a GPS Base Server for use in a base/rover setup with Real Time Kinematic (RTK) positioning for 
      centimeter-level accuracy.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/TrafficSimulators/wiki/Spatial-Coordinate-System">
      Spatial Coordinate System of Simulator
      </a>
      <br>
      This wiki page in the Traffic Simulation repo presents the coordinate systems for describing a point on the surface of the earth, compare the accuracy of various calculations using these coordinate systems, and provide the rationale for choosing a specified sequence of these coordinate systems (with the associated transformations) in the simulation environment built for the NSF CPS “Forgetful Databases” project.
    </li>

  </ul>

  <ul>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_GPSRelatedCodes_ReadingZED-F9PReceiverWithArduino">
      Reading ZED-F9P Receiver with Arduino
      </a>
      <br>
      This repo includes code for reading the ZED-F9P GNSS receiver with Arduino or Teensy microcontrollers.
    </li>

  </ul>

</details>

<a href="#field-data-collection">Back to top</a>


***

# Road Segment Codes

<!-- ROAD SEGMENT CODES -->
<details closed> 
  <summary> Click to see/unsee </summary>
  <ul>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_RoadSegments_RoadSegClassLibrary">
      The Road Segment Class Library
      </a>
      <br>
      Contains information comparing road segment definitions across open file types, defining basic concepts of road segments, defining process for network import of information, etc
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_RoadSegments_SegmentingInMATLAB/wiki">
      FieldDataCollection_RoadSegments_SegmentingInMATLAB
      </a>
      <br>
      A repo to host Dan Fescenmyer's work on road segmentation.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_RoadSegments_ImportingOSMxml/wiki">
      FieldDataCollection_RoadSegments_ImportingOSMxml
      </a>
      <br>
      A repo to demonstrate how to import and plot Open Street Map XML files.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_RoadSegments_ExportingOpenDRIVEfromMATLAB/wiki">
      FieldDataCollection_RoadSegments_ExportingOpenDRIVEfromMATLAB
      </a>
      <br>
      A repo to demonstrate how to export ASAM OpenDRIVE XML files from MATLAB.
    </li>
    <li>
      Logging into Open Street Maps from IVSG:
      <br>
      sbrennan@psu.edu
      <br>
      ConnectedVehicles(+last4digits of Brennan's cell, no spaces)
      <br>      
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/TrafficSimulators_ExportTrafficInfo_ExtractRoadNetworkFromAimsunShapeFile/wiki">
      TrafficSimulators_ExportTrafficInfo_ExtractRoadNetworkFromAimsunShapeFile
      </a>
      <br>
      This details the code in the Traffic Simulation repo area to extract road network information from shapefiles exported from AIMSUN.
    </li>
    <li>
      <a href="https://www.pasda.psu.edu/">
      Pennsylvania Spatial Data Access (PASDA)
      </a>
      <br>
      The PSU-hosted Pennsylvania Geospatial Data Clearinghouse
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_RoadSegments_ExportingRoadxml">      
FieldDataCollection_RoadSegments_ExportingRoadxml
      </a>
      <br>
      A repo to demonstrate how to generate roadxml files.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_RoadSegments_UpdateOSM">      
FieldDataCollection_RoadSegments_UpdateOSM
      </a>
      <br>
      This repo details the procedure to update OSM data, including fixing OSM erros, in particular to fix disconnected roads.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_RoadSegments_ParseXODR">
      FieldDataCollection_RoadSegments_ParseXODR
      </a>
      <br>
      A repo to demonstrate how to parse a XODR file, including creating, editing, and converting between XDOR and MATLAB struct.
    </li>
  </ul>
</details>

<a href="#field-data-collection">Back to top</a>


***

# Equipment Operational Procedures

<!-- EQUIPMENT OPERATIONAL PROCEDURES -->
<details closed> 
  <summary> Click to see/unsee </summary>
  <ul>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_RoadSegments_RoadSegClassLibrary">
      Mapping Van Operation and Maintenance
      </a>
      <br>
      MUST ADD REPO: Battery health checks, vehicle maintenance, sensor maintenance, how to fill gas on vehicles while equipment is running.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_VNL300/wiki">
      FieldDataCollection_VNL300
      </a>
      <br>
      Data collection from the Steer-by-Wire Tractor Trailer, the VNL300 Volvo Day Cab Tractor Trailer. This links to the repo for the tractor-trailer, which primarily includes the processing code for fuel economy analysis related to the NEXTCAR project (2016 to 2020).
    </li>
    <li>
      <a href="http://www.projects.bucknell.edu/Beal_Automotive/">
      Protocols for data collection from P1
      </a>
      <br>
      This links to the website maintained by Prof. Beal for this vehicle
    </li>
    <li>
      <a href="http://www.projects.bucknell.edu/Beal_Automotive/">
      MUST ADD REPO: Protocols for data collection for the autonomous wheelchair
      </a>
      <br>
      Information on how to operate the wheelchair.
    </li>
    <li>
      <a href="http://www.projects.bucknell.edu/Beal_Automotive/">
       MUST ADD REPO:Protocols for data collection with the Husky Robot
      </a>
      <br>
      Information on how to operate the Husky.
    </li>
  </ul>
</details>

<a href="#field-data-collection">Back to top</a>

***

# Typical Hardware Setups

<!-- TYPICAL HARDWARE SETUPS -->
<details closed> 
  <summary> Click to see/unsee </summary>
  <ul>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_TypicalHardwareSetups_PowerDistribution_ShorePowerArchitecture">
      FieldDataCollection_TypicalHardwareSetups_PowerDistribution_ShorePowerArchitecture
      </a>
      <br>
      Power architecture to enable "shore power" options, e.g. power sourced from batteries that are switchable to wall power or other sources.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_VNL300/wiki">
      MUST ADD: Ground loop
      </a>
      <br>
      How to avoid ground loops
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_TypicalHardwareSetups_TimeSync_ArduinoUsingGPSPPS/wiki">
      FieldDataCollection_TypicalHardwareSetups_TimeSync_ArduinoUsingGPSPPS
      </a>
      <br>
      A repo for the Arduino code that is used to synchronize the Arduino's internal clock to an external GPS's PPS signal, then use that synchronization to create external triggers for other sensors at designated rates, e.g. 25 pulses per second for triggering a camera.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_TypicalHardwareSetups_EncoderCodes_ReadingEncodersWithTeensy">
      FieldDataCollection_TypicalHardwareSetups_EncoderCodes_ReadingEncodersWithTeensy
      </a>
      <br>
      A repo for the Teensy 4.1 code that is used to measure counts from a high resolution US Digital Encoder.
    </li>
    <li>
      <a href="http://www.projects.bucknell.edu/Beal_Automotive/">
      MUST ADD: Real-time computing and the Audesse
      </a>
      <br>
      Information on real-time platforms and setting up the Audesse.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_TypicalHardwareSetups_CablesAndConnectors_Standards">
      FieldDataCollection_TypicalHardwareSetups_CablesAndConnectors_Standards
      </a>
      <br>
      A listing of the common cable and connector standards used across platforms. For example, this repo tells you: what connector should I use for CAN, for a trigger signal, for power connections, etc.?
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_TypicalHardwareSetups_V2x_ComsigniasDSRCplusCV2X">
      FieldDataCollection_TypicalHardwareSetups_V2x_ComsigniasDSRCplusCV2X
      </a>
      <br>
      Repo including test codes for Comsignia's DSRC/CV2x radio units.
    </li>
    <li>
     MUST ADD: Hardware Platforms
      </a>
      <br>
      Audesse
      </a>
      <br>
      Raspberry Pi
    </li>
  </ul>
</details>

<a href="#field-data-collection">Back to top</a>

***

# Typical Software Setups

<!-- TYPICAL SOFTWARE SETUPS -->
<details closed> 
  <summary> Click to see/unsee </summary>
  <ul>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_TypicalSoftwareSetups_ROS2deployments">
      FieldDataCollection_TypicalSoftwareSetups_ROS2deployments
      </a>
      <br>
      ROS2 deployments and sensor integrations, with focus on field data collection (mapping van, roadside computers, etc.).
    </li>
  </ul>
</details>

<a href="#field-data-collection">Back to top</a>

***

# Data Collection Procedures

<!-- DATA COLLECTION PROCEDURES -->
<details closed> 
  <summary> Click to see/unsee </summary>
  <ul>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_RoadSegments_RoadSegClassLibrary">
      MUST ADD: ROS setup and introduction
      </a>
      <br>
      How to set up ROS for IVSG, typical usage examples, learning.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_DataCollectionProcedures_ROSDiagnotsticInterface">
      FieldDataCollection_DataCollectionProcedures_ROSDiagnotsticInterface
      </a>
      <br>
      How to set up watchdog and health monitoring in ROS.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_RoadSegments_RoadSegClassLibrary">
      MUST ADD: ROS data recording methods
      </a>
      <br>
      How to start and end collection process, record data, and transmit data - includes code that shows how to parse bag files automatically into 1 GB file size.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_DataCollectionProcedures_RawDataParsing">
      FieldDataCollection_DataCollectionProcedures_RawDataParsing
      </a>
      <br>
      How to parse the raw *.bag files into .csv format then read into MATLAB for further processing. 
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_DataCollectionProcedures_PushingDataToDatabase">
       Pushing data from ROS into databases.
      </a>
      <br>
      How to parse the raw *.bag files into raw data database.
    </li>
    <li>
      <a href="http://www.projects.bucknell.edu/Beal_Automotive/">
      MUST ADD: Bridging ROS live into MATLAB/Simulink via UDP and SLRT
      </a>
      <br>
      How to push data live into SLRT.
    </li>
    <li>
      <a href="http://www.projects.bucknell.edu/Beal_Automotive/">
      MUST ADD: CANOpen blocksets for Simulink
      </a>
      <br>
      How to access CAN data from within Simulink
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_DataCollectionProcedures_DataTransferWithDMS">
      FieldDataCollection_DataCollectionProcedures_DataTransferWithDMS
      </a>
      <br>
      This repo details the work to push to and pull data from the PennDOT DMS.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_DataCollectionProcedures_AutomatingDataTransferToDMSUsingCommandLine">
      FieldDataCollection_DataCollectionProcedures_AutomatingDataTransferToDMSUsingCommandLine
      </a>
      <br>
      This repo details the work to automate the data transfer with DMS using command line.
    </li>
    <li>
      <a href="https://github.com/ivsg-psu/FieldDataCollection_DataCollectionProcedures_StitchingImagesToVideo">
     FieldDataCollection_DataCollectionProcedures_StitchingImagesToVideo
      </a>
      <br>
      This repo details the work to stitch images into a video.
    </li>
  </ul>
</details>

<a href="#field-data-collection">Back to top</a>




# ITEMS TO ADD

## Digital Twin Codes (Summer '21)



