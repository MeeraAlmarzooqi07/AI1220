# CampusPulse stakeholder analysis

Name or team: CampusPulse lab submission
Date: 2026-09-08

Stakeholder types: end user, operations, business, regulator, negative stakeholder

Power-interest quadrants: key player, keep satisfied, keep informed, minimal effort

## S1

- Stakeholder: Student attendee
- Stakeholder type: End user
- Power-interest quadrant: Keep informed
- Main goal: Find relevant campus announcements and events in one place and RSVP without repeatedly checking different communication channels.
- Main concern: An RSVP name may be exposed publicly; the service may also be difficult to use on a phone or with a screen reader.
- How you would involve or monitor this stakeholder: Include students in usability and accessibility testing, and monitor feedback about event discovery, RSVP privacy, and accessibility.

## S2

- Stakeholder: Group officer
- Stakeholder type: End user
- Power-interest quadrant: Key player
- Main goal: Create announcements and events and publish them to the correct audience.
- Main concern: An unauthorised officer may publish for the group, or RSVP'd students may miss an important time or location change.
- How you would involve or monitor this stakeholder: Review publication and correction workflows with approved officers during pilot testing and monitor publication errors and notification failures.

## S3

- Stakeholder: Campus moderator
- Stakeholder type: Operations
- Power-interest quadrant: Key player
- Main goal: Review reports, hide harmful events quickly, and preserve evidence for appeals.
- Main concern: A report may lack the reported content, reason, evidence, or a record of who made the moderation decision.
- How you would involve or monitor this stakeholder: Include moderators in workflow reviews and test report handling, immediate hiding, decision logging, evidence retention, and appeals.

## S4

- Stakeholder: Student Affairs
- Stakeholder type: Business
- Power-interest quadrant: Key player
- Main goal: Operate a trusted pilot for 5,000 students and 200 groups before Orientation Week.
- Main concern: Fake groups, missing verification, or an unreliable service could damage institutional trust.
- How you would involve or monitor this stakeholder: Obtain approval for the release scope and verification process, and monitor pilot readiness, group verification, adoption, and service performance.

## S5

- Stakeholder: Data Protection Officer
- Stakeholder type: Regulator
- Power-interest quadrant: Keep satisfied
- Main goal: Ensure that the service collects only necessary personal data and applies appropriate retention and privacy controls.
- Main concern: RSVP lists may be public by default, or cancelled-event attendance data may be retained longer than necessary.
- How you would involve or monitor this stakeholder: Review privacy and retention requirements before release, test privacy controls, and monitor privacy incidents and deletion records.

## S6

- Stakeholder: Abuse cases, including impersonators and compromised group accounts
- Stakeholder type: Negative stakeholder
- Power-interest quadrant: Minimal effort
- Main goal: Misuse the service to publish phishing events, impersonate verified groups, or repeat announcements.
- Main concern: Abuse could mislead students and reduce trust in verified content.
- How you would involve or monitor this stakeholder: Do not involve malicious actors in normal requirements decisions; monitor impersonation reports, repeated posts, suspicious activity, and moderation alerts.

## Conflicts to resolve

Describe at least two real tensions. For each one, name both sources and either propose a decision or write a specific question that should go back to the stakeholders.

### Conflict 1

- Stakeholders: S1 and S5
- What conflicts: S1 wants a convenient RSVP feature, while S5 requires RSVP information to remain private and personal data collection to be minimised.
- Proposed decision or follow-up question: RSVP lists will be private by default. A student must explicitly choose to make their RSVP visible. The service will collect only the attendance data needed for event management and notifications.

### Conflict 2

- Stakeholders: S2 and S3
- What conflicts: S2 wants approved officers to publish and correct event information quickly, while S3 needs to control harmful content and preserve evidence for moderation and appeals.
- Proposed decision or follow-up question: Approved officers may publish and edit their own group's content, but moderators may hide reported content immediately. The original content, report evidence, and moderation decision must remain available for an appeal.

### Conflict 3

- Stakeholders: S4 and S5
- What conflicts: S4 wants reliable verification and a useful pilot, while S5 wants to minimise the personal data retained about students and groups.
- Proposed decision or follow-up question: Use university sign-in and retain verification and attendance records only for defined operational purposes. Confirm the exact retention period for non-cancelled events before implementation.
