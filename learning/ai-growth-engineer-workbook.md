# AI Growth Engineer Workbook

A 12-week plan (28 Sep to 20 Dec 2026, ~15 h/week) to become an AI engineer and growth engineer, ending in a launched capstone project.

Interactive version with progress tracking: https://claude.ai/artifact/6GB2UzyNKZuCnZpgBkK8Jq

## Rules

1. 70% build, 30% watch. If you fall behind, cut videos, never the weekly ship.
2. Use your own data: ad reports, landing pages, funnels you know.
3. One public repo with a weekly log in the README.
4. Set an API spend limit in the Anthropic Console before week 1.

## Phases

| Weeks | Phase |
|---|---|
| 1-3 | Foundations |
| 4-6 | RAG, agents, MCP |
| 7-8 | Evals + growth |
| 9-12 | Capstone build + launch |

## Week 1: How LLMs actually work (28 Sept to 4 Oct)

- [ ] **Video:** Intro to Large Language Models, Andrej Karpathy ([link](https://www.youtube.com/watch?v=zjkBMFhNj_g)), 1 h. The one-hour mental model: what an LLM is, what it's good and bad at.
- [ ] **Video:** Deep Dive into LLMs like ChatGPT, Andrej Karpathy ([link](https://www.youtube.com/watch?v=7xTGNNLPyMI)), 3.5 h. Pretraining, fine-tuning, RL, hallucinations, tool use. Split it into three sittings.
- [ ] **Video:** Transformers, the tech behind LLMs + Attention in transformers, 3Blue1Brown ([link](https://www.youtube.com/watch?v=wjZofJX0v4M)), 1 h. Visual picture of tokens, embeddings and attention. Embeddings come back in week 4 for RAG. Watch chapter 6 right after.
- [ ] **Read:** The Rise of the AI Engineer, swyx, Latent Space ([link](https://www.latent.space/p/ai-engineer)), 0.5 h. The essay that named the role. Tells you what the job is and isn't.
- [ ] **Read:** What is Growth Engineering?, The Pragmatic Engineer with Alexey Komissarouk ([link](https://newsletter.pragmaticengineer.com/p/what-is-growth-engineering)), 0.5 h. “Writing code to help a company make more money.” The clearest definition of the role, from the person who built growth eng at MasterClass.
- [ ] **Read:** What is a growth engineer? (And why they're awesome), PostHog ([link](https://posthog.com/blog/what-is-a-growth-engineer)), 0.25 h. Short, practical take from a company that hires them.
- [ ] **Build:** First API calls in TypeScript and Python, You ([link](https://docs.claude.com/en/docs/get-started)), 3 h. Get an API key, set a spend limit, send a message from Node and from Python. Then paste in a real search-term report export and ask for a summary.

**Ship:** A public GitHub repo (ai-growth-lab) with your first two scripts and a README log.

## Week 2: Talk to models well (5 Oct to 11 Oct)

- [ ] **Course:** Building with the Claude API, Anthropic Academy (free, certificate) ([link](https://anthropic.skilljar.com/claude-with-the-anthropic-api)), 6 h. API basics, prompting, tool use, RAG and workflows in one course. Spread it over the week.
- [ ] **Course:** Prompt engineering interactive tutorial, Anthropic (GitHub notebooks) ([link](https://github.com/anthropics/prompt-eng-interactive-tutorial)), 3 h. Hands-on exercises. Do the chapters on structure, examples and output formatting.
- [ ] **Video:** How I use LLMs, Andrej Karpathy ([link](https://www.youtube.com/watch?v=EWvNQjAaOHw)), 2 h. Practical tour of thinking models, tools, file uploads. Good for your daily workflow too.
- [ ] **Course:** CS50's Introduction to Programming with Python (only if rusty), Harvard, free ([link](https://cs50.harvard.edu/python/)), optional. Skip if you can already write Python functions, loops and read a CSV. Otherwise do weeks 0 to 4 and 6 across weeks 2 and 3.
- [ ] **Build:** Structured-output classifier, You ([link](https://docs.claude.com/en/docs/build-with-claude/structured-outputs)), 3 h. Feed 500 search terms, get JSON back: term, intent, keep or negative, reason. Label 50 yourself and compare.

**Ship:** A search-term classifier script and a table showing where it agreed and disagreed with your own calls.

## Week 3: AI apps in TypeScript (12 Oct to 18 Oct)

- [ ] **Course:** Vercel AI SDK Tutorial, Matt Pocock, AI Hero (free, 16 lessons) ([link](https://www.aihero.dev/vercel-ai-sdk-tutorial)), 4 h. You already know TypeScript. This is the fastest path from zero to AI features in Next.js: streaming, structured output, tools, agents.
- [ ] **Docs:** AI SDK docs: Next.js App Router quickstart, Vercel ([link](https://ai-sdk.dev/docs)), 2 h. Reference for the build below.
- [ ] **Read:** Building Effective Agents, Anthropic ([link](https://www.anthropic.com/engineering/building-effective-agents)), 0.5 h. Workflows vs agents, and why you should start with the simplest pattern that works. Reread it in week 5.
- [ ] **Video:** Software Is Changing (Again), Andrej Karpathy, YC AI Startup School ([link](https://www.youtube.com/watch?v=LCEmiRjPEtQ)), 0.75 h. Software 3.0 and “partial autonomy” apps. Shapes how you design the capstone's human-in-the-loop.
- [ ] **Build:** Next.js chat with a ROAS/CPA tool, You ([link](https://ai-sdk.dev/docs/ai-sdk-core/tools-and-tool-calling)), 5 h. The model calls your calculator function instead of doing math in its head. Deploy to Vercel.

**Ship:** A live Vercel URL with a streaming chat that calls one tool.

## Week 4: RAG: give models your data (19 Oct to 25 Oct)

- [ ] **Video:** Learn RAG From Scratch, Lance Martin, freeCodeCamp ([link](https://www.youtube.com/watch?v=sVcwVQRHIc8)), 2.5 h. Indexing, retrieval, query rewriting, routing. Code along with the notebooks in github.com/langchain-ai/rag-from-scratch.
- [ ] **Read:** Introducing Contextual Retrieval, Anthropic ([link](https://www.anthropic.com/news/contextual-retrieval)), 0.5 h. A simple trick that cuts failed retrievals a lot. Easy to add to your build.
- [ ] **Book:** AI Engineering, chapters 1 and 2, Chip Huyen ([link](https://github.com/chiphuyen/aie-book)), 4 h. Foundation models, sampling, why outputs vary. Keep one page of notes per chapter.
- [ ] **Docs:** AI and Vectors guide (pgvector), Supabase ([link](https://supabase.com/docs/guides/ai)), 1 h. Store embeddings in Postgres. One database for app data and vectors.
- [ ] **Build:** Ad-policy RAG, You ([link](https://support.google.com/adspolicy/)), 5 h. Index Google Ads policy pages plus your own playbooks. Ask “why was this ad disapproved?” and return the answer with sources.

**Ship:** A RAG demo that answers ad-policy questions with a citation on every answer.

## Week 5: Agents and tool use (26 Oct to 1 Nov)

- [ ] **Course:** Hugging Face Agents Course, Units 1 and 2, Hugging Face (free, certificate) ([link](https://huggingface.co/learn/agents-course)), 6 h. The Thought, Action, Observation loop, then smolagents, LlamaIndex and LangGraph. Get the Unit 1 certificate.
- [ ] **Read:** Effective context engineering for AI agents, Anthropic ([link](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)), 0.75 h. What to put in the model's context and what to leave out. The skill that separates working agents from demos.
- [ ] **Read:** Patterns for Building LLM-based Systems & Products, Eugene Yan ([link](https://eugeneyan.com/writing/llm-patterns/)), 1 h. Evals, RAG, guardrails, caching, user feedback, all in one long post.
- [ ] **Book:** AI Engineering, chapters 5 and 6, Chip Huyen ([link](https://github.com/chiphuyen/aie-book)), 4 h. Prompt engineering, RAG and agents, with the reasoning behind each pattern.
- [ ] **Build:** Waste-finder agent with three tools, You ([link](https://docs.claude.com/en/docs/agents-and-tools/tool-use/overview)), 4 h. Tools: load report, compute CPA/ROAS per term, propose negatives. Log every tool call so you can debug it.

**Ship:** An agent that turns a raw search-term report into a ranked waste list with reasons.

## Week 6: MCP + pick your capstone (2 Nov to 8 Nov)

- [ ] **Course:** Introduction to Model Context Protocol, Anthropic Academy (free, certificate) ([link](https://anthropic.skilljar.com/introduction-to-model-context-protocol)), 3 h. Build MCP servers and clients: tools, resources, prompts.
- [ ] **Read:** Open Source Google Ads API MCP Server, Google Ads Developer Blog ([link](https://ads-developers.googleblog.com/2025/10/open-source-google-ads-api-mcp-server.html)), 1 h. Google's official, read-only Ads MCP server (code at github.com/googleads/google-ads-mcp). Your capstone's data source.
- [ ] **Build:** Connect ad data over MCP, You ([link](https://github.com/googleads/google-ads-mcp)), 5 h. Run Google's server against a test account, or write a small MCP server that serves a CSV export if API access takes too long.
- [ ] **Plan:** Write the capstone spec, You, 2 h. One page: who it's for, the problem, north-star metric, what you're cutting. See the capstone section below.
- [ ] **Video:** Pick 3 talks from AI Engineer World's Fair 2026, AI Engineer channel ([link](https://www.youtube.com/@aiDotEngineer)), 2 h. Choose talks on evals, agents in production, or AI for marketing. Note one idea to steal for each.

**Ship:** A one-page capstone spec and a working MCP connection to ad data.

## Week 7: Evals: prove it works (9 Nov to 15 Nov)

- [ ] **Read:** Your AI Product Needs Evals, Hamel Husain ([link](https://hamel.dev/blog/posts/evals/)), 1 h. Three levels: assertions, human and model grading, A/B tests. The most-cited post on the topic.
- [ ] **Read:** AI Evals FAQ, Hamel Husain and Shreya Shankar ([link](https://hamel.dev/blog/posts/evals-faq/)), 2 h. Start from real traces, find failure modes, then write evals for the ones that matter.
- [ ] **Course:** Evaluating AI Agents, DeepLearning.AI x Arize (free) ([link](https://www.deeplearning.ai/courses/evaluating-ai-agents)), 2 h. Tracing, structured experiments, monitoring an agent after launch.
- [ ] **Book:** AI Engineering, chapters 3 and 4, Chip Huyen ([link](https://github.com/chiphuyen/aie-book)), 4 h. Evaluation methods and how to build an evaluation pipeline.
- [ ] **Build:** Golden dataset + LLM judge, You ([link](https://hamel.dev/blog/posts/llm-judge/)), 5 h. Label 100 to 200 search terms from past accounts (remove client names). Measure precision and recall on “negative”. Add a judge that checks ad copy against compliance rules.

**Ship:** An eval script you run before every change, with the current score in your README.

## Week 8: Growth engineering core (16 Nov to 22 Nov)

- [ ] **Read:** A software engineer's guide to A/B testing, PostHog ([link](https://posthog.com/product-engineers/ab-testing-guide-for-engineers)), 0.5 h. Hypothesis, goal metric, one change at a time, run for at least a week.
- [ ] **Book:** Trustworthy Online Controlled Experiments, ch. 1 to 3 and 17, Kohavi, Tang, Xu ([link](https://experimentguide.com/)), 5 h. You know ad A/B tests. This covers product experiments and the stats behind a trustworthy result.
- [ ] **Tool:** Sample size calculator, Evan Miller ([link](https://www.evanmiller.org/ab-testing/sample-size.html)), 0.5 h. Plug in a real conversion rate from a past client. See how much traffic a test needs before it means anything.
- [ ] **Course:** Select Star SQL, Free interactive book ([link](https://selectstarsql.com/)), 4 h. Growth work lives in SQL: funnels, cohorts, retention. This is the fastest free way in.
- [ ] **Video:** The DNA of a Great Growth Engineer, Alexey Komissarouk, Reforge ([link](https://www.youtube.com/watch?v=fFZBZJrnUIg)), 1 h. What separates good growth engineers, from the person who teaches Reforge's growth engineering course.
- [ ] **Build:** Instrument the capstone landing page, You ([link](https://posthog.com/docs/libraries/next-js)), 3 h. PostHog events, a signup funnel, one feature flag. You know GTM event design; this is the product-side version.

**Ship:** A live PostHog funnel for your capstone landing page, with one feature flag.

## Week 9: AI-era growth + capstone sprint 1 (23 Nov to 29 Nov)

- [ ] **Podcast:** The new AI growth playbook for 2026, Elena Verna on Lenny's Podcast ([link](https://www.lennysnewsletter.com/p/the-new-ai-growth-playbook-for-2026-elena-verna)), 1.5 h. How Lovable grew: loops, retention first, and why much of the old growth playbook no longer applies.
- [ ] **Read:** Three posts from Elena's Growth Scoop, Elena Verna ([link](https://www.elenaverna.com/)), 1 h. Pick posts on growth loops and retention. Write down which loop your capstone could use.
- [ ] **Course:** Clay 101: GTM Automation (optional), Clay University (free) ([link](https://university.clay.com/courses/clay-101)), optional. GTM engineer roles overlap heavily with your background. About 2 hours if you want to keep that door open.
- [ ] **Docs:** Langfuse tracing quickstart, Langfuse (open source) ([link](https://langfuse.com/docs)), 1 h. See every prompt, tool call, cost and latency. You'll use traces to find what to fix in weeks 10 and 11.
- [ ] **Build:** Capstone sprint 1: core flow, You, 9 h. Connect data, classify, rank waste, show results behind a login. Tracing on from day one.

**Ship:** A private beta: the core flow working end to end, with tracing.

## Week 10: Capstone sprint 2 (30 Nov to 6 Dec)

- [ ] **Build:** Human approval step, You, 3 h. Nothing touches an ad account without a click. This is also your answer to “how do you handle AI mistakes?” in interviews.
- [ ] **Build:** Cost and latency budget, You ([link](https://docs.claude.com/en/docs/build-with-claude/prompt-caching)), 2 h. Show cost per analysis. Use prompt caching and smaller models where evals say quality holds.
- [ ] **Build:** Grow the eval set by 50 cases, You, 2 h. Every real failure becomes a test case. Re-run evals after every change.
- [ ] **Build:** Waitlist page + first A/B test, You ([link](https://posthog.com/docs/experiments)), 4 h. Test one headline. Let it run a full week before you call it.
- [ ] **Plan:** Get 5 testers from your network, You, 2 h. Past clients, agency contacts, marketers on LinkedIn. Watch them use it; don't explain it.

**Ship:** Five real marketers have tried it and you've logged what broke.

## Week 11: Capstone sprint 3 (7 Dec to 13 Dec)

- [ ] **Build:** Fix the top 3 failure modes, You, 5 h. Pick them from traces and tester notes, not from gut feel.
- [ ] **Build:** Onboarding: first insight in under 5 minutes, You ([link](https://posthog.com/product-engineers/growth-engineering)), 4 h. Measure time-to-value in PostHog. Cut steps until it's under five minutes.
- [ ] **Plan:** Case study draft, You, 4 h. Problem, architecture diagram, eval scores, funnel numbers, what you'd do next. Numbers beat adjectives.

**Ship:** Version 1.0, feature frozen, with a case study draft.

## Week 12: Launch and package (14 Dec to 20 Dec)

- [ ] **Build:** Record a 3-minute demo video, You, 2 h. Problem in 20 seconds, live demo, one number at the end.
- [ ] **Plan:** Publish the case study, You ([link](https://growveloper.com/)), 4 h. On growveloper.com, LinkedIn and the GitHub README. Link all three to each other.
- [ ] **Plan:** Launch post, You, 2 h. LinkedIn and X. Product Hunt is optional. Track signups from each channel with UTMs (your home turf).
- [ ] **Plan:** Update your CV and start applying, You, 3 h. Add the project as your lead proof point. Target: applied AI engineer, growth engineer, GTM engineer. Run the roles through career-ops before applying.

**Ship:** Public case study, demo video, and repo. CV updated.

## Capstone: SpendSentry (working name)

An AI agent that finds wasted Google Ads spend and proposes fixes, with a human approval step before anything changes in the account.

| Part | Proves | Done when |
|---|---|---|
| Search-term classifier | Structured output, prompting | >= 85% precision on "negative" vs golden set |
| Waste ranking agent | Tool use, agents, MCP | Raw report becomes a ranked list with $ at stake |
| Policy/compliance RAG | RAG with citations | Every copy suggestion cites its policy source |
| Eval suite | Evals, LLM-as-judge | One command runs 150+ cases and prints a score |
| Landing page + onboarding | Growth engineering | PostHog funnel live, one A/B test run to a decision |
| Tracing and cost | Production | Langfuse traces, cost per analysis shown |

Stack: Next.js, Vercel AI SDK, Claude API, Google Ads MCP, Supabase + pgvector, Langfuse, PostHog, Vercel.

North-star metric: dollars of wasted spend found per connected account.

## After the 12 weeks: certifications and paid courses

For January 2027 onward. Prices in USD; check before paying.

- Portfolio first, certificate second.
- Pick one cloud certificate (AWS or Microsoft), not three.
- Get employers to pay for Reforge, Maven and CXL.
- Apply for Coursera financial aid on any Coursera course.

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

### Growth and GTM engineering

| Verdict | Certificate / course | Cost | Valid | When |
|---|---|---|---|---|
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
| Jan 2027 | Free Google Ads + Analytics certs, Agentic AI certificate, apply to 3MTT DeepTech |
| Feb-Mar | One cloud cert: AWS GenAI Developer Pro ($300) or Microsoft AI-103 ($165 US list) |
| Apr-Jun | CXL Growth Marketing Minidegree ($699); Maven AI Evals if employer-paid |
| Year 2 | Reforge ($1,995/yr, employer-paid); Claude Certified Architect once at a Claude partner |

Lean path: about $200-350. Everything self-paid: about $3,050 plus Maven. With employer paying Reforge and Maven: about $1,050 or less.
