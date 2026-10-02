# n8n Architecture Validator 🚀 (Sanity Challenge)

An AI agent backend built on **Sanity Content Lake** and **Model Context Protocol (MCP)** to validate complex n8n workflows and prevent API rate-limit bottlenecks.

## The Problem
When chaining tools like HubSpot, Notion, and OpenAI in n8n, keyword searches aren't enough to prevent `429 Too Many Requests` errors. You need an agent that computes deterministic mathematical constraints.

## The Solution
We model API constraints (Rate Limits, Batching requirements, Tiered limits) as **Structured Data** in Sanity. The AI agent reads this through an MCP server and calculates the exact n8n node architecture needed (e.g., configuring a `Split In Batches` node to exactly 150 items/min).

## Try it
1. Clone this repo.
2. `cd studio && npm install && npm run dev`
3. Connect your MCP client (like Claude/Hermes) to your Sanity project.
