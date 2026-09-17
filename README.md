Enterprise Helpdesk Deployment, Custom Portal Development & Automated Reporting Pipeline
This comprehensive document serves as a complete technical portfolio piece for your GitHub repository and LinkedIn profile. It chronicles the end-to-end architecture, deployment, custom front-end development, and automated reporting pipeline for your enterprise IT support helpdesk system.

📋 Executive Summary
This project delivers a robust, containerised internal IT helpdesk solution built from bare-metal hardware up to a polished, branded user portal and automated reporting pipeline. Designed to streamline service requests across healthcare service areas (GP Federation, Outpatients, Talking Therapies, and PCN), the solution combines Ubuntu Server, Docker, Zammad, PostgreSQL, custom HTML5/JavaScript front-end engineering, and an automated Python/OpenPyXL export engine.

🛠️ Major Project Milestones
Milestone 1: Bare-Metal Infrastructure & Remote Administration
Hardware & OS Deployment: Provisioned a dedicated host machine, installed a fresh distribution of Ubuntu Server LTS on an SSD, configured static local networking, and established robust SSH access for headless remote management from a secondary workstation.

Security & Environment Preparation: Configured firewall rules, system user permissions, and directory structures to support containerised workloads.

Milestone 2: Containerised Helpdesk Architecture (Zammad & PostgreSQL)
Docker & Docker Compose: Deployed Zammad—an open-source, feature-rich ticketing system—alongside a PostgreSQL database backend inside isolated Docker containers.

Persistence & Network Bridges: Configured Docker volumes to ensure database persistence across container lifecycle events and mapped internal ports for local intranet accessibility ([http://10.203.182.72:8080](http://10.203.182.72:8080)).

Milestone 3: Custom Front-End Portal & Dynamic Enhancements
Branded Interface: Designed a clean, accessible, modern UI featuring corporate colour gradients (#5B1E63 and #A8056B), Inter typography, and responsive layout grids.

Service Area Routing: Integrated a custom radio-button selection grid forcing users to specify their DHC Service Area (GP Federation, Outpatients, Talking Therapies, PCN), automatically injecting this metadata into the ticket payload.

Asynchronous Success Handling: Implemented a MutationObserver script to intercept Zammad's asynchronous success callbacks, extract the generated ticket number (e.g., #10042), and render a bespoke, celebratory success card personalised with the user's name.

Daily IT Fact & Tip Rotator: Engineered a dynamic script that calculates the day of the year (dayOfYear % totalFacts) to rotate through a curated repository of cybersecurity, hardware, and IT history facts daily.

World ICT Day Special Feature: Added precise date-checking logic to automatically override standard tips on 17th May to display celebratory greetings and special information for World ICT Day.

Milestone 4: Automated PostgreSQL-to-Excel Reporting Pipeline
Direct Database Extraction: Utilised a one-liner Bash/Python execution pipeline leveraging PostgreSQL container commands (\copy) to query ticket metadata, customer names, state IDs, priorities, and timestamps directly into a clean CSV format.

Advanced Spreadsheet Styling: Developed an automated Python script using pandas and openpyxl to format the exported data with custom corporate palette fills (subtle pink/plum zebra striping), thin borders, frozen header panes, and auto-fitted column widths.

Dynamic View Bounding & Watermarking: Implemented automated bounding to hide extraneous empty rows and columns beyond active dataset boundaries, alongside programmatic insertion of a 20% opacity semi-transparent corporate logo watermark.


This project showcases full-stack capability ranging from Linux systems administration and Docker containerisation to front-end UI/UX engineering and automated data pipelines.
