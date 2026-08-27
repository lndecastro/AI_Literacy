# Module 7: Foundational Models, General-Purpose LLMs, and Applications

Artificial Intelligence has entered a new era driven by **foundational models**, that is, large-scale, general-purpose systems trained on massive multimodal datasets. These models can perform an extraordinary range of tasks, from reasoning and coding to generating text, images, and sound. They represent a shift from narrow, task-specific AI to universal, flexible architectures capable of adaptation across contexts.

Foundational models, particularly **Large Language Models (LLMs)**, are now the backbone of the modern AI ecosystem. Understanding their design, strengths, and limitations is essential for anyone engaging with AI critically and creatively. This module explores some of today's most influential foundational models, general-purpose AI systems and applications, such as **ChatGPT, Claude, Gemini, Meta AI, Grok, Copilot, and Perplexity**, comparing their capabilities, ecosystems, and implications for human-centered use.

> **Guiding Question:** How have LLMs changed what it means for a machine to "know", "create", and "collaborate"?

## Learning Objectives

By the end of this module, you will be able to:

- Define what foundational models and general-purpose LLMs are and explain their significance.
- Identify the key features and capabilities of ChatGPT, Claude, Copilot, Gemini, Meta AI, Perplexity, and Grok.
- Compare tools across dimensions such as reasoning, creativity, openness, and ethical alignment.
- Critically evaluate the trade-offs between open and proprietary AI systems.
- Distinguish **durable principles** from **volatile details** when reading about AI tools, and verify claims independently.
- Reflect on responsible and transparent use of general-purpose AI tools in academic, professional, and creative contexts.

```{admonition} How to read this module
:class: important

This module operates on **two layers**:

- **Durable layer**: what a foundation model is, the five comparative dimensions, the ethical questions, and the task-to-tool reasoning. These change slowly and are the real content of the module.
- **Snapshot layer**: specific model names, version numbers, menu labels, and feature lists. These change at a high frequency, e.g. monthly. Every table marked **📅 Snapshot** below is a photograph of a moving subject.

**Snapshot date: August 2026.** If you are reading this later, assume the snapshot tables are partly outdated and treat verifying them as part of the exercise (see Exercise 6). The durable layer will still hold.
```

---

## Before We Begin: What Makes a Model *Foundational*?

A **foundation model** (the term introduced by Bommasani et al. at Stanford's CRFM in 2021; "foundational model" is used interchangeably) is a model that is:

1. **Trained once, at scale, on broad data**, not on one task, but on enormous general-purpose corpora of text, code, images, and audio. This stage is called **pretraining**, and it is where nearly all the cost and compute live.
2. **Adapted afterwards to many tasks**, through **fine-tuning**, **instruction tuning**, **prompting**, or **retrieval**. One pretrained model becomes a translator, a tutor, a summarizer, and a coding assistant without being retrained from scratch.
3. **A shared base for other systems**, hence "foundation". Many products you use are not models at all; they are applications sitting on top of someone else's foundation model.

That third point explains the **Status** column in the table below, and it is the single most useful distinction in this module:

| Layer           | What it is                                                          | Who builds it                | Examples                                    |
| :-------------- | :------------------------------------------------------------------ | :--------------------------- | :------------------------------------------ |
| **Model layer** | The pretrained foundation model itself, usually reached via an API   | A handful of well-funded labs | GPT, Claude, Gemini, Llama, Grok families   |
| **Application layer** | The interface, tools, memory, and workflows wrapped around a model | Many companies, including the labs themselves | ChatGPT, Claude.ai, Copilot, Perplexity |

Some organizations occupy **both** layers: OpenAI builds the GPT models *and* the ChatGPT product. Others occupy only one: Perplexity builds a research application on top of models it largely licenses from others.

Two further terms you will meet in this module:

- **Open-weight** vs. **open-source.** A model is *open-weight* when you can download its trained parameters and run it yourself. It is *open-source* only when the code, data, and license also meet open-source criteria. Llama is open-weight, and its community license carries commercial restrictions, so calling it "open-source" is imprecise. The distinction matters for anyone deciding what they may legally build on.
- **Model family and tier.** Labs no longer ship one model; they ship a family with tiers trading capability against speed and cost (a large flagship, a balanced mid-tier, a small fast one). "Which model is best?" usually resolves to "which tier, for which task, at which price?"

```{note}
This section is not covered in the recorded video lectures. It provides the conceptual grounding for the comparisons that follow.
```

---

## 7.1 Main General-Purpose LLMs

```{admonition} 📅 Snapshot — August 2026
:class: warning

The descriptions and table in this section reflect each platform as of **August 2026**. Model versions, upload limits, and feature names change frequently. Always verify against the vendor's own documentation before relying on a specific capability.
```

### ChatGPT

ChatGPT is a versatile AI assistant developed by OpenAI, capable of interpreting natural language, performing statistical analyses, coding in Python, and generating data visualizations such as bar charts, pie charts, scatter plots, and histograms. It supports data uploads in common formats (CSV, XLSX, PDF, JSON, images) and can connect to cloud storage such as Google Drive and OneDrive. ChatGPT excels in broad general-purpose capabilities including data analysis, summarization, and storytelling, and it can retrieve current information from the web when browsing is enabled.

Access ChatGPT here: <https://chatgpt.com/>

### Claude.ai

Claude.ai is Anthropic's AI assistant, with strong natural language processing capabilities and well-developed tools for document and data work. It supports file uploads and can execute code within its Analysis Tool to perform complex calculations, data manipulation, and visualization, presenting results through its Artifacts feature. Claude is known for long context windows, which make it well suited to reasoning over large documents. It can also search the web for current information.

Access Claude.ai here: <https://claude.ai/>

### Grok

Grok is a conversational AI developed by xAI, designed to provide witty, insightful, and real-time responses. Integrated with the X platform, Grok emphasizes reasoning and personality-driven interaction, and it draws on live social data. It is positioned as a direct competitor to ChatGPT and Gemini.

Access Grok here: <https://grok.com/>

### Meta AI and Llama

It is worth separating two things that share a brand. **Llama** is Meta's family of **open-weight foundation models**, downloadable and deployable on your own infrastructure under Meta's community license. **Meta AI** is the consumer **application** built on those models, embedded across Facebook, Instagram, WhatsApp, and Messenger, and available as a standalone assistant. It offers multimodal capabilities including text and image generation, real-time chat, and creative and productivity tasks.

The distinction matters: Llama is what makes Meta significant to researchers and developers who need local or private deployment; Meta AI is what most people actually encounter.

Access Meta AI here: <https://www.meta.ai> — Llama models: <https://www.llama.com/>

### Copilot

Copilot is Microsoft's AI assistant integrated across tools like Word, Excel, PowerPoint, Outlook, and Teams. It leverages large language models to help users draft content, analyze data, summarize meetings, and automate workflows. In Excel, it can generate formulas, create charts, and explain data trends. In Word and PowerPoint, it assists with writing, editing, and designing presentations. Copilot is deeply embedded in Microsoft 365, enhancing productivity through natural language commands.

Access Copilot here: <https://copilot.microsoft.com>

### Gemini

Gemini is Google's family of multimodal AI models, integrated into Google Workspace and available via the Gemini web app. It assists users in drafting, summarizing, brainstorming, analyzing documents, and generating code. Within Docs, Gmail, and Sheets, Gemini enhances productivity by offering smart suggestions, data insights, and content generation. It also supports image, audio, and video understanding as well as code interpretation.

Access Gemini here: <https://gemini.google.com>

### Perplexity.ai

Perplexity.ai is an AI-powered research assistant designed to deliver real-time, cited answers by combining LLMs with live web retrieval. It excels at information synthesis, literature review, and market or scientific research, offering reference-based summaries rather than unsourced responses. Users can create **Spaces**, which serve as persistent, shareable research hubs to organize prompts, threads, and citations collaboratively. It is especially valuable for professionals and researchers who require up-to-date, verifiable information.

Access Perplexity here: <https://www.perplexity.ai/>

### Summary

The table below summarizes and compares the platforms discussed in this chapter. It identifies the developer, whether the product is a foundation model or an application built on one (or both), the underlying model family, key strengths, main capabilities, and sample use cases.

```{admonition} 📅 Snapshot — August 2026
:class: warning

The **Model Family** column is the fastest-ageing information in this module. Flagship versions turn over every few months. Read the column as "which family," not "which version."
```

| Product / Platform    | Developer          | Status (Foundation / Application / Both) | Model Family (Aug 2026)                                                       | Key Strengths                                                                                | Primary Capabilities                                    | Example Use Cases                                      |
| --------------------- | ------------------ | ---------------------------------------- | ----------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------ |
| **ChatGPT**           | OpenAI             | Both                                     | GPT family (multimodal transformer models, several tiers)                     | Conversational fluency, multimodal input (text, image, audio), broad tool and API ecosystem   | Text generation, coding, tutoring, analysis             | Education, productivity, software development          |
| **Claude.ai**         | Anthropic          | Both                                     | Claude family (Opus, Sonnet and Haiku tiers)                                  | Long context windows, stated safety focus, artifact creation, document reasoning              | Deep reading, structured writing, policy analysis       | Research synthesis, education, enterprise use          |
| **Copilot**           | Microsoft          | Application                              | Primarily OpenAI models via Azure, plus Microsoft's own in-house models        | Integration with Microsoft 365 and GitHub                                                     | Writing, summarizing, automating workflows              | Business productivity, programming support             |
| **Gemini**            | Google DeepMind    | Both                                     | Gemini family (multimodal, several tiers)                                     | Multimodal reasoning (text, image, video, audio), Google ecosystem integration                | Search, analysis, retrieval-augmented generation        | Data analytics, creative content, education            |
| **Perplexity.ai**     | Perplexity AI      | Application                              | Routes to multiple third-party frontier models, plus in-house retrieval models | Real-time web access with cited answers, source transparency, collaborative Spaces            | Research synthesis, source-based summarization          | Market intelligence, academic research, journalism     |
| **Meta AI / Llama**   | Meta Platforms     | Both (Llama = foundation, Meta AI = app) | Llama family (**open-weight**, community licence — not fully open-source)      | Downloadable weights, customizable, local and private deployment                              | Language generation, chatbot integration                | Research, privacy-preserving AI, app development       |
| **Grok**              | xAI                | Both                                     | Grok family (transformer-based; earlier generation weights released publicly)  | Real-time reasoning, personality, X platform integration                                      | Conversational analysis, summarization, trend detection | Social media insights, public data monitoring          |

## 7.2 Comparative Dimensions

To understand how these systems differ, we analyze them through five key lenses:

1. **Knowledge Base & Architecture**

   - Model scale, multimodal capacity, and update frequency.
   - How training data and architecture affect reasoning and creativity.

2. **Interface & User Experience**

   - Accessibility, collaboration tools, context length, and integration into daily workflows.

3. **Ethical Alignment & Safety Mechanisms**

   - Transparency, interpretability, bias mitigation, and alignment with human values.

4. **Customization & Ecosystem**

   - Plugin systems, fine‑tuning options, APIs, and open vs. closed models.

5. **Performance & Use Contexts**
   - When each model excels: logic, language, creativity, or data connectivity.

```{admonition} Read row 3 critically
:class: tip

The **Ethical Alignment & Safety** row below reports each vendor's **stated approach**, drawn largely from its own published materials. These are claims, not independently verified properties. A central skill in this program is telling the difference and Exercise 4 puts it into practice.
```

| **Dimension**                        | **ChatGPT (OpenAI)**                                                             | **Claude (Anthropic)**                                                       | **Copilot (Microsoft)**                                    | **Gemini (Google DeepMind)**                              | **Perplexity.ai**                                                        | **Meta AI / Llama**                                    | **Grok (xAI)**                                                   |
| ------------------------------------ | -------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------- | --------------------------------------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------ | ---------------------------------------------------------------- |
| **1. Knowledge Base & Architecture** | Trained on diverse multimodal data; strong general reasoning and creativity      | Long-context transformer; optimized for comprehension and document synthesis | Built on licensed and in-house models; connected to Microsoft 365 data | Multimodal (text, image, video, audio); retrieval for live data | Combines third-party frontier LLMs with real-time web retrieval and citation-based reasoning | Open-weight Llama family; customizable; self-hostable  | Uses X platform data; real-time awareness; humor and personality |
| **2. Interface & User Experience**   | Chat interface, custom GPTs, memory features, APIs                               | Structured chat, artifact outputs, projects, long-document workflows         | Embedded in Office, GitHub, Edge; seamless task automation | Integrated with Google ecosystem and Workspace tools      | Research-oriented interface with "Spaces" for saving and sharing threads | Accessible via API, consumer apps, and local deployments | Conversational interface inside X; real-time analytics           |
| **3. Ethical Alignment & Safety** *(stated approaches)* | RLHF, red-teaming, and continuous moderation                   | Constitutional AI; published safety research                                 | Enterprise compliance and data governance commitments      | Responsible AI framework; privacy controls                | Cited sources and visible evidence, intended to reduce unsupported claims | Open research approach; community safety collaboration | Lighter guardrails; more open tone; evolving policies            |
| **4. Customization & Ecosystem**     | Extensive tool and API ecosystem; fine-tuning options                            | Projects, artifacts, and document-based workflows; API                       | Strong app and cloud integration; enterprise focus         | Tightly coupled with Google services and APIs             | Focus on collaboration and knowledge curation through Spaces             | Downloadable weights; adaptable for research and private hosting | Current flagship weights not released; integrated with X        |
| **5. Performance & Best Use**        | Balanced across reasoning, creativity, and code                                  | Deep reading, analysis, long-document work                                   | Productivity and workflow automation                       | Data access, search, multimodal reasoning                 | Real-time research, literature reviews, market and academic intelligence | Research, privacy-preserving, experimentation          | Real-time conversation, social trend analysis                    |

## 7.3 Main Tools and Features of General-Purpose LLM Platforms

Understanding how users interact with general-purpose models is as important as knowing how they work. Each platform provides a unique interface and ecosystem of tools that shape the user experience, productivity, and creative potential. Their features and characteristics are constantly changing and evolving, so some of the features presented here may differ or have expanded by the time you visit this program.

```{admonition} 📅 Snapshot — August 2026
:class: warning

Menu names and feature sets in this table change faster than anything else in the module. Treat the **categories** (a place to chat, a place to persist context, a way to build a reusable assistant, a way to generate media) as durable, and the **labels** as disposable.
```

| **Platform**   | **Main Tools / Interface Elements**                                                                                                                                                                                                                                                        | **Unique Menus and Functionalities**                                                                                                                                                          | **Primary Strengths in Use**                                                                                       |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **ChatGPT**    | • **Chats** for conversation and multimodal input (text, image, file upload). <br>• **Projects** for organizing prompts, documents, and results. <br>• **Custom GPTs** that let users create specialized assistants with custom instructions and tools. <br>• **Library** of community GPTs. | • Menus for **Deep Research**, **Create Image**, **Agent Mode**, and **Explore GPTs**. <br>• **Advanced Data Analysis** for Python, data visualization, and file processing.                      | Comprehensive workspace that blends reasoning, coding, creative design, and research support in one interface.     |
| **Claude**     | • **Chats** for dialogue and document analysis. <br>• **Projects** to group related conversations and files with persistent instructions. <br>• **Artifacts** — live documents generated from chat results (e.g., essays, code, reports).                                                    | • **Extended Thinking**, **Projects**, file uploads, and the **Analysis Tool** for executing code. <br>• Long context windows enable deep reasoning over large documents.                        | Exceptional for reading, writing, and analyzing long documents.                                                    |
| **Copilot**    | • Integrated directly in **Microsoft 365 apps** (Word, Excel, PowerPoint, Outlook, Teams). <br>• **GitHub Copilot** for code completion and review. <br>• **Copilot Agents** for reusable, task-specific assistants.                                                                         | • Contextual actions such as **Ask Copilot**, **Summarize Email**, **Analyze Data**, or **Generate Slides** within each app. <br>• Enterprise data handling via Microsoft Graph.                  | Productivity automation across business and software environments; strong enterprise integration.                  |
| **Gemini**     | • **Chats** (text, image, and code). <br>• **Gems** — customizable mini-assistants for specific tasks. <br>• **NotebookLM** for source-grounded research over your own documents.                                                                                                            | • Menus for **Create Image**, **Deep Research**, and **Canvas**. <br>• Integration with Google Workspace (Docs, Sheets, Slides, Gmail).                                                          | Powerful multimodal reasoning and seamless connection with Google's knowledge graph and cloud tools.               |
| **Perplexity** | • **Chats** with real-time web search and citation-based responses. <br>• **Projects** — persistent, shareable research hubs for organizing queries and summaries. <br>• Collaboration tools for saving, sharing, and revisiting research threads.                                             | • Menus for **Discover**, guided multi-step research modes, and a **Library** of saved and public Spaces. <br>• Real-time retrieval with cited sources and transparent evidence display.         | Reliable, citation-driven research assistant ideal for fact-checking, academic reviews, and market intelligence.   |
| **Meta AI**    | • **Chat Interface** via web or Instagram/WhatsApp integration. <br>• **AI Studio** for creating simple custom AI characters and assistants. <br>• APIs and local deployment options for developers using Llama weights.                                                                     | • Tools for **Image Generation** and **Web Search**. <br>• Downloadable Llama weights for research and customization (community licence).                                                        | Research-friendly, privacy-preserving, and adaptable for custom deployments or local experimentation.              |
| **Grok**       | • **Chat interface** within the **X platform** and standalone app. <br>• **Projects** for organizing related work. <br>• Access to real-time social data streams.                                                                                                                            | • Menus for **Ask Grok**, trend summaries, and post explanation. <br>• Humor-infused persona and live awareness of current topics.                                                               | Real-time analysis of public discourse and social trends; conversational tone with personality.                    |

```{seealso}
The **Custom GPTs / Gems / Projects ** entries above are treated in depth in {ref}`Module 6, Section 6.6 <module6-workspaces>`, which explains *why* persistent context changes model behavior. This section covers *what each interface offers*; Module 6 covers *how to design what goes inside*.
```

### Interpretation and Discussion

- **ChatGPT**, **Claude**, and **Gemini** provide the richest standalone workspaces for general creative and analytical use.
- **Perplexity** distinguishes itself as a _research-oriented assistant_, combining real-time web retrieval with citation-based transparency and collaborative Spaces for organizing findings.
- **Copilot** excels in _embedded productivity_, bringing AI to familiar office applications.
- **Meta AI / Llama** emphasizes _openness and developer control_, aligning with research and privacy priorities.
- **Grok** is a _socially-aware assistant_, focused on real-time trend analysis and cultural insight.

Together, these ecosystems illustrate the **diversification of AI use contexts** — from private research and writing to collaborative productivity and live data reasoning.

### Choosing a Tool for the Task

Version numbers change; the shape of the task does not. This table is organized by **what you are trying to do** rather than by vendor, and should stay useful long after the snapshot tables above have aged.

| If you need to…                                          | Start with                          | Because…                                                              |
| :------------------------------------------------------- | :---------------------------------- | :-------------------------------------------------------------------- |
| Find current information **with sources you can check**   | A retrieval-first assistant          | Citations let you verify; a model answering from memory gives you nothing to check |
| Reason over a **long document or many documents**         | A long-context assistant with file upload and persistent projects | Context length and document workflows are the binding constraint |
| Work **inside Word, Excel, PowerPoint, or Outlook**       | An embedded office assistant         | The value is proximity to your files, not raw model capability        |
| Analyze a **dataset** and produce charts                  | Any assistant with a code-execution tool | Code execution gives reproducible arithmetic; text-only generation invents numbers |
| Build a **reusable assistant** others can use             | A platform with configurable assistants (custom GPTs, Gems, agents) | You configure once and reuse, instead of re-prompting each time |
| Keep data **on your own infrastructure**                  | An open-weight model you can self-host | The only reliable privacy guarantee is data that never leaves         |
| Track **live public conversation**                        | An assistant with real-time social data access | Most models' training data is months old                        |
| Generate images, audio, or video                          | A multimodal or dedicated generative tool | Text-only models cannot, regardless of how you prompt them          |

```{tip}
Notice that no row names a version number, and most rows name a **capability** rather than a product. That is the durable way to choose a tool: decide what the task requires, then check which current products offer it.
```

## 7.4 Ethical and Societal Dimensions

The growing dominance of foundational models and the applications built on them raises important societal questions:

- Who controls access to these systems and their data?
- How can transparency, fairness, and accessibility be ensured?
- What responsibilities do developers and users share in shaping AI behavior?

The discussion of **AI sovereignty**, that is, balancing innovation with independence, is now central to digital ethics. Open-weight models such as **Llama** and community-driven alternatives highlight the importance of democratizing AI infrastructure, while also raising questions about who is accountable when a downloadable model is misused.

### Practical Questions Before You Choose a Tool

Beyond the broad ethical debate, five practical questions affect every user directly. They are rarely visible in the interface, and all five have answers you can look up.

1. **Cost and access.** Which capabilities are free, and which require a paid tier? Free tiers typically cap usage, restrict the strongest model tier, and limit file uploads. Where a course or workplace requires a paid tool, that is a question of **equity**, not just budget.
2. **Data retention and training.** Are your conversations stored, and are they used to train future models? Policies differ by vendor and by plan; consumer plans and enterprise plans often have opposite defaults. Most platforms offer a setting to opt out; find it before you paste anything sensitive.
3. **What should never be pasted.** Student records, patient data, unpublished research, personnel matters, and anything under FERPA, HIPAA, or a non-disclosure agreement. Institutional accounts may carry contractual protections that personal accounts do not.
4. **Academic and professional integrity.** Disclosure norms vary by course, journal, and employer. The relevant question is not "is this allowed?" but "what am I expected to disclose, and to whom?"
5. **Vendor lock-in and continuity.** Assistants, workspaces, and custom instructions built on one platform rarely transfer to another. Providers also discontinue models with limited notice. Ask what happens to your work if the tool changes or disappears.

## 7.5 Hands‑On Exploration

Exercises are marked **Core** or **Optional**. The Core exercises are enough to meet this module's learning objectives; the others extend them for learners who want to go further.

### Exercise 1 – Compare Two LLMs · **Core**

**Goal:** Develop critical literacy by contrasting how models interpret and respond to the same task.

**Instructions:**

1. Choose **two models** (e.g., ChatGPT vs Claude, or Gemini vs Copilot).
2. Ask both to perform the same task — for example:

```
Summarize a recent AI policy report in 200 words and list three implications for education.
```

3. Compare results for **depth, tone, structure, accuracy, and bias**.
4. Write a short (300-word) reflection: _What do these differences reveal about each model's design and training?_

**Deliverable:** Reflection document or discussion post with screenshots or transcripts.

### Exercise 2 – Prompt Engineering Across Platforms · **Optional**

**Goal:** Explore how prompt structure affects creativity and precision in different ecosystems. This exercise applies the patterns from {ref}`Module 5 <module5-prompt-engineering>` across platforms.

**Instructions:**

1. Create a **base prompt**, e.g.:

```
Write a persuasive paragraph encouraging sustainable AI development.
```

2. Modify it three times using different techniques:

- Add context or persona:

```
You are a policy advisor.
```

- Add constraints:

```
Limit to 120 words and cite one credible source.
```

- Add tone:

```
Write in a motivational style.
```

3. Test each version in at least **two LLMs**.
4. Record and analyze how output changes with each variation.

**Deliverable:** Prompt table + 250-word analysis of prompt-response patterns.

### Exercise 3 – Explore Assistants and Workspaces Across Platforms · **Optional**

**Goal:** Experience how *different platforms* implement customization and contextual persistence.

```{note}
In {ref}`Module 6 <module6-workspaces>` you built a personalized assistant and a workspace in depth. This exercise is deliberately **shallow and wide**: the point is to compare how several platforms handle the same idea, not to build another assistant from scratch.
```

**Options — try at least two:**

- In **ChatGPT**, create a **Custom GPT** with a defined role, e.g.:

```
AI Writing Coach for Environmental Science.
```

- In **Claude**, organize a **Project** with custom instructions and use **Artifacts** to iteratively refine an essay or code snippet.
- In **Perplexity**, create a **Space** related to your work area. Explore the Spaces → Templates section and choose one for your project.
- In **Grok**, create a **Project** to organize your work or study material.
- In **Gemini**, design a **Gem** that assists with a research or creative task.

**Deliverable:** A short comparison (one paragraph per platform) of what each made easy, what it made hard, and what it did not support at all.

### Exercise 4 – Ethical Audit: Transparency & Bias · **Core**

**Goal:** Strengthen ethical reasoning and critical evaluation skills.

**Instructions:**

1. Choose one platform (e.g. ChatGPT, Claude, or Gemini).
2. Ask it to:

```
Explain your own limitations and potential biases.
```

```
List where your training data may introduce cultural or regional imbalance.
```

3. Evaluate how transparent and self-aware the model appears. Compare its self-description with the vendor's **published** documentation, do they agree?
4. Discuss potential societal impacts and propose one mitigation strategy.

**Deliverable:** 400-word analytical brief with evidence excerpts.

### Exercise 5 – AI Tool Showcase (Collaborative Project) · **Core, in-session**

**Goal:** Apply comparative insights to a real-world scenario.

**Instructions:**

1. Form small groups. Each group is assigned or selects **one of the platforms**.
2. Research its ecosystem, pricing, data policy, and integration options.
3. Demonstrate a practical use (e.g. Copilot for Excel analytics, Gemini for multimodal design).
4. Present findings as a 5-slide presentation or short recorded demo.

**Deliverable:** Presentation + one-page executive summary highlighting strengths, weaknesses, and best-fit contexts.

### Exercise 6 – Update the Snapshot · **Core**

**Goal:** Practice the most important skill in this module: recognizing that published information about AI tools decays, and verifying it yourself.

**Instructions:**

1. Pick **one row** from any table in Sections 7.1, 7.2, or 7.3.
2. Check the snapshot date at the top of the module. How old is the claim you selected?
3. Using the vendor's **own** documentation, verify every cell in that row. Note what is still accurate, what has changed, and what no longer exists.
4. Rewrite the row as it should read today, and note the date you verified it.
5. Answer: which cells changed, and which held? What does that tell you about which kinds of claims about AI tools are worth memorizing?

**Deliverable:** A corrected table row with a verification date, plus a short paragraph on what proved durable and what did not.

```{tip}
Corrections that hold up can be submitted to the instructor for inclusion in the next edition of this module. This module is designed to be maintained, not merely read.
```

## 7.6 Key Takeaways

- Foundational and general-purpose models act as **infrastructure for intelligence** — adaptable across domains and modalities.
- The **model layer** and the **application layer** are different things; knowing which you are using explains most of what a tool can and cannot do.
- Each platform embodies the **values and priorities** of its developer ecosystem, and its published safety claims are claims to be evaluated, not facts to be accepted.
- **Critical literacy and human oversight** remain essential for all AI interactions.
- The future lies in **interoperable and multimodal AI**, where systems collaborate across tools and contexts.
- **Specifics decay; principles persist.** Anything in this module with a version number or a menu name will be outdated within months. The five comparative dimensions, the task-to-capability reasoning, and the ethical questions will not.

## Reflection

> Return to the guiding question that opened this module: **How have LLMs changed what it means for a machine to "know", "create", and "collaborate"?**

- A model that answers from pretraining is doing something quite different from one that retrieves and cites sources. Which of the two better deserves the word **know**? What does your answer imply about how you should verify what a model tells you?
- When a model produces an essay, an image, or working code, what part of the result is yours? Where would you draw the line, and would you draw it in the same place for a student's assignment as for your own work?
- The platforms in this module all now offer persistent workspaces and configurable assistants. Does that make AI a **collaborator**, or a very well-organized tool? Does the distinction change how you should use it?
- Which of these seven platforms would you actually adopt for your own work, and which trade-off (cost, privacy, capability, or convenience), decided it?

Reflect on how your answers would have differed two years ago, and what that suggests about how confidently anyone should predict the next two.

## 📘 Further Reading (vendor‑neutral)

- Bommasani, R., Hudson, D. A., Adeli, E. et al. (2021). _On the Opportunities and Risks of Foundation Models._ Stanford Center for Research on Foundation Models (CRFM). <https://arxiv.org/abs/2108.07258>
- Bubeck, S., Chandrasekaran, V., Eldan, R. et al. (2023). _Sparks of Artificial General Intelligence: Early Experiments with GPT-4._ Microsoft Research. <https://arxiv.org/abs/2303.12712>
- Google DeepMind. _Gemini: A Family of Highly Capable Multimodal Models._ <https://arxiv.org/abs/2312.11805>
- Mollick, E. & Mollick, L. R. (2024). _Co-Intelligence: Living and Working with AI._ Portfolio.
- Stanford HAI. _AI Index Report_ (published annually; use the most recent edition). <https://aiindex.stanford.edu/report/>
- OpenAI. _Models and documentation._ <https://platform.openai.com/docs/models>
- Anthropic. _Research and model documentation._ <https://www.anthropic.com/research>
- Meta AI. _Llama models and licence terms._ <https://www.llama.com/>
- Microsoft. _Copilot learning hub._ <https://learn.microsoft.com/en-us/copilot>
- xAI. _Grok._ <https://x.ai/grok>
- Perplexity AI. _About Perplexity._ <https://www.perplexity.ai/about>
- Dendritic Institute (2025). _AI Literacy Series – Module 7: Foundational Models and General-Purpose LLMs._ (Slides & Video Lecture)


