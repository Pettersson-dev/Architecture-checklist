# Architecture Assessment Checklist for New Systems

## Overview

This checklist should be used whenever a new system, SaaS solution, platform, application, service, or vendor product is proposed for introduction into the enterprise landscape.

The purpose is to:

- Ensure alignment with business strategy and target architecture.
- Avoid duplication of capabilities and systems.
- Establish clear ownership and governance.
- Reduce technical debt and unnecessary complexity.
- Ensure security, compliance, and operational readiness.
- Create transparency around costs, risks, and dependencies.

---

# Architecture Questions

## 1. Business Context

### Business Need

- What business problem are we trying to solve?
- What business outcomes are expected?
- What is the cost of doing nothing?
- Is this a strategic initiative or a local optimization?

### Business Capabilities

- Which business capabilities does the system support?
- Is this a new capability or an enhancement of an existing one?
- Which business processes will be impacted?

### Success Criteria

- How will success be measured?
- What KPIs are expected to improve?

**Example**

| Area | Example |
|--------|----------|
| Objective | Reduce customer onboarding time |
| KPI | From 5 days to 1 day |
| Capability | Customer Management |

---

## 2. Existing Landscape

### Existing Solutions

- Does a system already provide similar functionality?
- Can an existing platform be extended?
- Have alternative solutions been evaluated?

### Duplication Assessment

- Does this introduce overlapping functionality?
- Does this create another source of truth?
- Will users need to maintain data in multiple systems?

### Architecture Impact

- Does this simplify or complicate the landscape?
- What existing systems will be affected?

**Example Red Flag**

- New customer database when CRM already owns customer data.

---

## 3. Ownership and Governance

### Business Ownership

- Who owns the business process?
- Who owns the budget?
- Who prioritizes future changes?

### Technical Ownership

- Who owns the application?
- Who owns integrations?
- Who owns operational support?

### Vendor Ownership

- Who manages the vendor relationship?
- Who owns contract management?

---

## 4. Information and Data

### Information Ownership

- What information is created or maintained?
- Who owns the information?
- Is ownership documented?

### Source of Truth

For each information object:

- What is the authoritative source?
- Is the system a producer or consumer?

**Example**

| Information | System of Record |
|------------|------------------|
| Customer | CRM |
| Product | PIM |
| Employee | HR |

### Data Quality

- How is data validated?
- How are duplicates handled?
- Who is responsible for data quality?

### Data Retention

- What retention requirements apply?
- What archiving requirements exist?
- How is data deleted?

---

## 5. Integration Architecture

### Integration Requirements

- What systems must integrate with this solution?
- Which interfaces are required?

### Integration Patterns

- API
- Event-driven
- Batch
- File transfer

### API Assessment

- Are APIs available?
- Is documentation available?
- Is versioning supported?
- Are there rate limits?

### Event Assessment

- Does the solution publish events?
- Does it consume events?
- Are event schemas documented?

### Dependency Assessment

- What upstream dependencies exist?
- What downstream dependencies exist?

---

## 6. Security and Compliance

### Identity and Access Management

- Does the solution support SSO?
- Does it support MFA?
- Does it support role-based access control?
- Does it integrate with the enterprise IAM platform?

### Security Controls

- Is encryption supported at rest?
- Is encryption supported in transit?
- Is audit logging available?

### Compliance

- Does the system process personal data?
- Does GDPR apply?
- Are there regulatory requirements?

### Security Review

- Has a security assessment been completed?
- Has a threat model been performed?
- Has penetration testing been completed?

---

## 7. Technology and Platform Fit

### Technology Alignment

- Does the solution align with technology standards?
- Does it fit cloud strategy?
- Does it fit platform strategy?

### Architecture Principles

Evaluate against principles such as:

- Cloud First
- SaaS First
- API First
- Event Driven
- Buy Before Build
- Reuse Before Buy

### Vendor Assessment

- Is the vendor financially stable?
- Is the product roadmap available?
- Is the vendor widely adopted?

---

## 8. Operational Readiness

### Support Model

- Who provides Level 1 support?
- Who provides Level 2 support?
- Who provides Level 3 support?

### Monitoring

- Are logs available?
- Are metrics available?
- Is alerting available?

### Resilience

- What are availability requirements?
- What are recovery requirements?
- What backup mechanisms exist?

### Service Management

- Is operational documentation available?
- Are support procedures defined?

---

## 9. Cost Assessment

### One-Time Costs

- Licensing
- Procurement
- Implementation
- Integrations
- Training

### Recurring Costs

- Subscription fees
- Support
- Hosting
- Managed services

### Hidden Costs

- Customizations
- Vendor dependencies
- API consumption
- Storage growth

### Exit Strategy

- Can data be exported?
- What is the migration effort?
- Is there vendor lock-in?

---

## 10. Architecture Impact Assessment

### Application Landscape

- How many new systems are introduced?
- How many integrations are introduced?

### Complexity

- Does the solution reduce complexity?
- Does the solution increase complexity?
- Is added complexity justified?

### Technical Debt

- Are temporary solutions required?
- Are manual workarounds introduced?
- Are customizations required?

---

## 11. Target Architecture Alignment

### Future State Fit

- Does the solution fit the target architecture?
- Will it fit in 3–5 years?

### Strategic Alignment

- Does the solution support strategic objectives?
- Does it align with architectural roadmaps?

### Dependencies

- What initiatives depend on this solution?
- What initiatives does this solution depend on?

---

## 12. Recommendation

### Decision

- Approve
- Approve with Conditions
- Reject
- Reassess

### Key Benefits

- Benefit 1
- Benefit 2
- Benefit 3

### Key Risks

- Risk 1
- Risk 2
- Risk 3

### Required Mitigations

- Mitigation 1
- Mitigation 2
- Mitigation 3

---

# Architecture Red Flags

Escalate immediately if any of the following apply:

- No business owner identified.
- No technical owner identified.
- Creates a duplicate source of truth.
- Significant customization required.
- No API capability available.
- No SSO support.
- Unclear data ownership.
- Unclear operational ownership.
- Vendor lock-in without exit strategy.
- Security assessment not completed.
- Misaligned with target architecture.

---

# Executive Architecture Questions

These are the ten questions every architect should ask before approving a new system:

1. Why do we need this system?
2. Which business capability does it support?
3. Why can’t an existing platform solve this?
4. What information will it own?
5. What systems will it integrate with?
6. Who owns it?
7. What security and compliance risks exist?
8. What complexity does it introduce?
9. What is the total lifecycle cost?
10. How does it support the target architecture?