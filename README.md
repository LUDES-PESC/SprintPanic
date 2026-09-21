# Sprint Panic! 🚀

[Português](README-pt.md)

**Sprint Panic!** is an educational game about Scrum, workflow, and decision-making in software projects.

The player follows a team responsible for developing an interplanetary pizza-delivery application. Across four Sprints, the player must define goals, select work, handle unexpected events, control work in progress, participate in Daily Scrums, Sprint Reviews, and Retrospectives, and adapt the plan without losing sight of the Product Goal.

The game is designed for classes, training sessions, workshops, and individual study.

---

## Educational goal

The purpose is not to teach Scrum as a bureaucratic sequence of ceremonies, but to show how its elements interact while developing a product under uncertainty.

The game addresses concepts such as:

- Product Goal;
- Product Backlog;
- Sprint Goal;
- Sprint Backlog;
- Increment;
- Definition of Done;
- Sprint Planning;
- Daily Scrum;
- Sprint Review;
- Sprint Retrospective;
- adapting the plan during a Sprint;
- emergent technical work;
- impediments;
- technical debt;
- quality;
- stakeholder feedback;
- WIP (*Work in Progress*);
- swarming;
- velocity;
- Burndown;
- Burnup;
- Cumulative Flow Diagram.

The game explicitly distinguishes the elements defined by the **Scrum Guide** from complementary practices often used by Scrum Teams.

For example, **Velocity, Burndown, Burnup, CFD, and WIP limits are not mandatory Scrum artifacts or events**. They appear in the game as practices that support forecasting, transparency, and flow management.

---

## Scenario

The product is a pizza-delivery application for Mars.

### Product Goal

> Enable a person on Mars to choose, pay for, and track a pizza with confidence.

The Product Backlog includes capabilities such as choosing a pizza, building a cart, entering a Martian address, orbital payment, receipt and status, delivery tracking, arrival estimates, failure handling, and accessibility.

---

## How to play

A game consists of **four Sprints**.

Each Sprint represents five simulated workdays.

Basic flow:

1. choose a **Sprint Goal**;
2. select items for the **Sprint Backlog**;
3. start the Sprint;
4. follow the team's work;
5. respond to events and emergent work;
6. participate in the **Daily Scrum**;
7. conduct the **Sprint Review**;
8. conduct the **Sprint Retrospective**;
9. adapt the Product Backlog and start the next Sprint.

The main button guides the player through the different phases of the simulation.

Whenever the game requires a decision, the interface automatically switches to the **Game** area, where the situation and available alternatives are shown.

---

## Sprint Backlog and flow

During a Sprint, work appears in three states:

```text
TO DO → IN PROGRESS → DONE
```

The team has three Developers.

The player can start or pause items, reduce WIP, and concentrate Developers on the same item.

### WIP

The simulation suggests approximately **two items in progress at the same time**.

This limit is a **pedagogical rule of the simulation**, not a rule of the Scrum Guide.

Excessive WIP reduces simulated efficiency by representing context switching, additional coordination, and greater difficulty in bringing work to Done.

### Swarming

More than one Developer can work on the same item.

The simulation uses diminishing returns:

```text
1 Developer  = 1.00×
2 Developers = 1.65×
3 Developers = 2.05×
```

---

## Velocity

The team is calibrated for a **typical velocity between 9 and 13 points per Sprint**, centered approximately around 11 points.

The first Sprint is deliberately simpler so that the player can understand the flow and has a high probability of achieving the first Sprint Goal.

In later Sprints, forecasting uses the observed history.

In the game, velocity is presented as:

> evidence for the team's own forecasting, not as a target, an individual productivity measure, or a tool for comparing teams.

Emergent technical work consumes capacity but does not artificially increase product velocity.

---

## Emergent work

Problems discovered during the Sprint do not silently increase the size of a PBI.

When necessary work emerges, it can appear explicitly in the Sprint Backlog.

Example:

```text
💳 Orbital payment
└── ⚙️ Update API authentication

🛰️ Track delivery
└── 🐛 Fix status-update error
```

These items can represent technical work, defects, integration, dependency updates, security, or infrastructure work.

A PBI cannot reach Done while it still has incomplete blocking work.

---

## Events

Starting with the second Sprint, unexpected events may occur.

### People

- one team member becomes ill;
- flu affects more than one Developer;
- partial absence;
- temporary Product Owner unavailability.

### Infrastructure

- power outage;
- Internet outage;
- VPN unavailable;
- broken laptop;
- expired certificate;
- CI service quota reached;
- unstable test environment.

### Dependencies and libraries

- Release Candidate (RC);
- patch release with bug fixes;
- security update;
- incompatible major version;
- API and dependency changes.

### Engineering

- flaky tests;
- merge conflicts;
- regressions;
- hidden dependencies;
- test automation;
- reuse opportunities;
- build caching.

Not every event is negative: some represent improvement opportunities.

---

## Quality and technical debt

The simulation tracks:

- delivered value;
- quality;
- stakeholder trust;
- technical debt.

Technical debt may arise, for example, when the player:

- postpones an important fix;
- accepts a security risk;
- uses a workaround;
- tries to deliver before meeting the Definition of Done;
- trades quality for short-term speed.

---

## Sprint Review

The Sprint Review is not treated merely as a demonstration.

The player must interpret feedback and decide whether to:

- change the ordering of the Product Backlog;
- record a new need;
- keep the current ordering until more evidence is available;
- adjust priorities;
- reconsider risks and launch conditions.

---

## Sprint Retrospective

In the Retrospective, the player chooses improvements related to what happened during the Sprint, such as:

- reducing WIP;
- automating tests;
- improving refinement;
- making dependencies explicit;
- reducing repetitive work;
- improving integration.

---

## Metrics and charts

The game presents:

- **Burndown** — remaining work during the Sprint;
- **Burnup** — delivered value versus scope;
- **Cumulative Flow Diagram** — work to do, in progress, and Done;
- **Velocity** — points from product PBIs completed per Sprint.

These visualizations support understanding of flow and forecasting, but are not presented as mandatory Scrum components.

---

## Internationalization

The game is available in five languages:

- Português;
- English;
- Español;
- Français;
- Italiano.

The language is selected in **Setup**.

Translations cover the interface, Sprint Goals, events, questions, alternatives, Daily Scrum, Sprint Review, Retrospective, feedback, and the final debrief.

---

## Interface

The interface is designed with mobile devices as a priority.

The top contains a fixed bar with:

- hamburger menu;
- title;
- Setup.

The menu provides access to:

- Game;
- Product Backlog;
- Sprint Backlog;
- Burndown;
- Burnup;
- Flow;
- Velocity;
- Scrum;
- Debrief.

---

## Running the game

There is no installation, server, or external dependency.

Simply open the HTML file in a modern browser.

```text
sprint_panic.html
```

The game can also be published directly with **GitHub Pages**.

---

## Architecture

The project is deliberately implemented as a **single-file application**.

The complete application is contained in one HTML file:

```text
HTML
CSS
JavaScript
data
translations
simulation rules
charts
interface
```

It does not require:

- JavaScript frameworks;
- external libraries;
- backend services;
- databases;
- CDNs;
- network calls.

Once loaded, the game can run entirely offline.

---

## Suggested repository structure

```text
/
├── README.md
├── README-pt.md
├── sprint_panic.html
├── LICENSE
└── docs/
    └── screenshots/
```

The game itself remains a single HTML file.

---

## Classroom use

A complete game can be used as:

- an introduction to Scrum;
- an exercise after a theoretical class;
- a group activity;
- a flow demonstration;
- a discussion of Product Backlog versus Sprint Backlog;
- a study of decisions under uncertainty;
- an introduction to agile metrics.

Useful discussion questions include:

1. Why were some Sprint Goals achieved while others were not?
2. When should the team reduce WIP?
3. When should technical work appear in the Sprint Backlog?
4. When should feedback change the Product Backlog?
5. Why should velocity not be treated as a target?
6. Which decisions created technical debt?
7. Which events should or should not change the Sprint Goal?

---

## Conceptual reference

The main reference is:

> Schwaber, K.; Sutherland, J. **The Scrum Guide — The Definitive Guide to Scrum: The Rules of the Game.** 2020.

<https://scrumguides.org/>

The game also incorporates flow practices and metrics commonly used in agile environments while attempting to distinguish them from the formal elements of the Scrum Guide.

---

## Contributing

Contributions are welcome, especially:

- new events;
- translation review;
- accessibility improvements;
- new scenarios;
- simulation balancing;
- testing on mobile devices;
- interface improvements;
- teaching material;
- studies about classroom use of the game.

When proposing a rule, it is useful to indicate whether it represents:

1. a formal Scrum rule;
2. a common practice;
3. a pedagogical simplification;
4. a simulation-specific rule.

This distinction helps prevent game-design decisions from being confused with prescriptions from the Scrum Guide.

---

## Credits

**Sprint Panic!** was conceived as an educational game about Scrum, workflow, and decision-making in software projects.

The project was developed in the context of teaching and research activities in Software Engineering, Games, and Simulations.

---

## License

MIT License

Copyright (c) 2026 Geraldo Xexéo

