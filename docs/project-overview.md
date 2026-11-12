# System Overview & Architecture — Salma ERP

## 1. System Context

This document describes the system-level structure and architectural overview of Salma ERP.

It focuses on how the ERP system is organized, how its major components interact, and how customized functionalities are integrated with the standard ERPNext framework.

Unlike the repository README, this document focuses on the system's internal organization and architectural perspective.

## 2. System Architecture

Salma ERP is built on the Frappe Framework and extends ERPNext's existing capabilities through custom application logic, configurations, and business-specific functionalities.

The system can be understood through the following layers:

### 2.1 Presentation Layer
- ERPNext Desk interface.
- Forms, lists, dashboards, and reports.
- Client-side scripts and UI customizations.
- Jinja-based templates and Print Formats.

### 2.2 Application Layer
- Frappe Framework and ERPNext application logic.
- Custom DocTypes and document controllers.
- Python server-side methods.
- JavaScript client-side logic.
- Hooks, workflows, and permission configurations.

### 2.3 Data Layer
- MariaDB database.
- DocType-based data storage.
- Relationships between business records.
- Transactional and master data.

### 2.4 Integration Layer
- Frappe REST APIs.
- Whitelisted server-side methods.
- Communication between frontend and backend components.
- Other integrations, where applicable.

## 3. Functional Module Organization

The system is organized into different business areas. Each module addresses specific operational requirements.

The major areas relevant to this documentation include:

- HR Management
- Payroll Management
- Certificate Management
- Dyeing Management

Each area may contain standard ERPNext functionality alongside project-specific customizations.

## 4. Business Process Architecture

Business processes are implemented through DocTypes, document relationships, workflows, validations, and server-side logic.

Examples of process areas include:

- Recruitment and employee lifecycle processes.
- Payroll-related operations.
- Stock-related certificate management.
- Dyeing-related operational processes.

Detailed process flows are documented separately in the relevant module documents and diagrams.

## 5. Data Organization

Frappe uses DocTypes as the foundation for organizing application data.

The system's data organization includes:

- Standard ERPNext DocTypes.
- Custom DocTypes developed for business-specific requirements.
- Link fields and document relationships.
- Child tables for related records.
- Naming and validation rules.
- Role-based access to records.

The exact DocType relationships should be documented using approved system diagrams without exposing confidential company data.

## 6. Customization Architecture

Project-specific functionality is implemented by extending the existing ERPNext/Frappe framework.

Customization areas include:

- Custom DocTypes and fields.
- Python-based server-side logic.
- JavaScript-based client-side behavior.
- Custom API methods.
- Hooks and event handlers.
- Workflow and permission configurations.
- Reports and Print Formats.

The implementation details and individual examples are covered in `technical-contributions.md`.

## 7. Development and Collaboration Workflow

Development activities are organized collaboratively based on assigned requirements and tasks.

The general development workflow involves:

1. Understanding and reviewing assigned requirements.
2. Implementing the required customization.
3. Integrating changes with the existing application.
4. Testing the implemented functionality.
5. Reviewing and refining changes.
6. Managing development tasks and collaboration through Jira and Git.

## 8. Module Documentation and Diagrams

Detailed functional descriptions and workflow diagrams are maintained separately.

| Resource | Purpose |
|---|---|
| `hr-module.md` | HR functionality and individual contributions |
| `payroll-module.md` | Payroll-related functionality and contributions |
| `certificate-management.md` | Certificate management functionality |
| `dyeing-module.md` | Dyeing-related functionality |
| `technical-contributions.md` | Technical implementation details |

## 9. Architecture Documentation Notes

This document presents a high-level architectural view of the system.

Detailed implementation, internal business rules, actual database structures, and company-specific configurations are intentionally excluded where they may contain confidential information.
