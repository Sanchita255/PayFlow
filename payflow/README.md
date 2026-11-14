# PayFlow

Secure digital payment and transaction management demo.

Features: account sign-up and login with JWT-style sessions, wallet top-ups, peer-to-peer transfers,
atomic transactions with rollback, idempotency keys to block duplicate payments, input validation,
an audit log, and a dashboard with transaction history and status filters.

This live demo runs entirely in the browser and keeps data in local storage.

## Deploy to Vercel
1. Push this folder to a new GitHub repository.
2. In Vercel, choose Add New > Project and import the repository.
3. Leave the framework as "Other" and click Deploy.

Or from a terminal: `npx vercel --prod`
