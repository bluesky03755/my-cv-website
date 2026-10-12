# Prep Room

A mock-interview coach for strategy & operations, product management, corporate strategy and chief of staff roles. It runs as a private Claude artifact; this folder holds its source.

What it does:

- **Practice**: Claude plays the interviewer. You pick the track, question type (behavioral, "how would you approach…", product sense, metrics & estimation, your narrative) and difficulty, optionally with a company and job description. You type your answer against a clock. You get a scorecard on five dimensions, a hire verdict, fixes, a tighter version of your answer with no invented facts, an accuracy check against your Experience Bank, and the follow-up a real interviewer would ask.
- **Story bank**: your STAR stories, indexed from the Notion Experience Bank. *Refresh from Notion* re-reads the page and updates the index. *Mine a story with the coach* interviews you to capture new episodes; *Copy for Notion* hands them back to the bank.
- **Progress**: score trend against the hire bar, per-dimension averages (last 10 vs prior 10), and the habits the coach keeps flagging. Session debriefs steer future questions toward weak spots.

Runtime: Claude (`sample`) for questions and scoring, the artifact database (`db`, owner-only) for profile, stories and sessions, and the Notion connector (`mcp`, `notion-fetch`) for the Experience Bank. Opened outside Claude, the page falls back to browser storage and the coach stays off.

No personal data lives in this file. Profile, stories and history are stored in the artifact's database.
