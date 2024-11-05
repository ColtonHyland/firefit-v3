# FireFit Championships Planning and Documentation

## Overview

The FireFit Championships is a competition based on essential firefighting tasks. The event structure includes various individual and team-based events, such as the **FireFit Relay**, **Tech2 Relay**, and **Individual Competitions**. Each type of event has specific rules, registration requirements, and participant roles.

This document will outline the project requirements, event structure, user flows, and planning steps for managing and enhancing the FireFit website.

---

## Event Structure and Categories

### Event Types

1. **FireFit Relay**: A 3-5 person team relay covering seven tasks with penalties for rule infractions.
2. **Tech2 Relay**: A 2-person relay with a cylinder exchange task at the halfway point.
3. **Individual Competition**: A single competitor completing all tasks independently.
4. **Team Competition**: A timed competition where a team’s score is derived from the three fastest times of its members.

### Categories and Divisions
- **Divisions**: Open Men, Open Women, Over 40, Over 50, Over 60, Industrial, Pre-Fire School, and others.
- **National Qualifications**: Teams and individuals can qualify for nationals based on specific time criteria.

---

## Registration Flow and Requirements

1. **Creating a Competitor Account**:
   - **Steps**: New users register with basic details, confirm via email, complete health questionnaires, and update their profiles.
   - **Admin Approval**: For over 60 or retired competitors, a medical clearance from a doctor is required.

2. **Event Registration Process**:
   - **Step-by-Step Registration**:
      - Competitor logs in, updates profile and health questionnaire, selects event type, adds team members, and completes payment.
      - Options for adding individuals, teams, and relays to a single cart for bulk payments.
   - **Payment Options**: Visa, MasterCard, Purchase Order/Cheque with up to 3 business days processing time.

3. **Team Requirements**:
   - Each team member must create or update their profile before team registration.
   - Teams can participate in multiple events; each member needs separate event entries.

---

## Flowcharts and ER Diagrams

### Lucidchart Diagrams
- **Flowcharts**:
   - **User Registration Flow**: Visualize the process from account creation to profile completion and health questionnaire.
   - **Event Registration Flow**: Outline each registration step for individuals and teams, including validation steps and payment processing.

- **Entity-Relationship Diagram (ERD)**:
   - **Entities**: User, Competitor Profile, Event, Team, Payment, Health Questionnaire.
   - **Relationships**:
      - **User - Competitor Profile**: One-to-One.
      - **User - Event**: Many-to-Many (via Team or Individual entries).
      - **Event - Team**: One-to-Many.
      - **Team - Payment**: One-to-One.

---

## Competition Rules and Requirements

### General Rules
1. **Eligibility**: Open to medically cleared fire/rescue personnel and pre-fire service students.
2. **Equipment Standards**: Competitors must wear NFPA 1971-labeled gear (boots, helmet, gloves, SCBA).
3. **Event-Specific Penalties**: Detailed penalties based on rule infractions (e.g., False Start, Missing Hydrant, Not Knocking Down Target).

### Tasks and Penalties
Each event task has specific rules, equipment standards, and penalties:
- **Stair Climb**: Carry Hi-Rise Pack to the top, place it in the designated box.
- **Hose Hoist**: Lift the hose roll using a hand-over-hand technique, adhering to height-specific adjustments.
- **Forcible Entry**: Use mallet to move beam by a set distance.
- **Run and Hose Advance**: Drag hose and hit target with water stream.
- **Victim Rescue**: Drag mannequin across the finish line.

### National Qualifying Times
- **Individual and Team Qualification**: Separate qualifying times per category for national events.
- **Seeding and Knockout Rounds**: Rounds to establish final rankings during national championships.

---

## Website Functionality

### User Stories

- **Competitor**: 
  - Can register for events, view profile, and track results.
  - Needs access to health questionnaires and waiver forms.

- **Event Organizer**:
  - Can manage event schedules, registration approvals, and scoring.
  - Tracks team and individual performance, including penalties.

- **Administrator**:
  - Full access to all functionalities, including user management and event records.

### Backend and Frontend Requirements

- **Authentication**: Password-protected accounts, reset options, and profile management.
- **Team and Event Management**:
  - Create, edit, and delete events with detailed descriptions.
  - Track competitor profiles, health clearances, and team registrations.
- **Payment System**:
  - Process and validate payments, generate invoices, and offer bulk registration options.

---

## Known Issues and Future Improvements

1. **Bugs**: Note issues found during testing, such as registration errors or payment processing delays.
2. **Enhancements**:
   - Streamlined user flow for multi-event registration.
   - Improved UI for penalty tracking and result display.

3. **Performance and Scalability**:
   - Address any slow-loading pages or database indexing needs.
   - Plan for handling high user loads, especially during registration windows.

---

## FAQ

### Account and Registration FAQs

- **Changing Email/Password**: Steps for updating login information.
- **Forgot Password**: Recovery process for lost credentials.

### Rules and Equipment FAQs

- **Eligibility**: Requirements for firefighters and pre-fire service students.
- **Gear**: Detailed equipment guidelines and NFPA compliance.

---

## Conclusion

This document will serve as the foundation for understanding and enhancing the FireFit Championship website. Refer to linked flowcharts and ER diagrams on Lucidchart for a visual breakdown of key processes.