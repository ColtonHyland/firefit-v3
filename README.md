# FireFit Championships Project Planning and Documentation

## Overview

The **FireFit Championships** is a competition rooted in essential firefighting skills and tasks. Designed to test both physical and mental endurance, the competition includes individual and team events that challenge participants across a range of high-intensity activities reflective of real-life firefighting scenarios. 

This document details the project requirements for a comprehensive FireFit Championships website that enables competitor registration, team formation, event management, scoring, and results tracking. It serves as a roadmap to ensure the website meets all functional, technical, and administrative needs for both users and organizers.

---

## Purpose of the FireFit Website

The FireFit website is the central platform for competitors and administrators to engage with FireFit events. Its main purposes are to:
1. **Facilitate Competitor Registration**: Enable individuals and teams to create profiles, register for events, and complete health requirements.
2. **Support Event Management**: Provide tools for admins to create and manage events, oversee registrations, enforce competition rules, and track competitor performance.
3. **Automate Scoring and Results**: Streamline scoring with automatic calculations based on tasks, penalties, and qualifying times for national-level events.
4. **Enhance Business Operations**: Integrate payment processing, invoicing, and documentation to support smooth and professional event administration.

### User Flow Through the Website
1. **User Registration**: Competitors create accounts and complete their profiles, providing required medical clearances where necessary.
2. **Event Registration**: Competitors register as individuals or as part of a team for various event types and categories.
3. **Event Participation and Scoring**: During events, admins score competitors, applying penalties and calculating results based on qualifying standards.
4. **Results Tracking**: Competitors view scores and see if they qualify for national championships, with records available for analysis and reporting.

---

## Event Structure and Categories

The FireFit Championships offer a variety of events, with each type involving distinct tasks, penalties, and scoring. Here’s an overview of each event type, category, and associated rules:

### Event Types

1. **FireFit Relay**
   - **Description**: A relay event where teams of 3-5 competitors complete a series of seven tasks, passing a flashlight baton between members as they transition from one task to the next.
   - **Categories**:
     - Men’s, Women’s, Mixed, Over 40, Over 50, Industrial Relay, and more.

2. **Tech2 Relay**
   - **Description**: A 2-person technical relay focused on high coordination and precise teamwork, featuring a mid-course cylinder exchange.
   - **Categories**:
     - Open Men’s, Open Women’s, Mixed, Over 40, Over 50, etc.

3. **Individual Competition**
   - **Description**: Individual competitors complete all tasks solo, testing overall fitness and firefighting skills.
   - **Categories**:
     - Open Men’s, Open Women’s, Over 40, Over 50, Over 55, Over 60, and Chief’s categories.

4. **Team Competition**
   - **Description**: Teams of 3-5 from the same department compete, with the three fastest times among team members summed to form the team score.
   - **Categories**:
     - Divisions such as Fire School Relay, Industrial Relay, Over 40 Relay, and more.

### Categories and Divisions

- **Divisions**: Open Men, Open Women, Over 40, Over 50, Over 60, Industrial, Pre-Fire School.
- **National Qualifications**: Competitors and teams qualify for nationals based on specific time standards for their division and category.

---

## Registration Flow and Requirements

The registration process on the FireFit website covers both individual and team entries, along with detailed requirements for medical clearance and account management.

### Creating a Competitor Account
   - **Steps**:
     - New users register with basic details: email, first name, last name, and password.
     - Users confirm their accounts via email, then log in to complete a health questionnaire and any additional profile details.
   - **Special Medical Requirements**:
     - Competitors over 60 or those who are retired must provide a doctor’s clearance by uploading a medical release form.
   - **Profile Updates**:
     - Competitors must update their profiles each season, confirming personal information and completing a new health questionnaire.

### Event Registration Process
   - **Step-by-Step Registration**:
     1. **Login**: Competitors log in to their account.
     2. **Profile and Health Clearance**: Complete or update their Competitor Profile and health questionnaire.
     3. **Event Selection**: Choose from individual or team event types, selecting the specific competition (Relay, Tech2, Individual).
     4. **Team Formation**: For team events, competitors invite teammates, assign roles, and specify team categories.
     5. **Confirmation and Payment**: Review event details, add registration to cart, and complete payment.
   - **Payment Options**:
     - Competitors can pay using Visa, MasterCard, or Purchase Order/Cheque, with a processing time of up to 3 business days.
   - **Registration Confirmation**:
     - Competitors receive a confirmation email detailing their registration and payment status.

### Team Registration Requirements
   - Each team member must have a Competitor Profile and complete the health questionnaire.
   - Teams can participate in multiple events, but each team member must register separately for each entry.
   - Team registration allows for bulk payments and flexible teammate management through the platform.

---

## Flowcharts and ER Diagrams

To clarify user processes and backend relationships, the following diagrams will be created in Lucidchart.

### Lucidchart Flowcharts

1. **User Registration Flow**:
   - **Purpose**: Visualize the process from account creation to profile completion and health questionnaire.
   - **Steps**:
     - Account setup with email verification.
     - Health questionnaire completion.
     - Profile updates for returning users.
  
2. **Event Registration Flow**:
   - **Purpose**: Outline each registration step for individuals and teams, including validation steps and payment processing.
   - **Steps**:
     - Event type selection (individual or team).
     - Team formation and role assignments.
     - Payment processing and confirmation.

3. **Scoring and Penalty Calculation**:
   - **Purpose**: Demonstrate how scores are calculated and penalties applied during event scoring.
   - **Steps**:
     - Task completion for each event.
     - Penalty application based on infractions.
     - Calculation of individual and team scores.

4. **Admin Tools and Data Management**:
   - **Purpose**: Depict the workflow for creating and managing events, updating competitor records, and exporting data.
   - **Steps**:
     - Event creation and scheduling.
     - Competitor and score management.
     - Data export and reporting functionalities.

### Entity-Relationship Diagram (ERD)

1. **Entities**:
   - **User**: Stores login details, profile information, and competitor data.
   - **Competitor Profile**: Includes health questionnaire, personal details, and medical clearance.
   - **Event**: Defines event name, type, location, date, and related competition data.
   - **Team**: Links competitors to events, with fields for team roles and event participation.
   - **Score**: Tracks individual and team scores, penalties, and times.
   - **Admin**: Holds permissions for event management and user administration.

2. **Relationships**:
   - **User - Competitor Profile**: One-to-One.
   - **User - Event**: Many-to-Many (through team entries or individual participation).
   - **Event - Team**: One-to-Many.
   - **Team - Score**: One-to-Many, as each team or individual accrues scores per event.

## Competition Rules and Requirements

Each event within the FireFit Championships follows strict guidelines and standards to ensure a fair and safe competition environment. The rules cover eligibility criteria, required equipment, specific task instructions, and penalty systems.

### General Rules and Eligibility

1. **Eligibility**:
   - Open to active, medically cleared fire/rescue personnel and enrolled, medically cleared pre-fire service students.
   - Competitors over the age of 60 and retired firefighters are required to provide medical clearance from a doctor.
   - Each competitor must sign a waiver and release form acknowledging the “drug-free” status of the competition.

2. **Equipment Standards**:
   - **Required Gear**: Competitors must wear NFPA 1971-compliant firefighting equipment, including boots, helmet, gloves, turnout pants and jacket.
   - **Provided Equipment**: SCBA units are supplied by FireFit and must be used as instructed; competitors may bring their own NFPA-approved facepiece.
   - **Inspection**: All gear is inspected prior to participation, with disqualifications for non-compliance, such as missing liners, frayed hems, or improper labeling.

3. **Event-Specific Penalties**:
   - Penalties are incurred for infractions, such as missing steps, failing to complete tasks, or interference with other competitors.
   - Each task has specific penalties; for example:
     - False Start: 2-second penalty.
     - Not touching every step when descending: 2 seconds per missed step.
     - Failing to hit a target with the water stream: 2-second penalty.
   - Un-sportsmanlike behavior or tampering with equipment can lead to disqualification at the discretion of the Course Marshal.

### Task-Specific Rules and Penalties

Each task within the events has defined rules to ensure uniformity in scoring and safety.

1. **Stair Climb**:
   - **Description**: Competitors must carry a 42-pound Hi-Rise Pack up six flights to the top of a tower.
   - **Penalty**: Failure to place the pack in the designated box at the top results in a 2-second penalty.
   - **Other Rules**: Competitors may use handrails and must touch each step on the descent, with penalties for missed steps.

2. **Hose Hoist**:
   - **Description**: Using a hand-over-hand technique, competitors hoist a 42-pound donut roll up a tower.
   - **Penalty**: If any part of the roll touches the deck, a 2-second penalty applies; dropping the roll off the platform results in disqualification.
   - **Special Provision**: Competitors under 5’6” are allowed to stand on the Hi-Rise pack for better reach.

3. **Forcible Entry**:
   - **Description**: Competitors use a 9-pound mallet to drive a beam a specified distance.
   - **Penalty**: A 2-second penalty if the mallet does not stay within the designated area after use.

4. **Run Hydrants**:
   - **Description**: Competitors run a 140-foot course around hydrants.
   - **Penalty**: Missing or knocking over a hydrant incurs a 2-second penalty per infraction.

5. **Hose Advance**:
   - **Description**: Competitors drag a charged hose line, aiming the stream at a designated target.
   - **Penalty**: A 2-second penalty for missing the target or failing to close the nozzle before passing the flashlight baton.

6. **Victim Rescue**:
   - **Description**: Competitors drag a 175-pound mannequin 100 feet to simulate a rescue.
   - **Penalty**: Carrying the mannequin incorrectly or “spiking” it results in a 2-second penalty.

---

## National Qualifying Standards

To qualify for the National Championships, competitors and teams must meet specified time standards. The qualifying process includes regional events where competitors can secure a spot based on performance.

### Individual and Team Qualification

1. **Qualifying Times by Category**:
   - **Open Men**: Under 2:30 minutes.
   - **Open Women**: Under 5:30 minutes.
   - **Chief’s Category**: Under 5:00 minutes.
   - **Over 40, Over 50, and Other Categories**: Times vary, generally increasing by category.

2. **Relay Teams**:
   - **Open Men’s Relay**: Under 1:50 minutes.
   - **Mixed Relay** (minimum 1 woman): Under 2:20 minutes.
   - **Over 50 Relay**: Under 2:30 minutes.
   - **Tech2 Relay**:
     - Open Men: Under 2:00 minutes.
     - Open Women: Under 3:00 minutes.
     - Mixed: Under 2:30 minutes.

3. **Seeding and Knockout Rounds**:
   - Seeding rounds are held during nationals to rank competitors and determine starting positions.
   - Knockout rounds progress based on performance, with penalties and timing used to narrow down the field to the top competitors.

---

## Website Functionality

The website is designed to meet all user needs, from registration to results tracking, with user-friendly interfaces and automated processes to streamline management.

### User Stories

1. **Competitor**:
   - Registers for events, creates or updates profile, and tracks personal results.
   - Accesses health questionnaire and waiver forms to complete registration requirements.
   - Pays for individual or team event participation and receives email confirmation.

2. **Event Organizer**:
   - Manages event details, including scheduling, team assignments, and scoring.
   - Monitors event progress, tracks team and individual performance, and applies penalties where necessary.
   - Updates competitor information and coordinates event logistics to ensure smooth operation.

3. **Administrator**:
   - Manages user accounts, competitor records, and health clearance validations.
   - Handles event creation, user permissions, and advanced features such as data export and report generation.

### Backend and Frontend Requirements

1. **Authentication**:
   - Password-protected accounts with secure login, password reset, and session management.
   - Separate access levels for competitors, organizers, and admins, with permission-based functionality.

2. **Team and Event Management**:
   - Event creation, modification, and deletion with detailed descriptions, task breakdowns, and scheduling.
   - Real-time event monitoring with live score updates, penalty tracking, and leaderboard displays.

3. **Competitor and Health Management**:
   - Profile management tools for updating personal details, uploading health questionnaires, and tracking event history.
   - Required medical clearance for specific groups, with admin approval.

4. **Payment System**:
   - Secure processing and validation for payments, including invoicing options.
   - Bulk payment processing for team registrations and options for purchase orders.

5. **Scoring and Penalty Automation**:
   - Automated score calculation based on task completion times and penalties.
   - Penalty application for each task, with adjustments reflected in final scores.
   - Results calculation for individual, team, and relay events, and display on competitor dashboards.

---

## Known Issues and Future Improvements

1. **Potential Bugs**:
   - Issues may include registration errors, payment delays, or profile update problems, which will be tracked in a GitHub issue tracker.
   
2. **Enhancements**:
   - **Multi-Event Registration**: Simplify flow for competitors registering in multiple events.
   - **Penalty Visualization**: Display penalty breakdowns for competitors to review post-event.
   - **Scalability**: Ensure the site can handle large user loads, especially during registration and event days.

3. **Performance and Scalability**:
   - Improvements to page loading times, especially during high-traffic periods.
   - Optimize database indexing and use of caching to handle large datasets efficiently.

---

## FAQ

### Account and Registration FAQs

1. **How do I change my email or password?**
   - Login to your FireFit Competitor Account, navigate to User Profile, and update your information.

2. **How do I reset a lost password?**
   - Use the “Forgot Password” option on the login page to receive a reset link via email.

3. **How do I add or update team members?**
   - During event registration, navigate to the Team Registration section, where you can add or modify teammates.

### Rules and Equipment FAQs

1. **Who is eligible to compete in FireFit Events?**
   - Active firefighters and medically cleared pre-service students, 19 years or older, who meet health requirements.

2. **What are the equipment requirements?**
   - All competitors must use NFPA-approved gear (boots, helmet, gloves, SCBA), with any missing or non-compliant equipment resulting in disqualification.

3. **Can I participate if I don’t receive an activation email?**
   - Check your spam folder; if it’s not there, contact FireFit support at admin@firefit.com.

---
