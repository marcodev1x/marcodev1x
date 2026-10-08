<p align="center">
  <img src="https://github.com/user-attachments/assets/854d1cc3-a946-4791-a713-fba6ac16b1ff" width="100%" alt="Marco Antonio, backend engineer. Go, distributed systems, insurance and financial platforms.">
</p>

I'm a backend engineer working in Go and Node.js. I build and operate services on a surety insurance platform of 250+ Go microservices connected through gRPC, Kafka and API gateways, used by some of the largest multinational insurance brokerages. There, data consistency and reliability are business requirements, not aspirations.

## What I own

- **Insurer integrations.** Responsible for the modules that carry issuance, endorsement and renewal flows between multinational brokerages and the platform's most-used insurers, multinational carriers included: API integrations behind a proxy layer, with OAuth2/OIDC, event webhooks, retries and observability in ELK.
- **Policy-chain cascade engine.** Designed and maintain the engine that propagates a single change across renewal and endorsement chains at 2,000 issuances a day, which ended manual chain fixes. Bidirectional BFS in semaphore-bounded waves, with cycle detection and field-mask propagation that keeps 10+ collections consistent through Redis, Elasticsearch and Kafka.
- **Authorization at brokerage scale.** Shipped the authorization layer for 5,000+ users: permissions per principal, user and bond type (quote, submit, view, manage), with configurable or uncapped sum-insured limits.
- **Data-path performance.** Replaced regex COLLSCANs over 200k+ documents, running for 9+ minutes, with Atlas Search and a custom Portuguese analyzer. Moved Redis session invalidation from KEYS/DEL to SCAN/UNLINK to keep blocking calls off read paths.
- **Production.** Diagnose incidents with OpenTelemetry, Elastic APM and Kibana, from mass pod evictions under memory pressure to MongoDB context-cancellation timeouts.

## Before that

In EdTech, I led the rewrite of a document generation service from Node.js to Go, making it 35% faster and cutting queries per operation from 110 to 5. I also designed an AI-assisted correction pipeline that scaled from 50 to 580+ operations per hour, with retries, rate limiting and fallbacks built in.

## Public work

Most of my production engineering lives in private, financial-sector repositories. What I can show:

- **[agents](https://github.com/audita-bids/agents)** (Go, go-kit, gRPC). Turns very large Brazilian procurement PDFs into structured JSON without sending the document to the LLM. Local text extraction, in-memory embeddings and per-field top-k retrieval feed a single schema-constrained call, so the full document only touches the cheap embedding model: about 15× fewer tokens, no vector database.
- **[audita-api-gateway](https://github.com/audita-bids/audita-api-gateway)** (Go, go-kit). Internal gateway that translates HTTP requests into gRPC calls and validates them at the edge.
- **[webhooks](https://github.com/audita-bids/webhooks)** (Go). Generic webhook receiver for third-party integrations.
- **[tema-certo-payments](https://github.com/tema-certo/tema-certo-payments)** (Node.js, TypeScript). Stripe checkout and webhooks: the HTTP layer verifies signatures and hands events to a durable RabbitMQ queue drained by a separate consumer.
- **[Automated testing course](https://youtu.be/_0Vt9ZjhFPw)** (free, pt-BR). A YouTube series on testing real codebases with Jest: async flows, mocking APIs and databases, coverage that means something, TDD in practice. Teaching it is how I made sure I actually understood it.
- **Go deep dives** on [LinkedIn](https://linkedin.com/in/marco-antonio-developer). Short carousels on runtime and performance topics such as singleflight, GOMEMLIMIT, atomics and pprof profiling.

## How I work

- **Measure first.** Performance work starts with a profiler and a baseline. The performance numbers on this page came from measurement, not intuition.
- **Tests are design pressure.** Code that is hard to test is telling you something.
- **Small changes win.** The smallest change that solves the problem beats the framework that solves every problem.

## Stack

| Area | Tools |
|---|---|
| Languages | Go, TypeScript, JavaScript |
| Services | go-kit, Gin, Fiber, gRPC, Protocol Buffers, NestJS, Express |
| Messaging | Kafka, RabbitMQ, BullMQ |
| Data | PostgreSQL, MySQL, MariaDB, MongoDB (Atlas Search), Redis, Elasticsearch |
| Infrastructure | Kubernetes (EKS, K3s), Docker, AWS, ArgoCD, Helm |
| Observability | OpenTelemetry, Elastic APM, ELK, Prometheus, Grafana, VictoriaMetrics, Vector |
| Delivery | GitHub Actions, GitLab CI, Jenkins |
| Architecture | Microservices, event-driven, CQRS, API gateways, BFF |
| AI | Embeddings, RAG, OpenAI APIs, Claude Code |
| Frontend | React, Next.js, TanStack Query |

## Contact

[contatomarcodev@gmail.com](mailto:contatomarcodev@gmail.com) · [LinkedIn](https://linkedin.com/in/marco-antonio-developer) · Brazil, remote (UTC-3)
