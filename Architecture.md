# Silver Decipherer – Conceptual Architecture

## High-Level Design

Mobile Apps (iOS / Android)
        |
        v
Backend Quote Normalization Service
        |
        +-- Shanghai price source (SGE / SHFE)
        +-- US price source (COMEX)
        +-- FX rate source (USD/CNY)
        |
        v
Cache / Aggregation Layer
        |
        v
Public API for Apps

---

## Design Principles

- Backend normalization to avoid client-side inconsistency
- Caching to reduce data costs
- Clear timestamps on all prices
- Graceful degradation if a market is closed

---

## Scalability Considerations

- Stateless backend services
- Horizontal scaling
- Alert processing via background workers
