# Week 2: Extract Layer and Raw Data Contracts

Week 2 is where students start turning the Week 1 plan into working project pieces.
The focus is the extract layer: API selection, location inputs, validation, API-facing code, mockable boundaries, and the raw data shape that later stages will depend on.
They should be building the first useful slice of the pipeline.

The AIR and PR references below point back to this instructor reference repo.
Use them as planning breadcrumbs and examples of the kind of work that will eventually exist in the student project.
Primary guideposts for Week 2 are AIR-003 and AIR-004 for location input handling and AIR-012.5 for extract setup.
The reference implementation follows the original air-pollution path, but students may choose current weather or forecasts instead.
Some PostgreSQL-backed behavior appears in these references, but Week 2 should focus on extract contracts and testable boundaries.
The database-specific implementation can be handed off into Week 3.

| Week 2 item | Related repo references | Practicum support or student deliverable? | What students should do | Story points |
|---|---|---|---|---|
| Week 1 handoff review | AIR-005, AIR-134; PRs #14, #135 | Student deliverable from Week 1, used in Week 2 | Use the Week 1 location input contract, target architecture diagram, and runtime flow as the starting point for implementation. Update these living documents when the team's API decision changes an earlier assumption. | N/A |
| Extract acceptance criteria | AIR-003, AIR-004, AIR-012.4, AIR-012.5, AIR-012.6, AIR-109; PRs #11, #12, #72-74, #112 | Practicum support material | Instructors should clarify what the extract layer must handle: valid and invalid location input, the selected OpenWeather API, raw response shape, clean-start behavior, and optional supporting APIs. | N/A |
| API direction and extraction plan | AIR-012.5; PR #74 as an air-pollution example | Student deliverable | Select a primary OpenWeather API, connect that choice to the future dashboard, and document its endpoint, parameters, important fields, errors, and a trimmed response sample. | 3 |
| Location input and validation | AIR-003, AIR-004, AIR-005, AIR-012.4; PRs #11, #12, #14, #72 | Student deliverable | Implement and validate one configurable location-input path for the selected API. Teams may supply coordinates directly or choose Geocoding as an optional integration. | 3 |
| Primary OpenWeather extract client | AIR-012.5; PR #74 | Student deliverable | Build API-facing code for the selected primary OpenWeather API. Keep the raw payload available for later transform work and make the client testable with mocked responses. | 5 |
| Raw response contract and sample | AIR-012.5; PR #74 | Student deliverable with Week 3 handoff | Define the context that should travel with each raw response, such as source location, selected API, request window, retrieval time, and raw payload. Note what the storage layer will need to accept and which questions remain unanswered. | 3 |
| Extract tests and verification notes | AIR-003, AIR-004, AIR-109; PRs #11, #12, #112 | Student deliverable | Add tests or manual verification notes for valid and invalid location input, missing configuration, empty or malformed responses, and predictable API errors. | 3 |
| Optional second API integration | AIR-012.6; PR #73 as a Geocoding example | Optional student deliverable | After the primary path works, integrate one additional data or supplementary API only when it directly supports the dashboard goal. | 5 |

**Total student story points:** 17 core, 22 with the optional second API integration

**Effort note:** Week 2 is a medium build week and should feel like the first real implementation push. If teams are moving quickly, they may add one supporting API; if they are struggling, keep the primary OpenWeather client mocked and finish the core extraction path.
