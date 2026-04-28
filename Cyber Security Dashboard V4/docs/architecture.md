# Cybersecurity Dashboard Architecture

## Goal

Build a full-stack cybersecurity dashboard that lets authenticated users:

- manage monitored assets
- launch and track scans
- review findings by severity and status
- view risk trends and KPIs
- generate reports
- receive near-real-time scan progress updates

## High-Level Architecture

### Frontend

- React for the SPA
- Tailwind CSS for styling
- Feature-based structure for dashboard, assets, findings, scans, reports, and settings
- API client for REST calls to FastAPI
- WebSocket client for live scan progress and dashboard refresh events

### Backend

- FastAPI as the HTTP API layer
- Pydantic schemas for request and response contracts
- Service layer for business logic
- Repository layer for database access boundaries
- Scanner integration layer for wrapping external security tools
- Background task layer for scans and report generation

### Data Layer

- PostgreSQL as the primary relational database
- Core entities:
  - users
  - assets
  - scans
  - findings
  - alerts
  - reports

### Async / Real-Time

- Background worker for long-running scan jobs
- Redis recommended as the queue and pub/sub backbone
- WebSocket manager for scan progress, status updates, and live dashboard counters

### Deployment

- Dockerized backend and frontend
- Nginx reverse proxy for frontend serving and API routing
- Environment-driven configuration

## Logical Flow

1. User signs in through the React app.
2. React calls FastAPI auth endpoints and stores the session token.
3. User creates or selects an asset.
4. User starts a scan.
5. FastAPI persists the scan request and dispatches a background job.
6. Scanner integrations execute and normalize raw output.
7. Findings are saved to the database.
8. WebSocket events push progress and completion updates to the frontend.
9. Dashboard pages query aggregates and render metrics, trends, and finding tables.

## Backend Layering Rules

- `api/` only handles transport concerns: routing, validation entry points, auth dependencies, HTTP errors.
- `services/` owns business workflows and orchestration.
- `repositories/` owns persistence queries.
- `models/` defines database entities.
- `schemas/` defines API contracts.
- `integrations/` isolates third-party scanners and enrichment providers.
- `tasks/` runs long-lived asynchronous jobs.

This separation matters because scan logic, persistence, and transport will evolve at different speeds.

## Frontend Layering Rules

- `features/` contains domain-specific UI and state by capability.
- `components/ui/` contains reusable generic building blocks.
- `components/charts/` and `components/tables/` contain shared dashboard visualizations.
- `services/` wraps network and websocket access.
- `app/` defines routing and top-level providers.
- `layouts/` contains shell-level structures such as sidebar, topbar, and content framing.

## Recommended Initial Modules

### Backend APIs

- `auth`
- `dashboard`
- `assets`
- `scans`
- `findings`
- `reports`
- `users`

### Frontend Screens

- login
- overview dashboard
- asset inventory
- scan management
- findings explorer
- report center
- settings

## Security Baseline

- JWT-based authentication
- role-based access hooks prepared from the start
- input validation on all API boundaries
- audit logging for sensitive actions
- rate limiting on auth and scan-trigger endpoints
- secret values provided only through environment variables

## Non-Goals For This Step

- no endpoint implementation
- no database migrations yet
- no React component implementation yet
- no scanner execution logic yet

This step only defines the architecture and the target repository layout so implementation can begin cleanly in the next phase.
