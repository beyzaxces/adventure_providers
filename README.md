# Adventure Providers

A Flutter-based mobile application developed to support safer, more informative, and more collaborative adventure experiences for hikers and off-road adventurers. Built as an undergraduate graduation project at OSTİM Technical University (2026).

## Overview

Conventional navigation platforms offer limited support for terrain-specific information, real-time group coordination, and safety-oriented communication in outdoor environments. Adventure Providers addresses this gap by combining route recording, community-driven route sharing, live group coordination, and emergency alerting into a single mobile platform.

## Features

- **Route recording & sharing** — GPS-based route tracking with live polyline visualization
- **Flag-based annotation** — mark scenic points, obstacles, and hazards with optional photos and notes
- **Live group coordination** — real-time location sharing among group members via WebSocket
- **Off-track alerts** — automatic notifications when a user deviates from the planned route
- **SOS emergency alerts** — one-tap emergency notification with GPS coordinates, delivered via Firebase FCM
- **Route discovery** — searchable, filterable repository of community-shared routes
- **Activity analytics** — post-session stats including distance, duration, step count, and estimated calorie expenditure

## Tech Stack

| Layer | Technology |
|---|---|
| Mobile client | Flutter |
| Backend / API | Node.js |
| Database | MongoDB |
| Real-time communication | WebSocket, Firebase (FCM) |
| Maps | Google Maps API |
| Admin panel | React |

## Architecture

A layered client-server architecture: mobile clients communicate with backend REST APIs for transactional operations, while WebSocket channels broadcast live location and event updates to subscribed clients. Data is persisted in MongoDB. Core entities include users, trails, hike sessions, flags, group sessions, emergency events, and route reviews. User roles (Explorer, Group Leader, Administrator) are enforced via role-based access control at the API middleware layer.

## Development Process

Built using a Scrum-based agile process across four two-week sprints:

1. **Sprint 1** — system architecture and user authentication
2. **Sprint 2** — live GPS tracking and map integration
3. **Sprint 3** — flag management, group-based location sharing, notifications
4. **Sprint 4** — social features, administrative tools, system stabilization

## Team

Developed by a 4-person team under the supervision of **Prof. Dr. Yücel Tekin**, Department of Computer Engineering, OSTİM Technical University.

| Team Member | Role / Responsibilities |
|---|---|
| **Ali Sumama** (Team Leader) | Coordinated overall project progress and team communication. Managed meeting organization, requirement analysis, sprint planning, and documentation follow-up. Supported system design decisions and supervised development, testing, and final report preparation. |
| **Beyza Cesur** | Contributed to the Flutter-based mobile interface and user experience design (route views, profile pages, group interfaces, and user interaction flows). Assisted a teammate with integrating GPS tracking, real-time location sharing, and SOS alerts with the Node.js backend. Assisted with application testing, interface refinement, report preparation, and presentation preparation. |
| **Esma Nur Özer** | Supported back-end development activities using Node.js services and MongoDB data structures. Contributed to authentication, route-related operations, notification workflows, and the integration of real-time communication requirements with the mobile client. Assisted with report and presentation preparation. |
| **Sharmarke Abdi Ahmed** | Contributed to adventure-specific feature development, including route information, tracking-related functions, and safety-oriented features. Prepared the user manual. Assisted with testing, debugging, feature verification, and documentation of implemented system behavior. |

## Status

Implemented as a minimum viable product (MVP) with all core functional requirements complete. Validated through controlled testing; real-world field validation with external users remains as future work.
