# Safety, privacy and control

## Who can see a patient
- A clinician sees the patients of their own unit and the patients they are responsible for elsewhere (attending or co-managing doctor, consultant, assigned nurse). The care team follows the patient, so access moves with a transfer.
- Everyone else can find a patient in the index but cannot open the chart. In an emergency they can start **emergency access (break-glass)**: a written justification is required, the access is time-limited, and a reviewer examines it afterwards.
- Administrative tabs (identifiers, billing, access log) are hidden from clinical staff.

## Who can do what
- Roles carry permissions, and permissions are granted at a scope: the whole system, the hospital, a department, or a single piece of work (one shift, one consultation, one surgical case).
- **Separation of duties.** The person who prescribes is not the person who verifies; the person who raises a purchase is not the person who approves it; a controlled drug needs a second signature.

## What is recorded
- Every view and every change goes to an **append-only audit log**: who, what, when, which patient, and whether emergency access was used. Denied attempts are logged too.
- Medication administrations are immutable once charted. Mistakes are corrected by a new entry, never by editing history.

## Safety nets in the clinical workflow
- **Pharmacy verification** before a dose can be given; an emergency dose needs a written reason that pharmacy reviews.
- **Allergy checks** at charting, with an override reason when a match is overridden.
- **Double-dose guard** for the same dose charted twice.
- **Critical results** must be acknowledged by a clinician; unacknowledged ones are escalated after a target time.
- **Early warning (NEWS2)** is calculated from the latest vital signs and raises an alert at medium and high scores.
- **Look-alike / sound-alike and high-alert medication** flags.

## Accounts
Hashed passwords, temporary passwords that must be changed at first sign-in, lockout after repeated failures, rate-limited sign-in, short-lived tokens bound to a server-side session that can be revoked, and an optional second factor.

## Demonstration data only
This showcase and the demonstration installation contain only fictitious people. The system is **not a certified medical device** and must not be used for patient care.
