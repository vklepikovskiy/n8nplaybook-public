## 📁 The n8n Playbook Workflows
A collection of production-ready n8n workflow templates optimized for self-hosted environments.

### 🏗️ 1. Core Architecture & Logic
Standards for building maintainable, testable, and complex logic without heavy coding.
| File | Description | Blog Post |
| :--- | :--- | :--- |
| `testable_sub_workflow.json` | A "dual-input" structure allowing for isolated sub-workflow testing. Uses a `Manual Trigger` and `Test Input` node to mock data payloads. | [How to Properly Test Your n8n Sub-workflows](https://n8nplaybook.com/post/2025/06/how-to-test-n8n-subworkflows/) |
| `asynchronous_poc.json` | A Proof of Concept (PoC) for asynchronous processing in n8n. It demonstrates how to trigger long-running sub-workflows and use `Wait` nodes with webhooks to re-sync parallel tracks. | [Asynchronous n8n Workflows: A Parallel Processing POC](https://n8nplaybook.com/post/2025/09/asynchronous-n8n-workflows-parallel-processing-poc/) |
| `fibonacci.json` | An iterative implementation of the Fibonacci sequence. It showcases how to handle state, variables, and loops using standard nodes (Switch, Edit Fields) instead of custom JavaScript. | [A Fun Project: Building an Iterative Fibonacci Generator in n8n](https://n8nplaybook.com/post/2025/09/n8n-iterative-fibonacci-sequence/) |
| `nested_loops.json` | A blueprint for handling nested iteration in n8n. Solves the "loop-in-loop" limitation by offloading the inner logic to a modular sub-workflow. | [How to Handle Nested Loops in n8n with Sub-workflows](https://n8nplaybook.com/post/2025/07/how-to-handle-nested-loops-in-n8n-with-sub-workflows/) |

### 🤖 2. AI & LLM Automation
Leveraging Large Language Models and AI Agents to build intelligent assistants.
| File | Description | Blog Post |
| :--- | :--- | :--- |
| `ai_inventory_assistant.json` | A smart AI assistant that uses Google Sheets as a database. Features conversational memory to handle follow-up questions and partial matching for product lookups. | [Build Your Own AI Sales Assistant: The Simplest Inventory Agent](https://n8nplaybook.com/post/2026/02/simple-n8n-inventory-ai-agent/) |

### 🛡️ 3. Resilience & Error Handling
Patterns to handle API rate limits, service outages, and execution conflicts.
| File | Description | Blog Post |
| :--- | :--- | :--- |
| `retry_delay_logic.json` | An advanced retry pattern that overcomes n8n's default node limits. Supports custom retry counts, long delays, and logic for exponential backoff to handle unstable APIs. | [Mastering Custom Retry and Delay Logic in n8n](https://n8nplaybook.com/post/2025/06/mastering-custom-retry-and-delay-logic-in-n8n/) |
| `google_sheets_quota_errors.json` | Specifically designed to prevent "Too Many Requests" errors with Google APIs. It uses a recursive `Wait` loop to automatically retry batch updates after a 1-minute backoff if rate limits are hit. | [Handling Google Sheets API Rate Limits in n8n](https://n8nplaybook.com/post/2025/07/handling-google-sheets-api-rate-limits-in-n8n/) |
| `simultaneous_executions.json` | Prevents multiple instances of a scheduled workflow from running concurrently by utilizing n8n's **Execution Timeout** setting. This ensures sequential processing and avoids race conditions or data duplication. | [How to Prevent Concurrent n8n Workflows with a Simple Trick](https://n8nplaybook.com/post/2025/07/how-to-prevent-concurrent-n8n-workflows/) |

### 💾 4. Data Transformation & Web Tools
Automating the extraction, conversion, and processing of web-based data.
| File | Description | Blog Post |
| :--- | :--- | :--- |
| `web_scraper.json` | A highly configurable multi-page scraper. Allows defining target URLs, CSS selectors for fields, and pagination links via a single JSON configuration node. | [Flexible Web Scraping with n8n: A Configurable, Multi-Page Template](https://n8nplaybook.com/post/2025/10/flexible-n8n-scraper-template/) |
| `screenshot_scraping.json` | A comparative workflow for **ScraperAPI**, **Scrapingdog**, and **ScreenshotOne**. Ideal for selecting the best screenshot service for your needs. | [Taking Website Screenshots in n8n: A Review of Three Services](https://n8nplaybook.com/post/2025/09/n8n-screenshot-services-review/) |
| `no_code_base64.json` | A pure no-code solution to convert multiple binary files to Base64 strings. Uses native nodes to unzip, extract, and transform data. | [The No-Code Evolution: Base64 Encoding Multiple Files in n8n (Part 2)](https://n8nplaybook.com/post/2025/10/no-code-base64-encoding-in-n8n/) |
| `base64_encode.json` | Demonstrates how to download a ZIP file, extract its contents, and use a **Code** node to Base64-encode multiple binary files for API uploads. | [From Binary to Base64: A Guide to File Encoding in n8n Workflows](https://n8nplaybook.com/post/2025/08/from-binary-to-base64-in-n8n/) |

### 🔗 5. API & Interface Integration
Turning n8n into a backend service or using external apps as a frontend.
| File | Description | Blog Post |
| :--- | :--- | :--- |
| `rest_api.json` | A full CRUD (Create, Read, Update, Delete) REST API implementation using n8n Webhooks. It uses Google Sheets as the database backend to store and retrieve data. | [Build a Simple REST API in 10 Minutes with n8n & Google Sheets](https://n8nplaybook.com/post/2025/08/n8n-google-sheets-rest-api/) |
| `google_sheets_ui.json` | Demonstrates how to use Google Sheets as a low-code interface to control n8n. Features a status-based loop (`READY` -> `DONE`) to trigger actions and write back results to specific rows. | [Elevate Your n8n Workflows: Google Sheets as Your Intuitive UI 🚀](https://n8nplaybook.com/post/2025/06/google-sheets-as-n8n-ui/) |
