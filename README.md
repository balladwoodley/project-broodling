# Project Broodling

**A Distributed Cognitive Architecture Built from Self-Spawning Agents**

---

## Overview

Project Broodling is an experimental framework for building intelligent systems composed of many small, autonomous agents called *Broodlings*.

Instead of relying on a single large model or centralized controller, Broodling distributes cognition across a swarm of lightweight agents that communicate through a shared Field layer.

This approach explores a different scaling path for AI:

* Scale by increasing the number of agents
* Not by increasing the size of a single model

The system is designed to support adaptive spawning, distributed reasoning, and persistent simulation.

---

## Core Architecture

Broodling consists of three fundamental components:

### 1. Broodlings

Broodlings are autonomous agents that:

* Receive information from the Field
* Process information according to their role
* Publish new information back into the Field
* Spawn new Broodlings when necessary

They are lightweight, disposable, and specialized.

---

### 2. The Field

The Field is the shared communication and coordination layer.

It acts as:

* Message bus
* Shared memory layer
* Coordination substrate

Broodlings do not communicate directly with each other.
All interaction occurs through the Field.

This enables flexible, scalable coordination without centralized control.

---

### 3. Spawn Manager

The Spawn Manager controls the lifecycle of Broodlings.

It is responsible for:

* Creating new Broodlings
* Managing active Broodlings
* Advancing the simulation

Future versions will allow Broodlings to spawn new Broodlings autonomously.

---

## Design Principles

Project Broodling follows these principles:

* Distributed over centralized
* Lightweight over heavyweight
* Many small agents over one large agent
* Emergent coordination over rigid pipelines
* Adaptive scaling over fixed capacity

---

## Current Features (v0.1)

* Broodling agent abstraction
* Shared Field communication system
* Topic-based message routing
* Spawn Manager for agent lifecycle
* Simulation environment loop
* Working example demonstration

---

## Repository Structure

```
broodling/
│
├── core/
│   ├── broodling.py
│   ├── field.py
│   ├── spawn.py
│   ├── message.py
│
├── simulation/
│   ├── environment.py
│
├── experiments/
│   ├── simple_task_demo.py
│
├── main.py
├── requirements.txt
└── README.md
```

---

## Example: Basic Usage

```python
from core.field import Field
from core.spawn import SpawnManager

field = Field()
spawner = SpawnManager(field)

broodling = spawner.spawn(role="worker")
broodling.subscribe("task")

broodling.publish("task", "Process this data")

spawner.step_all()
```

---

## What This Enables

This architecture enables experimentation with:

* Distributed reasoning systems
* Agent-based computation
* Adaptive scaling architectures
* Persistent simulation environments
* Autonomous agent ecosystems

---

## Roadmap

### v0.2

* Autonomous agent spawning
* Role specialization
* Parallel execution

### v0.3

* Persistent memory layer
* Long-running agent environments
* Distributed execution across machines

### v1.0

* Fully autonomous agent ecosystem
* Self-scaling cognitive infrastructure
* Integration with external models and tools

---

## Status

Active development — early prototype stage

---

## Getting Started

Clone the repository:

```
git clone https://github.com/yourname/broodling.git
cd broodling
```

Run the demo:

```
python main.py
```

---

## Vision

Project Broodling explores an alternative path for building intelligent systems.

Not as a single monolithic model.

But as a distributed ecosystem of cooperating agents.

---

## License

TBD

---

## Author

Ballad Woodley
Founder, Project Broodling
