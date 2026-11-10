<p align="center">
  <img src="https://github.com/user-attachments/assets/854d1cc3-a946-4791-a713-fba6ac16b1ff" width="100%" alt="Marco Antonio, backend engineer. Go, distributed systems, insurance and financial platforms.">
</p>

I'm a backend engineer working mainly in Go (Golang), with two years of Node.js and TypeScript before that. I build and operate services on a surety insurance platform of 260+ Go microservices connected through gRPC, Kafka and API gateways, used by some of the largest multinational insurance brokerages.

[Email](mailto:contatomarcodev@gmail.com) · [LinkedIn](https://linkedin.com/in/marco-antonio-developer) · Brazil, remote (UTC-3)

## What I own

- **Insurer integrations.** The modules that carry issuance, endorsement and renewal flows between large brokerages and the platform's most-used insurers, global carriers included: API integrations behind a proxy layer, with OAuth2/OIDC, event webhooks, retries and observability in ELK.
- **Policy-chain cascade engine.** I designed and maintain the engine that propagates a single change across renewal and endorsement chains at 1,000 issuances a day, which ended manual chain fixes. Bidirectional BFS in semaphore-bounded waves, with cycle detection and field-mask propagation that keeps 10+ collections consistent through Redis, Elasticsearch and Kafka.
- **Access control.** I designed the authorization layer for 5,000+ brokerage users, with permissions scoped by client, user and bond type.
- **Production.** I diagnose incidents with OpenTelemetry, Prometheus, Elastic APM and Kibana, from mass pod evictions under memory pressure to MongoDB context-cancellation timeouts.

## How I work

- **Every retry needs a ceiling.** I once found a retry loop on failed policy issuances that fanned out chained retry events across several services, unnoticed for a year or more: over 900,000 retries through Kafka, day and night. Removing it saved cost and took away load that could have brought the service down. In the Go services I work on, each Kafka consumer declares its own retry count, messages that still fail go to a dead-letter queue, and payment calls carry an idempotency key.
- **A limit per pod is not a global limit.** Eight replicas with an in-memory limit of 2 each allow 16. When a limit has to hold across replicas, it lives in Redis.
- **Measure first.** Performance work starts with a profiler and a baseline. When I led the move of a document-generation service from Node.js to Go, processing time dropped 35.3% and queries per operation went from 110 to 5, measured before and after. For CPU and memory under load, I use pprof.
- **Tests are design pressure.** Code that is hard to test is telling you something. I write unit tests with gomock and contract tests between services.
- **Small changes win.** The smallest change that solves the problem beats the framework that solves every problem.

## Public work

Most of my production engineering lives in private, financial-sector repositories. What I can show:

- **[agents](https://github.com/marcodev1x/agents)** (Go, go-kit, gRPC). Turns very large Brazilian procurement PDFs into structured JSON without sending the document to the LLM. Local text extraction, in-memory embeddings and per-field top-k retrieval feed a single schema-constrained call, so the full document only touches the cheap embedding model: about 15× fewer tokens, no vector database.
- **[tema-certo-payments](https://github.com/tema-certo/tema-certo-payments)** (Node.js, TypeScript). Stripe checkout and webhooks: the HTTP layer verifies signatures and hands events to a durable RabbitMQ queue drained by a separate consumer.
- **[Automated testing course](https://youtu.be/_0Vt9ZjhFPw)** (free, pt-BR). A YouTube series on testing real codebases with Jest: async flows, mocking APIs and databases, coverage that means something, TDD in practice. Teaching it is how I made sure I actually understood it.
- **Go deep dives** on [LinkedIn](https://linkedin.com/in/marco-antonio-developer). Short carousels on runtime and performance topics such as singleflight, GOMEMLIMIT, atomics and pprof profiling.

## Stack

| Area | Day to day | Also used |
|:---|:---|:---|
| Languages | Go | TypeScript, JavaScript |
| Services | go-kit, gRPC, Protocol Buffers, Gin | NestJS, Express, Fiber |
| Messaging | Kafka | RabbitMQ, BullMQ, Debezium (CDC) |
| Data | MongoDB (Atlas Search), PostgreSQL, Redis, Elasticsearch | MySQL, MariaDB |
| Infrastructure | Kubernetes (EKS), AWS, Docker, ArgoCD | K3s, Helm |
| Observability | OpenTelemetry, Prometheus, Elastic APM, ELK | Grafana, VictoriaMetrics, Vector |
| Testing | go test, gomock, contract tests, pprof | Jest |
| Delivery | GitHub Actions | GitLab CI, Jenkins |
| Patterns | Event-driven microservices, API gateways, BFF, idempotency, dead-letter queues, rate limiting | Outbox |
| AI | Claude Code | Embeddings, RAG, OpenAI APIs |
| Frontend | React, Next.js, TanStack Query | Tailwind |

## Contact

Email is the fastest way to reach me: [contatomarcodev@gmail.com](mailto:contatomarcodev@gmail.com). I'm also on [LinkedIn](https://linkedin.com/in/marco-antonio-developer).
