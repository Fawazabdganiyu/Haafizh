# Haafizh

## 🔖 Project Title & Description

**Haafizh — Your digital ledger for personal and shared finances.**

Haafizh is a secure, user-friendly application for recording, tracking, and managing funds—whether personal savings or money entrusted by others. Users can log amounts given, received, or collected, with transparent running balances and transaction histories per contact.

**Who it’s for:**

* Individuals managing personal loans or shared expenses
* Small groups or families needing clear financial records
* Anyone who wants peace of mind through organized tracking

**Why it matters:**
Financial exchanges between people are often undocumented, leading to confusion or disputes. Haafizh provides clarity, accountability, and trust with a well-structured digital ledger.

This repository contains the **frontend (Next.js + Apollo Client)** for Haafizh. The backend (NestJS + GraphQL + PostgreSQL) is hosted in a separate repository.

👉 Backend Repository: [Haafizh API](https://github.com/fawazabdganiyu/haafizh-api)

---

## ✨ Features (MVP)

* Record funds given, received, or collected
* Track balances per contact
* Transaction history with timestamps
* Authentication & authorization (JWT)
* GraphQL API for flexible queries and mutations

**Future Enhancements:**

* Multi-currency support
* Exportable reports (CSV, PDF)
* Asset and item tracking
* Real-time updates (GraphQL subscriptions)
* Mobile app

---

## 🛠️ Tech Stack

* **Frontend:** Next.js (React + TypeScript), Apollo Client, TailwindCSS
* **Backend:** NestJS (Node.js + TypeScript), Apollo Server (`@nestjs/graphql`) → [Haafizh API](https://github.com/fawazabdganiyu/haafizh-be)
* **Database:** PostgreSQL + Prisma ORM
* **Authentication:** JWT in GraphQL context (optional Auth0 integration)
* **Testing:** Jest (unit & integration) + React Testing Library
* **Documentation:** GraphQL Playground + auto-generated schema docs
* **Dev Tools:** GitHub (repo & PRs), Docker (optional), GitHub Actions (CI/CD)

---

## 🧠 AI Integration Strategy

Haafizh leverages AI tools throughout development to boost productivity and ensure maintainability.

### Code Generation

Use AI-powered IDE tools (e.g., Zed with GitHub Copilot, Gemini AI, CodeRabbit) to scaffold React components, backend endpoints, and database models.

* **Prompt Example:** “Generate a React form component for adding a transaction with fields for amount, type, date, and contact.”

### Testing

Employ AI to draft unit and integration tests for key functions.

* **Prompt Example:** “Generate a Jest test suite for the transaction API integration.”

### Documentation

Use AI to create docstrings, inline comments, and maintain an up-to-date README.

* **Prompt Example:** “Write documentation for the transaction tracking feature in Haafizh.”

### Context-aware Techniques

Feed API specs (via GraphQL schema), database schemas, and file diffs into AI workflows for more accurate code and doc generation.

---

## 🏗️ Architecture

* **haafizh (this repo)** → Next.js app with Apollo Client
* **haafizh-api** → NestJS GraphQL API + PostgreSQL
* **Separation of concerns:** frontend and backend live in separate repos for scalability and clean collaboration

---

## 🚀 Installation

### Frontend (Next.js + Apollo Client)

```bash
# Clone frontend repo
git clone https://github.com/fawazabdganiyu/haafizh.git
cd haafizh

# Install dependencies
npm install

# Setup environment variables (API URL, etc.)
cp .env.example .env.local

# Start dev server
npm run dev
```

By default, the frontend connects to the backend GraphQL API. Make sure the backend (`haafizh-api`) is running or update the API URL in your `.env.local` file.

---

## 📝 GraphQL Example

```graphql
# Query contacts and balances
query {
  contacts {
    id
    name
    balance
    transactions {
      id
      amount
      type
      date
    }
  }
}
```

---

## 📌 Roadmap

* [x] Setup Next.js frontend
* [ ] Implement authentication flow
* [ ] Build contacts management UI
* [ ] Build transaction management UI
* [ ] Integrate GraphQL backend
* [ ] Deployment

---

## License

[MIT](LICENSE)

---

✨ With Haafizh, financial clarity is just a record away.
