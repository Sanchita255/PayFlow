# PayFlow – Secure Digital Payment & Transaction Management System

A secure digital payment and transaction management demo that simulates a digital wallet platform. PayFlow allows users to create accounts, manage wallet balances, transfer funds between users, and track transactions through an interactive dashboard.

The application demonstrates important fintech engineering concepts, including transaction consistency, duplicate payment prevention, input validation, authentication flows, and audit logging.

> **Note:** This is a demonstration application. All data is stored locally in the browser using Local Storage. It does not process real payments or connect to banking infrastructure.

## Features

### 1. User Authentication
- User sign-up and login.
- JWT-style session management simulation.
- User-specific wallet access.
- Input validation for authentication forms.

### 2. Digital Wallet Management
- Wallet creation for registered users.
- Wallet balance tracking.
- Simulated wallet top-ups.
- Real-time balance updates.

### 3. Peer-to-Peer Transfers
- Transfer funds between registered users.
- Validate available wallet balance before transfers.
- Prevent invalid transaction requests.
- Update sender and receiver balances.

### 4. Transaction Management
- Complete transaction history.
- Transaction status tracking.
- Transaction filtering by status.
- Transaction details and timestamps.

### 5. Transaction Reliability
- Atomic transaction simulation.
- Rollback mechanism for failed transactions.
- Idempotency keys to prevent duplicate payment requests.
- Input validation and error handling.

### 6. Audit Logging
- Record transaction activities.
- Maintain transaction logs.
- Track payment operations and statuses.

### 7. Dashboard
- Overview of wallet balance.
- Transaction history.
- Payment activity monitoring.
- Status-based transaction filtering.

## Technology Stack

| Category | Technologies |
|---|---|
| Frontend | React.js, JavaScript, HTML5, CSS3 |
| Data Storage | Browser Local Storage |
| Authentication | JWT-style session simulation |
| Transaction Management | Atomic transaction simulation |
| Reliability | Idempotency Keys, Rollback Handling |
| Development Tools | Git, GitHub, VS Code |
| Deployment | Vercel |

## Application Architecture

The current version follows a browser-based architecture:

```text
                User
                  |
                  v
          React.js Interface
                  |
                  v
          Application Logic
                  |
          +-------+-------+
          |       |       |
          v       v       v
       Wallet  Transaction Audit
       Logic    Logic     Logs
          |       |       |
          +-------+-------+
                  |
                  v
            Local Storage
```

## Transaction Workflow

A typical peer-to-peer payment follows these steps:

1. User initiates a transfer.
2. Validate sender, receiver, and transfer amount.
3. Check the sender's available wallet balance.
4. Check the idempotency key to prevent duplicate processing.
5. Execute the simulated transaction.
6. Update sender and receiver balances.
7. Roll back changes if the transaction fails.
8. Record the transaction in the audit log.
9. Display the transaction status on the dashboard.

## Installation and Setup

### Prerequisites
- Node.js and npm
- Git
- A GitHub account

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/payflow.git
```

### 2. Navigate to the Project Directory

```bash
cd payflow
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Start the Development Server

```bash
npm run dev
```

Open the local URL displayed in your terminal.

> If your project uses a different development command, update this instruction according to its package.json.

## Deployment on Vercel

PayFlow can be deployed using Vercel.

### Method 1: GitHub Integration

1. Push the project to a GitHub repository.
2. Log in to Vercel.
3. Select **Add New → Project**.
4. Import your GitHub repository.
5. Configure the build settings according to your project.
6. Click **Deploy**.

### Method 2: Vercel CLI

Install and run the deployment command:

```bash
npx vercel --prod
```

Follow the terminal instructions to complete deployment.

## Security Considerations

PayFlow demonstrates several payment-security concepts:

- Input validation to reject invalid requests.
- Duplicate transaction prevention using idempotency keys.
- Balance validation before fund transfers.
- Rollback handling for failed transactions.
- Audit logging for transaction traceability.

**Security limitation:** The current browser-only implementation is not production-grade payment infrastructure. Local Storage is user-accessible and can be modified. JWT-style sessions are simulated, not server-verified authentication. Production deployment would require server-side authentication, authorization, persistent database transactions, secure secret management, and appropriate payment compliance controls.

## Future Enhancements

- [ ] Node.js and Express.js backend integration.
- [ ] MySQL database integration.
- [ ] Server-side JWT authentication and authorization.
- [ ] Database-level ACID transactions.
- [ ] Persistent transaction and audit records.
- [ ] Payment gateway sandbox integration.
- [ ] Automated unit and integration testing.
- [ ] Rate limiting and enhanced security controls.
- [ ] Real-time transaction notifications.

## Learning Outcomes

This project demonstrates practical understanding of:

- Full-stack application development.
- Client-server architecture.
- REST API concepts.
- Authentication and authorization.
- Database transaction principles.
- Idempotency and duplicate request prevention.
- Error handling and rollback mechanisms.
- Financial transaction workflows.
- Software reliability and audit logging.

## Disclaimer

PayFlow is an educational demonstration project. It is not affiliated with PayPal or any financial institution. It does not support real-money transfers, actual banking operations, or real payment processing.

## Author

**Sanchita Dubey**

