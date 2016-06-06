# OpenBudgets.eu Technical Platform

This repository is for the implementation of the OpenBudgets.eu platform (WP4). 

You'll find here:

- The [Issue Tracker](https://github.com/openbudgets/platform/issues) which deals with requirements and tasks for bringing up the platform
- A revised description of the [platform architecture](#platform-architecture)

While the issue tracker has specific areas for action by partners in WP4 (and other work packages, for the purpose of integration), a higher-level view of "product requirements" is captured in the [OpenSpending User Stories](https://trello.com/b/JfUwEUQ2) board. 

OpenSpending supports many use cases, and those of OpenBudgets.eu are a subset. To see *only* user stories for OpenBudgets.eu on this board, you can use Trello's label filter.

# Platform architecture

![OpenBudgets.eu Architecture][https://docs.google.com/drawings/d/1IoetSkV1X8AtGy1NuWtpC1S_nsLT1usn7zU2SdY45Qg/pub?w=960&h=720]

## Overview of components

### OpenSpending Core

#### Packager

A user interface to model and upload data into OpenSpending.

#### Python Client

A tool for command line and 3rd party use for bulk import of Fiscal Data Packages to the Datastore.

#### ETL Pipelines

A suite of pipelines to automate the import of data into OpenSpending.

#### Datastore (flat files)

The "single point of truth" for data in OpenSpending, stored as flat files, and used to load data onwards to specialised databases.

#### Cubes API

An API server for OLAP-style queries over data in OpenSpending.

#### Search API

An API server for text search over data in OpenSpending.

#### Indicators API

An API server providing contectual information for use in user interfaces, such as population, currency, and geographical information.

#### DataMine

A user interface for ad hoc exploration of the OpenSpending database.

#### Explorer

A user interface to search / discover data in the OpenSpending database.

#### Viewer

A user interface to interact with and visualise data in an OpenSpending data package.

#### Custom UIs

A range of customised apps providing specific views onto a subset of the data in OpenSpending.

### OpenBudgets.eu Extensions

#### Custom RDF Pipelines

LinkedPipes-backed data processing pipelines to generate enriched RDF representations of raw source data.

#### Triple Store (staging and production)

Primary storage for RDF data.

#### RDF-based API

API providing access to the data in RDF form.

#### Reverse Proxy Server

A web server to provide a range of features over the OpenBudgets.eu components, such as access control, and URI dereferencing, and access to static outputs from offline data mining.

#### Static Outputs from Offline Data Mining

A set of files generated from offline data mining and analytical processes.

#### Alignment UI

A user interface for matching/linking across code lists.
