# SuRaksha_Cyber_Hackathon_2.0_Architecture
Architecture diagram for SuRaksha Cyber Hackathon 2.0

Document upload (PDF / image)
              │
              ▼
   ┌──────────────────────┐
   │   Pre-processing      │  OCR + page rasterisation
   └──────────┬───────────┘
              │
   ┌──────────┼───────────────────────┐
   ▼          ▼                        ▼
Forensics   Content              Cross-Reference
 Agent       Agent                   Agent
 (ELA,      (field logic,        (IFSC / PAN /
  copy-move, font & date          land-record
  metadata)  consistency)          validation)
   │          │                        │
   └──────────┴───────────┬────────────┘
                          ▼
              ┌────────────────────────┐
              │  Underwriter Agent      │  synthesises signals →
              │  (LLM orchestration)    │  risk score + annotated
              └───────────┬─────────────┘  image + explanation
                          ▼
              Underwriter dashboard (React)
