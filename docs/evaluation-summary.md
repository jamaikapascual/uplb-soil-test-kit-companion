# Evaluation Summary

The UPLB Soil Test Kit Companion was evaluated through usability testing and expert/staff checking to assess the usability, functionality, and consistency of the system with the UPLB Soil Test Kit (STK) references used in the study.

## System Usability Scale (SUS)

The mobile application was evaluated by 10 participants using the System Usability Scale (SUS).

| Participant Group | n | Mean SUS | Lowest | Highest |
| --- | ---: | ---: | ---: | ---: |
| STK Expert/Familiar | 4 | 86.88 | 77.5 | 92.5 |
| Non-STK Expert/User | 6 | 88.33 | 82.5 | 97.5 |
| Overall | 10 | 87.75 | 77.5 | 97.5 |

Overall standard deviation:6.17

The overall mean SUS score of 87.75 indicates that the application was generally perceived positively in terms of usability by the participants who tested the system.

## Expert/Staff Functional Testing

An expert/staff evaluation was conducted using controlled soil samples to check the primary mobile application workflow.

All evaluated features were marked as Pass, including:

- Application startup and new soil test creation
- Camera capture
- Camera guide box visibility and positioning
- Color extraction from guided sampling areas
- Manual selection fallback
- Soil pH interpretation
- Nitrogen interpretation
- Phosphorus interpretation
- Potassium manual input
- Fertilizer recommendation generation
- Lime requirement output
- Local result saving
- Saved result viewing
- Offline and online operation

## Controlled Soil Testing

Controlled soil samples were used to compare expected STK-based interpretations with application-generated results.

| Test | Expected STK Result | Application Result | Match |
| --- | --- | --- | :---: |
| BTB pH | 8.1 | 8.0 | Yes |
| BCG pH | 3.6 | 4.0 | Yes |
| Nitrogen | High | High | Yes |
| Nitrogen | Low | Low | Yes |
| Phosphorus | Low | Low | Yes |
| Phosphorus | High | High | Yes |
| Potassium | Sufficient | Sufficient | Yes |
| Potassium | Deficient | Deficient | Yes |

For pH, the application returns the nearest available value from the STK color references rather than an exact laboratory soil pH measurement. This is why expected readings such as 8.1 and 3.6 were interpreted as their closest available STK reference values of 8.0 and 4.0.

For the evaluated controlled samples, the application-generated interpretations were consistent with the expected STK-based interpretations.

## Recommendation and Computation Checking

The fertilizer recommendation workflow was checked against the UPLB STK references used in the study.

For the evaluated crop scenario:

- Generated fertilizer recommendation values were within the corresponding STK recommendation ranges.
- Fertilizer material computations were consistent with the reference values used in the study.
- Household measurement conversions were considered reasonable based on the STK references.
- No differences in the recommendation or computation were reported during the evaluation.

The evaluation covered a selected crop scenario and should not be considered exhaustive validation of every crop and nutrient combination encoded in the application.

## Administrative Dashboard Testing

The web-based administrative dashboard was also evaluated.

All evaluated dashboard functions were marked as Pass, including:

- Administrator login
- User information display
- Synchronized soil test record display
- Consistency between mobile and dashboard records
- Search and filtering
- CSV export
- Exported record content
- Dashboard navigation and layout

## Evaluation Scope

The evaluation demonstrates that the tested system features worked as expected and that the generated interpretations and recommendations were consistent with the UPLB STK references used for the evaluated cases.

The study did not include laboratory validation against standard soil analysis. The application is therefore intended as a companion to the physical UPLB Soil Test Kit and not as a replacement for laboratory soil testing.