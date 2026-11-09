# AI Engineer Roadmap

**Goal:** Land a Canadian AI engineer job (applied LLM / ML systems), with skills that also transfer to an engineering + AI business later.
**Pace:** ~10 h/week. Course hours below are course time only. Projects and LeetCode add time. Core courses total ~330 h, roughly 8 months at 10 h/week.
**Rules:** One "Next" item at a time. Every section ends with a project in `/projects`, not just a certificate. Start applying after Section 4.

> Coursera links go to the specialization or certificate page. You don't have to finish a whole program: the "Take" lines say which courses to do. Check each is covered by your Coursera Plan before starting. Hours are from the course pages and sometimes conflict with each other, so treat them as estimates.

---

## Next

- [ ] Section 1: IBM Introduction to Software Engineering — module 1

---

## 1. Software foundations (~43 h)

Why: Git, the shell and how software is built are assumed by every job.

**Coursera:** [IBM Applied Software Engineering Fundamentals](https://www.coursera.org/specializations/software-engineering-fundamentals) (specialization, beginner)
- [ ] Introduction to Software Engineering — 15 h (SDLC, architecture, design and deployment patterns)
- [ ] Getting Started with Git and GitHub — 11 h
- [ ] Hands-on Introduction to Linux Commands and Shell Scripting — 17 h
- [ ] Skip: Python for Data Science, AI & Development (you know Python) and Developing AI Applications with Python and Flask (you'll use FastAPI)

**Free alternative:** [OSSU: The Missing Semester](https://github.com/ossu/computer-science#cs-tools) (shell, Git, tooling, 2 weeks)

**Done when:** you can clone, branch, open a pull request and run a script from the terminal without help. Make this repo's commits your practice.

## 2. Databases and SQL (~62 h)

**Coursera:** [Databases for Data Scientists](https://www.coursera.org/specializations/databases-for-data-scientists) (University of Colorado Boulder, beginner, ~79 h total)
- [ ] The Structured Query Language (SQL) — 27 h (do this first)
- [ ] Relational Database Design — 35 h (ER models, normalization)
- [ ] Optional: Advanced Topics and Future Trends in Database Technologies — 17 h (NoSQL: MongoDB, Redis)

**Free alternative:** [OSSU: Stanford Databases](https://github.com/ossu/computer-science#core-applications) (Relational Databases and SQL; Modeling and Theory), ~2 weeks each.

**Project 1:** Design a schema and write 20 non-trivial queries on a real dataset (e.g. your Canadian household spending data). Push the SQL and a README.

## 3. Backend, APIs and Docker (~53 h)

Why: this is where models become services other people can use.

**Coursera:**
- [ ] [Ultimate Guide to FastAPI and Backend Development](https://www.coursera.org/specializations/packt-ultimate-guide-to-fast-api-and-backend-development) (Packt, intermediate, ~36 h): REST APIs, SQL via SQLModel, OAuth2/JWT, pytest, Docker, async, deployment. Its program rating is 4.1 from only 27 reviews, so preview before committing.
- [ ] From [IBM Back-End Development Professional Certificate](https://www.coursera.org/professional-certificates/ibm-backend-development): Introduction to Containers w/ Docker, Kubernetes & OpenShift — 17 h (focus on Docker; skim Kubernetes)
- [ ] Optional from the same certificate: Application Development using Microservices and Serverless — 16 h
- [ ] Skip the rest of that certificate (Flask/Django, security, monitoring) for now.

**Project 2:** Deploy your AI-image-detection model as a Dockerized FastAPI service with pytest tests, logging and a GitHub Actions workflow. Include a README with a demo.

**Checkpoint:** after Section 4, start applying.

## 4. Deploying ML (~11 h)

**Coursera:** [Machine Learning in Production](https://www.coursera.org/learn/introduction-to-machine-learning-in-production) (DeepLearning.AI, Andrew Ng, standalone course, 4.8 rating)
- [ ] Complete the course (ML lifecycle, deployment patterns, concept drift, data definition, error analysis)
- [ ] Add to Project 2: a short note on how you would monitor drift and retrain

## 5. Data structures and algorithms (~29 h, run alongside Sections 3–8)

Why: many AI and software interviews have coding rounds.

**Coursera:** [Algorithms Specialization](https://www.coursera.org/specializations/algorithms) (Stanford, Tim Roughgarden, intermediate, 4.8 rating). It expects some discrete probability and comfort with proofs.
- [ ] Course 1: Divide and Conquer, Sorting and Searching, and Randomized Algorithms — 15 h
- [ ] Course 2: Graph Search, Shortest Paths, and Data Structures — 14 h
- [ ] Courses 3–4 (dynamic programming, NP-completeness) — only if interviews demand them
- [ ] ~100 LeetCode problems (easy/medium: arrays, hashing, trees, graphs, basic DP)

## 6. LLM foundations (~42 h)

**Free:** [Karpathy: Neural Networks: Zero to Hero](https://karpathy.ai/zero-to-hero.html), lectures 1, 2, 7 and 8 (micrograd, makemore, build GPT, GPT tokenizer): ~8.5 h video, plan ~25 h to code along.
- [ ] Lectures 1, 2, 7, 8

**Coursera:** [Generative AI with Large Language Models](https://www.coursera.org/learn/generative-ai-with-llms) (DeepLearning.AI + AWS, intermediate, ~17 h): transformers, instruction fine-tuning, LoRA/PEFT, RLHF, three labs on AWS (setup can be rough).
- [ ] Complete the course

**Don't take:** Edureka's "Learn Generative AI with LLMs" specialization. It's mostly classic ML/NLP and its rating is lower (3.9).

**Project 3:** Fine-tune or adapt a small model for one task, with a short write-up of what worked and what didn't.

## 7. RAG and vector databases (~34 h)

**Coursera:** [IBM RAG and Agentic AI Professional Certificate](https://www.coursera.org/professional-certificates/ibm-rag-and-agentic-ai) (advanced, ~101 h for all 10 courses)
- [ ] Develop Generative AI Applications: Get Started — 10 h
- [ ] Build RAG Applications: Get Started — 7 h
- [ ] Vector Databases for RAG: An Introduction — 9 h
- [ ] Advanced RAG with Vector Databases and Retrievers — 8 h
- [ ] After each course, rebuild the same example with plain API calls (no framework).

**Project 4:** A RAG app on a real document set, served through your FastAPI + Docker setup, with a small test set to check answer quality.

## 8. Agents, tool calling and MCP (~32 h)

**Coursera:** same [IBM RAG and Agentic AI Professional Certificate](https://www.coursera.org/professional-certificates/ibm-rag-and-agentic-ai)
- [ ] Fundamentals of Building AI Agents — 11 h
- [ ] Agentic AI with LangChain and LangGraph — 11 h
- [ ] Build AI Agents using MCP — 10 h
- [ ] Optional: RAG and Agentic AI Capstone Project — 14 h (can serve as Project 5)
- [ ] Skip: Multimodal Generative AI and Agentic AI with LangGraph, CrewAI, AutoGen and BeeAI (frameworks change fast)

**Don't take separately:** IBM's "Building AI Agents and Agentic Workflows" specialization. Its courses overlap with the certificate above. Also skip Edureka's "Agentic AI Engineering" (rated 3.3 from 12 reviews).

**Project 5 (capstone):** An agent app with tool calling, deployed with a demo link and a short write-up, including a small test set to catch failures.

## 9. Cloud: Azure (~21 h + exam prep)

**Before you book anything:** check Microsoft Learn for the current Azure AI associate exam. Microsoft's AB-100 page lists AI-103 (and not AI-102) among the qualifying prerequisites, so AI-102 may be being replaced. I couldn't confirm this, so verify first.

**Coursera:** [Microsoft AI & ML Engineering Professional Certificate](https://www.coursera.org/professional-certificates/microsoft-ai-and-ml-engineering) (5 courses, ~176 h, intermediate)
- [ ] Only course 4: Microsoft Azure for AI and Machine Learning — 21 h
- [ ] Skip the other four for now (they overlap with your earlier sections)
- [ ] Take the current Azure AI associate exam once you've picked it
- [ ] Later, only if relevant: [AB-100](https://learn.microsoft.com/en-us/credentials/certifications/agentic-ai-business-solutions-architect/) (expert level, needs a qualifying associate certification)

**Project 6:** Deploy Project 4 or 5 on Azure.

## 10. Software design and system design (optional, ongoing)

**Coursera:** [Software Design and Architecture](https://www.coursera.org/specializations/software-design-architecture) (University of Alberta, beginner, ~52 h). It uses **Java** and an Android capstone, so it's a language detour for your path.
- [ ] If you do it: Object-Oriented Design (17 h), Design Patterns (15 h), Software Architecture (10 h)
- [ ] Skip the Service-Oriented Architecture course and the Android capstone

**Also:** one book or guide on system design and one on clean code. ~2 h/week.

---

## Job-search track (starts after Section 4)

- [ ] Fix CV: remove the "(one only of the following two)" note
- [ ] Pull 30–40 Canadian AI/ML/data postings and tally required skills in `notes/postings.md`
- [ ] Re-order this roadmap based on what postings ask for most
- [ ] Add each project to the CV and GitHub profile (README + demo)
- [ ] Apply within 3–7 days of posting; ask for referrals; state work authorization briefly
- [ ] Check with your Western supervisor before open-sourcing research code

## Skip list (decided)

- Intro Python, calculus, most OSSU math ([Core math](https://github.com/ossu/computer-science#core-math)), Nand to Tetris and OS/architecture courses ([Core systems](https://github.com/ossu/computer-science#core-systems))
- Machine Learning basics, Deep Learning Specialization (~129 h)
- Boulder Data Structures and Algorithms specialization (~199 h)
- Edureka specializations, IBM multi-framework agents course, Microsoft AI & ML cert courses 1–3 and 5

## Gap checklist

Use [roadmap.sh](https://roadmap.sh/) (AI Engineer and Backend roadmaps) to spot topics you've missed. Don't follow them top to bottom.

## Weekly review (15 min, same day each week)

1. Tick what you finished.
2. Write the one next item at the top.
3. Note anything you were stuck on in `notes/`.

## Repo layout

```
README.md
ROADMAP.md
projects/     one folder per project, each with README + demo
notes/        short write-ups, postings.md
```
