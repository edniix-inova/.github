# Fleet Oriented Enhancement for Controls and Strategies - FOrECaSt
**FOrECaSt** is a framework to support simulation and development of control strategies as an open-source architecture. Two areas are central to the framework:
* **Traffic Simulation**:
  To support the generation of large-scale synthetic data and the development and evaluation of controls features. Traffic simulation is supported by the use of [SUMO - Simulation of Urban Mobility](https://www.eclipse.org/sumo/).
* **Knowledge graph**:
  To efficiently manage and analyze large-scale data. Knowledge graphs are implemented as a graph databases using the [Neo4j graph database](https://neo4j.com/).

## GitHub Development Process.
* A PowerPoint presentation with some guidelines about the use of this repository: [Git Development Process](https://github.ford.com/RDEConnectedPTCtrl/DrivingProfiling/blob/master/sw_ref/DevProcess/GitDevProcess.pptx)

* More information about the use of GitHub can be found in the [Software Development Ecosystem - Github](https://azureford.sharepoint.com/sites/SDE/SitePages/GitHub.aspx) SharePoint.

:question: To suggest changes in the structure of the repository please raise an **Issue** by clicking [here](https://github.ford.com/FOrECaSt/Fleet_Control_Framework/issues/new/choose) and assign (right pane) to any of the following team members:
  * :love_letter: [Mohit Yadav - MYADAV5](https://github.ford.com/MYADAV5)
  * :love_letter: [Eduardo Pérez Guzmán - PGUZMAN4](https://github.ford.com/PGUZMAN4)

## Repository Folder Structure
Some general explanation around FOrECaSt and its use can be found in the [FOrECaSt's Wiki](https://github.ford.com/FOrECaSt/Fleet_Control_Framework/wiki). *-Currently under development-*

* **containers**:
  Docker files for creating necessary images. More information in the directory's [README](containers/README.md).

* **docs**:
  Source files to create the project's documentation.

* **env**:
  Main programing language used in FOrECaSt is **Python**. This folder contains the necessary files to create python 
  virtual environments. See [here](env/README.md) for more information. For questions on how to get and use Python at 
  Ford? Please visit the [Python Center of Excellence](https://azureford.sharepoint.com/sites/CustomersML/SitePages/Python-CoE.aspx).

* **ext_dep**:
  This folder contains YAML files (.yml) to add required external applications, packages and data in the way it is required for FOrECaSt to work. Main dependencies include:
  * SUMO traffic simulation.
  * Neo4j graph database.
  * RabbitMQ messaging broker.
  * Java SE platform.
  * Open Street Map data.
  * SRTM elevation data.

  External dependencies are maintained through the [ext_dep_unix](https://github.ford.com/FOrECaSt/Fleet_Control_Framework/tree/ext_dep_unix) branch committed in Git-LFS. (Currently only POSIX)

* **gvs**:
  The content of this folder describes the main building blocks of FOrECaSt mapping the On-Road Simulation Framework based on SAE J3049, which is a recommendation for Ground Vehicle Simulation (GVS).

  <img src="images/onroadsimulation.png" width="100%">

* **main**:
  Python scripts that accomplish a specific task using the subpackages in this Repository. For example, 
  initialization of the knowledge graph.

* **tests**:
  We currently use pytest to run unit- and integration tests. 

* **utilities**:
  Scripts supporting some specific tasks not part of the main framework structure.

* **visualization**:
  Supporting scripts for dashboard generation and visualization of results.
