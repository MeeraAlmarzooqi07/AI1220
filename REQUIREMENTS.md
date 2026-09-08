# CampusPulse requirements

Name or team: CampusPulse lab submission

Date: 2026-09-08

Status: completed draft

Use the source IDs `S1` to `S6` from the lab handout. Keep every requirement short enough to test and trace.

## 1. Release scope

### In scope

- Verified groups can publish announcements and events.
- Students can follow verified groups and RSVP to events.
- Events can be public or members-only.
- Students who RSVP can receive notifications when event details change.
- Moderators can review reports, hide harmful events, preserve evidence, and support appeals.
- The service uses university sign-in and supports the pilot of 5,000 students and 200 groups.

### Out of scope

- Direct messaging between students and groups.
- External users who do not have university sign-in.
- Payments or ticket sales.
- Video hosting.
- AI-based recommendations.
- A native mobile application.

## 2. User requirements

- UR-1 [Must] Students can follow verified groups and view their announcements and events. [Source: S1]
- UR-2 [Must] Students can RSVP to events without their names appearing publicly by default. [Source: S1, S5]
- UR-3 [Must] Approved group officers can publish announcements and events to a selected audience. [Source: S2]
- UR-4 [Must] Students who RSVP are informed when an event's time, location, or cancellation status changes. [Source: S2]
- UR-5 [Must] Moderators can review reports, hide harmful events, and retain evidence for appeals. [Source: S3]
- UR-6 [Should] Student Affairs can identify verified groups before their official content is published. [Source: S4]
- UR-7 [Must] Attendance data for a cancelled event is deleted within 30 days of cancellation. [Source: S5]

## 3. Functional requirements

- FR-1 [Must] The system shall allow an authenticated student to follow or unfollow a verified group. [Source: UR-1]
- FR-2 [Must] The system shall allow an authenticated student to RSVP to an event and shall keep the RSVP hidden from public viewers unless the student explicitly chooses otherwise. [Source: UR-2]
- FR-3 [Must] The system shall allow only approved officers of a verified group to publish announcements or events for that group. [Source: UR-3]
- FR-4 [Must] The system shall notify students who have RSVP'd when the event time, location, or cancellation status changes. [Source: UR-4]
- FR-5 [Must] The system shall allow a moderator to view a report, hide the reported event, record the moderation decision, and retain reported evidence for an appeal. [Source: UR-5]
- FR-6 [Should] The system shall display the verification status of each group before its official announcements or events are published. [Source: UR-6]
- FR-7 [Must] The system shall delete attendance data associated with a cancelled event within 30 days of cancellation. [Source: UR-7]

## 4. Non-functional requirements

- NFR-1 [Must] The system shall display the event list within 2 seconds for at least 95% of requests during normal pilot usage by up to 5,000 students and 200 groups. [Measure: response time is no more than 2 seconds for 95% of event-list requests under normal pilot usage] [Source: UR-1]
- NFR-2 [Must] The system shall allow a screen-reader user to complete the follow and RSVP workflows using keyboard navigation and accessible labels. [Measure: 100% of critical follow and RSVP controls pass the agreed accessibility test cases] [Source: UR-2]
- NFR-3 [Should] The system shall make a moderator's confirmed hide action effective within 60 seconds. [Measure: the reported event is hidden from ordinary users within 60 seconds in at least 95% of moderation tests] [Source: UR-5]
- NFR-4 [Must] The system shall prevent an unauthorised public viewer from viewing a student's private RSVP. [Measure: 0 successful unauthorised disclosures in privacy test cases] [Source: UR-2]

## 5. User stories and acceptance criteria

### US-1 [Source: S1, UR-1, UR-2]

As a student attendee,

I want to follow verified groups and RSVP to events privately,

so that I can find useful activities without exposing my attendance.

Acceptance criteria:

- Given that I am signed in, when I follow a verified group, then its announcements and events appear in my followed-group view.
- Given that I RSVP to an event, then my name is not shown in a public RSVP list unless I explicitly choose to make it visible.
- Given that I am using keyboard navigation or a screen reader, then I can complete the follow and RSVP actions.

### US-2 [Source: S2, UR-3, UR-4]

As an approved group officer,

I want to publish an event to a selected audience and notify people who RSVP when it changes,

so that the correct students receive accurate information.

Acceptance criteria:

- Given that I am an approved officer, when I publish an event, then I can select whether it is public or members-only.
- Given that the event time, location, or cancellation status changes, then students who have RSVP'd receive the correction or cancellation notification.
- Given that I am not an approved officer, when I attempt to publish for the group, then publication is rejected.

### US-3 [Source: S3, UR-5]

As a campus moderator,

I want to review reports and hide harmful events while preserving evidence,

so that abuse is controlled and legitimate appeals can be investigated.

Acceptance criteria:

- Given a submitted report, when I open it, then I can see what was reported, the reason, and the available evidence.
- Given that I confirm a hide decision, then the event is hidden from ordinary users and the decision records my moderator identity.
- Given that the group appeals the decision, then the original reported content and evidence remain available to the appeal process.

## 6. MoSCoW summary

- Must: UR-1, UR-2, UR-3, UR-4, UR-5, UR-7, FR-1, FR-2, FR-3, FR-4, FR-5, FR-7, NFR-1, NFR-2, NFR-4.
- Should: UR-6, FR-6, NFR-3.
- Could: Improved group discovery and optional event reminders beyond correction and cancellation notifications.
- Won't this release: Direct messaging, external users, payments, video hosting, AI recommendations, and a native mobile application.

## 7. Traceability

| Stakeholder need | User requirement | System requirement | User story |
|---|---|---|---|
| S1 wants to find club events in one place. | UR-1 | FR-1, NFR-1 | US-1 |
| S1 and S5 require private RSVP information. | UR-2 | FR-2, NFR-2, NFR-4 | US-1 |
| S2 requires only approved officers to publish to the correct audience. | UR-3 | FR-3 | US-2 |
| S2 requires RSVP'd students to receive event changes. | UR-4 | FR-4 | US-2 |
| S3 requires reports, evidence, and moderation records. | UR-5 | FR-5, NFR-3 | US-3 |
| S5 requires cancelled-event attendance data to be deleted. | UR-7 | FR-7 | US-3 |

## 8. Assumptions and open questions

Separate decisions your team has assumed from questions that still need an answer.

### Assumptions

- A1: The pilot will support up to 5,000 students and 200 groups, as stated by S4.
- A2: The 2-second response-time target in NFR-1 is a team assumption because the brief provides no performance target.
- A3: The 60-second moderation target in NFR-3 is a team assumption because the brief provides no moderation timing target.
- A4: University sign-in will be available for the service, as stated in the first-release brief.
- A5: The service can send notifications to students who have RSVP'd.

### Open questions

- Q1: What peak concurrent usage and request volume must the service support during Orientation Week?
- Q2: What retention period should apply to attendance data for events that are not cancelled?
