# Team contributions

This project was developed by a four-person team for the Object-Oriented Software Engineering class at Carleton University. The breakdown below is based on the contribution record included with the team's April 24, 2025 final submission.

## Khalifeh Basiri

- Designed the `BolusManager` calculation and delivery flow, including carbohydrate and correction components, validation, and safety limits.
- Built the manual-bolus interface logic and integrated manual delivery with the body/glucose simulation.
- Implemented correction-bolus confirmation behavior.
- Developed insulin- and glucose-related alert definitions, including out-of-range glucose and potential overdose conditions.
- Designed the `ControlSystem` for automated insulin delivery, glucose input, insulin-rate adjustment, safety checks, and suspend/resume behavior.
- Connected glucose trends to insulin-rate response across the interface and backend.
- Contributed to the final extended-bolus integration and demo preparation.

## Julien Larivière-Chartier

- Built major `MainWindow` interface components and signal/slot connections.
- Created application-wide QSS styling, images, and dependency-installation support.
- Implemented reusable battery and insulin-cartridge gauge behavior.
- Developed battery and insulin-cartridge management.
- Built the CGM visualization and its graph, highlight, and vertical-line components.
- Developed the initial body simulator and simulated-time management.
- Set up team collaboration infrastructure, assembled submissions, and produced the final demo videos.
- Collaborated on extended-delivery visualization and timer/increment behavior.

## Shang Shi

- Drafted use cases and established Doxygen as the project's code-documentation standard.
- Built personal-profile management workflows for viewing, creating, editing, deleting, activating, and deactivating profiles.
- Implemented personal-profile input validation and list-model rendering.
- Developed alert entities and the UI-facing alert creation, handling, display, and log-window workflow.
- Collaborated with Matthew Murphy on profile persistence.

## Matthew Murphy

- Developed the database manager for profiles, bolus injections, basal-rate changes, and alerts.
- Built the records window used to review persisted application events.

## Collaboration boundaries

Features were integrated across shared Qt windows, signals/slots, simulation state, and SQLite persistence. A component listed under one contributor may therefore include integration work or later refinements from another teammate. This showcase attributes primary responsibility and explicitly calls out known shared work; it does not claim that any one person created the complete application.
