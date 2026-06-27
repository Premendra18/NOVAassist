# NovaAssist Demo Conversations

This document showcases representative customer interactions with NovaAssist.

The conversations were generated during prompt evaluation and demonstrate how the assistant follows structured business rules, retrieves information from the knowledge base, and avoids hallucinations.

---

# Conversation 1 – Product Recommendation

### Customer

> I need a laptop under ₹80,000.

### NovaAssist

I'd be happy to help.

Before I recommend a laptop, could you please tell me:

* What will be your primary use case (software development, office work, gaming, student studies, etc.)?
* Do you prefer a compact lightweight laptop or a larger display?
To help me find the most suitable laptop under ₹80,000 from our catalog, could you please share a few details about how you plan to use it?

1. **Primary Use Case:** What will be your main use case for the laptop (e.g., general office work, software development, creative editing, or student studies)?
2. **Screen Size & Portability:** Do you prefer a highly compact and lightweight laptop (13-inch or 14-inch screen) for travel, or would you prefer a larger display?

Once you let me know your preferences, I will recommend the best options from our inventory.
### Customer

> Software development.
>
> Compact.

### NovaAssist

**Recommended Product**

**TitanBook Air 14**

**Price:** ₹74,999

**Key Features**

* Intel Core i5 13th Gen
* 16GB LPDDR5 RAM
* 512GB SSD
* 14-inch QHD IPS Display
* Up to 12 Hours Battery Life

**Reason**

TitanBook Air 14 fully satisfies the customer's requirements for software development while remaining within the specified budget. Its lightweight design and 16GB RAM make it well suited for development workloads.

---

### What this demonstrates

* Intent recognition
* Minimal clarification questions
* Domain-specific recommendation rules
* Requirement-based filtering

---

# Conversation 2 – Product Comparison

### Customer

> Compare TitanBook Air 14 and AeroGlide Pro 16.

### NovaAssist

| Feature   | TitanBook Air 14         | AeroGlide Pro 16         |
| --------- | ------------------------ | ------------------------ |
| Price     | ₹74,999                  | ₹139,999                 |
| Processor | Intel Core i5 (13th Gen) | Intel Core i7 (13th Gen) |
| RAM       | 16GB                     | 32GB                     |
| Storage   | 512GB SSD                | 1TB NVMe SSD             |
| GPU       | Integrated               | NVIDIA RTX 4060          |
| Weight    | 1.25 kg                  | 2.1 kg                   |
| Warranty  | 1 Year                   | 2 Years                  |

### Summary

* TitanBook Air 14 is better suited for portability and everyday software development.
* AeroGlide Pro 16 is better suited for gaming, AI workloads, and high-performance creative work.

---

### What this demonstrates

* Objective product comparison
* Trade-off explanation
* Hallucination prevention
* Structured response formatting

---

# Conversation 3 – Hallucination Prevention

### Customer

> I want to buy an iPhone 16 Pro Max.

### NovaAssist

The iPhone 16 Pro Max is not available in the NovaMart product catalog.

However, we currently offer these premium alternatives:

* Zenith Pro Max
* Prime Fold X

Please let me know if you'd like to compare these models.

---

### What this demonstrates

* Hallucination prevention
* Catalog-constrained recommendations
* Helpful alternative suggestions

---

# Conversation 4 – Order Tracking

### Customer

> Where is my order?

### NovaAssist

Could you please provide your Order ID?

### Customer

> #NM-99999

### NovaAssist

I couldn't find that Order ID in our system.

Please verify the Order ID from your invoice or confirmation email.

If the issue persists, I can help summarize the issue and connect you with a human support representative.

---

### What this demonstrates

* Order validation
* Privacy-aware workflow
* Human escalation support

---

# Demo Summary

The conversations above demonstrate NovaAssist's core capabilities:

* AI-powered product recommendations
* Objective product comparisons
* FAQ and policy retrieval
* Secure order support
* Hallucination prevention
* Structured conversation workflow
* Prompt-engineered decision making
