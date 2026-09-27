# AI Growth Engineer Workbook

A 12-week plan (28 Sep to 20 Dec 2026, ~16 h/week alongside a full-time job and agency) to become an AI engineer and growth engineer. Starts with Python from zero and backend basics, then builds a new career-ops from scratch. Ends with career-ops and marketing-ops shipped.

Interactive version with progress tracking: https://claude.ai/artifact/6GB2UzyNKZuCnZpgBkK8Jq

## Rules

1. 70% build, 30% watch. If you fall behind, cut videos, never the weekly ship.
2. Every build feeds a real product: the new career-ops or the next ops product. On a bad week, do only the Ship item.
3. TypeScript for products you ship; Python for notebooks, data scripts and Python-only tools.
4. Weeks 1-3 use the Claude API (billed separately from Max): add $5-10 prepaid credit in the Claude Console, auto-reload off. From week 4 the Agent SDK can use your Max plan's monthly Agent SDK credit.

## Phases

| Weeks | Phase |
|---|---|
| 1-3 | Python, LLMs, backend |
| 4-6 | Agent SDK, RAG, MCP |
| 7-8 | Evals + growth |
| 9-12 | Ship career-ops + marketing-ops |

## Week 1: Python from zero + how LLMs work (28 Sept to 4 Oct)

- [ ] **Video:** Learn Python: Full Course for Beginners, freeCodeCamp ([link](https://www.youtube.com/watch?v=rfscVS0vtbw)), 4.5 h. Zero to working Python in one sitting-split video. You know TypeScript, so map as you go: list = array, dict = object, def = function, None = null. Type every example yourself.
- [ ] **Course:** Python track, first 10 exercises, Exercism (free, mentor feedback) ([link](https://exercism.org/tracks/python)), 3 h. Short exercises with tests, built for people who already know another language. Request a mentor review on two of them.
- [ ] **Video:** Intro to Large Language Models, Andrej Karpathy ([link](https://www.youtube.com/watch?v=zjkBMFhNj_g)), 1 h. The one-hour mental model: what an LLM is, what it's good and bad at.
- [ ] **Read:** The Rise of the AI Engineer, swyx, Latent Space ([link](https://www.latent.space/p/ai-engineer)), 0.5 h. The essay that named the role. Tells you what the job is and isn't.
- [ ] **Read:** What is Growth Engineering?, The Pragmatic Engineer with Alexey Komissarouk ([link](https://newsletter.pragmaticengineer.com/p/what-is-growth-engineering)), 0.5 h. “Writing code to help a company make more money.” The clearest definition of the role.
- [ ] **Course:** Google Digital Marketing & E-commerce Certificate: restart, Google on Coursera ([link](https://grow.google/certificates/digital-marketing-ecommerce/)), 4 h. Log in first: Coursera usually keeps completed work on your account, so check what's done before you assume a restart. Apply for financial aid, then skim videos you already know and go straight to graded work.
- [ ] **Build:** First Claude API call in TypeScript, then Python, You ([link](https://docs.claude.com/en/docs/get-started)), 2 h. Create an API key in the Claude Console and add $5 to $10 of prepaid credit with auto-reload off; your Max plan doesn't cover direct API calls. Write it in TypeScript (familiar), then rewrite it in Python. Comparing the two teaches you Python faster than any video.

**Ship:** A public GitHub repo (ai-growth-lab) with the same Claude call written in TypeScript and in Python, and a README log.

## Week 2: Python for real work + prompting (5 Oct to 11 Oct)

- [ ] **Book:** Automate the Boring Stuff with Python: files, CSV/JSON, web requests, Al Sweigart (free to read online) ([link](https://automatetheboringstuff.com/)), 4 h. Practical Python for the exact work you'll do: read files, parse CSV and JSON, call web APIs.
- [ ] **Docs:** uv: Python projects and packages, Astral ([link](https://docs.astral.sh/uv/)), 0.5 h. The npm of Python. Use it for every Python project so environments never break.
- [ ] **Course:** Prompt engineering interactive tutorial, Anthropic (Jupyter notebooks) ([link](https://github.com/anthropics/prompt-eng-interactive-tutorial)), 3 h. Prompting skills plus real Python notebook practice. Two birds, one course.
- [ ] **Video:** Transformers, the tech behind LLMs + Attention in transformers, 3Blue1Brown ([link](https://www.youtube.com/watch?v=wjZofJX0v4M)), 1 h. Visual picture of tokens, embeddings and attention. Embeddings come back in week 5 for RAG.
- [ ] **Video:** Deep Dive into LLMs like ChatGPT (optional), Andrej Karpathy ([link](https://www.youtube.com/watch?v=7xTGNNLPyMI)), optional. 3.5 h on pretraining, fine-tuning, RL and hallucinations. Watch it when you have spare evenings; the Intro video covers the essentials.
- [ ] **Course:** Google Digital Marketing & E-commerce Certificate: keep going, Google on Coursera ([link](https://grow.google/certificates/digital-marketing-ecommerce/)), 4 h. Same slot every week until it's done.
- [ ] **Build:** Job-post classifier in Python, You ([link](https://docs.claude.com/en/docs/build-with-claude/structured-outputs)), 3 h. Read job posts from a file, send each to Claude, get JSON back: archetype, fit score, reasons. Label 50 yourself and compare.

**Ship:** A Python script that classifies 50 job posts from your own job search, plus a table of where it agreed with you.

## Week 3: Claude API + backend basics (12 Oct to 18 Oct)

- [ ] **Course:** Building with the Claude API, Anthropic Academy (free, certificate) ([link](https://anthropic.skilljar.com/claude-with-the-anthropic-api)), 6 h. API basics, prompting, tool use, RAG and workflows in one course. Do the exercises in Python for practice.
- [ ] **Course:** Next.js Learn: the dashboard app (database, server actions, auth), Vercel (free, official) ([link](https://nextjs.org/learn/dashboard-app)), 5 h. Fills your backend gap in the framework you know: Postgres, fetching, mutations, authentication. Every ops product needs these.
- [ ] **Video:** How I use LLMs (optional), Andrej Karpathy ([link](https://www.youtube.com/watch?v=EWvNQjAaOHw)), optional. 2 h practical tour of thinking models, tools, file uploads.
- [ ] **Course:** Google Digital Marketing & E-commerce Certificate: keep going, Google on Coursera ([link](https://grow.google/certificates/digital-marketing-ecommerce/)), 4 h. Same slot every week until it's done.
- [ ] **Build:** Add a Claude route to the dashboard app, You ([link](https://docs.claude.com/en/docs/get-started)), 2 h. A route that takes a job post, calls Claude, and saves the result to Postgres.

**Ship:** A deployed Next.js app with a Postgres database, login, and one Claude-powered route.

## Week 4: Agents in TypeScript: Claude Agent SDK (19 Oct to 25 Oct)

- [ ] **Docs:** Claude Agent SDK overview + quickstart, Anthropic ([link](https://docs.claude.com/en/docs/agent-sdk/overview)), 2.5 h. Opt in to your Max plan's monthly Agent SDK credit first, so these runs don't use your API balance. The same agent loop, tools, subagents and MCP support that power Claude Code, in TypeScript or Python. This is how you connect career-ops to Claude agents properly.
- [ ] **Course:** Vercel AI SDK Tutorial, Matt Pocock, AI Hero (free, 16 lessons) ([link](https://www.aihero.dev/vercel-ai-sdk-tutorial)), 4 h. For the web UI side: streaming, structured output, tool calls in Next.js.
- [ ] **Read:** Building Effective Agents, Anthropic ([link](https://www.anthropic.com/engineering/building-effective-agents)), 0.5 h. Workflows vs agents, and why you start with the simplest pattern that works.
- [ ] **Video:** Software Is Changing (Again), Andrej Karpathy, YC AI Startup School ([link](https://www.youtube.com/watch?v=LCEmiRjPEtQ)), 0.75 h. Software 3.0 and “partial autonomy” apps: humans approve, agents do the work. That's the ops model.
- [ ] **Course:** Select Star SQL, Free interactive book ([link](https://selectstarsql.com/)), 3 h. Backend and growth work both live in SQL: funnels, cohorts, retention.
- [ ] **Course:** Google Digital Marketing & E-commerce Certificate: keep going, Google on Coursera ([link](https://grow.google/certificates/digital-marketing-ecommerce/)), 3 h. Same slot every week until it's done.
- [ ] **Build:** Build career-ops' first agent, You ([link](https://docs.claude.com/en/docs/agent-sdk/overview)), 4 h. Start with job evaluation: an agent with tools to read your CV, read the job post, and write a scored report. Your own design, from an empty repo.

**Ship:** career-ops' first agent, built from scratch on the Claude Agent SDK, with its own tools.

## Week 5: RAG: give agents your data (26 Oct to 1 Nov)

- [ ] **Video:** Learn RAG From Scratch, Lance Martin, freeCodeCamp ([link](https://www.youtube.com/watch?v=sVcwVQRHIc8)), 2.5 h. Indexing, retrieval, query rewriting, routing. The notebooks are Python: more practice.
- [ ] **Read:** Introducing Contextual Retrieval, Anthropic ([link](https://www.anthropic.com/news/contextual-retrieval)), 0.5 h. A simple trick that cuts failed retrievals a lot.
- [ ] **Book:** AI Engineering, chapters 1 and 2, Chip Huyen ([link](https://github.com/chiphuyen/aie-book)), 4 h. Foundation models, sampling, why outputs vary. One page of notes per chapter.
- [ ] **Docs:** AI and Vectors guide (pgvector), Supabase ([link](https://supabase.com/docs/guides/ai)), 1 h. Embeddings in Postgres. One database for app data and vectors.
- [ ] **Course:** Google Digital Marketing & E-commerce Certificate, Google on Coursera ([link](https://grow.google/certificates/digital-marketing-ecommerce/)), 3 h. Same slot every week until it's done.
- [ ] **Build:** RAG over your CV, story bank and past reports, You, 5 h. Every answer cites the file and line it used. This upgrades career-ops' CV tailoring.

**Ship:** career-ops answers “what's my best proof point for this JD?” with citations from your own files.

## Week 6: Agents, MCP + plan the ops suite (2 Nov to 8 Nov)

- [ ] **Course:** Hugging Face Agents Course, Unit 1, Hugging Face (free, certificate) ([link](https://huggingface.co/learn/agents-course)), 3 h. The Thought, Action, Observation loop from first principles, in Python. Get the Unit 1 certificate.
- [ ] **Read:** Effective context engineering for AI agents, Anthropic ([link](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)), 0.75 h. What to put in an agent's context and what to leave out. Directly useful for career-ops' modes and profile files.
- [ ] **Read:** Patterns for Building LLM-based Systems & Products, Eugene Yan ([link](https://eugeneyan.com/writing/llm-patterns/)), 1 h. Evals, RAG, guardrails, caching, user feedback, in one long post.
- [ ] **Course:** Introduction to Model Context Protocol, Anthropic Academy (free, certificate) ([link](https://anthropic.skilljar.com/introduction-to-model-context-protocol)), 3 h. Build MCP servers and clients. MCP is how every ops product will share tools.
- [ ] **Book:** AI Engineering, chapter 6, Chip Huyen ([link](https://github.com/chiphuyen/aie-book)), 2 h. RAG and agents, with the reasoning behind each pattern. Read chapter 5 (prompting) later if you have time.
- [ ] **Build:** MCP server for the career-ops tracker, You ([link](https://modelcontextprotocol.io/)), 3 h. Expose applications, pipeline and follow-ups as MCP tools, in TypeScript. Any agent in the suite can then use them.
- [ ] **Plan:** Write the ops suite spec, You, 2 h. One page: shared core, career-ops scope, marketing-ops MVP scope, what waits until after week 12.
- [ ] **Course:** Google Digital Marketing & E-commerce Certificate: keep going, Google on Coursera ([link](https://grow.google/certificates/digital-marketing-ecommerce/)), 3 h. Same slot every week until it's done. From scratch, it may run into January; that's fine.

**Ship:** An MCP server for your career-ops tracker, and a one-page ops suite spec.

## Week 7: Evals: prove it works (9 Nov to 15 Nov)

- [ ] **Read:** Your AI Product Needs Evals, Hamel Husain ([link](https://hamel.dev/blog/posts/evals/)), 1 h. Three levels: assertions, human and model grading, A/B tests.
- [ ] **Read:** AI Evals FAQ, Hamel Husain and Shreya Shankar ([link](https://hamel.dev/blog/posts/evals-faq/)), 2 h. Start from real traces, find failure modes, then write evals for the ones that matter.
- [ ] **Course:** Evaluating AI Agents, DeepLearning.AI x Arize (free) ([link](https://www.deeplearning.ai/courses/evaluating-ai-agents)), 2 h. Tracing, structured experiments, monitoring an agent after launch.
- [ ] **Book:** AI Engineering, chapters 3 and 4, Chip Huyen ([link](https://github.com/chiphuyen/aie-book)), 4 h. Evaluation methods and how to build an evaluation pipeline.
- [ ] **Build:** Golden set from your own job search history, You ([link](https://hamel.dev/blog/posts/llm-judge/)), 5 h. 50+ JDs you've scored by hand, including ones where the agent's score was wrong. Measure how close the agent gets. Add an LLM judge for report quality.
- [ ] **Course:** Google Digital Marketing & E-commerce Certificate: keep going, Google on Coursera ([link](https://grow.google/certificates/digital-marketing-ecommerce/)), 3 h. Same slot every week until it's done. From scratch, it may run into January; that's fine.

**Ship:** An eval script for career-ops scoring that you run before every change, with the score in the README.

## Week 8: Growth engineering core (16 Nov to 22 Nov)

- [ ] **Read:** A software engineer's guide to A/B testing, PostHog ([link](https://posthog.com/product-engineers/ab-testing-guide-for-engineers)), 0.5 h. Hypothesis, goal metric, one change at a time, run for at least a week.
- [ ] **Book:** Trustworthy Online Controlled Experiments, ch. 1 to 3, Kohavi, Tang, Xu ([link](https://experimentguide.com/)), 3 h. You know ad A/B tests. This covers product experiments and the stats behind a trustworthy result.
- [ ] **Tool:** Sample size calculator, Evan Miller ([link](https://www.evanmiller.org/ab-testing/sample-size.html)), 0.5 h. Plug in a real conversion rate from a past client and see how much traffic a test needs.
- [ ] **Video:** The DNA of a Great Growth Engineer, Alexey Komissarouk, Reforge ([link](https://www.youtube.com/watch?v=fFZBZJrnUIg)), 1 h. What separates good growth engineers, from the person who teaches Reforge's course.
- [ ] **Course:** Clay 101: GTM Automation, Clay University (free) ([link](https://university.clay.com/courses/clay-101)), 2 h. Prep for prospect-ops: find, enrich, transform, export. GTM engineering in two hours.
- [ ] **Build:** career-ops landing page + PostHog, You ([link](https://posthog.com/docs/libraries/next-js)), 4 h. Waitlist page, events, a signup funnel, one feature flag. Your GTM event design skills, product side.
- [ ] **Course:** Google Digital Marketing & E-commerce Certificate: keep going, Google on Coursera ([link](https://grow.google/certificates/digital-marketing-ecommerce/)), 3 h. Same slot every week until it's done. From scratch, it may run into January; that's fine.

**Ship:** A career-ops landing page with a live PostHog funnel and one feature flag.

## Week 9: AI-era growth + career-ops sprint (23 Nov to 29 Nov)

- [ ] **Podcast:** The new AI growth playbook for 2026, Elena Verna on Lenny's Podcast ([link](https://www.lennysnewsletter.com/p/the-new-ai-growth-playbook-for-2026-elena-verna)), 1.5 h. How Lovable grew: loops, retention first, giving the product away. Directly relevant to launching career-ops.
- [ ] **Read:** Three posts from Elena's Growth Scoop, Elena Verna ([link](https://www.elenaverna.com/)), 1 h. Pick posts on growth loops and retention. Write down which loop career-ops could use.
- [ ] **Docs:** Langfuse tracing quickstart, Langfuse (open source) ([link](https://langfuse.com/docs)), 1 h. See every prompt, tool call, cost and latency across all your agents.
- [ ] **Build:** career-ops sprint: agents, RAG, MCP, tracing together, You, 10 h. Wire everything from weeks 4 to 7 into one product. Human approval before anything is sent.
- [ ] **Course:** Google Digital Marketing & E-commerce Certificate: keep going, Google on Coursera ([link](https://grow.google/certificates/digital-marketing-ecommerce/)), 3 h. Same slot every week until it's done. From scratch, it may run into January; that's fine.

**Ship:** career-ops running on the Agent SDK end to end, with tracing, used by you daily.

## Week 10: career-ops: ship it (30 Nov to 6 Dec)

- [ ] **Build:** Cost and latency budget, You ([link](https://docs.claude.com/en/docs/build-with-claude/prompt-caching)), 3 h. Show cost per evaluation. Use prompt caching and smaller models where evals say quality holds.
- [ ] **Build:** Grow the eval set by 30 cases, You, 2 h. Every real failure becomes a test case. Re-run evals after every change.
- [ ] **Build:** Onboarding: first evaluated job in under 10 minutes, You ([link](https://posthog.com/product-engineers/growth-engineering)), 4 h. Measure time-to-value in PostHog. Cut steps until new users get a scored job fast.
- [ ] **Build:** First A/B test on the landing page, You ([link](https://posthog.com/docs/experiments)), 2 h. Test one headline. Let it run a full week before you call it.
- [ ] **Plan:** Get 5 testers, You, 3 h. Friends job hunting, classmates graduating in 2026, LinkedIn. Watch them use it; don't explain it.
- [ ] **Course:** Google Digital Marketing & E-commerce Certificate: keep going, Google on Coursera ([link](https://grow.google/certificates/digital-marketing-ecommerce/)), 3 h. Same slot every week until it's done. From scratch, it may run into January; that's fine.

**Ship:** Five other job seekers have used career-ops and you've logged what broke.

## Week 11: marketing-ops MVP (7 Dec to 13 Dec)

- [ ] **Read:** Open Source Google Ads API MCP Server, Google Ads Developer Blog ([link](https://ads-developers.googleblog.com/2025/10/open-source-google-ads-api-mcp-server.html)), 1 h. Google's official read-only Ads MCP server. It's Python, so your Python weeks pay off here.
- [ ] **Build:** Connect ad data over MCP, You ([link](https://github.com/googleads/google-ads-mcp)), 5 h. Run it against a test account, or serve a CSV export through your own MCP server if API access takes too long.
- [ ] **Build:** Wasted-spend agent, You, 6 h. Classify search terms, rank waste in dollars, propose negatives with evidence. Same Agent SDK core, tracing and eval harness as career-ops.
- [ ] **Build:** Small eval set for marketing-ops, You, 2 h. 100 search terms from past accounts (remove client names), labelled keep or negative.
- [ ] **Course:** Google Digital Marketing & E-commerce Certificate: keep going, Google on Coursera ([link](https://grow.google/certificates/digital-marketing-ecommerce/)), 3 h. Same slot every week until it's done. From scratch, it may run into January; that's fine.

**Ship:** marketing-ops finds wasted ad spend in a real account, reusing the career-ops core.

## Week 12: Launch and package (14 Dec to 20 Dec)

- [ ] **Build:** Record two 3-minute demo videos, You, 2 h. Problem in 20 seconds, live demo, one number at the end.
- [ ] **Plan:** Publish the case studies, You ([link](https://growveloper.com/)), 4 h. On growveloper.com, LinkedIn and GitHub. Lead with results: jobs landed with career-ops, dollars of waste found with marketing-ops.
- [ ] **Plan:** Launch career-ops, You, 2 h. LinkedIn, X, Product Hunt optional. UTMs on every link, funnel in PostHog.
- [ ] **Plan:** Update your CV and start applying, You, 3 h. The ops suite is your lead proof point. Target: applied AI engineer, growth engineer, GTM engineer, marketing engineer.
- [ ] **Course:** Google Digital Marketing & E-commerce Certificate: keep going, Google on Coursera ([link](https://grow.google/certificates/digital-marketing-ecommerce/)), 3 h. Same slot every week until it's done. From scratch, it may run into January; that's fine.

**Ship:** Public case studies for career-ops and marketing-ops, a demo video, and an updated CV.

## Projects: the ops suite

One shared core (Claude Agent SDK runtime and subagents, MCP connectors, RAG, eval harness, Langfuse tracing, PostHog, human approval step), built inside career-ops and reused.

| Product | What it does | Proves | When |
|---|---|---|---|
| career-ops (new build) | Job search agents: evaluate offers, tailor CVs, track applications | AI engineering | Weeks 4-10 |
| marketing-ops | Ad account agents: wasted spend, negatives, compliant copy | Growth engineering + paid media | MVP week 11 |
| prospect-ops | Find, enrich and draft outreach to leads | GTM engineering | After week 12 |
| content-ops | Plan, draft, repurpose content; track performance | Growth marketing + SEO | After week 12 |
| U-ops | Defined later | | Later |

Run marketing-ops on agency clients first. Name check: career-ops is also the name of a known open-source project; a distinct name helps if you sell yours.

## After the 12 weeks: certifications and paid courses

Prices in USD; check before paying.

### AI engineering

| Verdict | Certificate / course | Cost | Valid | When |
|---|---|---|---|---|
| take | [Agentic AI](https://www.deeplearning.ai/courses/agentic-ai), Andrew Ng, DeepLearning.AI | Free to audit, ~$25/month for the certificate | No expiry | Jan 2027 |
| take | [AWS Certified Generative AI Developer – Professional (AIP-C01)](https://aws.amazon.com/certification/certified-generative-ai-developer-professional/), Amazon Web Services | $300 | 3 years | Feb–Mar 2027 |
| take | [Azure AI App and Agent Developer Associate (AI-103)](https://learn.microsoft.com/en-us/credentials/), Microsoft | $165 US list; Microsoft prices exams by country, so check the Nigeria price at checkout | 1 year, free online renewal | Feb–Mar 2027 |
| later | [AI Evals For Engineers & PMs](https://maven.com/parlance-labs/evals), Hamel Husain and Shreya Shankar, Maven | Four-figure cohort price; check the page. Promos of $1,250 off have run | Lifetime access | Mid 2027, employer-paid |
| later | [Claude Certified Architect (Foundations, then Professional)](https://www.pearsonvue.com/us/en/anthropic.html), Anthropic, via Pearson VUE | $125 Foundations, $175 Professional | 12 months | When eligible |
| maybe | [NVIDIA-Certified Associate: Generative AI LLMs](https://www.nvidia.com/en-us/learn/certification/generative-ai-llm-associate/), NVIDIA | $125–135 | 2 years | Optional |
| skip | [Google Cloud Professional Machine Learning Engineer](https://cloud.google.com/learn/certification/machine-learning-engineer), Google Cloud | $200 | 2 years | Skip for now |

### Growth, GTM and marketing

| Verdict | Certificate / course | Cost | Valid | When |
|---|---|---|---|---|
| take | [Google Digital Marketing & E-commerce Professional Certificate](https://grow.google/certificates/digital-marketing-ecommerce/), Google on Coursera | $49/month on Coursera, or free with approved financial aid | No expiry | Weeks 1–12, may run into Jan 2027 |
| take | [Google Ads and Google Analytics certifications](https://skillshop.withgoogle.com/), Google Skillshop | Free | 1 year | Jan 2027 |
| take | [CXL Growth Marketing Minidegree](https://cxl.com/institute/programs/growth-marketing-training/), CXL | $699 one-off (or $1,599/year for all CXL programs, incl. the CRO minidegree) | Lifetime | Apr–Jun 2027 |
| later | [Reforge membership (incl. Growth Engineering by Alexey Komissarouk)](https://www.reforge.com/courses/growth-engineering/details), Reforge | $1,995/year; courses aren't sold one by one | While subscribed | Year 2, employer-paid |
| maybe | [Clay University certification](https://university.clay.com/certifications), Clay | Courses free | n/a | Watch for relaunch |

### Nigeria

| Verdict | Certificate / course | Cost | Valid | When |
|---|---|---|---|---|
| take | [3MTT DeepTech_Ready programme](https://3mtt.nitda.gov.ng/deeptech/), NITDA / 3 Million Technical Talent with Data Science Nigeria, backed by Google.org | Free | n/a | Next open cohort |
| skip | [ALX AI Career Essentials](https://www.alxafrica.com/programme/ai-career-essentials/), ALX Africa | Free | n/a | Skip |

### Suggested order

| When | What |
|---|---|
| Weeks 1-12 | Finish Google Digital Marketing & E-commerce certificate |
| Jan 2027 | Free Google Ads + Analytics certs, Agentic AI certificate, apply to 3MTT DeepTech |
| Feb-Mar | One cloud cert: AWS GenAI Developer Pro ($300) or Microsoft AI-103 ($165 US list) |
| Apr-Jun | CXL Growth Marketing Minidegree ($699); Maven AI Evals if employer-paid |
| Year 2 | Reforge ($1,995/yr, employer-paid); Claude Certified Architect once at a Claude partner |
