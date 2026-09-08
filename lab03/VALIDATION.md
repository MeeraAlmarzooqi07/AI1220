# CampusPulse requirements review

Name or team: CampusPulse lab submission

Reviewer: Requirements team

Date: 2026-09-08

Review the completed `stakeholders.md` and `REQUIREMENTS.md`. Refer to specific IDs and evidence in every answer. A yes or no by itself is not enough.

## Validity

Do the requirements represent what the stakeholders need? Which IDs did you check, and what evidence supports them?

Response:

The requirements represent the main stakeholder needs in the source notes. UR-1 and UR-2 reflect S1's need to follow clubs, find events, and keep RSVP information private. UR-3 and UR-4 reflect S2's need for controlled publication, audience visibility, and notifications when the place or time changes. UR-5 reflects S3's need to review reports, hide events, preserve evidence, and record moderation decisions. UR-6 reflects S4's requirement for verified groups, while UR-7 reflects S5's requirement to delete cancelled-event attendance data within 30 days. The abuse risks described by S6 are addressed through the permission boundary in FR-3 and the reporting and moderation process in FR-5.

## Consistency

Do any requirements contradict one another or the release scope?

Response:

The requirements are consistent with the first-release scope. UR-2 and FR-2 require RSVP privacy, and no requirement requires public RSVP lists. FR-3 limits publishing to approved officers, which agrees with S2's permission boundary. FR-6 and UR-6 require verification before official publication, which supports S4's trust goal. The Out of scope list and the Won't list both exclude direct messaging, external users, payments, video hosting, AI recommendations, and a native mobile application. None of the functional or non-functional requirements depends on those excluded capabilities.

## Completeness

Is an important actor, normal flow, failure, permission, privacy rule, or boundary missing?

Response:

The normal student flow is covered by UR-1, UR-2, FR-1, and FR-2. The officer permission failure is covered by FR-3 and the third acceptance criterion of US-2. Event corrections and cancellations are covered by UR-4 and FR-4. The privacy rule is covered by UR-2, FR-2, NFR-2, and NFR-4. The moderation, evidence, and appeal case is covered by UR-5, FR-5, and US-3. The retention boundary is covered by UR-7 and FR-7. The main remaining boundary is Orientation Week peak traffic; because the brief gives no peak figure, it is recorded as open question Q1 rather than being hidden inside an unsupported requirement. Q2 also asks for the retention period for attendance data from events that are not cancelled.

## Realism

Can the proposed release and its quality targets reasonably be delivered? Mark unsupported targets as assumptions or open questions.

Response:

The proposed first release is realistic because it is a browser-based service for verified groups, announcements, events, following, RSVP, visibility, corrections, reports, moderation, and appeals. The brief explicitly excludes more complex features such as direct messages, payments, video hosting, and AI recommendations. The pilot size of 5,000 students and 200 groups comes from S4 and is recorded as A1. The 2-second response target in NFR-1 and the 60-second moderation target in NFR-3 are team assumptions, not figures supplied by a stakeholder; they are recorded as A2 and A3. The actual Orientation Week traffic is still unknown and is recorded as Q1.

## Verifiability

Could a tester decide whether each requirement passes or fails? Identify any wording that is still vague.

Response:

FR-1 through FR-7 are verifiable through functional test cases: a tester can check following, RSVP privacy, officer permissions, notifications, moderation, verification display, and deletion timing. NFR-1 specifies a response-time target and percentage, NFR-2 specifies accessibility test coverage, NFR-3 specifies a maximum hide time and success percentage, and NFR-4 specifies zero unauthorised disclosures in privacy tests. The acceptance criteria in US-1 through US-3 use given/when/then conditions that can pass or fail. The remaining uncertainty is the phrase "normal pilot usage" in NFR-1 because the brief does not define Orientation Week peak traffic; Q1 must be answered before final performance testing.

## One requirement you revised

- Requirement ID: UR-4
- Before: Students can receive event updates.
- What was wrong or missing: The wording was vague. It did not identify which changes trigger a notification, who receives it, or what the notification is about, so a tester could not determine the expected behaviour.
- After: Students who RSVP are informed when an event's time, location, or cancellation status changes. [Source: S2]
- Evidence or stakeholder to confirm the change: S2 specifically requested that people who RSVP'd be informed when the place or time changes. The cancellation case was made explicit so that the requirement aligns with the event status behaviour in the first-release brief.

## Final check

- [x] Stakeholder conflicts have a decision or a follow-up question.
- [x] Scope exclusions agree with the Won't list.
- [x] Every FR and NFR traces to a user requirement.
- [x] Every NFR contains a measurable target and condition.
- [x] Traceability rows use IDs that exist in the document.
- [x] The revised requirement has also been updated in the traceability table.
