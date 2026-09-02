# ServiceDesk Issue Management Platform

Enterprise issue and support-ticket management backend built with Java and Spring Boot.

## Overview
The platform manages the support-ticket lifecycle from creation and assignment through SLA monitoring, escalation, resolution and closure.

## Existing Technologies
- Java 17+
- Spring Boot 3.2+
- Spring Data JPA / Hibernate
- REST APIs
- Flyway / Gradle
- PostgreSQL, MySQL-compatible persistence and H2
- WebSocket / STOMP / SockJS
- Spring Scheduling

## Architecture
```text
Client
  |
  v
REST Controllers
  |
  v
Service Layer
  |
  v
Spring Data JPA Repositories
  |
  v
Relational Database

Supporting components:
Security | SLA Scheduler | Automation | Audit Logging | Webhooks | WebSockets
```

## Currently Implemented
- ticket lifecycle, assignment, status and priorities
- configurable SLA policies and escalation
- business-hour/holiday-aware SLA processing
- roles and permissions
- audit logging
- API-token authentication and token hashing
- two-factor authentication support
- saved views, knowledge base and custom fields
- merge/link/split/snooze ticket workflows
- guest ticket access, webhooks, real-time events and CSAT

## Security
Existing functionality includes API-token authentication, hashed tokens, granular permissions, 2FA support, signed webhooks and guest access tokens. JWT user authentication is not claimed as implemented here.

## Testing
```bash
./gradlew test
```

## Planned Portfolio Enhancements
- standalone ServiceDesk application
- MySQL-first deployment
- Docker Compose application + database
- optimistic locking
- concurrent ticket-update tests
- additional JUnit integration tests

## Running Locally
```bash
./gradlew build
./gradlew test
```
