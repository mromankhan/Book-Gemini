# Research for Interactive Book with RAG Chatbot

## 1. Frontend Testing Framework

### Decision
We will use **Jest** and **React Testing Library** for testing the Docusaurus frontend.

### Rationale
-   Docusaurus is built with React, and Jest and React Testing Library are the de-facto standards for testing React applications.
-   They provide a good balance of unit and integration testing capabilities.
-   There is a large community and plenty of documentation available.

### Alternatives Considered
-   **Cypress**: Cypress is a good end-to-end testing framework, but it might be overkill for this project's needs.
-   **Playwright**: Similar to Cypress, Playwright is a powerful end-to-end testing framework, but it's more complex to set up and use than Jest and React Testing Library.

## 2. Scale and Scope

### Decision
-   **Expected number of users**: The project is a portfolio piece and is not expected to have a large number of concurrent users. We will design the system to handle up to 100 concurrent users.
-   **Book size**: The book is expected to have around 10 chapters, with each chapter having 5-10 pages. This translates to roughly 50-100 pages in total.

### Rationale
-   This is a reasonable scale for a portfolio project and will not incur significant costs for the Qdrant Cloud Free Tier.
-   The architecture can be scaled up in the future if needed.

### Alternatives Considered
-   Designing for a larger scale would require more complex infrastructure and would be more expensive.
