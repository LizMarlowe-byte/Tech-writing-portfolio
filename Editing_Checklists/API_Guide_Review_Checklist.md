_Use this checklist to make sure that an API Guide follows the defined style, structure and writing guidelines in your tech writing portfolio_.

## API Guide Review Checklist

### 🧭 Global Guide Checklist

- [ ] Verify the **About this guide** section appears at the top.
- [ ] Ensure the **Table of Contents** follows the About section and accurately reflects all Heading 1s.
- [ ] Confirm the Introduction includes:
  - [ ] Overview of the API
  - [ ] Use cases
  - [ ] API standards or conventions used (REST, GraphQL, versioning, etc.)
  - [ ] Target audience
- [ ] Ensure all endpoint names, HTTP methods, and parameters use consistent technical formatting:
  - [ ] Code formatting for endpoints (e.g., `/v1/users`)
  - [ ] Uppercase for HTTP verbs (e.g., GET, POST)
  - [ ] Snake_case, camelCase, or kebab-case consistently applied
- [ ] Verify all examples are accurate and runnable (if applicable):
  - [ ] Request examples
  - [ ] Response payloads
  - [ ] Error examples
- [ ] Review all diagrams and graphics for:
  - [ ] Clear alt text
  - [ ] `---` separators above and below
  - [ ] Readability and accurate representation

---

### 🧩 Heading 1s Checklist

- [ ] Heading 1 names should be nouns (e.g., “Authentication,” “Endpoints,” “Schemas”).
- [ ] Each Heading 1 contains:
  - [ ] 1–2 sentence summary
  - [ ] **Topics:** label
  - [ ] Bulleted list of included Heading 2s

---

### 🔐 Authentication & Authorization Checklist

- [ ] Confirm authentication flow is clearly described:
  - [ ] OAuth, API keys, JWT, etc.
- [ ] Include examples of:
  - [ ] Token retrieval
  - [ ] Token refresh (if applicable)
  - [ ] Required headers
- [ ] Verify security requirements are clearly stated:
  - [ ] Rate limits
  - [ ] Scopes
  - [ ] Permissions

---

### 🔧 Endpoint Documentation Checklist

- [ ] For each endpoint:
  - [ ] Clear summary of what it does
  - [ ] Supported HTTP method(s)
  - [ ] Endpoint path formatted in code style
  - [ ] Required and optional parameters documented
  - [ ] Request example provided
  - [ ] Response example provided
  - [ ] Status codes explained
  - [ ] Error scenarios included
- [ ] Ensure sequential workflows reference relevant endpoints.

---

### 📘 Schema & Data Model Checklist

- [ ] Object models include:
  - [ ] Field names
  - [ ] Types
  - [ ] Descriptions
  - [ ] Constraints
  - [ ] Examples where helpful

- [ ] Verify all sample JSON is valid and properly formatted.
