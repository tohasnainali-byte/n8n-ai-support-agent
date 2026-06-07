# AI Customer Support Agent

An automated workflow that handles inbound customer support emails using AI.

## What it does
- Reads incoming customer emails (Gmail trigger)
- Retrieves the relevant answer from a company's help docs using RAG (retrieval-augmented generation)
- Scores its own confidence in the answer
- If confident: drafts a reply automatically
- If not confident: escalates the email to a human instead of guessing

The confidence gate means the agent never sends hallucinated answers to customers — unknown questions go to a person.

## Stack
- n8n (workflow orchestration)
- Google Gemini (LLM + embeddings)
- In-memory vector store for retrieval
- Confidence-gated routing for human handoff

## Demo
[Watch the 90-second demo](YOUR_VIDEO_LINK_HERE)

## Setup
Import `support-agent.json` into n8n, add your Gemini and Gmail credentials, load your help docs via the ingest form, and activate.
