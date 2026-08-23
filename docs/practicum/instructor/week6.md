# Week 6: Dashboard, Integration, and Final Demo

Week 6 is where students turn the completed pipeline into something a user can inspect.
The focus is the dashboard/API surface, final integration checks, and a clear demo that explains what the team built.
This week should make the project feel complete without hiding the tradeoffs or unfinished stretch work.

Sprint 6 gives teams a choice of dashboard stack: a Vite/React UI backed by a small Python API (matching this reference implementation), or an all-Python Streamlit + Plotly dashboard that queries PostgreSQL directly with no separate API layer. Both packages are already in `requirements.txt`. The AIR-007 references below describe the React/API path this repo actually built — treat them as one example of the shape the work can take, not a requirement to use React specifically. A team that chooses Streamlit should still satisfy the same acceptance criteria: a data-serving layer, a user-facing interface with loading/empty/error states, and an end-to-end integration check.

The AIR and PR references below point back to this instructor reference repo.
Use them as planning breadcrumbs and examples of the kind of work that will eventually exist in the student project.
Primary guideposts for Week 6 are AIR-007 for dashboard/API work and final integration.
Some references point back to earlier data-contract work, but Week 6 should focus on integration, presentation, and handoff.

| Week 6 item | Related repo references | Practicum support or student deliverable? | What students should do | Story points |
|---|---|---|---|---|
| Week 5 handoff review | AIR-010.x, AIR-011.x; PRs #137, #146, #147 | Student deliverable from Week 5, used in Week 6 | Review the pipeline runtime, available data, runtime settings, and validation notes before building the final dashboard/API path. | N/A |
| Dashboard/API acceptance criteria | AIR-007.x; PRs #45, #90, #92, #93 | Practicum support material | Instructors should clarify the minimum final experience: what the dashboard must show, what API/data shape it can rely on, and what the final demo should include. | N/A |
| Dashboard data-serving layer | AIR-007.3; PR #92 | Student deliverable | Build or finish the layer that turns database rows into what the dashboard displays: API endpoints for the React path, or query functions for the Streamlit path. Students should keep the response shape aligned with the Week 4 dashboard-ready data contract. | 5 |
| Dashboard interface (React or Streamlit) | AIR-007.1, AIR-007.2; PRs #45, #90, #93 | Student deliverable | Build or finish the dashboard UI in the team's chosen stack. The dashboard should show useful air-quality summaries, city-level data, and at least one view that helps users compare or understand trends. | 8 |
| Empty, loading, and error states | AIR-007.x; PRs #90, #93 | Student deliverable | Handle common user-facing states clearly: no data yet, dashboard loading, API error, and stale or incomplete data. | 3 |
| End-to-end integration check | AIR-007.3; PR #92 | Student deliverable | Verify that pipeline output can flow into PostgreSQL, through the API, and into the dashboard. Students should document the exact smoke test they used. | 5 |
| Demo workflow | AIR-007.x; PRs #90, #92, #93 | Student deliverable | Prepare the local demo path. Students should be able to show how data moves from pipeline output into the dashboard. | 3 |
| Runtime configuration notes | AIR-007.x; PRs #90, #92, #93 | Student deliverable with instructor support | Document the settings the demo dashboard needs, including database connection settings, secrets, and local environment choices. | 2 |
| Final project documentation | AIR-002, AIR-007, AIR-012 | Student deliverable | Update the project README or handoff docs so another person can understand what was built, how to run the main pieces, and where known limitations remain. | 3 |
| Final demo and handoff | AIR-007 | Student deliverable | Present the working project. Students should explain the product, the data flow, the team split, the hardest tradeoffs, and what they would improve with more time. | 3 |
| Week 6 final PR | AIR-007.x; PRs #45, #90, #92, #93 | Student deliverable | Submit one or more final PRs that complete the dashboard/API/demo story. The PR should include final verification notes and any demo/handoff documentation. | 2 |

**Total student story points:** 34

**Effort note:** Week 6 is still a strong week, but much of the risk depends on what is finished before it starts. If the class needs to trim scope, keep AIR-007 focused on a simple dashboard/API path and move extra chart views, display settings, or polish into Week 7.
