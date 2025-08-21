---
applyTo: '**'
---

This project is a demo for showing the capabilities for the FINOS CALM project.  Documentation about CALM can be found in #githubRepo finos/architecture-as-code.

Instructions:
- CALM files should have extension `.calm.json`.
- When generating or updating CALM files, make sure to validate the file afterwards, and check what errors there are.
- For the CALM schema, use https://calm.finos.org/release/1.0/meta/calm.json
- References to "C4" are talking about the C4 model for visualizing the architecture of software systems.  "C4 DSL" is synonymous with Structurizr DSL.
- When generating C4 DSL, make sure to validate it, then work on fixing any errors shown.
- You don't need to worry about installing or running the docusaurus server, as we will do this manually
- When implementing controls in CALM, the control requirements should be in a separate file from the main model, following the structure outlined in the CALM documentation at https://calm.finos.org/core-concepts/controls.