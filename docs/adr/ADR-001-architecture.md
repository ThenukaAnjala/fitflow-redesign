# ADR-001: Adopt a Microservice Architecture with Flutter Frontend for FitFlow

## Status

Accepted

## Context

FitFlow needs to support iOS, Android, and Web users while providing AI personalization, real-time social features, nutrition tracking, wearable integrations, and secure handling of health-related information. The system must be flexible enough to support different user workflows, integrate with external health platforms, and separate AI/ML concerns from the core application logic.

## Decision

Use the following architecture and technology choices:

- Flutter frontend
- NestJS core API
- FastAPI AI/ML and nutrition services
- PostgreSQL
- MongoDB
- Redis
- Auth0
- API Gateway
- Message Queue
- WebSocket real-time service

## Positive Consequences

- High frontend code reuse across iOS, Android, and Web
- Easier cross-platform development and UI consistency
- Independent AI/ML service that can evolve separately from the core API
- Scalable real-time architecture for social and live features
- Clear separation of responsibilities across services and data stores

## Negative Consequences

- Increased DevOps complexity
- Multiple services to maintain
- Monitoring and CI/CD requirements across separate services
- Service-to-service authentication complexity

## Alternatives Considered

- All-NestJS monolithic backend
- Fully native Swift + Kotlin frontend
