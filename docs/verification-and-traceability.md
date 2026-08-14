# Verification and traceability summary

The final submission included use cases, normal-use and safety-event sequence diagrams, state machines, a UML class diagram, Doxygen output, and a 23-item traceability matrix connecting requirements to implementation components and scenario-based tests.

This showcase summarizes that work without republishing the full course solution or source documentation.

## Verification approach

The team used scenario-driven acceptance testing in the running Qt application. Each scenario combined user actions, simulated time, visible state changes, stored records, and safety outcomes.

| Area | Representative checks | Observable evidence |
| --- | --- | --- |
| Startup and status | Launch UI, battery state, cartridge amount, insulin-on-board state, and navigation | Main dashboard and status indicators |
| Personal profiles | Create, validate, activate, schedule, edit, and delete a profile | Profile manager state and persisted profiles |
| Manual bolus | Validate glucose/carbohydrate inputs, calculate carb and correction components, preview, confirm/override, and deliver | Bolus window, insulin-on-board change, glucose simulation, and history |
| Extended bolus | Select a duration, deliver incrementally, visualize the active interval, and stop or complete delivery | Graph highlight, cartridge change, completion alert, and stored event |
| Automated control | Feed glucose readings, adjust basal delivery, suspend below the safety threshold, and resume after recovery | Rate changes, graph state, delivery icon, and history |
| Alerts and safety | Trigger glucose, battery, cartridge, and delivery-resumption conditions | Modal alert, alert log, persisted record, and delivery state |
| Persistence | Record bolus injections, basal-rate changes, warnings, and profiles | Records and alert-log windows after scenario execution |

## Final demonstration set

The four final videos exercise two successful-use scenarios and two safety scenarios:

1. [Profiles and automatic insulin delivery](https://youtu.be/dCezgP-P2d4)
2. [Manual, extended, and automatic bolus delivery](https://youtu.be/tJMpMrLWkEg)
3. [Battery warnings and shutdown](https://youtu.be/DuQRoASgmRc)
4. [Empty-cartridge delivery stop](https://youtu.be/sf8nXzPyNlg)

## Example requirement-to-component mapping

| Requirement theme | Primary components |
| --- | --- |
| Bolus calculation and delivery | `BolusWindow`, `BolusManager`, `BodySimulator`, `ControlSystem` |
| Automatic basal control | `ControlSystem`, `BodySimulator`, `MainWindow`, graph/highlight components |
| Personal delivery profiles | profile manager windows, `PersonalProfile`, list model, `DBManager` |
| Pump history | `DBManager`, `RecordsWindow`, alert log |
| Safety and error handling | `Alerts`, `Alert`, `AlertCreator`, `AlertHandler`, `AlertLogWindow` |
| Battery and cartridge state | `BatteryManager`, `InsulinChargeManager`, `Refillable`, `MainWindow` |

## Scope note

These checks demonstrate course-project behavior, not medical-device verification. The simulator was not evaluated under clinical, regulatory, hardware, cybersecurity, or safety-certification standards.
