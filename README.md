# KneeTrack Pro

A wearable knee brace system for measuring how the kneecap moves as the knee bends, developed as a biomedical engineering project at the University of Leeds.

## The problem

Patellofemoral pain affects around 23% of the population, and a leading cause is patella maltracking, where the kneecap moves abnormally as the knee bends. Clinicians frequently diagnose maltracking, but they don't usually measure how severe it is. KneeTrack Pro aims to give them a number: mediolateral patella displacement plotted against knee flexion angle.

## How it works

An iPhone 14 Pro is mounted on a commercial Össur CTi3 knee brace, 15 cm from the patella. Its LiDAR depth sensor tracks coloured pen marks on the patient's knee, while a rotary encoder in a bespoke hinge cap records the flexion angle through an Arduino. A Python script combines the two data streams to calculate patella shift across 0-90° of flexion, then exports the results to Excel.

## Project stages

1. **Initial design:** I wrote a design specification for a knee-mounted device using an Intel RealSense D405 stereo camera.
2. **Regulation and risk:** I classified the design under the UK Medical Devices Regulations 2002, then carried out an FMEA risk analysis following ISO 14971. This led to design changes.
3. **Group build:** I led a team of six to develop the concept into a working prototype, moving from stereo cameras to the iPhone's depth sensor.
4. **Testing and documentation:** We tested the prototype and its components, then produced a design file covering the user guide, assembly, cleaning protocols, safety analysis and code.

## Key results

| Measure | Result |
|---|---|
| Depth accuracy | ±1.013 mm |
| Field of view at 15 cm | 9.1 cm wide, covering the 1.93 cm patella movement range reported in the literature |
| Mount strength | Safety factor of 10 (81.9 MPa PLA flexural yield stress, 0.136 MPa operating stress) |
| Battery testing | Surface reached 45 °C after 6 minutes, so the design uses a USB connection instead of an internal battery |
| Device classification | Class Im (measuring function) |

## Documents

| Document | Description |
|---|---|
| [Initial design specification](Initial_Design.pdf) | The original stereo camera concept, covering the biomechanics and design requirements |
| [Compliance and risk report](Complience.pdf) | Regulatory classification, FMEA and the resulting design changes |
| [Patella position calculation](lateral%20patella%20position%20calculation.docx) | The maths behind the knee angle and patella position measurements |

## Status

This is a university prototype. It is not a certified medical device and is not intended for clinical use.
