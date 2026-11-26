---
title: "Token System (NPC Manager)"
excerpt: "A data-oriented Unreal Engine C++ & Blueprint plugin for coordinating NPCs and gameplay objects through dynamic token and task allocation."
header:
  teaser: /assets/images/TokenSystem_Thumbnail.png
categories:
  - Unreal Engine
  - Plugins
tags:
  - C++
  - Blueprint
  - AI
  - NPC Management
  - Combat Systems
---

## Overview

In game development, token systems are widely used to coordinate NPC behaviors by assigning them explicit jobs (tokens) rather than letting every agent act independently.
With **Token System (NPC Manager)**, I built a high-performance, generic framework that lets developers orchestrate any group of actors or objects through dynamic token and task distribution.

## Key Features

* **Full Blueprint & C++ Support:** Expose and extend core functionality seamlessly in either C++ or Blueprints.
* **Data-Oriented Architecture:** Built with a custom ECS-inspired architecture using Structure-of-Arrays (SoA) layouts for cache-friendly execution on hot paths.
* **Token & Task Distribution:** Assign tokens to define high-level roles and dispatch token-specific tasks to drive goals or update subscriber states.
* **Custom Scoring & Evaluation:** Define custom calculation logic for both tokens and tasks to fit your game's specific AI or gameplay rules.
* **Multi-Instance Token Ownership:** Allow subscribers to hold a configurable number of token instances simultaneously.
* **Exclusive Tokens (Temporary Jobs):** Assign exclusive tokens to subscribers to override normal behavior with high-priority, temporary jobs.
* **Source Subscriber Stealing:** Allow higher-priority sources to dynamically steal subscribers from other sources when demand shifts.
* **Runtime Customization:** Modify how tokens and tasks are evaluated and distributed—or adjust available instance counts—dynamically at runtime.
* **Data Asset & GameplayTag Driven:** Configure tokens and tasks via Data Assets for rapid iteration and integrate cleanly with existing systems using `GameplayTags`.
