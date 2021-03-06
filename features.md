---
layout: default
title: Features
description: Features of grano which have already been implemented.
#menu_parent: about/index.md
permalink: features/
---

Grano is a rapidly developing open source software project. This page is intended as a guide of both existing features and an agenda of functions that we're planning to work on in the future.

# Existing features

Some of the key features of the core engine as well as some extensions are listed here.

## Backend

* Social **network data storage** based on the Postgres database backend.
* **Multi-tenancy** based on projects, each describing a separate network.
* **Revisions** for property data of each entity and relationship in the database.
* User-editable **data [schemata](/docs/schema)** (i.e. property definitions) for entities and relationships.
* Read/write **web API** exposing all system elements as REST resources.
* Project-level **access control** for users.
* **Plugin interface** to allow modular extensions of the core software.
* File uploads and **bulk data import** from CSV files.
* **OAuth login** with support for Twitter, Facebook and GitHub.
* Asynchronous **background processing** support.


## User Interface

* AngularJS-based user interface for **managing and exploring grano projects**.
* Support for project creation, schema editing and permissions management.
* Editing entities and relations.
* Bulk data import helper for CSV files.

## Extensions

For more information, see [the extensions page](/extensions).

* ElasticSearch-based full-text search and faceting support.
* OpenRefine entity name reconciliation endpoint (Freebase API emulation).
* OpenCorporates reconciliation client service to import company information.

# Development Roadmap

This roadmap details some of the planned functionality for grano over the next few months. It is intended to give a high-level overview, while detailed descriptions and discussion is publicly available on the [issue tracker](https://github.com/granoproject/grano/issues).

## Improved user interface
* Testing with non-technical users.
* Workflow: published vs. draft objects for the Poderopedia use case.
* Bulk editing and adding of entities and relations for manual entry [Poderopedia use case](http://poderopedia.org/).
* Internationalisation of the interface and localisation to Spanish
* Various items: featured entities; entity images; WYSIWYG text editing

## Sources and data provenance
* Managing sources as entities in their own right, with explicit metadata on trust levels.
* Filtering data by source trust levels.

## Query and analytical capabilities
* Conduct a workshop to determine typical queries in journalistic settings. 
* Develop a custom query language or tie in an existing tool like Neo4J.
* Provide a simple, non-visual query builder and results interface for analysis. Research existing query builders and re-use if possible.
* Determine when recursive query ability (i.e. shortest paths) and graph metrics (e.g. centrality, betweenness) are journalistically useful.
* Explore the implementation of pre-defined queries (i.e. red flags for corruption based on entity/relation interlock): how much metadata would be required?

## Data visualisation
* Build a custom network map builder, oriented along the lines of the [LittleSis map tool](http://littlesis.org/map/101) - this should be based on the existing grano-explorer.
* Consider re-use of Poderopedia's analytical visualisations, especially the [simple D3 tool](http://poderopedia.github.io/panama-network/).
* Explore integration of time-based visualisations, based on [CargoGrafias](http://cargografias.org/). 

## Grano SDK
* Template repository for grano extensions; with documentation on how to develop plugins with their own API and data model.
* Template for front-end news apps with entity and relationship profiles (like [MachtVZ](http://machtvz.okfn.de/) and [OpenInterests.eu](http://openinterests.eu/)).
* Consider developing a JavaScript client library.

## Text mining and entity extraction
* Support entity extraction service based on the entities present in a specific grano project, ideally based on [Stanford NER](http://nlp.stanford.edu/software/CRF-NER.shtml).
* Explore re-use and development of stand-alone tools for manual/computer-assisted relationship extraction from news content (MMA Dexter?).

## Activity feeds / narrative relationships
* Prototype narrative connections between entities, as shown in [this mockup](http://opendatalabs.org/misc/demo/grano/_mockup/)
* Following feeds and customised timelines.
* Generate narrative updates from entity/relationship CRUD operations.

## Software as a service
* Work out a partnership with a commercial organisation to operate a hosted instance of grano.
* Develop a revenue model for the service.
