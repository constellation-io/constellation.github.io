---
layout: default
title: Concepts
nav_order: 1
permalink: /docs/concepts
---

# Concepts

## Nebula

## Tasks

Tasks are the building blocks of a pipeline. All tasks in a pipelien are run in the order they are defined in the pipeline.

## Pipelines

Pipelines are re-usable blocks of configured Tasks. Pipelines are used in Nebulas to provide the nodes and their metadata (Input Pipelines), process the collection of nodes (Main Pipelines) and to update metadata on the nodes (Scheduled Pipelines).

### Input Pipelines

Are used mainly to discover and load nodes into the Nebula. Input pipelines can have both tasks thta load nods, but also tasks that do manipulations on those nodes and even filter out nodes so these are excluded from processing in the Main Pipeline.

Input pipelines are run in parallel.

### Main Pipelines

Are used to process the loaded nodes in various ways:
- Detect and build relations between nodes
- Filter out nodes
- Even create outputs, for ex. files, push data into databases, or other systems

Main Pipeliens are run in sequence after the Input Pipelines have finished starting.

