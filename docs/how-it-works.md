# How it works, role by role

All people and data below are fictitious (demonstration installation).

## Nurse (ICU)
1. **Dashboard.** The home screen shows the **Tasks to do** card (red when something is due and not charted), beds occupied, nurses on the shift against the unit's ratio, patients with a NEWS2 score of 7 or more, and a list of patients who need attention now.
2. **Tasks to do.** One row per task: the time, the bed, the task. Doses come from the prescriptions' schedule, IV lines from their planned re-site date, STAT specimens from the orders. A task is red from its due time until it is charted, and it leaves the list by itself.
3. **Charting.** "Open" takes the nurse to the right tab of the patient's chart (medications, lines, services). A dose that pharmacy has not verified yet shows a badge; it can only be given in an emergency, with a written reason that pharmacy reviews afterwards.
4. **Unit board.** Every bed with its patient, attending doctor, nurse for the shift, last vital signs and coloured alerts: red means act now, amber needs attention, blue is new information.

## Doctor
1. **Dashboard.** My patients, critical results waiting for me, consult requests, notes waiting for my signature.
2. **Results back.** What came back in the last 24 hours, critical results first. A critical result turns red when it has waited longer than the laboratory's acknowledgement target.
3. **NEWS2.** My patients ordered by early-warning score, so the one who is deteriorating comes first.
4. **Orders.** Laboratory, imaging and medication orders. CT and MRI need the insurer's approval, recorded by billing; STAT orders are exempt.

## Moving a patient
A doctor places a **transfer order**. The receiving unit accepts it and gives the patient a bed, and the handover is recorded. The chart moves with the patient: the old unit loses access, the new one gains it. No re-registration.

## Emergency department
Patients are triaged on a five-level scale. The board puts untriaged patients first, then the most urgent, and shows how long each has waited.

## Pharmacy and laboratory
- **Pharmacy** reviews and dispenses prescriptions. A prescriber can never review or dispense their own order.
- **Laboratory** enters and verifies results. A result beyond the configured critical limits notifies the ordering doctor at once and must be acknowledged; if it is not, it is escalated.

## Operating theatre
Cases are booked with a team. A safety checklist gates the start of a case; the intra-operative record and the recovery score are kept with the case.

## Billing
Charges are posted to the patient's stay. At discharge the final bill is split between the insurer and the patient according to the coverage the insurer pays.

## Administration
User accounts, roles and scoped role assignments, the audit log and the review of emergency ("break-glass") access.
