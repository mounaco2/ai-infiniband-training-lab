
# AI/ML Infrastructure Networking — Training Lab

RoCEv2/RDMA fabric concepts, then a hands-on InfiniBand control-plane lab
(OpenSM + ibsim), built on real Arista EVPN/VXLAN foundations. Every
command in the lab documents is tagged CONFIRMED, NOT YET VERIFIED, or
CORRECTED — evidence-based, not assumed.

## Reading order

1. **AI_Network_Engineer_Career_Pivot.docx** — context: why this track
2. **Workbook_AI_RoCEv2_RDMA.docx** — read A1 through A7 in full
3. **InfiniBand_Simulator_Runbook.docx** — run this first, 3-node smoke test
4. **Fat_Tree_InfiniBand_Training.pptx** — skim for architecture
5. **Fat_Tree_Training_Lab_Guide.docx**, Sections 1-4 — build the fat-tree
6. Re-read the PPTX exercise slides (7-13)
7. **Fat_Tree_Training_Lab_Guide.docx**, Sections 5-11 — run Exercises 1-7
8. **RDMA_Verbs_Deep_Dive.docx** — companion read, alongside Workbook AI Appendix B

## Host

PA-ALT-N11, working directory `~/ibsim-lab`

## Push authentication

Pushes from PA-ALT-N11 use a GitHub Personal Access Token (classic, `repo`
scope), stored via `git config --global credential.helper store`.

**Token expires ~30 days from 2026-09-03.** When pushes start failing with
an auth error after that:

1. GitHub.com -> avatar -> Settings -> Developer settings -> Personal
   access tokens -> Tokens (classic) -> Generate new token (classic)
2. Same settings as before: `repo` scope checked, ~30 day expiry
3. Next `git push` will prompt for username/token again -> paste the new
   token -> it's stored again automatically

## Push authentication

Pushes from PA-ALT-N11 use a GitHub Personal Access Token (classic, `repo`
scope), stored via `git config --global credential.helper store`.

**Token expires ~30 days from 2026-09-03.** When pushes start failing with
an auth error after that:

1. GitHub.com -> avatar -> Settings -> Developer settings -> Personal
   access tokens -> Tokens (classic) -> Generate new token (classic)
2. Same settings as before: `repo` scope checked, ~30 day expiry
3. Next `git push` will prompt for username/token again -> paste the new
   token -> it's stored again automatically

## Workbook AI — Appendices (reference, not sequential reading)

A1–A7 are the actual curriculum, read straight through. Appendices A–E
inside `Workbook_AI_RoCEv2_RDMA.docx` are reference material — pull each
up *while doing* the module it supports, not after finishing A7:

| Appendix | Consult it... |
|---|---|
| Appendix (unlabeled) — Soft-RoCE build procedure | Before attempting any A2/A3/A5 exercise tagged with the soft-RoCE icon — it's the actual setup steps those exercises assume |
| Appendix B — Real ENOSPC case study | Alongside `RDMA_Verbs_Deep_Dive.docx` — same debugging session, read together (step 8 in the reading order) |
| Appendix C — Consolidated command reference | Anytime, as a lookup — especially useful mid-Exercise 1–7 in the Fat-Tree Guide when you want to confirm a flag's real status |
| Appendix D — Arista AI hardware line | After A2/A3, once you've seen ECN fail on cEOS — explains *why*, via real chipset mapping |
| Appendix E — Untested exercise (hardware flow tracking) | Optional, after A7 — closes the one deliberately-open loop in the workbook with real evidence, if you choose to run it |

## Lecture Companion (reference, not sequential)

`Lecture_Companion_RDMA_InfiniBand_Concepts.docx` — RDMA, Verbs/Queue
Pairs, LID vs GID vs GUID, RXE, RoCEv2 packet anatomy, MAD, Work Request
Flushed errors, and the diagnostic escalation method. Covers everything
explained mid-conversation that never made it into a formal module. Read
alongside Workbook AI, or as a standalone glossary when a term comes up
mid-lab.
