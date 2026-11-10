# AI Engineer Roadmap

**Goal:** Land a Canadian AI engineer job (applied LLM / ML systems), with skills that also transfer to an engineering + AI business later.

**Pace:** ~10 h/week. Hours are course or reading time (from the course pages, which sometimes conflict, so treat them as estimates). Projects add time.

**How the tiers work (inside every section):**
- **1st** = what you need to be hireable for this role. Do these first.
- **2nd** = likely useful. Do next, or earlier if postings ask for it.
- **3rd** = things you *might* need. Only if postings or interviews ask for them.

**How I chose them:** the 1st tier targets the gaps visible in your CV (no deployed service, CI, backend, cloud or system-design practice) plus what these roles routinely test (Python, SQL, coding rounds, building LLM apps). It is not copied from any one source. Some sources sell the products they recommend (DeepLearning.AI sells courses, and Anthropic, the maker of Claude, made the Claude Code course), so I judged those on content and flagged them. **Your own postings tally (`notes/postings.md`) is the real arbiter: re-order the tiers after you've tallied 30–40 postings.**

**Rough totals (my estimates):** 1st tier ≈ 170 h (~4 months), 1st + 2nd ≈ 500 h (~12 months), everything ≈ 750 h.
**Checkpoint:** start applying after the 1st tier of Sections 1–4 and Project 2 deployed (~90 h, ~2–3 months). Keep learning while you apply.

> Coursera links go to the specialization or certificate page. Check each is covered by your Coursera Plan. DeepLearning.AI courses are on its own platform: free to audit (some "free for a limited time"), with certificates tied to a paid membership. Confirm current terms on each page.

---

## Next

- [ ] Section 1, 1st: The Missing Semester, lecture 1 (shell)

---

# Core sequence

## 1. Dev workflow and tooling
Why: your experience is research code and analysis. Teams expect Git, pull requests, tests and CI as habits.

- **1st**
  - [ ] [The Missing Semester](https://github.com/ossu/computer-science#cs-tools) (shell, Git, debugging, tooling), ~24 h
  - [ ] Environments: [Python venv tutorial](https://docs.python.org/3/tutorial/venv.html), then [uv](https://docs.astral.sh/uv/) (`pyproject.toml`, lock files), ~2 h
  - [ ] Tests: [pytest Get Started](https://docs.pytest.org/en/stable/getting-started.html), ~3 h
  - [ ] Lint and format: [ruff tutorial](https://docs.astral.sh/ruff/tutorial/), ~2 h
  - [ ] [GitHub Skills: Introduction to GitHub](https://github.com/skills/introduction-to-github), the Review pull requests course on [GitHub Skills](https://learn.github.com/skills), and [Test with Actions](https://github.com/skills/test-with-actions) (CI), ~6 h
- **2nd**
  - [ ] [IBM Applied Software Engineering Fundamentals](https://www.coursera.org/specializations/software-engineering-fundamentals): Introduction to Software Engineering (15 h) and Getting Started with Git and GitHub (11 h). Take these if Git or software-process vocabulary still feels shaky after the 1st tier. They are beginner level.
- **3rd**
  - [ ] IBM: Hands-on Introduction to Linux Commands and Shell Scripting, 17 h (same specialization)
  - [ ] `.env` files and keeping secrets out of Git, type hints, project layout (`src/`, `tests/`), pre-commit hooks
  - [ ] One small open-source contribution, to experience real code review

Practice on this repo: a GitHub Issue per task, a branch, a pull request that closes it, and CI running pytest and ruff before merge.
**Done when:** a new project of yours has an isolated environment, `pyproject.toml`, tests, linter, CI workflow and README, created from scratch.

## 2. Backend, APIs and Docker
Why: this is where a model becomes a service other people can use.

- **1st**
  - [ ] [FastAPI official tutorial](https://fastapi.tiangolo.com/tutorial/): routes, validation, dependencies, auth basics, testing, ~10 h
  - [ ] [Docker: Get Started](https://docs.docker.com/get-started/), then write a Dockerfile for Project 2, ~6 h
  - [ ] Add structured logging to Project 2
- **2nd**
  - [ ] [Ultimate Guide to FastAPI and Backend Development](https://www.coursera.org/specializations/packt-ultimate-guide-to-fast-api-and-backend-development) (Packt, ~36 h): a structured course covering SQLModel, OAuth2/JWT, pytest, Docker, async and deployment. Rated 4.1 from only 27 reviews, so preview it first.
  - [ ] From the [IBM Back-End Development Professional Certificate](https://www.coursera.org/professional-certificates/ibm-backend-development): Introduction to Containers w/ Docker, Kubernetes & OpenShift (17 h, focus on Docker) and Monitoring and Observability for Development and DevOps (16 h)
- **3rd**
  - [ ] IBM: Application Development using Microservices and Serverless, 16 h
  - [ ] Kubernetes beyond the basics

## 3. SQL and data modeling
- **1st**
  - [ ] SQL fluency: joins, CTEs, window functions, indexes and query plans on a real dataset. A structured option is [The Structured Query Language (SQL)](https://www.coursera.org/specializations/databases-for-data-scientists) (Boulder, 27 h).
- **2nd**
  - [ ] Relational Database Design (Boulder, same specialization, 35 h). While you do it, practice choosing a data model from an app's access patterns. Free alternative: [OSSU: Stanford Databases](https://github.com/ossu/computer-science#core-applications).
- **3rd**
  - [ ] Advanced Topics and Future Trends in Database Technologies (Boulder, 17 h): NoSQL such as MongoDB and Redis
  - [ ] Reading: transactions, concurrency, schema migrations, data privacy and the data lifecycle

## 4. Deploying ML and cloud
- **1st**
  - [ ] [Machine Learning in Production](https://www.coursera.org/learn/introduction-to-machine-learning-in-production) (DeepLearning.AI, Andrew Ng, ~11 h, 4.8 rating): ML lifecycle, deployment patterns, concept drift, error analysis
  - [ ] Deploy Project 2 to one managed cloud service (Azure Container Apps or similar) using Microsoft Learn docs, then write down how you'd monitor drift and what the service costs per 1,000 requests
- **2nd**
  - [ ] [Microsoft AI & ML Engineering Professional Certificate](https://www.coursera.org/professional-certificates/microsoft-ai-and-ml-engineering): only course 4, Microsoft Azure for AI and Machine Learning, 21 h
- **3rd**
  - [ ] An Azure AI associate exam. Before booking, check Microsoft Learn for the current one: Microsoft's AB-100 page lists AI-103 (and not AI-102) among its prerequisites, so AI-102 may be on its way out. I couldn't confirm that.
  - [ ] Later, only if relevant: [AB-100](https://learn.microsoft.com/en-us/credentials/certifications/agentic-ai-business-solutions-architect/) (expert level, needs a qualifying associate certification)

Azure is my default because it was suggested to you and one salary guide lists Azure experience as a differentiator in Canada. Confirm against your postings tally. The skills transfer between clouds.

## 5. LLM application basics
Why: knowing how tokens, context windows and tool calling work tells you when to trust a model and how to choose one.

- **1st**
  - [ ] [Karpathy: Let's build the GPT Tokenizer](https://karpathy.ai/zero-to-hero.html) (lecture 8, 2h13m)
  - [ ] Your model provider's docs on structured output, tool calling, context windows, prompt caching and sampling parameters. Try each in a notebook, ~6 h.
- **2nd**
  - [ ] Karpathy lectures 1, 2 and 7 (micrograd, makemore, build GPT), ~6 h of video, plan ~15 h to code along
  - [ ] [Generative AI with Large Language Models](https://www.coursera.org/learn/generative-ai-with-llms) (DeepLearning.AI + AWS, ~17 h): fine-tuning, LoRA, RLHF, three labs on AWS (setup can be rough). Useful if roles involve adapting models, less so for pure application work.
- **3rd**
  - [ ] Project 6 (optional): fine-tune or adapt a small model for one task, with a short write-up
  - [ ] Self-hosting models and fine-tuning vs. prompting tradeoffs

You already have the ML foundations (bias/variance, error analysis, data engineering). Re-read as needed.

## 6. Grounding models with data (RAG)
- **1st**
  - [ ] [Building and Evaluating Advanced RAG](https://www.deeplearning.ai/courses/building-evaluating-advanced-rag) (DeepLearning.AI, ~2 h, free for a limited time), then build Project 4 using provider docs and one library of your choice
  - [ ] Rebuild the core retrieval with plain API calls and a vector store, so you understand what the library does
- **2nd**
  - [ ] [IBM RAG and Agentic AI Professional Certificate](https://www.coursera.org/professional-certificates/ibm-rag-and-agentic-ai): Develop Generative AI Applications (10 h), Build RAG Applications (7 h), Vector Databases for RAG (9 h), Advanced RAG with Vector Databases and Retrievers (8 h). These teach LangChain and watsonx specifics, so always rebuild the example without the framework.
- **3rd**
  - [ ] Beyond vector search: what to put in the prompt vs. let the model retrieve with tools, turning PDFs and HTML into model-ready text, and when a knowledge graph or a semantic layer over SQL fits better

## 7. Agents and tool calling
- **1st**
  - [ ] [Agentic AI](https://www.deeplearning.ai/courses/agentic-ai) (DeepLearning.AI, Andrew Ng, ~10 h): reflection, tool use and MCP, evals and error analysis, planning, multi-agent patterns. Free to audit; the certificate needs the paid membership.
- **2nd**
  - [ ] From the [IBM RAG and Agentic AI certificate](https://www.coursera.org/professional-certificates/ibm-rag-and-agentic-ai): Fundamentals of Building AI Agents (11 h) and Agentic AI with LangChain and LangGraph (11 h)
- **3rd**
  - [ ] IBM: Build AI Agents using MCP, 10 h
  - [ ] IBM: RAG and Agentic AI Capstone Project, 14 h (can serve as Project 5)

## 8. Evaluation
Why: this is the strongest asset you already have. You need to apply it to deployed apps, not learn it from scratch.
- **1st**
  - [ ] Build an eval set for Project 4 and Project 5, look at traces and outputs, and run error analysis to decide what to fix next
  - [ ] The evals module of [Agentic AI](https://www.deeplearning.ai/courses/agentic-ai) (module 4)
- **2nd**
  - [ ] Use all three eval types where each fits: code-based checks, LLM-as-judge (validated against human labels) and human review. Reuse your Western research methods. Write up one eval, what it found and what you changed, in `notes/` or a public post.
- **3rd**
  - [ ] Skim [LLM Optimization & Evaluation](https://www.coursera.org/specializations/llm-optimization-evaluation) (Coursera, 13 short courses, ~34 h)
  - [ ] Look for "Evaluating and Improving Agentic Applications" on [deeplearning.ai/courses](https://www.deeplearning.ai/courses) (advertised on its skills map page; I could not verify it)

## 9. Coding interviews (data structures and algorithms)
- **1st**
  - [ ] ~50 easy/medium problems from a curated list such as Blind 75 or NeetCode 150: arrays, hashing, two pointers, trees, graphs, basic DP (~40 h). Explain each solution out loud.
- **2nd**
  - [ ] [Algorithms Specialization](https://www.coursera.org/specializations/algorithms) (Stanford, 4.8 rating), courses 1–2: Divide and Conquer, Sorting and Searching, and Randomized Algorithms (15 h) and Graph Search, Shortest Paths, and Data Structures (14 h). It expects some discrete probability and comfort with proofs. Follow with ~50 more problems.
- **3rd**
  - [ ] Courses 3–4 of the same specialization (greedy/dynamic programming, NP-completeness), 28 h

## 10. System and software design
Why: knowing the tradeoffs (latency, availability, consistency, cost) lets you steer coding agents and answer design interviews.
- **1st**
  - [ ] One system-design primer (~10 h) covering caching, queues, databases, load balancing and consistency. Then sketch three designs on paper, including an LLM app such as your RAG service.
- **2nd**
  - [ ] Selected chapters of *Designing Data-Intensive Applications* (~30 h)
- **3rd**
  - [ ] [Software Design and Architecture](https://www.coursera.org/specializations/software-design-architecture) (University of Alberta, ~52 h). It uses **Java**, so it is a language detour; take the ideas.
  - [ ] One book on clean code and design (e.g. *A Philosophy of Software Design*)

## 11. Security
- **1st** (~5 h)
  - [ ] [OWASP Top 10](https://owasp.org/www-project-top-ten/) overview, secrets management, authentication basics (JWT/OAuth), dependency scanning in CI
  - [ ] Prompt injection and data leakage for LLM apps (the OWASP Top 10 for LLM applications)
- **2nd**
  - [ ] [Application Security for Developers and DevOps Professionals](https://www.coursera.org/learn/application-security-for-developers-devops) (IBM, ~17 h, 4.7 rating)
- **3rd**
  - [ ] [Fundamentals of Secure Software Design](https://www.coursera.org/learn/fundamentals-of-secure-software-design) (STARWEAVER, ~9 h; the page shows no rating)
  - [ ] [Principles of Secure Coding](https://www.coursera.org/learn/secure-coding-principles) (UC Davis, ~16 h, 4.4 rating; labs lean on C)

---

# Tracks that run alongside (start around Section 2)

## A. Working with coding agents
- **1st**
  - [ ] Apply it on your own projects: write a spec before building, keep a `CLAUDE.md`/`AGENTS.md` describing the codebase, give the agent tests to check its own work, review everything it writes, and never give it access to production data. Note what failed.
- **2nd**
  - [ ] [Claude Code: A Highly Agentic Coding Assistant](https://www.deeplearning.ai/courses/claude-code-a-highly-agentic-coding-assistant) (DeepLearning.AI + Anthropic, ~2 h; free for a limited time). Anthropic makes Claude, so judge it on content. It's short.
- **3rd**
  - [ ] Hooks, MCP servers and skills; parallel agents; a short retrospective after each project on what worked
  - [ ] A weekly habit: try one new tool or workflow change and note the result

## B. Shaping the build
- **1st**
  - [ ] For every project, write a one-page spec: the problem, who it's for, what success looks like
- **2nd**
  - [ ] Show an early version to 2–3 real users and change it based on what they say. Ship in small batches (prototype, then MVP, then polish). Your volunteer program is a source of real users.
- **3rd**
  - [ ] Basic product and business sense: costs, unit economics, go-to-market
  - [ ] Practice explaining technical tradeoffs to non-technical people; propose and own one small improvement end to end

---

## Projects (details in `projects/README.md`)

1. SQL schema and queries (Section 3)
2. Dockerized FastAPI model service with tests, CI and logging (Sections 1, 2)
3. Project 2 deployed to Azure (Section 4)
4. RAG app with an eval set (Sections 6, 8)
5. Agent app with tools, evals, guardrails and a user-feedback round (Sections 7, 8, 11, Track B)
6. Optional: small-model fine-tuning write-up (Section 5, 2nd tier)

Each project gets a one-page spec, a README and a demo link or screenshots.

## Job-search track (starts after the checkpoint)

- [ ] Fix CV: remove the "(one only of the following two)" note; use the honest QuantumIntel wording we drafted
- [ ] Pull 30–40 Canadian AI/ML/data postings and tally required skills in `notes/postings.md`
- [ ] Re-order this roadmap's tiers based on what postings ask for most
- [ ] Add each project to the CV and GitHub profile (README + demo)
- [ ] Apply within 3–7 days of posting; ask for referrals; state work authorization briefly
- [ ] Check with your Western supervisor before open-sourcing research code

## Not needed (skip)

- Intro Python, calculus, most OSSU math ([Core math](https://github.com/ossu/computer-science#core-math)), Nand to Tetris and OS/architecture courses ([Core systems](https://github.com/ossu/computer-science#core-systems))
- Machine learning basics and the Deep Learning Specialization (~129 h): you already have these
- Boulder Data Structures and Algorithms specialization (~199 h): too long and theoretical for interview prep
- The IBM Python for Data Science and Flask courses (you'll use FastAPI)
- Edureka's "Learn Generative AI with LLMs" (mostly classic ML/NLP, 3.9 rating) and "Agentic AI Engineering" (3.3 from 12 reviews)
- IBM's multi-framework agents course and its separate "Building AI Agents and Agentic Workflows" specialization (they duplicate the certificate)
- Microsoft AI & ML Engineering certificate courses 1–3 and 5 (they overlap with earlier sections)

## Gap checklist
Use [roadmap.sh](https://roadmap.sh/) (AI Engineer and Backend roadmaps) and the [AI Engineering Skills Map](https://www.deeplearning.ai/resources/ai-engineering-skills) to spot topics you've missed. Don't follow them top to bottom.

## Weekly review (15 min, same day each week)
1. Tick what you finished.
2. Write the one next item at the top.
3. Note anything you were stuck on in `notes/`.

## Repo layout

```
README.md
ROADMAP.md
projects/     one folder per project, each with README + spec + demo
notes/        short write-ups, postings.md
```
