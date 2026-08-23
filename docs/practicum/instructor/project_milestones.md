# Project Milestones

## Suggested Week 1 Turn-In

By the end of Week 1, each team should submit:

1. A link to a practice PR that went through review.
2. A short product and pipeline summary written in their own words.
3. A target architecture diagram.
4. A planned runtime flow diagram or written runtime walkthrough.
5. A short city input contract.
6. A team working agreement.

## Suggested Week 2 Turn-In

By the end of Week 2, each team should submit:

1. An API direction and extraction plan with a trimmed response sample.
2. A location input and validation implementation.
3. A raw extract client for the selected primary OpenWeather API.
4. A short raw response contract, sample, and Week 3 handoff describing later storage needs and unanswered questions.
5. Extract tests or verification notes for invalid input, missing configuration, and API response failures.
6. An optional second API integration with tests and documentation, if included.

## Suggested Week 3 Turn-In

By the end of Week 3, each team should submit:

1. A transform input and output contract with updated process flow diagrams.
2. A data dictionary for the transformed fields.
3. A raw-to-clean transform implementation for the team's selected API.
4. A normalization and data-quality rules table with the Sprint 3 rules implemented in the transform.
5. Automated transform tests using Sprint 2 response samples.

## Suggested Week 4 Turn-In

By the end of Week 4, each team should submit:

1. A database schema based on the Sprint 3 transform contract and data dictionary.
2. A migration or bootstrap workflow that creates the schema from scratch.
3. Persistence for raw responses and transformed records.
4. Record keys, uniqueness rules, and update/upsert behavior.
5. Pipeline run tracking with useful status and count information.
6. Storage tests or verification notes for empty, repeated, and updated data.
7. Optional Parquet or archive output and verification notes, if included.
8. A Week 5 handoff note explaining how the pipeline runner should call the transform and storage paths.

## Suggested Week 5 Turn-In

By the end of Week 5, each team should submit:

1. A shared pipeline runner that coordinates extract, transform, and load.
2. A manual CLI run path that uses the shared runner.
3. Runtime logs for stage start, stage completion, success, and failure.
4. Runner and CLI tests for success and failure cases.
5. A scheduler-friendly entrypoint or schedule configuration plan.
6. Runtime configuration and secrets guidance.
7. A validation note showing how the team knows a run completed successfully.
8. A Week 6 handoff note explaining what dashboard/API data is available and what runtime settings the frontend team will need.

## Suggested Week 6 Turn-In

By the end of Week 6, each team should submit:

1. A dashboard API or data-serving path connected to the gold data contract.
2. A React or Streamlit dashboard with useful summary and city-level views.
3. Loading, empty, and error states.
4. An end-to-end smoke test from pipeline output to dashboard display.
5. A documented local demo path.
6. Runtime configuration notes.
7. Final project documentation and known limitations.
8. A final demo that explains the product, architecture, data flow, team process, and tradeoffs.

## Suggested Week 7 Turn-In

By the end of Week 7, each team that chooses optional work should submit:

1. One selected optional task with a short scope statement.
2. A PR implementing the extension or a clearly documented partial implementation.
3. Tests, verification notes, or screenshots appropriate to the task.
4. Updated documentation explaining how to run, review, or maintain the extension.
5. A short reflection on what was completed, what remains, and whether the story-point estimate felt accurate.
