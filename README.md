# AI-Assisted JIRA Ticket Creation with Cursor

## Overview

This repository enables users to leverage **Cursor** as the user interface for creating JIRA tickets of the following types:
- **EPIC**
- **USER STORY**
- **GENERAL TASK**
- **SPIKE**
- **BUG**

The system uses AI to ensure that all required fields for each ticket type are populated according to your project’s standards. For **USER STORY**, **GENERAL TASK**, **SPIKE**, and **BUG** ticket types, the AI always provides a reasonable, relative measure of effort (using Story Points), rather than exact hours, to support agile estimation practices.

## What are Cursor Rules?

[Cursor Rules](https://docs.cursor.com/context/rules) are a way to provide context and enforce standards for AI-powered workflows in Cursor. Rules can:
- Define how the AI should behave in your workspace
- Enforce best practices and required fields
- Guide the AI to ask clarifying questions and ensure completeness

In this repository, Cursor Rules ensure that all JIRA tickets are created with the required fields, structure, and estimation practices that match your team's standards.

## What is `.cursor/rules/jira-ticket.mdc`?

The `.cursor/rules/jira-ticket.mdc` file is a configuration file that defines your team's JIRA ticket requirements, field definitions, and best practices. It tells the AI assistant exactly how to structure tickets, what information to request, and how to estimate effort. This ensures consistency and quality across all generated tickets.

### How to Set Up Your Configuration
1. **Copy** the `.cursor/rules/jira-ticket.sample` file to a new file named `.cursor/rules/jira-ticket.mdc` in the same directory.
2. **Edit** `.cursor/rules/jira-ticket.mdc` to match your team’s JIRA practices. You can:
   - Add or remove required fields
   - Update field definitions and expectations
   - Include examples of well-scoped, well-estimated JIRA tickets from your team
3. **Save** the file. Cursor will use this configuration to guide ticket creation.

> **Note:** The `.cursor/rules/jira-ticket.mdc` file is included in `.gitignore` by default, so your team can customize it without affecting version control.

### Example of a Well-Scoped JIRA Ticket

```md
**Summary**: Add user management page to admin UI
**Description**: Implement a new admin page for managing user accounts, including create, read, update, and delete (CRUD) operations. The page should allow searching, filtering, and editing user details.
**Supporting documentation**: No docs provided; please add if available.
**Definition of Done**: As an admin, I want to manage users from a single page so that I can efficiently control access.
**Acceptance Criteria**:
- Admin can view a paginated list of users
- Admin can create, edit, and delete users
- Form validation for email and required fields
- Success and error feedback for all actions
**Requirements**: React frontend, REST API integration
**End to End Test**: Admin creates a user, edits details, and deletes the user
**Severity**: Important
**Component/s**: User Management UI
**Labels**: AI-Generated
**Story Points**: 5
```

## Example Prompts to Try

- Create an epic and user stories to capture the requirements and tasks for adding a new web UI page to control user management with usual CRUD functionality.
- Write a JIRA bug ticket for when the email field in the user creation form shows a red border but no error message.
- Generate a user story for adding search and filter functionality to the user management page.
- Create a spike ticket to investigate integrating SSO with the user management system.

## Getting Started
1. **Install and launch Cursor** (see [Cursor documentation](https://www.cursor.so/) for setup instructions).
2. **Open this repository** in Cursor.
3. **Configure your JIRA project** by editing your configuration file as described above.
4. **Use Cursor’s AI assistant** to create new JIRA tickets. The assistant will prompt you for any missing information and ensure all required fields are populated.

## Example Workflow
1. Open Cursor and start a new JIRA ticket creation session.
2. Select the ticket type (EPIC, USER STORY, GENERAL TASK, SPIKE, BUG).
3. Provide a brief description or context.
4. The AI assistant will generate a ticket with all required fields, including Story Points for applicable types.
5. Review, validate, and copy the ticket into your JIRA system.

## Support
For questions or issues, please refer to the `sample-cursor-config.md` for field definitions and configuration guidance. For Cursor-specific help, see the [Cursor documentation](https://docs.cursor.com/welcome).

---

**Empower your team to create clear, complete, and consistent JIRA tickets with AI and Cursor!** 