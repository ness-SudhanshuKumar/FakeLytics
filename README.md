# FakeLytics
multi-channel fact checking multi agent system
# initial architecture

User Input (text / article / headline)
        │
        ▼
┌─────────────────────┐
│   Agent 1           │
│   Claim Extractor   │  → Breaks input into atomic, verifiable claims
└─────────┬───────────┘
          │
    ┌─────┴──────┐
    ▼            ▼
┌────────┐  ┌──────────┐
│Agent 2 │  │ Agent 3  │   ← Run in PARALLEL
│Evidence│  │  Bias    │
│Hunter  │  │ Detector │
└────┬───┘  └────┬─────┘
    └──────┬─────┘
           ▼
┌──────────────────────┐
│   Agent 4            │
│   Verdict Synthesizer│  → Final ruling + confidence score
└──────────────────────┘
           │
           ▼
     VERDICT REPORT
  TRUE / FALSE / MISLEADING / UNVERIFIED
  + Confidence % + Red Flags
