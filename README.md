# Robotic Manipulators Portfolio

> **Confidentiality & IP Notice**  
> This repository presents a high-level, non-proprietary overview of robotic manipulators developed in an industrial setting. Specific dimensions, tolerances, part numbers, supplier details, costs, control algorithms, and internal test data have been intentionally abstracted or omitted to comply with company confidentiality and intellectual property policies. The focus is on design intent, system-level architecture, and engineering trade-offs rather than proprietary implementation details.

---

## My Role & Contributions

**Position:** Mechanical Engineer (Intern → FTE)  
**Timeline:** January 2024 - Present  
**Company:** Twara Robotics  
**Team Size:** Small cross-functional team (5-8 people)

### What I Owned
- **Complete mechanical design** from concept through production for 5 manipulator variants
- **End-to-end development:** calculations → CAD → manufacturing → assembly → testing
- **Manufacturing coordination** with 8+ vendors across multiple processes (CNC, sheet metal, laser cutting, wire EDM)
- **Design iteration** based on testing feedback and cost constraints
- **First-principles analysis:** kinematics, workspace optimization, torque calculations

### Key Achievements
- Designed **5 manipulator generations** in 11 months (Jan - Dec 2024)
- Reduced system weight by **27%** (TR5_G1: 30kg → TR5_G3: 25kg) while improving rigidity
- Contributed to TR12 development, company's **first 12kg payload manipulator**
- Achieved cost reduction of ~30% through manufacturing process optimization
- Successfully transitioned from intern to full-time engineer based on design impact

---

## Quick Visual Overview

### Key Metrics Across Generations

| Model | Payload | Weight | Primary Material | Cost Index* | Status |
|-------|---------|--------|------------------|-------------|---------|
| TR5_G1 | 5 kg | ~30 kg | CNC Aluminum | 100 | Baseline |
| TR3 | 5 kg | ~18 kg | Plastic + Belts | 60 | Exploratory |
| TR5_G2 | 5 kg | ~22 kg | Sheet Metal | 70 | Limited Production |
| TR12_G1 | 12 kg | ~40 kg | Rolled Sheet Metal | 150 | Production |
| TR5_G3 | 5 kg | ~25 kg | Al Extrusion | 85 | Current Production |

*Relative cost index (TR5_G1 = 100)

### Design Philosophy Evolution
```
Generation 1: Prove it works (rigidity first)
           ↓
Generation 2: Make it affordable (cost/weight focus)
           ↓
Generation 3: Make it scalable (balanced optimization)
```

---

## Overview

This repository documents the design and development of multiple industrial robotic manipulators across different payload classes. The work involved starting from first principles, iterating across several design generations, and closing the loop through manufacturing, assembly, and validation testing.

I owned the workflow end-to-end: from early calculations and architecture definition, through detailed mechanical design, vendor coordination, manufacturing, assembly, and testing.

---

## Industrial Manipulator Development

The manipulators were developed under real-world constraints including cost, manufacturability, lead time, and performance requirements. Multiple design branches were explored in parallel, with learnings transferred across projects to converge toward more mature and scalable architectures.

**Overall development sequence:**  
**TR5_G1 → TR3 → TR5_G2 → TR12_G1 → TR5_G3**

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
- Longer lead times due to CNC dependency (4-6 weeks)

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
- Approximate system weight: ~22 kg (27% reduction from TR5_G1)
- Lower manufacturing cost (~30% reduction)
- Faster and easier assembly  
- Reduced lead time (2-3 weeks)

**Limitations Identified**
- Reduced structural rigidity compared to CNC baseline
- Lower repeatability under load  
- Torsional stiffness insufficient for precision applications

**Assessment**  
TR5_G2 validated weight and cost reduction strategies but highlighted rigidity and repeatability as critical constraints for industrial use.

---

### TR12_G1 — 12 kg Payload Manipulator (Learning Accelerator)

**Context**  
Development of the organization's first ~12 kg payload-class manipulator introduced higher structural, accuracy, and robustness requirements.

**Key Contributions**
- Structural design using rolled sheet-metal construction  
- New joint orientations and configurations to increase payload capacity and reach  
- Design changes to improve overall system rigidity  
- Introduction of features to enhance robustness  
- Unveiled at IMTEX 2025 exhibition

**Outcome**  
TR12_G1 served as a major learning milestone, with insights directly influencing subsequent TR5 designs.

---

### TR5_G3 — Optimized Architecture (Current Generation)

**Architecture**
- Aluminum extrusion-based structure informed by TR12 learnings  

**Key Improvements**
- Significantly improved rigidity and repeatability while maintaining weight efficiency
- Modular and repeatable manufacturing process  
- Simplified and more reliable assembly workflow  
- Balanced cost, stiffness, and scalability  
- Weight: ~25 kg (maintains most of G2's weight savings while recovering rigidity)

**Outcome**  
TR5_G3 combined the rigidity of early CNC-based designs with the manufacturability and scalability lessons learned from later programs, resulting in a more mature and production-ready architecture.

---

## Design Evolution Summary

| Generation | Primary Focus | Approx. Weight | Key Trade-off |
|----------|---------------|----------------|---------------|
| TR5_G1 | Rigidity | 30 kg | High cost, long lead time |
| TR3 | Concept exploration | ~18 kg | Deprioritized |
| TR5_G2 | Weight & cost | 22 kg | Lower stiffness |
| TR12_G1 | Higher payload | ~40 kg | Manufacturing complexity |
| TR5_G3 | Balance & scalability | ~25 kg | Optimized across parameters |

---

## Technical Challenges Solved

### Challenge 1: Rigidity vs Weight Trade-off (TR5_G2 → TR5_G3)

**Problem:** TR5_G2 sheet metal design achieved 27% weight reduction but suffered from insufficient rigidity under load, causing repeatability issues.

**Analysis:** 
- Identified that thin-wall sheet metal lacked torsional stiffness
- Quantified deflection at end-effector exceeded acceptable limits
- Testing revealed performance degradation under dynamic loading

**Solution:**
- Transitioned to aluminum extrusion architecture (TR5_G3)
- Strategic reinforcement at high-moment joints
- Maintained weight savings while recovering rigidity
- Improved joint design to minimize compliance

**Outcome:** Achieved comparable weight (25kg vs 22kg, only 14% increase) with significantly improved stiffness and repeatability meeting industrial requirements.

---

### Challenge 2: Manufacturing Scalability (TR5_G1 → TR12_G1)

**Problem:** CNC-intensive TR5_G1 had prohibitive lead times (4-6 weeks) and high per-unit cost.

**Analysis:**
- Identified CNC machining as bottleneck in production scaling
- Cost breakdown showed CNC operations represented 60%+ of manufacturing cost
- Lead time prevented rapid iteration and market responsiveness

**Solution:**
- Explored sheet metal fabrication for TR5_G2 and TR12_G1
- Designed for laser cutting, bending, and riveting (faster, cheaper processes)
- Developed modular joint designs compatible with sheet metal construction
- Established relationships with sheet metal vendors

**Outcome:** Reduced lead time to 2-3 weeks and manufacturing cost by ~30%, enabling faster iteration cycles and better unit economics.

---

### Challenge 3: Actuator Integration & Wobble Reduction (TR5_G1)

**Problem:** Initial prototype exhibited unacceptable actuator wobble, degrading positional accuracy during operation.

**Root Cause Analysis:**
- Insufficient shaft support and bearing preload
- Tolerance stack-up in joint assembly creating clearances
- Inadequate bearing housing stiffness

**Solution:**
- Redesigned bearing housing with improved support geometry
- Implemented bearing preload mechanism to eliminate play
- Tightened critical tolerances in manufacturing specifications
- Improved assembly process with better fixturing and procedures

**Outcome:** Wobble reduced below acceptable threshold, system met accuracy requirements for intended applications.

---

## Engineering & Analysis Approach

All manipulators were designed starting from first principles rather than relying on off-the-shelf sizing tools.

### Kinematic Analysis & Workspace Optimization
- Developed workspace analysis tools to evaluate reach-payload trade-offs
- Calculated joint torques for worst-case loading across full range of motion
- Optimized link lengths to maximize workspace volume while minimizing arm weight
- Generated payload–reach trade-off graphs to guide architecture decisions

### Tool Evolution
The analysis workflow evolved over time:
- **Phase 1:** Hand calculations for early feasibility studies
- **Phase 2:** Spreadsheet-based models (Excel) for rapid iteration and parameter sweeps
- **Phase 3:** Script-based analysis using GNU Octave for repeatable torque, payload, and reach evaluation with visualization

This progression enabled faster iteration, clearer visualization of design limits, and more informed component selection.

### Typical Analysis Workflow (Abstracted)
For a given payload P at maximum reach R:
1. Calculate joint torques considering arm weight + payload across workspace
2. Size actuators based on peak torque + appropriate safety factors
3. Validate structural deflection under load using FEA
4. Iterate link geometry to balance stiffness, weight, and cost
5. Generate performance envelopes (torque-speed curves, workspace maps)

### Structural Analysis
- FEA validation of critical load paths and stress concentrations
- Deflection analysis at maximum reach and payload conditions
- Fatigue considerations for cyclic loading scenarios
- Modal analysis for dynamic performance evaluation
- **Outcome:** Design decisions backed by quantitative analysis, not assumptions

### Component Selection Methodology
- **Actuator sizing:** Evaluated torque, speed, and precision requirements with appropriate derating
- **Reducer selection:** Analyzed harmonic vs planetary vs cycloidal trade-offs (efficiency, backlash, cost)
- **Bearing selection:** Optimized for load capacity, stiffness, and cost constraints
- **Material selection:** Compared aluminum vs steel vs composites based on stress/weight/cost analysis

---

## Manufacturing & Cost Considerations

Manufacturing strategy evolved with each generation to balance cost, performance, and scalability.

### Manufacturing Processes Utilized
- **CNC turning (lathe)** for shafts and precision rotational components
- **CNC milling (VMC)** for joint housings and structural parts
- **Laser cutting** of sheet and tube profiles
- **Wire EDM** for high-precision features and complex geometries
- **Sheet-metal fabrication** (bending, riveting) for cost-effective structures
- **Custom jigs and fixtures** for manufacturing, assembly, and testing repeatability

### Design for Manufacturing Evolution
- **TR5_G1:** CNC-centric, high precision, high cost
- **TR5_G2/TR12:** Sheet metal focused, cost optimization
- **TR5_G3:** Balanced approach using aluminum extrusion for modularity

### Vendor & Process Coordination
- Preparation of fabrication-ready design packages with complete specifications
- GD&T definition and clarification with manufacturing partners
- Technical discussions and design-for-manufacturability reviews with vendors
- Order placement, procurement tracking, and follow-up
- Assembly process definition and sequencing for efficiency
- Quality control and dimensional verification protocols

---

## Assembly, Testing & Validation Ownership

- End-to-end assembly of manipulators from component level to system integration
- Payload testing under multiple configurations and operating conditions
- Repeatability evaluation across extended cycles
- Performance validation against design specifications
- Iterative feedback from testing incorporated into subsequent design revisions
- Field deployment support and troubleshooting

---

## Key Engineering Lessons Learned

### Design Principles That Emerged

1. **Actuator stiffness dominates system performance**
   - Even with rigid links, actuator compliance limits repeatability
   - **Lesson:** Size actuators for stiffness and precision, not just torque capacity

2. **Early architecture decisions compound over time**
   - Switching from CNC to sheet metal required complete redesign, not simple adaptation
   - **Lesson:** Evaluate manufacturability in concept phase, not after detailed design completion

3. **Modular design accelerates iteration**
   - TR5_G3 benefited from modular joint designs allowing rapid testing of variants
   - **Lesson:** Design for configurability early, even if first units don't exploit it

4. **Design for assembly is as critical as design for manufacturing**
   - TR5_G2 was economical to manufacture but difficult to assemble with required precision
   - **Lesson:** Assembly time, complexity, and tolerance stack-up directly impact unit economics and quality

5. **Testing reveals hidden assumptions**
   - Multiple design "wins" on paper failed under real loading and environmental conditions
   - **Lesson:** Prototype and test early and often; analysis has blind spots that only hardware reveals

6. **Cost and performance must be balanced systemically**
   - Optimizing individual components doesn't guarantee system-level optimization
   - **Lesson:** Evaluate trade-offs at system level, considering manufacturing, assembly, and lifecycle costs

### What I Would Do Differently

**If starting TR5_G1 today:**
- Begin with sheet metal/extrusion architecture (skip CNC-heavy approach for prototypes)
- Prototype critical joints independently before full arm integration
- Build in sensor mounting provisions and cable routing from day one
- Design assembly jigs and fixtures in parallel with parts (not as afterthought)
- Document assembly process more thoroughly for knowledge transfer
- Implement design reviews earlier in the process

**For next-generation design (TR5_G4 concept):**
- Further weight reduction targeting ~20kg system weight
- Increased modularity with standardized joint interfaces across payload classes
- Integrated cable/hose routing designed from the start, not retrofitted
- Design for automated testing and calibration procedures
- Enhanced serviceability for field maintenance
- Cost target: 20% reduction from TR5_G3 through design optimization

---

## Repository Roadmap

This repository will be progressively updated with additional technical content:

### Phase 1 (Current) ✅
- High-level system architecture and evolution
- Design philosophy and trade-offs
- Manufacturing and validation approach
- Key challenges and solutions

### Phase 2 (In Progress - Q1 2025) 🔄
- Kinematics implementation for TR5 series (forward/inverse)
- Motion planning and trajectory generation algorithms
- Workspace analysis and visualization tools
- ROS2 integration and simulation setup

### Phase 3 (Planned - Q2 2025) ⏳
- Control system integration strategies
- Dynamic modeling and analysis
- Design optimization case studies with quantitative results
- Performance benchmarking methodologies

---

## About Me

**Current Role:** Mechanical Engineer at Twara Robotics  
**Focus Areas:** Robotic manipulator design, kinematics, mechatronics integration  
**Location:** Bangalore, India

### Technical Interests
- Motion planning and trajectory optimization
- Mechatronics system integration and cross-domain design
- Design for manufacturing and assembly (DFMA)
- Industrial automation and collaborative robotics
- First-principles engineering and analytical modeling

### Professional Goals
Seeking opportunities in robotics engineering roles focusing on:
- Manipulator and mechatronic system design
- Full-stack robotics development (mechanical + controls integration)
- Product engineering in robotics/automation companies
- System-level architecture and technical leadership

---

## Contact

- **Email:** [adityabundelawork@gmail.com]
- **LinkedIn:** [www.linkedin.com/in/adityasinghbundela]
- **GitHub:** [github.com/AdityaSinghBundela](https://github.com/AdityaSinghBundela)

**Note:** For detailed technical discussions about specific projects, collaboration opportunities, or job inquiries, please reach out via email or LinkedIn.

---

*This portfolio is continuously updated as new projects and implementations are completed. Last updated: December 2024*
