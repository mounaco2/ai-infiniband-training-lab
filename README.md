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
