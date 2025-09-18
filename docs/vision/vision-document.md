<p align="center">
  <a href="https://github.com/pedrohcdsouza/nodio" rel="noopener">
    <img width=200px height=200px src="https://github.com/pedrohcdsouza/nodio/blob/main/nodio.svg">
  </a>
</p>

<a href="https://github.com/pedrohcdsouza/nodio/blob/main/docs/">Back</a>

# Vision Document

## Revision History  

| Date | Version | Description      | Authors |
| :--: | :----: | :--------------: | :-----: |
| 2025-09-18 | 0.0.1 | Initial version | Pedro Henrique Cardoso de Souza |

---

## 1. Project Objective  

Nodio is a web application designed to **unify diagramming and software development workflows**.  
Unlike traditional diagramming tools that produce static files, Nodio connects diagrams directly to **Git repositories** and allows them to **generate or update code automatically**.  

The goal is to make diagrams **first-class development artifacts**, ensuring they remain synchronized with the codebase and empowering development teams to use them not only for visualization but also as part of their daily workflow.  

The platform will be **self-hostable** and **developer-friendly**, enabling teams to version, collaborate, and code directly from their diagrams.  

---

## 2. Problem Description  

|     |      |
| --- | --- |
| **Problem**   | Diagrams created with traditional tools (e.g., draw.io, Astah, Visio) are static and often outdated, disconnected from real source code. |
| **Affects**   | Software developers, architects, and technical teams. |
| **Impacts**   | Causes misalignment between documentation and implementation, duplicated effort, and loss of trust in diagrams as a reliable source of truth. |
| **Solution**  | Provide a system where diagrams are versioned, linked to Git repositories, and capable of updating or generating code, transforming them into active parts of the software lifecycle. |

---

## 3. User Description  

| Role       | Description                                                                 | Responsibility |
| ---------- | --------------------------------------------------------------------------- | -------------- |
| Visitor      | External user with no direct involvement in the project. Can only see the landing page and system overview. | Explore public-facing summary of Nodio, but cannot access diagrams. |
| Developer  | Uses the platform to create and maintain diagrams tied to their projects.   | Keep diagrams updated and integrate them with the codebase. |
| Administrator | Manages the platform, user access, and repository integration.              | Configure system, control permissions, and oversee projects. |

---

## 4. User Environment  

**Visitor:**  
A minimal interface showing only the landing page with system summary and public information.   

**Developer:**  
A modern web interface with diagram editing tools, Git integration, and options to generate/update code.  

**Administrator:**  
An overview dashboard to manage projects, control permissions, access version history, and track changes across diagrams.  

---

## 5. Main User Needs  

**Visitor:**  
- Access a clear and concise overview of Nodio.  
- Understand the platform’s purpose and capabilities without seeing internal diagrams.  

**Developer:**  
- Create diagrams that can generate or update code.  
- Keep diagrams versioned and in sync with Git repositories.  
- Collaborate in real time with other team members.  

**Administrator:**  
- Ensure diagrams serve as living documentation.  
- Access version history and compare diagram versions.  
- Track system evolution alongside source code.  
- Manage user permissions and system configurations.  

---

## 6. Competing Alternatives  

- **Mermaid**  
  - Diagram-as-code  
  - Git integration via Markdown  
  - Limited interactivity and automation  

- **Astah UML**  
  - UML diagramming features  
  - Focused on modeling, but not on Git or code sync  

- **IBM Systems Design Rhapsody**  
  - Can generate code in C, C++, Java, Ada, and C# from models  
  - Desktop-based, not directly integrated with Git workflows for automatic code updates  

---

## 7. Product Overview  

A **unified platform for versioned, code-aware diagramming**, enabling teams to:  
- Design system architectures, workflows, and database schemas.  
- Version diagrams like source code (using Git).  
- Keep documentation and implementation synchronized.  

---

## 8. Functional Requirements  

| Code | Name | Description | Priority |
| :--: | :--: | :---------: | :------: |
| F01 | Project Creation | Allow users to create new projects connected to Git repositories. | High |
| F02 | Diagram Editor | Provide a web-based editor for creating and editing diagrams. | High |
| F03 | Git Versioning | Enable push, pull, and commit history tracking for diagrams. | High |
| F04 | Code Generation | Generate boilerplate code (e.g., classes, schemas) from diagrams. | High |
| F05 | Code Synchronization | Update existing code when diagrams change. | High |
| F06 | Collaboration | Support multiple users editing and commenting on diagrams. | Medium |
| F07 | Version Comparison | Allow users to compare diagram versions and visualize differences. | Medium |
| F08 | Project Dashboard | Provide an overview with recent changes, contributors, and sync status. | Medium |
| F09 | API Access | Expose APIs to integrate Nodio with external tools (CI/CD, IDEs). | Medium |
| F10 | Notifications | Notify users about updates, conflicts, or sync issues. | Low |

---

## 9. Non-Functional Requirements  

| Code | Name | Description | Category | Classification |
| :--: | :--: | :---------: | :------: | :------------: |
| NF01 | Data Security | Protect user and repository data with encryption and secure practices. | Security | Mandatory |
| NF02 | High Availability | Ensure the system is available 99.9% of the time for continuous use. | Reliability | Mandatory |
| NF03 | Responsive Interface | The system must be usable on desktops, tablets, and smartphones. | Usability | Mandatory |
| NF04 | Performance | Diagram editing and Git operations should respond in near real time. | Performance | Recommended |
| NF05 | Backup | Automatic daily backup of diagrams and linked repository data. | Security | Recommended |
| NF06 | Accessibility | Follow accessibility guidelines (WCAG) for inclusive use. | Usability | Recommended |
| NF07 | Privacy Controls | Ensure access rights per project and user role. | Security | Recommended |
| NF08 | Scalability | Support sudden growth in active users without loss of performance. | Performance | Recommended |
| NF09 | Integration APIs | Support integration with external systems (CI/CD, IDEs, project management). | Extensibility | Recommended |

---