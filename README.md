# SurvivalSim

## Idea
Project aiming to create an autonomous survival experience.

SurvivalSim is an autonomous survivor simulation engine.

It is not a traditional game. There is no predefined story or scripted scenario. Instead, each character makes their own decisions based on their needs, relationships, memories, personality, and environment.

Every simulation evolves differently, creating its own unique story through the interactions and consequences of the world's rules.

The goal is to create a living survival world with its own characters and rules, but without a predefined story.

Think of it as an experiment in causality.

This is an ongoing C++ project that I started to get back into coding after a difficult time in my life (Rest in peace, Dad), which prevented me from completing my I.T. studies just a few months before graduation.

## Philosophy

* No main character.
* No predefined story.
* No mandatory events.
* Every character follows the exact same decision-making system.
* The player (or observer) watches a story emerge rather than following one that has been written.

The goal is for even the developer to be surprised by what happens.

---

## Survivors

Each survivor has their own:

* Name
* Skills (construction, combat, medicine, farming, etc.)
* Personality (altruistic, selfish, cautious, impulsive, curious...)
* Needs (hunger, sleep, safety, social interaction...)
* Memory of past events
* Knowledge of the world
* Emotional state
* Affinity with every other survivor

A survivor's personality does not suddenly change, but their experiences gradually shape their future decisions and behavior.

---

## Skills

Every action requires one or more skills.

For example:

* Build a wall
* Cook a meal
* Chop wood
* Repair a radio
* Treat an injured survivor

Characters naturally choose tasks that match their abilities, and they can learn and improve over time.

---

## The Needs Board

The core of the simulation revolves around a **Needs Board**.

Whenever a survivor cannot satisfy one of their own needs, they create a request.

Examples:

* "20 units of wood are required to build a workshop."
* "Someone needs to treat Cloud."
* "The water supply is running low."
* "We need more food."

Every survivor regularly checks the board.

For each request, they compute a score based on factors such as:

* Their own skills
* Personal priorities
* Distance
* Physical condition
* Relationship with the requester
* Urgency
* Expected benefit for the colony

The highest score is not always selected. A small amount of variability is introduced to produce more believable and less deterministic behavior.

---

## Relationships

Every survivor has a unique relationship with every other survivor.

Relationships evolve naturally through shared experiences:

* Working together
* Sharing resources
* Saving someone's life
* Being rescued
* Stealing
* Lying
* Abandoning someone
* Arguing
* Spending time together

These relationships directly influence future decisions.

A survivor is naturally more willing to help a close friend than a complete stranger.

Relationships may evolve into:

* Friendship
* Rivalry
* Trust
* Distrust
* Love

None of these outcomes are scripted.

---

## Memory

Survivors remember what they experience.

For example:

* Who helped them
* Who betrayed them
* Who regularly shares resources
* Who lies
* Who runs away from danger

These memories gradually influence future decisions.

---

## Causality

The entire project is built around one central idea:

**Every important event must be explainable.**

If, on Day 300, one survivor kills another, it should be possible to trace the complete chain of causes:

* Old arguments
* Broken promises
* Jealousy
* Famine
* The loss of a loved one
* Long-standing rivalries

The simulation should never produce an important event simply "because of randomness."

Randomness may influence a decision.

It should never replace logic.

---

## Randomness

A small amount of randomness exists to avoid perfectly deterministic behavior.

For example, a survivor may choose between several nearly equivalent tasks instead of always selecting the mathematically optimal one.

Randomness creates variety.

The rules create the story.

---

## Architecture

Development begins entirely in a console application.

The simulation engine has no knowledge of graphics or rendering.

Its only responsibility is to simulate:

* Survivors
* The world
* Events
* Decisions
* Statistics

A graphical interface can be added later without modifying the core simulation.

---

## Technical Goals

This project is also an opportunity to deepen my understanding of:

* Modern C++
* Software architecture
* Multi-agent systems
* Decision-making algorithms
* Data structures
* Simulation persistence
* Testing
* Object-oriented programming and SOLID principles

---

## Vision

**SurvivalSim is not designed to tell a story.**

It builds a world.

The characters will tell the rest.
