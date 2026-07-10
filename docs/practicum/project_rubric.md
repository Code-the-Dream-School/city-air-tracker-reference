# Sample Practicum Rubric

Use this as a starting point for assigning work across a 6-week version of the practicum.
Each team should adjust the scope based on group size, class pace, and instructor guidance.

## Component Buckets

1. Foundation and collaboration
2. Extract layer and raw persistence
3. Load layer and PostgreSQL storage
4. Transform layer and gold data contract
5. Scheduler/data pipeline and observability
6. Frontend React, dashboard API, and deployment

## Week-by-Week Plan

| Week | Focus | Ticket grouping | Student assignment |
|---|---|---|---|
| 1 | Project setup, Git workflow, architecture | Practicum materials and setup references: AIR-001, AIR-002.x, AIR-005, AIR-134; PRs #10, #13, #47, #50, #54-57, #109, #135 | Use the provided docs to get local setup running, understand the pipeline, create a small practice PR, and practice the review flow. |
| 2 | Extract layer and city/raw data inputs | AIR-003, AIR-004, AIR-012.4, AIR-012.5, AIR-012.6, AIR-109; PRs #11, #12, #72-74, #112 | Implement or trace city loading, invalid city handling, geocoding cache, raw OpenWeather persistence, and fresh-start fixes. |
| 3 | Load/storage and PostgreSQL-first backend | AIR-009.x, AIR-012.1, AIR-012.2, AIR-012.3, AIR-012.7, AIR-012.9, AIR-012.10, AIR-012.12, AIR-012.13; PRs #65, #66, #69-71, #76, #81, #83, #87, #89, #95 | Build schema and migrations, DB-first load behavior, gold-table upserts, optional Parquet/Azure Blob output, and setup docs. |
| 4 | Transform layer, data contract, and tests | AIR-012.8, AIR-012.10, AIR-012.11, AIR-007.3; PRs #78, #83, #85, #92 | Convert raw records into gold rows, validate output columns and keys, add integration/regression tests, and confirm the dashboard-ready data shape. |
| 5 | Scheduler/data pipeline runtime | AIR-010.x, AIR-011.x, AIR-013.1, AIR-013.2, AIR-013.4; PRs #67, #68, #94, #137, #146-149 | Refactor into a reusable pipeline runner, wire the CLI/Prefect entrypoint, preserve manual runs, and add logs, runtime config, and env profile switching. |
| 6 | Frontend React, API, deployment, and demo | AIR-007.1, AIR-007.2, AIR-007.3, AIR-013.6; PRs #45, #90, #92, #93, #155 | Finish the React dashboard, connect it to the PostgreSQL-backed API, containerize/deploy the dashboard workflow, and prepare the final demo and handoff docs. |

## Suggested Team Roles

For a 3-person group, rotate these roles each week:

1. Data/backend
2. Frontend/API or DevOps
3. QA, docs, and integration

For 4-5 students, split QA from docs and split backend into pipeline and database.

The main sequencing point is that PostgreSQL/load work should come before most frontend work.
The React dashboard depends on the gold data contract, so Week 4 is the handoff from the data pipeline into the dashboard.
