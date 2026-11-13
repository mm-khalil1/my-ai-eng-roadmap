# AI Engineer Roadmap

**Goal:** Land a Canadian AI engineer job (applied LLM / ML systems), with skills that also transfer to an engineering + AI business later.

**Pace:** ~10 h/week. Hours are course or reading time (from the course pages, which sometimes conflict, so treat them as estimates). Projects add time.

**The three levels (inside every section):**
- **MUST** = what postings and interviews for this role routinely require. Without these you will likely fail screens or the first days on the job.
- **RECOMMENDED** = improves your odds or speed. Do after the MUSTs, or earlier if postings ask for it.
- **EXTRA** = depth, credentials, or things you *might* need. Only if postings or interviews ask for them, or you have spare time.

**How I decided:** this is my judgment, not any one source's. It's built on the gaps visible in your CV (no deployed service, CI, backend, data-structures, design or cloud practice) and on what these roles usually test (Python, SQL, coding rounds, building LLM apps with evals). I can't know for certain what you truly need without real postings. **Tally 30–40 Canadian postings in `notes/postings.md` and move items between levels based on what they ask for.** Some sources sell what they recommend (DeepLearning.AI sells courses, and Anthropic, the maker of Claude, made the Claude Code course), so I judged those on content and flagged them.

**Rough totals (my estimates):** MUST ≈ 200 h (~5 months), MUST + RECOMMENDED ≈ 640 h, everything ≈ 1,060 h. At 15 h/week the MUSTs take ~3.5 months.
**Checkpoint:** start applying after the MUST items of Sections 1–8 with Projects 2 and 4 deployed (~180 h, ~4–5 months). Keep learning, especially DSA, while you apply.

> Coursera links go to the specialization, certificate or course page. Check each is covered by your Coursera Plan. DeepLearning.AI courses are on its own platform: free to audit (some "free for a limited time"), with certificates tied to a paid membership. I opened the Coursera, DeepLearning.AI, Karpathy, GitHub Skills, uv/pytest/ruff, OWASP LLM, Cosmic Python and refactoring.guru pages. The other links (FastAPI, Docker, PostgreSQL, SQLBolt, Mode, NeetCode, LeetCode, OpenAI and Anthropic docs, Microsoft Learn, system-design-primer, dataintensive.net, MCP and Claude Code docs) are well-known sites I didn't open here. If one is broken, tell me.

---

## Next

- [ ] Section 1, MUST: The Missing Semester, lecture 1 (shell)

---

# Core sequence

## 1. Dev workflow and tooling
Why: your experience is research code and analysis. Teams expect Git, pull requests, tests and CI as habits.

- **MUST**
  - [ ] [The Missing Semester](https://github.com/ossu/computer-science#cs-tools) (shell, Git, debugging, tooling), ~24 h
  - [ ] Environments: [Python venv tutorial](https://docs.python.org/3/tutorial/venv.html), then [uv](https://docs.astral.sh/uv/) (`pyproject.toml`, lock files), ~2 h
  - [ ] Tests: [pytest Get Started](https://docs.pytest.org/en/stable/getting-started.html), ~3 h
  - [ ] Lint and format: [ruff tutorial](https://docs.astral.sh/ruff/tutorial/), ~2 h
  - [ ] [GitHub Skills: Introduction to GitHub](https://github.com/skills/introduction-to-github), the Review pull requests course on [GitHub Skills](https://learn.github.com/skills), and [Test with Actions](https://github.com/skills/test-with-actions) (CI), ~6 h
- **RECOMMENDED**
  - [ ] Practice on this repo: a GitHub Issue per task, a branch, a pull request that closes it, and CI running pytest and ruff before merge
- **EXTRA**
  - [ ] [IBM Applied Software Engineering Fundamentals](https://www.coursera.org/specializations/software-engineering-fundamentals): Introduction to Software Engineering (15 h), Getting Started with Git and GitHub (11 h) and Linux Commands and Shell Scripting (17 h). Beginner level; take them only if Git or software-process vocabulary still feels shaky.
  - [ ] `.env` files and keeping secrets out of Git ([Twelve-Factor App: Config](https://12factor.net/config)), type hints ([Python typing docs](https://docs.python.org/3/library/typing.html)), pre-commit hooks ([pre-commit.com](https://pre-commit.com/))
  - [ ] One small open-source contribution ([First Contributions](https://github.com/firstcontributions/first-contributions)), to experience real code review

**Done when:** a new project of yours has an isolated environment, `pyproject.toml`, tests, linter, CI workflow and README, created from scratch.

## 2. Data structures and algorithms (start now, runs alongside Sections 3–10)
Why: you haven't studied DSA before, and coding rounds gate many interviews. Solve everything in Python.

- **MUST** (in this order, ~77 h)
  - [ ] [Foundations of Data Structures & Algorithms in Python](https://www.coursera.org/learn/packt-foundations-of-data-structures-algorithms-in-python-0odnl) (Packt, ~14 h): Big-O, arrays, sorting, linked lists and hash tables, with LeetCode-style problems. No prior DSA needed. The page shows no rating and can't be audited.
  - [ ] [Data Structures](https://www.coursera.org/specializations/data-structures-algorithms) (course 2 of the UC San Diego specialization, ~23 h): dynamic arrays, priority queues and heaps, hash tables, balanced trees
  - [ ] Practice, ~40 h: after each course, solve the matching problems from the [NeetCode roadmap](https://neetcode.io/roadmap) on [LeetCode](https://leetcode.com/problemset/) (about 50 easy/medium in total, including stacks, queues, trees and BFS/DFS on graphs). Explain each solution out loud. Don't save practice for the end.
- **RECOMMENDED**
  - [ ] Algorithmic Toolbox (course 1 of the same [UC San Diego specialization](https://www.coursera.org/specializations/data-structures-algorithms), ~41 h): greedy algorithms, binary search, divide and conquer, dynamic programming
  - [ ] Algorithms on Graphs (course 3, ~55 h): traversal, shortest paths, minimum spanning trees. If short on time, do traversal and shortest paths first.
  - [ ] ~60 more mixed-topic problems, timed, plus a few mock interviews (~50 h)
- **EXTRA**
  - [ ] A rigorous second pass: [Algorithms Specialization](https://www.coursera.org/specializations/algorithms) (Stanford, 4.8 rating, ~57 h; expects discrete probability and comfort with proofs) or [Algorithms, Part I](https://www.coursera.org/learn/algorithms-part1) (Princeton, 4.9 rating, free but no certificate, ~54 h; assignments in **Java**)
  - [ ] UC San Diego: Algorithms on Strings (~19 h) and Advanced Algorithms and Complexity (~27 h)

About the UC San Diego specialization: Python is allowed, it assumes you can follow proofs by induction and contradiction, and it has ~100 auto-checked coding problems. Its page says "5 months at 10 hours a week" but the six courses' hours add up to ~182 h. It is rated 4.6 from about 16,800 reviews.

## 3. Software design (OOP, SOLID, patterns)
Why: you'll write and review code that others maintain, including code written by coding agents. Basic design principles let you steer both.

- **MUST** (~8 h)
  - [ ] [Object Oriented Python](https://www.coursera.org/learn/packt-object-oriented-python-bptn4) (Packt, ~8 h): classes, encapsulation, inheritance, polymorphism, composition, and a refactoring project. No prior OOP needed. It covers no SOLID, patterns or testing, and shows no rating.
- **RECOMMENDED**
  - [ ] [Mastering Python Design Patterns](https://www.coursera.org/learn/packt-mastering-python-design-patterns) (Packt, ~18 h): SOLID, Factory, Adapter, Decorator, Facade, Observer, Strategy, dependency injection, anti-patterns. Some assignments are AI-graded, it shows no rating, and some module descriptions promise more than the lessons cover. Take the SOLID and core-pattern modules and skim the rest.
  - [ ] [Cosmic Python](https://www.cosmicpython.com/) (the free online book *Architecture Patterns with Python*, Part 1, chapters 1–7, ~20 h): domain modeling, repository pattern, service layer, TDD, unit of work. See the [table of contents](https://www.cosmicpython.com/book/preface.html). It uses Flask, SQLAlchemy and pytest. Apply it to Project 2.
  - [ ] Reference: [Design Patterns in Python (refactoring.guru)](https://refactoring.guru/design-patterns/python), a catalog of pattern examples in Python. Check the site's terms for free access to the full catalog.
- **EXTRA**
  - [ ] Cosmic Python Part 2: events and the message bus, commands, CQRS, dependency injection (chapters 8–13)
  - [ ] [Software Design and Architecture](https://www.coursera.org/specializations/software-design-architecture) (University of Alberta, ~52 h). It uses **Java**, so it is a language detour; take the ideas.

## 4. Backend, APIs and Docker
Why: this is where a model becomes a service other people can use.

- **MUST** (~17 h)
  - [ ] [FastAPI official tutorial](https://fastapi.tiangolo.com/tutorial/): routes, validation, dependencies, testing, ~10 h
  - [ ] [Docker: Get Started](https://docs.docker.com/get-started/), then write a Dockerfile for Project 2 following [FastAPI in Containers](https://fastapi.tiangolo.com/deployment/docker/), ~7 h
  - [ ] Add structured logging to Project 2 ([Python logging how-to](https://docs.python.org/3/howto/logging.html))
- **RECOMMENDED**
  - [ ] [Ultimate Guide to FastAPI and Backend Development](https://www.coursera.org/specializations/packt-ultimate-guide-to-fast-api-and-backend-development) (Packt, ~36 h): a structured course covering SQLModel, OAuth2/JWT, pytest, Docker, async and deployment. Rated 4.1 from only 27 reviews, so preview it first.
  - [ ] Free alternative: [freeCodeCamp FastAPI course](https://www.classcentral.com/course/freecodecamp-fastapi-course-for-beginners-104922) (YouTube, ~19 h): Postgres, SQLAlchemy, JWT auth, testing and deployment. Do this or the Packt course, not both.
  - [ ] From the [IBM Back-End Development Professional Certificate](https://www.coursera.org/professional-certificates/ibm-backend-development): Introduction to Containers w/ Docker, Kubernetes & OpenShift (17 h, focus on Docker) and Monitoring and Observability for Development and DevOps (16 h)
- **EXTRA**
  - [ ] IBM: Application Development using Microservices and Serverless, 16 h (same certificate)
  - [ ] Kubernetes beyond the basics ([Kubernetes docs: tutorials](https://kubernetes.io/docs/tutorials/))

## 5. SQL and data modeling
- **MUST** (pick one path, ~15–27 h)
  - [ ] Structured: [The Structured Query Language (SQL)](https://www.coursera.org/specializations/databases-for-data-scientists) (Boulder, 27 h)
  - [ ] Or free: [SQLBolt](https://sqlbolt.com/) and the [Mode SQL tutorial](https://mode.com/sql-tutorial/)
  - [ ] Either way, practice joins, CTEs, indexes and [window functions](https://www.postgresql.org/docs/current/tutorial-window.html) on a real dataset (Project 1), plus [LeetCode's Top SQL 50](https://leetcode.com/studyplan/top-sql-50/)
- **RECOMMENDED**
  - [ ] Relational Database Design (Boulder, same [specialization](https://www.coursera.org/specializations/databases-for-data-scientists), 35 h). While you do it, practice choosing a data model from an app's access patterns. Free alternative: [OSSU: Stanford Databases](https://github.com/ossu/computer-science#core-applications).
- **EXTRA**
  - [ ] Advanced Topics and Future Trends in Database Technologies (Boulder, 17 h): NoSQL such as MongoDB and Redis
  - [ ] Reading: transactions, concurrency, schema migrations, data privacy and the data lifecycle ([dataintensive.net](https://dataintensive.net/) chapters 7 and 12)

## 6. Deploying ML and cloud
- **MUST** (~4 h of docs plus project time)
  - [ ] Deploy Project 2 to one managed cloud service (for example Azure Container Apps) using the [Azure Container Apps docs](https://learn.microsoft.com/en-us/azure/container-apps/). Then write down how you'd monitor drift and what the service costs per 1,000 requests.
- **RECOMMENDED**
  - [ ] [Machine Learning in Production](https://www.coursera.org/learn/introduction-to-machine-learning-in-production) (DeepLearning.AI, Andrew Ng, ~11 h, 4.8 rating): ML lifecycle, deployment patterns, concept drift, error analysis
  - [ ] [Microsoft AI & ML Engineering Professional Certificate](https://www.coursera.org/professional-certificates/microsoft-ai-and-ml-engineering): only course 4, Microsoft Azure for AI and Machine Learning, 21 h
- **EXTRA**
  - [ ] An Azure AI associate exam. Before booking, check [Microsoft Learn certifications](https://learn.microsoft.com/en-us/credentials/certifications/) for the current one: Microsoft's AB-100 page lists AI-103 (and not AI-102) among its prerequisites, so AI-102 may be on its way out. I couldn't confirm that.
  - [ ] Later, only if relevant: [AB-100](https://learn.microsoft.com/en-us/credentials/certifications/agentic-ai-business-solutions-architect/) (expert level, needs a qualifying associate certification)

Azure is my default because it was suggested to you and one salary guide lists Azure experience as a differentiator in Canada. Confirm against your postings tally. The skills transfer between clouds.

## 7. LLM application basics
Why: knowing how tokens, context windows and tool calling work tells you when to trust a model and how to choose one.

- **MUST** (~8 h)
  - [ ] [Karpathy: Let's build the GPT Tokenizer](https://karpathy.ai/zero-to-hero.html) (lecture 8, 2h13m)
  - [ ] Your model provider's docs: [OpenAI docs](https://platform.openai.com/docs) or [Anthropic docs](https://docs.claude.com/en/docs/). Cover structured output, tool calling, context windows, prompt caching and sampling parameters, and try each in a notebook (~6 h).
- **RECOMMENDED**
  - [ ] [Karpathy lectures 1, 2 and 7](https://karpathy.ai/zero-to-hero.html) (micrograd, makemore, build GPT), ~6 h of video, plan ~15 h to code along
  - [ ] [Generative AI with Large Language Models](https://www.coursera.org/learn/generative-ai-with-llms) (DeepLearning.AI + AWS, ~17 h): fine-tuning, LoRA, RLHF, three labs on AWS (setup can be rough). Useful if roles involve adapting models, less so for pure application work.
- **EXTRA**
  - [ ] Project 6 (optional): fine-tune or adapt a small model for one task, with a short write-up ([Hugging Face LLM course](https://huggingface.co/learn/llm-course))
  - [ ] Self-hosting models and fine-tuning vs. prompting tradeoffs

You already have the ML foundations (bias/variance, error analysis, data engineering). Re-read as needed.

## 8. Grounding models with data (RAG)
- **MUST** (~2 h plus Project 4)
  - [ ] [Building and Evaluating Advanced RAG](https://www.deeplearning.ai/courses/building-evaluating-advanced-rag) (DeepLearning.AI, ~2 h, free for a limited time), then build Project 4 using your provider's docs and one library of your choice
  - [ ] Rebuild the core retrieval with plain API calls and a vector store, so you understand what the library does
- **RECOMMENDED**
  - [ ] From the [IBM RAG and Agentic AI Professional Certificate](https://www.coursera.org/professional-certificates/ibm-rag-and-agentic-ai): Vector Databases for RAG (9 h) and Advanced RAG with Vector Databases and Retrievers (8 h). They teach LangChain and watsonx specifics, so rebuild each example without the framework.
- **EXTRA**
  - [ ] IBM: Develop Generative AI Applications (10 h) and Build RAG Applications (7 h), same certificate
  - [ ] Beyond vector search: what to put in the prompt vs. let the model retrieve with tools, turning PDFs and HTML into model-ready text, and when a knowledge graph or a semantic layer over SQL fits better

## 9. Agents and tool calling
- **MUST** (~10 h)
  - [ ] [Agentic AI](https://www.deeplearning.ai/courses/agentic-ai) (DeepLearning.AI, Andrew Ng, ~10 h): reflection, tool use and MCP, evals and error analysis, planning, multi-agent patterns. Free to audit; the certificate needs the paid membership.
- **RECOMMENDED**
  - [ ] IBM: Agentic AI with LangChain and LangGraph (11 h, from the [IBM RAG and Agentic AI certificate](https://www.coursera.org/professional-certificates/ibm-rag-and-agentic-ai)). LangChain and LangGraph appear often in postings; check yours.
  - [ ] [Model Context Protocol docs](https://modelcontextprotocol.io/): build one small MCP server for Project 5
- **EXTRA**
  - [ ] IBM: Fundamentals of Building AI Agents (11 h), Build AI Agents using MCP (10 h) and the RAG and Agentic AI Capstone Project (14 h, can serve as Project 5)

## 10. Evaluation
Why: this is the strongest asset you already have. You need to apply it to deployed apps, not learn it from scratch.
- **MUST**
  - [ ] Build an eval set for Project 4 and Project 5, look at traces and outputs, and run error analysis to decide what to fix next. Guide: the evals module (module 4) of [Agentic AI](https://www.deeplearning.ai/courses/agentic-ai).
- **RECOMMENDED**
  - [ ] Use all three eval types where each fits: code-based checks, LLM-as-judge (validated against human labels) and human review. Reuse your Western research methods. Write up one eval, what it found and what you changed, in `notes/` or a public post.
- **EXTRA**
  - [ ] Skim [LLM Optimization & Evaluation](https://www.coursera.org/specializations/llm-optimization-evaluation) (Coursera, 13 short courses, ~34 h)

(DeepLearning.AI's skills map page advertises a course called "Evaluating and Improving Agentic Applications". I could not verify it; check [deeplearning.ai/courses](https://www.deeplearning.ai/courses).)

## 11. System design
Why: knowing the tradeoffs (latency, availability, consistency, cost) lets you steer coding agents and answer design interviews. It builds on the data structures from Section 2.
- **MUST** (~10 h)
  - [ ] Skim the [System Design Primer](https://github.com/donnemartin/system-design-primer): caching, queues, databases, load balancing and consistency. Then sketch three designs on paper, including an LLM app such as your RAG service.
- **RECOMMENDED**
  - [ ] Selected chapters of *Designing Data-Intensive Applications* ([dataintensive.net](https://dataintensive.net/), ~30 h)
- **EXTRA**
  - [ ] Software Architecture and Service-Oriented Architecture courses in the Alberta [Software Design and Architecture](https://www.coursera.org/specializations/software-design-architecture) specialization (Java, 10 h each)

## 12. Security
- **MUST** (~5 h)
  - [ ] [OWASP Top 10](https://owasp.org/www-project-top-ten/) overview and the [OWASP Top 10 for LLM applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) (prompt injection, data leakage)
  - [ ] [FastAPI security tutorial](https://fastapi.tiangolo.com/tutorial/security/) (JWT/OAuth basics), secrets management, and dependency scanning in CI
- **RECOMMENDED**
  - [ ] [Application Security for Developers and DevOps Professionals](https://www.coursera.org/learn/application-security-for-developers-devops) (IBM, ~17 h, 4.7 rating)
- **EXTRA**
  - [ ] [Fundamentals of Secure Software Design](https://www.coursera.org/learn/fundamentals-of-secure-software-design) (STARWEAVER, ~9 h; the page shows no rating)
  - [ ] [Principles of Secure Coding](https://www.coursera.org/learn/secure-coding-principles) (UC Davis, ~16 h, 4.4 rating; labs lean on C)

---

# Tracks that run alongside (start around Section 4)

## A. Working with coding agents
- **MUST**
  - [ ] Apply it on your own projects, following the [Claude Code docs](https://docs.claude.com/en/docs/claude-code/overview) or your tool's: write a spec before building, keep a `CLAUDE.md`/`AGENTS.md` describing the codebase, give the agent tests to check its own work, review everything it writes, and never give it access to production data. Note what failed.
- **RECOMMENDED**
  - [ ] [Claude Code: A Highly Agentic Coding Assistant](https://www.deeplearning.ai/courses/claude-code-a-highly-agentic-coding-assistant) (DeepLearning.AI + Anthropic, ~2 h; free for a limited time). Anthropic makes Claude, so judge it on content. It's short.
- **EXTRA**
  - [ ] Hooks, MCP servers and skills; parallel agents; a short retrospective after each project on what worked
  - [ ] A weekly habit: try one new tool or workflow change and note the result

## B. Shaping the build
- **MUST**
  - [ ] For every project, write a one-page spec with [`projects/SPEC_TEMPLATE.md`](projects/SPEC_TEMPLATE.md): the problem, who it's for, what success looks like
- **RECOMMENDED**
  - [ ] Show an early version to 2–3 real users and change it based on what they say. Ship in small batches (prototype, then MVP, then polish). Your volunteer program is a source of real users.
- **EXTRA**
  - [ ] Basic product and business sense: costs, unit economics, go-to-market
  - [ ] Practice explaining technical tradeoffs to non-technical people; propose and own one small improvement end to end

---

## Projects (details in `projects/README.md`)

1. SQL schema and queries (Section 5)
2. Dockerized FastAPI model service with tests, CI and logging (Sections 1, 3, 4)
3. Project 2 deployed to Azure (Section 6)
4. RAG app with an eval set (Sections 8, 10)
5. Agent app with tools, evals, guardrails and a user-feedback round (Sections 9, 10, 12, Track B)
6. Optional: small-model fine-tuning write-up (Section 7, EXTRA)

Each project gets a one-page spec, a README and a demo link or screenshots.

## Job-search track (starts after the checkpoint)

- [ ] Fix CV: remove the "(one only of the following two)" note; use the honest QuantumIntel wording we drafted
- [ ] Pull 30–40 Canadian AI/ML/data postings and tally required skills in `notes/postings.md`
- [ ] Re-order MUST / RECOMMENDED / EXTRA based on what postings ask for most
- [ ] Add each project to the CV and GitHub profile (README + demo)
- [ ] Apply within 3–7 days of posting; ask for referrals; state work authorization briefly
- [ ] Check with your Western supervisor before open-sourcing research code

## Not needed (skip)

- Intro Python, calculus, most OSSU math ([Core math](https://github.com/ossu/computer-science#core-math)), Nand to Tetris and OS/architecture courses ([Core systems](https://github.com/ossu/computer-science#core-systems))
- Machine learning basics and the Deep Learning Specialization (~129 h): you already have these
- The Boulder Data Structures and Algorithms specialization (~199 h, advanced and theory-heavy) and the UC San Diego Genome Assembly capstone (~17 h)
- BITS Pilani's "Software Design Principles" on Coursera (~54 h; no clear programming language and it spends time on GUI frameworks)
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
