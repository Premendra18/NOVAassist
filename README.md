# RetailAssist AI

![Status](https://img.shields.io/badge/Status-Completed-success)
![LLM](https://img.shields.io/badge/LLM-Google%20Gemini-orange)
![Prompt%20Engineering](https://img.shields.io/badge/Focus-Prompt%20Engineering-blue)
![Knowledge%20Base](https://img.shields.io/badge/Knowledge%20Base-JSON-brightgreen)

RetailAssist AI is a prompt-engineered AI retail sales and customer support assistant designed for online consumer electronics stores.

The project demonstrates how Large Language Models (LLMs) can be structured using modular prompts, business rules, and a curated knowledge base to provide reliable, consistent, and explainable customer support.

Unlike a generic chatbot, **NovaAssist** follows predefined workflows for:

* Product Recommendations
* Product Comparisons
* FAQ Support
* Order Tracking
* Human Escalation

The project focuses on **AI Product Design, Prompt Engineering, Knowledge Base Design, Prompt Evaluation, and AI System Behavior** rather than traditional software development.

---

# Problem Statement

Online retail businesses receive thousands of repetitive customer queries every day regarding products, deliveries, returns, warranties, refunds, and order tracking.

Handling these requests manually increases operational costs, response time, and customer support workload.

Generic AI chatbots often hallucinate product information, invent policies, or produce inconsistent answers, making them unreliable for customer-facing retail environments.

---

# Solution

RetailAssist AI addresses this challenge by providing a structured retail assistant called **NovaAssist**.

NovaAssist operates using:

* Structured System Prompt
* Product Knowledge Base
* FAQ Knowledge Base
* Mock Order Database
* Business Rules
* Conversation Workflows

Instead of generating unrestricted responses, NovaAssist answers customer queries only using approved information from the provided knowledge base.

---

# Demo Gallery

The screenshots below demonstrate NovaAssist handling common customer interactions.

## Product Recommendation

![Product Recommendation](screenshots/product-recommendation.png)

NovaAssist asks only the minimum clarification questions required before recommending products that satisfy all mandatory customer requirements.

---

## Product Comparison

![Product Comparison](screenshots/product-comparison.png)

NovaAssist compares products objectively using only approved catalog information and explains trade-offs without unsupported claims.

---

## Hallucination Prevention

![Hallucination Prevention](screenshots/hallucination-prevention.png)

When asked about products outside the catalog, NovaAssist refuses to invent information and instead recommends valid alternatives.

---

## Order Tracking

![Order Tracking](screenshots/order-tracking.png)

NovaAssist validates Order IDs before retrieving order information from the mock order database.

---

# Features

## AI-Powered Product Recommendations

* Understands customer intent before recommending products.
* Collects only the minimum information required.
* Applies domain-specific recommendation rules.
* Recommends only products available in the NovaMart catalog.
* Filters products based on mandatory customer requirements.

---

## Product Comparison

* Compares products using factual specifications.
* Explains objective trade-offs.
* Avoids marketing language.
* Never invents specifications.

---

## Customer Support

* Answers FAQs using the structured knowledge base.
* Provides consistent information regarding:

  * Shipping
  * Returns
  * Refunds
  * Warranty
  * Payments

---

## Order Support

* Requires a valid Order ID.
* Retrieves information from the mock order database.
* Simulates order tracking.
* Protects customer information by following predefined workflows.

---

## Human Escalation

* Detects situations requiring human assistance.
* Escalates unsupported requests.
* Avoids making promises beyond defined business rules.

---

## Hallucination Prevention

* Uses only approved knowledge base information.
* Never invents products, policies, specifications, or order details.
* Clearly communicates when information is unavailable.

---

# System Architecture

```text
                    Customer
                        │
                        ▼
                 NovaAssist AI
                        │
        ┌───────────────┼────────────────┐
        ▼               ▼                ▼
 Product Catalog     FAQ Database     Order Database
(products.json)      (faqs.json)      (orders.json)
        │               │                │
        └───────────────┼────────────────┘
                        ▼
          Business Rules & System Prompt
                        │
                        ▼
                 Customer Response
```

---

# Repository Structure

```text
RetailAssist-AI/
│
├── README.md
│
├── data/
│   ├── products.json
│   ├── faqs.json
│   └── orders.json
│
├── prompts/
│   └── system_prompt.md
│
├── evaluation/
│   ├── test_cases.md
│   └── prompt_iterations.md
│
├── demo/
│   └── sample_conversations.md
│
└── screenshots/
    ├── Product Recommendation.png
    ├── Product Recommended.png
    ├── Product Comparison.png
    ├── iPhone Hallucination Test.png
    └── Ordert Tracking.png
```

---

# Prompt Engineering Approach

RetailAssist AI was designed using an iterative prompt engineering methodology rather than a single monolithic prompt.

## System Prompt

The system prompt defines:

* Assistant identity
* Responsibilities
* Conversation workflow
* Business rules
* Recommendation logic
* Safety guardrails
* Human escalation policy
* Response formatting

---

## Knowledge Base

NovaAssist is constrained using three structured datasets:

* **products.json** — Product catalog
* **faqs.json** — Store policies and FAQs
* **orders.json** — Mock customer order database

This approach minimizes hallucinations and improves response consistency.

---

## Conversation Workflow

For every customer interaction, NovaAssist follows a structured workflow:

1. Identify customer intent.
2. Determine whether sufficient information is available.
3. Ask only the minimum clarification questions when required.
4. Retrieve information from the appropriate knowledge source.
5. Apply business rules and recommendation policies.
6. Generate a structured response.
7. Escalate to a human representative when appropriate.

---

## Hallucination Prevention

NovaAssist is explicitly instructed to:

* Never invent products.
* Never invent specifications.
* Never invent prices.
* Never fabricate order information.
* Never create store policies.
* Clearly state when required information is unavailable.

---

# Evaluation Strategy

NovaAssist was evaluated using structured scenario-based testing.

Evaluation categories included:

* Product Recommendations
* Product Comparisons
* FAQ Responses
* Order Support
* Hallucination Prevention
* Human Escalation
* Out-of-Scope Requests

Prompt behavior was continuously refined using observations collected during testing.

Detailed evaluation reports are available in:

* `evaluation/test_cases.md`
* `evaluation/prompt_iterations.md`

---

# Key Learnings

During development, NovaAssist was improved through multiple prompt iterations driven by structured testing rather than trial and error.

The project demonstrates that reliable AI assistants require more than a well-written prompt—they also require:

* Clearly defined business rules
* Structured knowledge bases
* Controlled conversation workflows
* Systematic evaluation
* Iterative prompt refinement

---

# Future Improvements

Potential enhancements for production deployment include:

* Integration with live inventory APIs
* Live order management APIs
* Retrieval-Augmented Generation (RAG)
* Vector database integration
* Voice-enabled customer support
* Multi-language support
* Customer analytics dashboard
* Real-time inventory synchronization
* CRM and ERP integration

---

# Conclusion

RetailAssist AI demonstrates how prompt engineering, structured knowledge bases, business rules, and iterative evaluation can be combined to build a reliable AI-powered retail assistant.

Rather than functioning as a generic chatbot, NovaAssist follows predefined workflows, uses only approved knowledge sources, and continuously improves through structured prompt refinement—reflecting an AI product engineering approach suitable for real-world customer support systems.

