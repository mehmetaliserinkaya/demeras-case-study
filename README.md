# DEMERAS - Mobile Operations Case Study

DEMERAS is a role-based mobile operations app built as an MIS/YBS portfolio case-study. It explores how small businesses can move from informal chat and verbal follow-up toward clearer operational communication, role-aware conversations and documented demo evidence. Demo Freeze v1 focuses on Android smoke-tested direct and group conversation flows.

Current checkpoint: Final Smoke Evidence Package completed with 14/14 manually reviewed Android emulator screenshots marked PASS. The evidence covers owner dashboard, account modal, direct chat, group chat, multi-select remove, soft-delete behavior, Owner <-> Worker emergency lifecycle, and open/resolved incident filters.

---

## Problem Statement

Small-business teams often coordinate work through informal chat, phone calls or verbal reminders. This can make it hard to track who is responsible, which request belongs to which group, and whether an operational message actually reached the right person.

DEMERAS models that problem as a mobile product and turns it into a case-study for business analysis, product thinking and mobile development.

---

## Solution Overview

DEMERAS is designed as a controlled operations inbox rather than a general social chat app.

The app focuses on:

* Role-based access and communication.
* ChatList as the main operations surface.
* Direct conversation creation for focused one-to-one coordination.
* Group conversation creation for small team coordination.
* Evidence-driven checkpoints and Android smoke testing.

---

## Core Features Completed In Demo Freeze v1

* Login/session path verified during Android smoke testing.
* ChatList opened successfully.
* Owner dashboard / ChatList reviewed.
* Account modal reviewed.
* Direct conversation creation flow completed.
* Direct conversation reviewed.
* Group conversation creation flow completed.
* Group conversation reviewed.
* ChatDetail navigation verified.
* First group message sent successfully.
* Return to ChatList and new group card verified.
* Multi-select remove reviewed.
* Soft-delete behavior reviewed.
* Emergency send/visibility/take/resolve reviewed.
* Open incidents and resolved incidents filters reviewed.
* No red screen observed during the tested direct/group paths.

---

## Post-freeze Interaction Polish

After the initial demo freeze, the interaction layer was tightened for portfolio evidence:

* Soft-deleted messages no longer leave empty outgoing bubbles.
* Normal/job outgoing messages use conservative sent indicators only; reliable delivered/read receipt modeling is not claimed.
* Emergency send failures now show a safe user-facing alert instead of failing silently.
* Emergency send resets narrowed message filters so the new emergency remains visible.
* Resolved incident filter helper copy was corrected.

---

## Final Smoke Evidence Package

The final evidence package was collected separately as:

`DEMERAS_FINAL_SMOKE_EVIDENCE.zip`

The ZIP is kept outside the public repository as portfolio evidence. The final smoke evidence screenshots listed below are not stored in this public repo.

* `01_chatlist_owner_header.png` - PASS
* `02_account_modal_owner.png` - PASS
* `03_direct_conversation.png` - PASS
* `04_group_conversation.png` - PASS
* `05_multiselect_remove.png` - PASS
* `06_soft_delete.png` - PASS
* `07_owner_to_worker_emergency_visible.png` - PASS
* `08_worker_take_emergency.png` - PASS
* `09_worker_resolve_emergency.png` - PASS
* `10_worker_to_owner_emergency_visible.png` - PASS
* `11_owner_take_emergency.png` - PASS
* `12_owner_resolve_emergency.png` - PASS
* `13_open_incidents_filter.png` - PASS
* `14_resolved_incidents_filter.png` - PASS

This evidence is manual Android emulator smoke evidence, not production QA certification. Normal/job chat messages use conservative sent indicators; reliable delivered/read receipt modeling is not claimed.

---

## Emergency Lifecycle Proof

The latest smoke-tested flow verifies that an Owner-created emergency can be seen by a Worker, taken by the Worker and resolved by the Worker. It also verifies the reverse direction: a Worker-created emergency can be seen by the Owner, taken by the Owner and resolved by the Owner.

Status path: Active -> Taken -> Resolved / Aktif -> Üstlenildi -> Çözüldü.

---

## Direct Conversation Flow Proof

Android smoke-tested direct flow:

1. `+ Sohbet` CTA visible.
2. Eligible users listed.
3. User selected.
4. ChatDetail opened.
5. Empty/direct conversation state rendered.
6. No red screen observed.

---

## Group Conversation Flow Proof

Android smoke-tested group flow:

1. `+ Grup` CTA visible.
2. Group creation modal opened.
3. Group name input worked.
4. Eligible participants listed.
5. Participant selection worked.
6. Group creation submitted.
7. ChatDetail opened for the new group.
8. First group message sent.
9. Returned to ChatList and the new group card appeared.
10. No red screen observed.

---

## Tech Stack

* React Native / Expo.
* Supabase Auth.
* Supabase RLS/RPC boundaries.
* Role-based access design.
* Android smoke testing.
* Git checkpoint and evidence discipline.

---

## Architecture Summary

The application is organized around role-aware product flows:

* UI screens present the role-based operations experience.
* Conversation services handle direct and group creation boundaries.
* Supabase Auth provides identity/session behavior.
* Supabase RLS/RPC supports safer backend access patterns.
* Documentation records tested behavior, known deferred scope and demo readiness.

---

## Demo Freeze v1 Status

Status: reached and documented.

Demo Freeze v1 means the project has a stable, explainable portfolio checkpoint with Android smoke evidence for the direct and group conversation vertical slices. It does not mean production launch, customer deployment or app-store publication.

---

## Intentionally Deferred

* Media/photo upload hardening and broader attachment workflows.
* Incident center redesign.
* Broader Supabase PR19/21/22/23/24/25 work.
* Notification polish.
* Production hardening.
* Google Play release, unless completed in a future checkpoint.
* Full employee/business-systems management surface, currently archived/vNext.

---

## What I Learned

* How to translate a business communication problem into scoped product flows.
* How to define demo evidence instead of relying on vague “it works” claims.
* How to build React Native / Expo flows backed by Supabase Auth and role-aware service boundaries.
* How to separate completed demo proof from deferred technical work.
* How to keep portfolio language honest and useful for CV, internship and interview contexts.

---

## Honest Disclaimer

DEMERAS is presented as a portfolio/demo project and MIS/YBS case-study.

It does not claim:

* real paying customers,
* revenue,
* production usage,
* real company adoption,
* live pilot results,
* Google Play publication.

The current proof is Demo Freeze v1 plus the Final Smoke Evidence Package with documented Android emulator smoke evidence.
