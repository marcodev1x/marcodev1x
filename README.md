# Marco Antonio

Backend Software Engineer focused on Go, distributed systems, event-driven architectures and financial services.

I build and operate services on a surety insurance platform: an ecosystem of
150+ Go microservices connected through gRPC, Kafka and API gateways, where
data consistency and reliability are business requirements rather than
aspirations.

Before that, I led the rewrite of a document generation system from Node.js to
Go 35% faster, with a significant drop in memory usage, and designed an
asynchronous, AI-assisted correction pipeline that scaled from 50 to 500+
operations per hour, with retries, rate limiting and fallback built in.

## Areas

- Distributed Systems
- Backend Architecture
- Event-driven Systems
- High Performance APIs
- Financial & Insurance Platforms
- AI-assisted Processing Pipelines
- Microservices

## How I work

- Tests are a design pressure. Code that is hard to test is telling you something.
- Performance work starts with measurement. The numbers above came from profiling, not intuition.
- The smallest change that solves the problem beats the framework that solves every problem.

## Stack
| | |
|---|---|
| **Languages** | Go, TypeScript, JavaScript |
| **Backend** | go-kit, Gin, gRPC, Protocol Buffers |
| **Messaging** | Kafka, RabbitMQ |
| **Databases** | MariaDB, MySQL, PostgreSQL, MongoDB, Redis |
| **Search** | Elasticsearch |
| **Infrastructure** | Docker, Kubernetes, AWS |
| **Observability** | Prometheus, Grafana |
| **Architecture** | Microservices, Event-driven, CQRS, API Gateway |
| **CI/CD** | GitHub Actions, Jenkins |
| **AI** | Claude Code, OpenAI APIs, Embeddings, RAG |
| **Frontend** | React, Next.js |

## Public work

Most of my production engineering lives in private, financial-sector
repositories. What I can show:

- **[Automated testing course — free, pt-BR](https://youtu.be/_0Vt9ZjhFPw?si=lU3FEoPXRl15FC0u)** —
  a YouTube series on testing real codebases: async flows, mocking APIs and
  databases, coverage that means something, TDD in practice. Teaching it is
  how I made sure I actually understood it.
- **[Api gateway example, with Go. — HTTP to gRPC!](https://github.com/audita-bids/audita-api-gateway)** — An HTTP to gRPC internal api gateway, comes from client, goes to internal with a lot of validations.
- **[Agent Go microservice](https://github.com/audita-bids/agents)** — Go microservice
  (go-kit, gRPC) that turns very large Brazilian procurement PDFs into structured
  JSON without sending the document to the LLM: local text extraction, in-memory
  embeddings and per-field top-k retrieval feed a single schema-constrained call.
  The full document only ever touches the cheap embedding model.
  
## Contact

[contatomarcodev@gmail.com](mailto:contatomarcodev@gmail.com) · [LinkedIn](https://linkedin.com/in/marco-antonio-developer)

## Git

<p align="center">
  <img src="https://streak-stats.demolab.com?user=marcodev1x&theme=github-dark&hide_border=true"/>
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=marcodev1x&theme=github-compact&hide_border=true"/>
</p>
