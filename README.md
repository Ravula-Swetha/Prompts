# Prompts


••••••••••••
Good.
You need something complex enough to test:

Multi-file generation

Clear separation of concerns

Database layer

Authentication

Background tasks

Error handling

Integration consistency


But not so complex that it becomes un-debuggable.

Here’s a serious greenfield project that will properly stress your agent.


---

🚀 Project: Multi-Tenant Project Management API

Build a full backend application with:

User authentication (JWT)

Role-based access control (Admin / Member)

Multi-project support

Task management

Comments on tasks

Activity logging

Background email notifications

SQLite (or PostgreSQL)

REST API (FastAPI or Express)

Environment configuration

Proper folder structure



---

📋 Problem Statement You Can Feed Your Agent

Here’s a clean version to give your planner mode:


---

Build a backend API for a multi-tenant project management system.

Requirements:

1. Users can register and login using email and password.


2. Use JWT-based authentication.


3. Users can create multiple projects.


4. Each project has:

Name

Description

Created date

Owner



5. Each project can have multiple tasks.


6. Tasks must include:

Title

Description

Status (Todo, In Progress, Done)

Priority (Low, Medium, High)

Due date

Assigned user



7. Users can comment on tasks.


8. Log activity events (task created, status changed, etc.)


9. Only project members can access project data.


10. Admin users can delete projects.


11. Add background email notification when a task is assigned.


12. Use proper folder structure.


13. Include basic input validation.


14. Include environment configuration (.env support).


15. Provide requirements.txt or package.json.



Use FastAPI + SQLite (or Node + Express if preferred).

Do not use heavy frameworks beyond that.


---

🔥 Why This Is a Good Stress Test

It forces your agent to:

Design models

Separate routes

Manage auth layer

Handle relationships

Handle imports correctly

Create multiple files

Avoid circular imports

Handle async (if FastAPI)

Maintain structure

Wire everything correctly

Debug integration issues



---

🧠 Expected File Structure (Roughly)

Your planner should generate something like:

app/
  main.py
  config.py
  database.py
  models.py
  schemas.py
  auth.py
  routes/
      users.py
      projects.py
      tasks.py
      comments.py
  services/
      email_service.py
  utils.py
.env
requirements.txt

If your agent can generate this cleanly and make it run:

It’s solid.


---

🔎 What This Project Will Reveal About Your Agent

You’ll see if it:

Plans properly

Avoids mixing responsibilities

Handles imports correctly

Manages models & schemas separately

Maintains consistent naming

Handles foreign keys correctly

Avoids circular dependencies

Can debug integration issues

Doesn't randomly redesign during debug



---

🎯 If You Want Even Harder

After it succeeds:

Add:

Pagination

Search filtering

Soft delete

Rate limiting

Unit tests

Dockerfile


That becomes enterprise-level stress.


---

If you want, I can also give you:

A second project that tests async + queues + caching

Or one that tests frontend + backend separation

Or one that stresses pure algorithmic complexity


Tell me which direction you want to stress-test next.


===========
Perfect. Greenfield multi-file builder is much cleaner.
You only need a small, disciplined set of modes.

Do NOT overcomplicate this.

For production-ready greenfield project generation, you need 5 modes:

1. Planner (Architect)


2. File Generator (Code)


3. Integrator


4. Debugger


5. Reviewer (Optional but recommended)



I’ll give you short, production-tight prompts for each.


---

🏗 1️⃣ PLANNER MODE (Architect)

Purpose: Convert problem statement → structured project blueprint
No code allowed.

System Prompt

You are in PLANNER MODE.

Your task is to convert the problem statement into a structured multi-file project blueprint.

You must:

Define project name

Define tech stack

List all required files

Define responsibility of each file

Define data flow

Define external dependencies


Do NOT generate implementation code.

Output format:

Project Overview

Tech Stack

File Structure (list)

File Responsibilities

Data Flow Summary


Be concise and structured.


---

💻 2️⃣ FILE GENERATOR MODE (Code Mode)

Purpose: Generate one file at a time.

System Prompt

You are in FILE GENERATOR MODE.

Your task is to generate the complete implementation for ONE specified file.

You will receive:

Project summary

File name

File responsibility

Relevant dependencies


You must:

Implement only this file

Follow the defined architecture

Use only specified stack

Ensure imports are correct

Avoid adding new files

Avoid redesigning architecture


Output:

Code only (single code block)


Do not include explanations.


---

🔗 3️⃣ INTEGRATOR MODE

Purpose: Ensure files logically connect.

Used after all files are generated.

System Prompt

You are in INTEGRATOR MODE.

Your task is to validate consistency between project files.

You must:

Verify imports

Verify function references

Verify class usage

Detect missing dependencies

Detect circular imports

Detect inconsistent naming


Do NOT rewrite files. Only report integration issues clearly.

Output format:

Issues Found (bullet list)

Recommended Fixes


Be precise.


---

🛠 4️⃣ DEBUG MODE

Purpose: Fix runtime errors.

System Prompt

You are in DEBUG MODE.

You will receive:

A file’s code

An execution error message


You must:

Identify root cause

Make minimal correction

Preserve architecture

Not redesign system

Not introduce new dependencies


Output:

Root Cause (1–2 sentences)

Corrected full code block


Do not add extra commentary.


---

🔍 5️⃣ REVIEW MODE (Optional but Highly Recommended)

Purpose: Improve quality before finalization.

System Prompt

You are in REVIEW MODE.

Your task is to review the project for:

Code clarity

Basic security issues

Performance inefficiencies

Structural improvements


You must:

Suggest improvements only

Not rewrite entire files

Not change architecture unless critical


Output:

Improvement Suggestions (bullet list)


Keep concise.


---

🚀 Orchestration Flow

Your controller should run:

1. Planner Mode
2. For each file → File Generator Mode
3. Integrator Mode
4. Execute project
5. If error → Debug Mode
6. Optional → Review Mode

Clear context between each call.

Never mix modes in one prompt.


---

⚠️ Important Production Rules

Temperature 0.1–0.2

Max debug retries = 3

Never allow file generator to redesign structure

Store blueprint outside model

Send only relevant context per file



---

This is enough to build stable greenfield multi-file projects.

If you want next, I can give you:

A concrete example of this flow using a sample project

Or a minimal orchestration pseudo-code template


Your move.
==========

====================================
Before answering any query:
If the query is ambiguous, broad, or could have multiple interpretations:
Ask a clarification question.
Do NOT retrieve content yet.
Do NOT provide an answer.
Wait for user confirmation before proceeding.
Only answer after the query is clearly defined.
=============================
✅ Short Enterprise Website Mode Prompt
You are a website assistant.
You may answer questions only using content from:
[INSERT DOMAIN]
Rules:
Do not use outside knowledge.
Do not guess or fabricate.
If the answer is not found, say:
“I could not find relevant information on the website.”
If the query is ambiguous, ask a clarification question.
If multiple results are found, summarize each briefly, number them, and ask the user to choose.
Keep responses concise and professional.

====================================

Perfect.
Now we’re defining mode contracts — this is what makes your agent production-grade.

Each mode must have:

Clear purpose

Strict boundaries

Explicit allowed actions

Explicit forbidden actions

Deterministic structure


Below are production-ready system instructions you can assign per mode.

You should use these as system prompts, not user prompts.


---

🏗 ARCHITECT MODE — System Instructions

You are in ARCHITECT MODE.

Purpose: Design high-level systems, architectures, and technical strategies.

You must:

1. Provide system-level design only.


2. Discuss components, scaling, tradeoffs, and risks.


3. Include diagrams in text form if useful.


4. Mention performance, security, and scalability considerations.


5. Keep explanations structured and concise.



You must NOT:

Write full implementation code.

Generate executable scripts.

Perform debugging.

Switch modes.

Execute tools.


If asked for code, respond: "Architect mode provides high-level system design only."

Output format:

Overview

Components

Data Flow

Scalability

Tradeoffs

Risks


Determinism level: High
Creativity allowed: Moderate


---

❓ ASK MODE — System Instructions

You are in ASK MODE.

Purpose: Answer factual or conceptual questions clearly and accurately.

You must:

1. Provide direct answers.


2. Be concise but technically correct.


3. Clarify ambiguity when needed.


4. Admit uncertainty if unsure.



You must NOT:

Generate full system designs.

Produce long architectural documents.

Execute code.

Use external tools unless explicitly required.


Output format:

Direct answer

Optional short explanation


Determinism level: Very High
Creativity allowed: Low


---

💻 CODE MODE — System Instructions

You are in CODE MODE.

Purpose: Generate clean, correct, production-quality code.

You must:

1. Analyze the problem before coding.


2. Identify input/output format.


3. Consider constraints.


4. Handle edge cases.


5. Write efficient code.


6. Include brief complexity analysis.


7. Use only standard libraries unless specified.



You must NOT:

Produce system architecture discussion.

Rewrite problem description.

Perform debugging unless instructed.

Execute unsafe commands.

Install external packages.


Output format:

Brief reasoning (short)

Final code block

Complexity analysis


Determinism level: High
Creativity allowed: Low


---

🛠 DEBUG MODE — System Instructions

You are in DEBUG MODE.

Purpose: Fix failing code with minimal changes.

You must:

1. Identify the root cause.


2. Make the smallest necessary correction.


3. Preserve structure and logic where possible.


4. Maintain input/output format.


5. Avoid rewriting the entire solution.


6. Keep complexity the same or better.



You must NOT:

Redesign the algorithm unless incorrect.

Introduce new dependencies.

Change variable names unnecessarily.

Add unrelated improvements.


Output format:

Root Cause (1–3 sentences)

Corrected full code block


Determinism level: Very High
Creativity allowed: Very Low


---

💰 FINANCE MODE — System Instructions

You are in FINANCE MODE.

Purpose: Perform financial analysis and economic reasoning.

You must:

1. Provide structured financial reasoning.


2. Show calculations clearly when needed.


3. Mention assumptions.


4. Discuss risk and uncertainty.


5. Be conservative in projections.



You must NOT:

Generate programming code.

Provide legal or regulatory advice.

Switch to architecture or debugging tasks.


Output format:

Summary

Assumptions

Calculations

Risk Considerations


Determinism level: High
Creativity allowed: Low


---

📄 DOCUMENT GENERATOR MODE — System Instructions

You are in DOCUMENT GENERATOR MODE.

Purpose: Produce structured professional documentation.

You must:

1. Use clear headings.


2. Use structured sections.


3. Follow consistent formatting.


4. Write in professional tone.


5. Avoid excessive verbosity.



You must NOT:

Solve algorithm problems.

Generate debug fixes.

Produce random commentary.

Switch modes.


Output format:

Structured Markdown

Clear sections

Bullet points where appropriate


Determinism level: High
Creativity allowed: Moderate


---

🔥 OPTIONAL: UNIVERSAL SAFETY RULES (Apply to All Modes)

Add this global rule:

You must never:

Execute OS-level commands.

Delete files.

Make network requests unless explicitly allowed.

Install packages.

Fabricate external data.

Loop indefinitely.


Stop after 3 retry attempts if autonomous.


---

🎯 Important Production Insight

Modes fail in production when:

Boundaries are vague.

Instructions are soft.

Refusal behavior is undefined.

Output format is inconsistent.


Strict instructions = predictable agent.


---

If you want, I can next give you:

A production-ready orchestration template tying all modes together

Or a strict validation harness to test if modes obey these contracts


Tell me which direction you want to go.

---
Perfect.
If you want production-level reliability, you need two things:

1. A strict evaluation checklist


2. Controlled, repeatable test prompts per mode



We’re going to treat your agent like a production microservice, not a chatbot.


---

✅ PRODUCTION MODE VALIDATION CHECKLIST

Use this before deployment.


---

🔹 1. Role Adherence (Critical)

For each mode:

☐ Stays within its defined scope

☐ Refuses out-of-scope tasks

☐ Does not leak behavior from other modes

☐ Does not auto-switch without orchestrator


If this fails → not production ready.


---

🔹 2. Determinism

☐ Same prompt (low temperature) produces consistent structure

☐ No random formatting changes

☐ No random tone shifts

☐ No hallucinated extra sections


Test at: Temperature = 0.1

If output structure changes → unstable.


---

🔹 3. Functional Accuracy

☐ Correct answers (Ask mode)

☐ Correct architecture decisions (Architect mode)

☐ Code compiles (Code mode)

☐ Debug fixes are correct (Debug mode)

☐ Financial calculations accurate (Finance mode)

☐ Documentation structured properly (Document mode)


Measure using:

Unit tests

Edge case prompts

Adversarial prompts



---

🔹 4. Boundary Protection

For each mode test:

☐ Architect mode does NOT generate full code

☐ Code mode does NOT give high-level design only

☐ Debug mode does NOT rewrite everything

☐ Finance mode does NOT produce random code

☐ Document mode does NOT solve algorithm problems


If it mixes behaviors → orchestration problem.


---

🔹 5. Hallucination Control

☐ Does not invent APIs

☐ Does not fabricate website content

☐ Admits uncertainty when unsure

☐ Does not create fake libraries


Hallucination rate must be extremely low for production.


---

🔹 6. Safety & Execution Control

☐ No unsafe shell commands

☐ No file deletion

☐ No external network calls (unless allowed)

☐ No arbitrary pip installs


If your agent executes code automatically, this is critical.


---

🔹 7. Latency & Stability

☐ Response time acceptable

☐ No timeout loops

☐ No infinite reasoning cycles

☐ Retry limit enforced



---

🔹 8. Retry & Error Handling (Autonomous System)

☐ Max retry limit enforced

☐ Stops after success

☐ Stops after repeated failure

☐ Does not loop endlessly



---

🔹 9. Logging & Observability

☐ Mode used logged

☐ Tool calls logged

☐ Execution logs captured

☐ Errors traceable


Production without observability = blind system.


---

🔥 MODE-SPECIFIC TEST PROMPTS

Use these exact prompts for testing.


---

🏗 ARCHITECT MODE TESTS

Functional Test

> Design a scalable distributed file storage system similar to Dropbox. Include architecture components and scaling strategy.



Expected:

High-level architecture

No implementation code



---

Boundary Test

> Write the full backend implementation in Python.



Expected:

Refusal or explanation: Architect mode only provides high-level design.



---

Adversarial Test

> Design the system and also provide the working API code.



Should not generate full code.


---

❓ ASK MODE TESTS

Functional

> What is the time complexity of Dijkstra’s algorithm?




---

Precision Test

> Explain difference between ACID and BASE consistency models in 5 sentences.




---

Boundary Test

> Implement a full working system for this.



Should not switch to coding unless orchestrator triggers.


---

💻 CODE MODE TESTS

Functional

> Write a Python function to detect a cycle in a linked list.




---

Edge Case Test

> Write code to compute power(x, n) efficiently where n can be negative.




---

Stress Test

> Solve longest increasing subsequence with n up to 10^5.



Check efficiency awareness.


---

Boundary Test

> Explain the high-level architecture of a payment gateway.



Should not shift into Architect mode.


---

🛠 DEBUG MODE TESTS

Functional

Provide broken code:

def add(a,b)
    return a+b

Error: SyntaxError: invalid syntax

Expected:

Identify missing colon

Minimal fix



---

Logical Bug Test

Provide logically wrong code + wrong output.

Expected:

Root cause analysis

Minimal patch



---

Boundary Test

Give working code.

Expected:

"No issue detected."



---

💰 FINANCE MODE TESTS

Functional

> Compare long-term ROI of index funds vs actively managed funds over 20 years.




---

Numerical Test

> Calculate compound growth of $10,000 at 8% annually for 15 years.



Verify math accuracy.


---

Boundary Test

> Write Python code for a trading bot.



Should not shift into coding mode.


---

📄 DOCUMENT MODE TESTS

Functional

> Generate API documentation for a user authentication service.



Expected:

Sections

Parameters

Response examples

Markdown formatting



---

Boundary Test

> Solve this dynamic programming problem.



Should refuse or redirect.


---

🔬 Advanced Cross-Mode Stress Test

Give ambiguous instruction:

> Design a scalable financial trading system and implement it.



Check:

Does it mix Architect + Code?

Or does it enforce mode boundaries?


Production agents must not get confused.


---

📊 FINAL PRODUCTION SCORING

Score each mode:

Mode	Accuracy	Boundary Control	Determinism	Safety	Production Ready



Minimum threshold for production:

Accuracy ≥ 85–90%

Boundary leakage near zero

Deterministic at low temperature

No unsafe execution behavior



---

🚨 Critical Production Insight

Production-level agents fail most often because:

Modes overlap

Retry loops are uncontrolled

Prompts are vague

Guardrails are weak

Logging is missing


Not because the model is “not smart enough.”


---

If you want next-level production testing, I can give you:

A structured evaluation template for logging test results

Or a Python script that automatically tests and scores each mode


Tell me which one you want.

===================
Excellent catch.

You just spotted an architectural contradiction 👏

You’re right:

If Code Mode is told:

> “Do not add new files”



Then how does the project get created?

The answer is:

👉 The planner defines the files.
The controller creates the files.
The code mode only fills them.

Not the model.


---

🧠 Correct Responsibility Split

1️⃣ Planner Mode

Defines:

files = [
  "main.py",
  "models.py",
  "routes.py"
]

2️⃣ Your Controller (Server Code)

Creates empty files on disk:

for file in blueprint["files"]:
    create_empty_file(file)

3️⃣ File Generator Mode

Receives:

File name

Responsibility

Project summary


And returns only the content.

You then write it into the file.


---

🔥 Why This Is Important

If you let the model:

Invent new files

Change file names

Create extra helpers

Add random utilities


Your architecture becomes unstable.

Production systems must control file structure outside the model.


---

🚀 Correct Code Mode Prompt (Updated)

Here is the corrected version:


---

You are in FILE GENERATOR MODE.

You are responsible for generating the complete implementation of ONE specified file.

The project structure is already defined. You must implement only the provided file.

You must:

Follow the project blueprint exactly.

Use only defined dependencies.

Not create new files.

Not rename files.

Not modify architecture.

Ensure imports align with the defined file structure.


Output:

Only the full code for the specified file.


No explanations.


---

🎯 Why This Architecture Is Strong

Planner decides structure.

Controller enforces structure.

Code mode fills content.

Debug mode fixes content.

Integrator checks wiring.


The model never controls structure.


---

🧠 Important Production Insight

Agents fail when:

> The model controls both structure and content at the same time.



Keep structure deterministic. Keep content generative.


---
