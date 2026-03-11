# Product Requirements Document (PRD) - TODO App Upgrade (Due Dates, Priority, and Filters)

## 1. Overview

We are upgrading the existing TODO app from a minimal task model (title + completed) to a simple, teachable enhancement set that improves day-to-day task planning without increasing implementation complexity.

This PRD is based on the requirements meeting transcript and follow-up Slack scope lock. The meeting identified desired capabilities, and the Slack thread finalized what is MVP vs Post-MVP vs out of scope.

Primary goals:
- Help users identify urgent work with due dates.
- Help users triage work with simple priority levels.
- Help users focus quickly using date-based filters.
- Keep the implementation lean: local-only storage and no backend changes.

---

## 2. MVP Scope

- Add a task field: dueDate.
- dueDate is optional.
- dueDate must use ISO format: YYYY-MM-DD.
- If dueDate is invalid, ignore it and treat the task as having no dueDate.
- Add a task field: priority.
- priority is an enum with values: P1, P2, P3.
- Default priority value is P3.
- Add filter views: All, Today, Overdue.
- Filter behavior: All includes completed and incomplete tasks.
- Filter behavior: Today and Overdue show incomplete tasks only.
- Keep data storage local only.
- Do not introduce backend or external storage changes.
- Data validation: title is required.
- Data validation: priority must be one of P1, P2, P3 (default P3).
- Data validation: dueDate is optional and must be valid ISO YYYY-MM-DD when present.

---

## 3. Post-MVP Scope

- Add visual highlighting for overdue tasks.
- Sorting rule: overdue tasks first.
- Sorting rule: then priority order (P1 to P3).
- Sorting rule: then due date ascending.
- Sorting rule: tasks without dueDate last.
- Consider color-based priority badges (for example: red for P1, orange for P2, gray for P3) as part of enhanced visual presentation.

---

## 4. Out of Scope

- Notifications/reminders.
- Recurring tasks.
- Multi-user support.
- Keyboard navigation enhancements.
- External storage integrations.
