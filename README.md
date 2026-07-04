# RiverSense AI

> AI-powered eDNA analysis for Indian river health monitoring

**Team Creatus** · Biothon 2026 · Marwadi University · Top 50 Nationally

RiverSense AI reads environmental DNA (eDNA) extracted from river water
samples, classifies biological communities using AI, and generates a
real-time Biodiversity Health Score — automatically alerting government
agencies when a river is at risk.

---

## The problem

River health monitoring in India is manual, infrequent, and slow.
By the time lab results confirm a pollution event, the damage is done.
No automated early-warning system exists for Indian agencies.

---

## What RiverSense AI does

1. **Sequences** — pulls real metagenomic eDNA data from river samples
   (source: NCBI-SRA, Ganga river, run SRR8837334)
2. **Classifies** — runs Kraken2 taxonomic classification on organisms
   present in the water sample
3. **Scores** — computes a 0–100 Biodiversity Health Score from the
   abundance profile
4. **Alerts** — sends an automated email directly to government agencies
   when the score crosses a risk threshold

### Automated government alerts

When a river scores below the healthy threshold, RiverSense AI
automatically dispatches an alert email (via Gmail SMTP) to:

- **CPCB** — Central Pollution Control Board
- **Jal Shakti Ministry** — national water resource authority
- **WCCB** — Wildlife Crime Control Bureau
- **NFDB** — National Fisheries Development Board

No manual trigger needed. The pipeline runs, scores the river,
and sends the alert — end to end.

---

## Tech stack

| Layer | Technology |
|-------|-----------|
| ML / AI | DNABERT (fine-tuned), Kraken2, Gemini 1.5 Flash |
| Backend | FastAPI, MongoDB Atlas, Redis |
| Frontend | React, Tailwind CSS |
| Alerts | Gmail SMTP |
| Data | NCBI-SRA (SRR8837334) |

---

## Team contributions

  TEAM LEADER : THIVISHA
  ROLE : AI/ML Pipeline (DNABERT FINETUNING AND AUTOMATION )
   
   TEAM MEMBER: KOYEL GHOSH
   ROLE:BACKEND(FASTAPI +MONGODB)

   TEAM MEMBER 2 : SWATI GHARA
   ROLE: FRONTEND 


> ML pipeline details: see [ML_CONTRIBUTION.md](./ML_CONTRIBUTION.md)

---

## Running the project

### Frontend (Next.js)

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) to see the app.

### Backend

See backend setup instructions in `/app` or contact the backend lead.

---

## Data source

Real metagenomic sequencing data from the Ganga river:
- Study: SRP190174
- Run: SRR8837334
- Source: NCBI Sequence Read Archive

---

*Built for Biothon 2026 — Environment & Biodiversity track*
