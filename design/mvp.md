# AI Complaint Desk: MVP

Pain: complaints wait in a single queue, urgent ones behind trivial ones,
and replies to the same problem are inconsistent.

Product: an assistant for customer service agents. For each complaint, it
determines the category and urgency and drafts a reply that follows the
company's policies. The agent reviews the draft, asks for changes if needed,
and sends it.

| Feature                                               | Technique               |
| ----------------------------------------------------- | ----------------------- |
| Determining the category and urgency of a complaint   | LLM call                |
| Storing the complaint with its department and urgency | Ordinary code (not AI)  |
| Looking up the customer's order and its status        | Tool calling            |
| Drafting a reply that follows the company's policies  | RAG, LLM call           |
| Revising the reply based on the agent's requests      | Multi-turn conversation |