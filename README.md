# Robotic Manipulators Overview

> **Confidentiality & IP Notice**  
> This repository presents a high-level, non-proprietary overview of robotic manipulators developed in an industrial setting. Specific dimensions, tolerances, part numbers, supplier details, costs, control algorithms, and internal test data have been intentionally abstracted or omitted to comply with company confidentiality and intellectual property policies. The focus is on design intent, system-level architecture, and engineering trade-offs rather than proprietary implementation details.

---

## Overview

This repository documents the design and development of multiple industrial robotic manipulators across different payload classes. The work involved starting from first principles, iterating across several design generations, and closing the loop through manufacturing, assembly, and validation testing.

I owned the workflow end-to-end: from early calculations and architecture definition, through detailed mechanical design, vendor coordination, manufacturing, assembly, and testing.

---

## Industrial Manipulator Development (Twara Robotics)

The manipulators were developed under real-world constraints including cost, manufacturability, lead time, and performance requirements. Multiple design branches were explored in parallel, with learnings transferred across projects to converge toward more mature and scalable architectures.

---

## TR5 Series — 5 kg Payload Manipulator

### TR5_G1 — CNC + Aluminum Extrusion (Initial Baseline)

**Architecture**
- CNC-machined joints
- Aluminum extrusion-based links

**Key Characteristics**
- Payload class: ~5 kg  
- Approximate system weight: ~30 kg  
- High structural rigidity and stiffness  
- Expensive to manufacture  
- Longer lead times due to CNC dependency  

**Assessment**  
TR5_G1 established a rigid and reliable baseline but was not well-suited for cost-effective scaling or rapid iteration.

---

### TR3 — Lightweight Plastic Arm (Exploratory Branch)

**Architecture**
- Fully plastic structural design  
- Belt-driven transmission stages  
- In-house developed solenoid-actuated brake mechanism  

**Objective**
- Explore lightweight, low-cost manipulator concepts  
- Evaluate belt-drive transmission and integrated braking strategies  

**Outcome**  
While technically promising, TR3 was deprioritized to focus resources on higher-impact industrial manipulators.

**Key Learnings**
- Belt-driven joints can simplify transmission layouts  
- Integrated braking mechanisms improve safety and serviceability  
- Weight reduction must be balanced against stiffness and repeatability  

---

### TR5_G2 — Sheet Metal Architecture (Weight & Cost Focus)

**Architecture**
- Sheet-metal fabricated links and structures  

**Key Characteristics**
- Approximate system weight: ~22 kg  
- Significant weight reduction compared to TR5_G1  
- Lower manufacturing cost  
- Faster and easier assembly  

**Limitations Identified**
- Reduced structural rigidity  
- Lower repeatability under load  

**Assessment**  
TR5_G2 validated weight and cost reduction strategies but highlighted rigidity and repeatability as critical constraints for industrial use.

---

### TR12_G1 — 12 kg Payload Manipulator (Learning Accelerator)

**Context**  
Development of the organization’s first ~12 kg payload-class manipulator introduced higher structural, accuracy, and robustness requirements.

**Key Contributions**
- Structural design using rolled sheet-metal construction  
- New joint orientations and configurations to increase payload capacity and reach  
- Design changes to improve overall system rigidity  
- Introduction of features to enhance robustness  

**Outcome**  
TR12_G1 served as a major learning milestone, with insights directly influencing subsequent TR5 designs.

---

### TR5_G3 — Optimized Architecture (Current Generation)

**Architecture**
- Aluminum extrusion-based structure informed by TR12 learnings  

**Key Improvements**
- Significantly improved rigidity and repeatability  
- Modular and repeatable manufacturing process  
- Simplified and more reliable assembly workflow  
- Balanced cost, stiffness, and scalability  

**Outcome**  
TR5_G3 combined the rigidity of early CNC-based designs with the manufacturability and scalability lessons learned from later programs, resulting in a more mature and production-ready architecture.

---

## Design Evolution Summary

**Overall development sequence:**  
**TR5_G1 → TR3 → TR5_G2 → TR12_G1 → TR5_G3**

| Generation | Primary Focus | Approx. Weight | Key Trade-off |
|----------|---------------|----------------|---------------|
| TR5_G1 | Rigidity | 30 kg | High cost |
| TR3 | Concept exploration | Moderate | Deprioritized |
| TR5_G2 | Weight & cost | 22 kg | Lower stiffness |
| TR12_G1 | Higher payload | 40kg | Manufacturing Challenges |
| TR5_G3 | Balance & scalability | 25kg | Optimized |

---

## Engineering & Analysis Approach

All manipulators were designed starting from first principles rather than relying on off-the-shelf sizing tools.

### Kinematic & Load Analysis
- Link lengths and joint layouts developed using analytical calculations  
- Torque requirements evaluated across the workspace for multiple payload conditions  
- Payload–reach trade-off graphs generated to guide architecture decisions  

### Toolchain Evolution
The analysis workflow evolved over time:
- Hand calculations for early feasibility  
- Spreadsheet-based models (Excel) for rapid iteration  
- Script-based analysis using GNU Octave for repeatable torque, payload, and reach evaluation  

This progression enabled faster iteration, clearer visualization of design limits, and more informed component selection.

---

## Manufacturing & Cost Considerations

Manufacturing strategy evolved with each generation to balance cost, performance, and scalability.

- CNC machining used where precision and stiffness were critical  
- Sheet-metal fabrication adopted for weight and cost reduction  
- Aluminum extrusion selected for modularity and repeatability  
- Design decisions evaluated against supplier capability and lead time  

---

## Manufacturing, Supply Chain & Validation Ownership

I handled the complete development cycle from design release through fabrication, assembly, and testing.

### Manufacturing Processes Utilized
- CNC turning (lathe) for shafts and precision components  
- CNC milling (VMC) for joint housings and structural parts  
- Laser cutting of sheet and tube profiles  
- Wire EDM for high-precision features  
- Sheet-metal fabrication  
- Custom jigs and fixtures for manufacturing, assembly, and testing  

### Vendor & Process Coordination
- Preparation of fabrication-ready design packages  
- GD&T definition and clarification with vendors  
- Technical discussions and vendor communication  
- Order placement, procurement tracking, and follow-up  
- Assembly process definition and sequencing  

---

## Assembly, Testing & Validation

- End-to-end assembly of manipulators  
- Payload testing under multiple configurations and operating conditions  
- Repeatability evaluation across cycles  
- Iterative feedback from testing incorporated into subsequent design revisions  

---

## Key Lessons Learned

- Early architectural decisions strongly influence long-term performance and cost  
- Actuator and joint stiffness are critical for repeatability  
- Simplification often improves both performance and manufacturability  
- Designing for assembly and serviceability reduces iteration time significantly  

---

## What I Would Improve in the Next Iteration

- Further modularization of joint designs  
- Improved stiffness-to-weight ratio  
- Greater controls and sensing readiness  
- Additional cost optimization for scaled production  
