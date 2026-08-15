\# Final Integration Test Plan



\## Scope

\- Full stack testing (UI + API + .NET + SQL + MongoDB)

\- Cross-browser testing

\- Performance testing

\- Security testing

\- Accessibility testing

\- Regression testing



\## Test Environments

\- Docker containers (localhost)

\- Chrome, Firefox, Safari/Edge

\- Mobile viewport testing



\## Critical User Journeys

1\. View homepage → Browse stablecoins → View details

2\. Search for currency → View results → Add to watchlist

3\. Manage profile → Update settings → Connect social accounts

4\. View watchlist → Update holdings → Remove from watchlist



\## Integration Points to Test

\- Next.js UI ↔ Node API

\- Next.js UI ↔ .NET API

\- .NET API ↔ SQL Server

\- .NET API ↔ MongoDB

\- Frontend optimistic updates ↔ Backend persistence

