# Module 7: Foundational Models, General-Purpose LLMs, and Applications

Artificial Intelligence has entered a new era driven by **foundational models** — large-scale, general-purpose systems trained on massive multimodal datasets. These models can perform an extraordinary range of tasks, from reasoning and coding to generating text, images, and sound. They represent a shift from narrow, task-specific AI to universal, flexible architectures capable of adaptation across contexts.

Foundational models, particularly **Large Language Models (LLMs)**, are now the backbone of the modern AI ecosystem. Understanding their design, strengths, and limitations is essential for anyone engaging with AI critically and creatively. This module explores some of today’s most influential foundational models, general-purpose AI systems and applications — **ChatGPT, Claude, Gemini, Meta.ai, Grok, Copilot, and Perplexity** — comparing their capabilities, ecosystems, and implications for human-centered use.

> **Guiding Question:** How have LLMs changed what it means for a machine to “know”, “create”, and “collaborate”?

## Learning Objectives

By the end of this module, you will be able to:

- Define what foundational models and general-purpose LLMs are and explain their significance.
- Identify the key features and capabilities of ChatGPT, Claude, Copilot, Gemini, Meta.ai, Perplexity, and Grok.
- Compare tools across dimensions such as reasoning, creativity, openness, and ethical alignment.
- Critically evaluate the trade-offs between open and proprietary AI systems.
- Reflect on responsible and transparent use of general-purpose AI tools in academic, professional, and creative contexts.

---

## 7.1 Main General-Purpose LLMs

### ChatGPT

ChatGPT is a versatile AI language model developed by OpenAI, capable of interpreting natural language, performing various statistical analyses, coding in Python, and generating data visualizations such as bar charts, pie charts, scatter plots, and histograms. It supports data uploads in formats like CSV, XLSX, PDF, and JSON (up to 50MB) and can integrate with cloud storage like Google Drive and OneDrive. ChatGPT excels in broad AI capabilities including data analysis, summarization, and storytelling. It requires web browsing for real-time data updates.
Access ChatGPT here: [https://chat.openai.com/]

### Claude.ai

Claude.ai is an AI assistant with strong natural language processing capabilities and expanding tools for data analysis. It supports data uploads and can process data using JavaScript within its Analysis Tool. Claude.ai can perform complex calculations, data manipulation, and create visualizations through its Analysis Tool and Artifacts feature. It primarily analyzes uploaded data and does not rely on real-time web browsing.
Access Claude.ai here: [https://claude.ai/]

### Grok

Grok is a conversational AI developed by Elon Musk’s xAI, designed to provide witty, insightful, and real-time responses. Integrated with X (formerly Twitter), Grok emphasizes reasoning and humor, offering a more personality-driven interaction style. It supports real-time data access and is positioned as a competitor to ChatGPT and Gemini. Access Grok here: [https://x.ai]

### Meta AI

Meta AI is Meta’s suite of generative AI tools embedded across Facebook, Instagram, WhatsApp, and Messenger. It offers multimodal capabilities including text, image, and video generation, and supports real-time chat, creative content generation, and productivity tasks. Meta AI is powered by the Llama 4 model and is accessible via Meta’s apps and a standalone assistant. Access Meta AI here: [https://www.meta.ai]

### Copilot

Copilot is Microsoft’s AI assistant integrated across tools like Word, Excel, PowerPoint, Outlook, and Teams. It leverages large language models to help users draft content, analyze data, summarize meetings, and automate workflows. In Excel, it can generate formulas, create charts, and explain data trends. In Word and PowerPoint, it assists with writing, editing, and designing presentations. Copilot is deeply embedded in Microsoft 365, enhancing productivity through natural language commands. Access Copilot here: [https://copilot.microsoft.com]

### Gemini

Gemini is Google’s family of multimodal AI models integrated into Google Workspace and available via the Gemini web app. It assists users in drafting, summarizing, brainstorming, analyzing documents, and generating code. Within Docs, Gmail, and Sheets, Gemini enhances productivity by offering smart suggestions, data insights, and content generation. It also supports image understanding and code interpretation through its advanced model versions. Access Gemini here: [https://gemini.google.com]

### Perplexity.ai

Perplexity.ai is an AI-powered research assistant designed to deliver real-time, cited answers by combining LLMs with live web retrieval. It excels at information synthesis, literature review, and market or scientific research, offering clear, reference-based summaries rather than speculative responses. Users can create Spaces, which serve as persistent, shareable research hubs to organize prompts, threads, and citations collaboratively. It is especially valuable for professionals and researchers who require up-to-date, verifiable information. Access Perplexity here: [https://www.perplexity.ai/]

### Summary

The table below summarizes and compares the models that are discussed in this chapter. It identifies the developer, the identification if it is a foundational model or an app on top of one, the foundational model being used, key etrengths, main capabilities, and some sample use cases.

| Model                  | Developer          | Status (Foundation / Application / Both) | Underlying Foundational Model(s)                          | Key Strengths                                                                                  | Primary Capabilities                                    | Example Use Cases                                      |
| ----------------------- | ------------------ | ---------------------------------------- | ---------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------ |
| **ChatGPT (GPT-4/5)**   | OpenAI             | Both                                     | GPT-4 and GPT-5 multimodal transformer models              | Conversational fluency, multimodal input (text, image, audio), plugin and API ecosystem        | Text generation, coding, tutoring, analysis             | Education, productivity, software development          |
| **Claude**              | Anthropic          | Both                                     | Claude 3 family (Opus, Sonnet, Haiku)                      | Long context windows, ethical alignment, artifact creation, document reasoning                 | Deep reading, structured writing, policy analysis       | Research synthesis, education, enterprise use          |
| **Copilot**             | Microsoft + OpenAI | Application                              | GPT-4 (Azure OpenAI Service) + domain-specific fine-tuning | Integration with Microsoft 365 and GitHub                                                      | Writing, summarizing, automating workflows              | Business productivity, programming support             |
| **Gemini**              | Google DeepMind    | Both                                     | Gemini 1.5 multimodal family                               | Multimodal reasoning (text, image, video, audio), Google integration                           | Search, analysis, retrieval-augmented generation        | Data analytics, creative content, education            |
| **Perplexity.ai**       | Perplexity Labs    | Application                              | Uses OpenAI GPT-4 and Claude models via retrieval layer     | Real-time web access with cited answers, transparent reasoning, collaborative Spaces feature   | Research synthesis, source-based summarization          | Market intelligence, academic research, journalism      |
| **Meta.ai (LLaMA)**     | Meta Platforms     | Foundation                               | LLaMA-3 and upcoming LLaMA-4 open-weight models             | Open-source, customizable, local deployment                                                    | Language generation, chatbot integration                | Research, privacy-preserving AI, app development       |
| **Grok**                | xAI                | Both                                     | xAI’s proprietary Grok-1 (transformer-based) model          | Real-time reasoning, humor, X platform integration                                             | Conversational analysis, summarization, trend detection | Social media insights, public data monitoring          |

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

To understand how these systems differ, Let us analyze them through these five key lenses:

| **Dimension**                        | **ChatGPT (OpenAI)**                                                             | **Claude (Anthropic)**                                                       | **Copilot (Microsoft)**                                    | **Gemini (Google DeepMind)**                              | **Perplexity.ai**                                                        | **Meta.ai (LLaMA)**                                    | **Grok (xAI)**                                                   |
| ------------------------------------ | -------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------- | --------------------------------------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------ | ---------------------------------------------------------------- |
| **1. Knowledge Base & Architecture** | Trained on diverse multimodal data; GPT-4/5 with strong reasoning and creativity | Long-context transformer; optimized for comprehension and document synthesis | Built on GPT models; integrated with Microsoft 365 data    | Multimodal (text, image, video, audio); RAG for live data | Combines LLMs (GPT-4, Claude) with real-time web retrieval and citation-based reasoning | Open-source LLaMA family; customizable; lightweight    | Uses X platform data; real-time awareness; humor and personality |
| **2. Interface & User Experience**   | Chat interface, custom GPTs, memory features, APIs                               | Structured chat, artifact outputs, clear reasoning chains                    | Embedded in Office, GitHub, Edge; seamless task automation | Integrated with Google ecosystem and Workspace tools      | Research-oriented interface with “Spaces” for saving and sharing threads | Accessible via API and local deployments               | Conversational interface inside X; real-time analytics           |
| **3. Ethical Alignment & Safety**    | RLHF, red-teaming, and continuous moderation                                     | Constitutional AI for safety and transparency                                | Microsoft’s enterprise compliance and data governance      | Google’s Responsible AI framework; privacy controls       | Cited sources, transparent outputs, minimizes hallucinations             | Open research approach; community safety collaboration | Lighter guardrails; more open tone; developing policies          |
| **4. Customization & Ecosystem**     | Extensive plugin and API ecosystem; fine-tuning options                          | Artifact creation and document-based workflows                               | Strong app and cloud integration; enterprise focus         | Tightly coupled with Google services and APIs             | Focus on collaboration and knowledge curation through Spaces             | Fully open; adaptable for research and private hosting | Closed-source; integrated with X social network                  |
| **5. Performance & Best Use**        | Balanced across reasoning, creativity, and code                                  | Deep reading, analysis, ethical reasoning                                    | Productivity and workflow automation                       | Data access, search, multimodal reasoning                 | Real-time research, literature reviews, market and academic intelligence | Research, privacy-preserving, experimentation          | Real-time conversation, social trend analysis                    |

## 7.3 Main Tools and Features of General-Purpose LLM Platforms

Understanding how users interact with general-purpose models is as important as knowing how they work. Each platform provides a unique interface and ecosystem of tools that shape the user experience, productivity, and creative potential. Their features and characteristics are constanly changing and evolving, thus some of the features presented here may be different or expanded when you visit this program.

| **Model**      | **Main Tools / Interface Elements**                                                                                                                                                                                                                                                                             | **Unique Menus and Functionalities**                                                                                                                                                                                                                             | **Primary Strengths in Use**                                                                                       |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **ChatGPT**    | • **Chats** for conversation and multimodal input (text, image, file upload). <br>• **Projects** for organizing prompts, documents, and results. <br>• **Custom GPTs** that let users create specialized assistants with custom instructions and APIs. <br>• **Library** of community GPTs. | • Menus for **Deep Research**, **Create Image** (DALL·E 3), **Agent Mode**, **Add Sources**, and **Explore GPTs**. <br>• **Code Interpreter / Advanced Data Analysis (Codex)** for Python, data visualization, and file processing.                                  | Comprehensive workspace that blends reasoning, coding, creative design, and research support in one interface.     |
| **Claude**     | • **Chats** for dialogue and document analysis. <br>• **Projects** to group related conversations and files. <br>• **Artifacts** — live documents generated from chat results (e.g., essays, code, reports).                                                                  | • Menus for **Extended Thinking**, **Projects Panel**, **File Uploads**, and **Document Mode**. <br>• Long-context windows (200k+ tokens) enable deep document reasoning.                                                                                        | Exceptional for reading, writing, and analyzing long documents with strong ethical alignment and clarity.          |
| **Copilot**    | • Integrated directly in **Microsoft 365 apps** (Word, Excel, PowerPoint, Outlook, Teams). <br>• **GitHub Copilot** for code completion and review.                                                                                                                        | • Contextual menus such as **Ask Copilot**, **Summarize Email**, **Analyze Data**, or **Generate Slides** within each app. <br>• Enterprise-grade data security via Microsoft Graph.                                                                               | Productivity automation across business and software environments; strong enterprise integration.                  |
| **Gemini**     | • **Chats** (text, image, and code). <br>• **Gems** — customizable mini-assistants for specific tasks.                                                                                                                              | • Menus for **Create Image**, **Write**, **Build**, **Deep Research**, and **Learn**. <br>• Integration with Google Workspace (Docs, Sheets, Slides, Gmail).                                                                                                     | Powerful multimodal reasoning and seamless connection with Google’s knowledge graph and cloud tools.               |
| **Perplexity** | • **Chats** with real-time web search and citation-based responses. <br>• **Spaces** — persistent, shareable research hubs for organizing queries and summaries. <br>• Collaboration tools for saving, sharing, and revisiting research threads.                            | • Menus for **Discover**, **Copilot Mode** (guided multi-step research), and **Library** of public Spaces. <br>• Real-time retrieval with cited sources and transparent evidence display.                                                                          | Reliable, citation-driven research assistant ideal for fact-checking, academic reviews, and market intelligence.   |
| **Meta.ai**    | • **Chat Interface** via web or Instagram/WhatsApp integration. <br>• APIs and local deployment options for developers.                                                                                                             | • Tools for **Image Generation**, **Web Search**, and **Open Model Access** through LLaMA 3. <br>• Fully open-source weights for research and customization.                                                                                                     | Research-friendly, privacy-preserving, and adaptable for custom deployments or local experimentation.              |
| **Grok**       | • **Chat interface** within the **X platform**. <br>• Access to real-time social data streams.                                                                                                                                      | • Menus for **Ask Grok**, **Trends**, **Summarize**, and **Explain Posts**. <br>• Humor-infused persona and live awareness of current topics.                                                                              | Real-time analysis of public discourse and social trends; conversational tone with personality.                    |

### Interpretation and Discussion

- **ChatGPT**, **Claude**, and **Gemini** provide the richest standalone workspaces for general creative and analytical use.  
- **Perplexity** distinguishes itself as a _research-oriented assistant_, combining real-time web retrieval with citation-based transparency and collaborative Spaces for organizing findings.  
- **Copilot** excels in _embedded productivity_, bringing AI to familiar office applications.  
- **Meta.ai** emphasizes _openness and developer control_, aligning with research and privacy priorities.  
- **Grok** is a _socially-aware assistant_, focused on real-time trend analysis and cultural insight.  

Together, these ecosystems illustrate the **diversification of AI use contexts** — from private research and writing to collaborative productivity and live data reasoning.

## 7.4 Ethical and Societal Dimensions

The growing dominance of foundational models and some applications raises important societal questions:

- Who controls access to these systems and their data?
- How can transparency, fairness, and accessibility be ensured?
- What responsibilities do developers and users share in shaping AI behavior?

The discussion of **AI sovereignty** — balancing innovation with independence — is now central to digital ethics. Open models such as **LLaMA** and community-driven alternatives highlight the importance of democratizing AI infrastructure.

> **Reflection Prompt:** What trade‑offs exist between convenience and control when choosing between open and proprietary AI systems?

## 7.5 Hands‑On Exploration

### Exercise 1 – Compare Two LLMs

**Goal:** Develop critical literacy by contrasting how models interpret and respond to the same task.
**Instructions:**

1. Choose **two models** (e.g., ChatGPT vs Claude or Gemini vs Copilot).
2. Ask both to perform the same task — for example:

```
Summarize a recent AI policy report in 200 words and list three implications for education.
```

4. Compare results for **depth, tone, structure, accuracy, and bias**.
5. Write a short (300-word) reflection: _What do these differences reveal about each model’s design and training?_

   **Deliverable:** Reflection document or discussion post with screenshots or transcripts.

### Exercise 2 – Prompt Engineering Across Platforms

**Goal:** Explore how prompt structure affects creativity and precision in different ecosystems.
**Instructions:**

1. Create a **base prompt**, e.g.:

```
Write a persuasive paragraph encouraging sustainable AI development”
```

3. Modify it three times using different techniques:

- Add context or persona:

```
You are a policy advisor
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

### Exercise 3 – Build or Customize a Personalized Assistant or Project

**Goal:** Experience model customization and contextual persistence.
**Options:**

- In **ChatGPT**, create a **Custom GPT** with a defined role, e.g.:

```
AI Writing Coach for Environmental Science.
```

- In **Claude**, organize a **Project** and use **Artifacts** to iteratively refine an essay or code snippet.
- In **Perplexity** create a **Space** related with your work area. Explore the Spaces -> Templates section and choose one for your project.
- In **Grok** create a **Project** to organize your work or study material. Explore the projects available to understand the structure, functionalities, and operation.
- In **Gemini**, design a **Gem** that assists with a research or creative task.

  **Deliverable:** Short demo or written description of your assistant’s purpose, instructions used, and sample output.

### Exercise 4 – Ethical Audit: Transparency & Bias

**Goal:** Strengthen ethical reasoning and critical evaluation skills. <p>
**Instructions:**

1. Choose one platform (e.g. ChatGPT, Claude, or Gemini).
2. Ask it to:

```
Explain its own limitations and potential biases.
```

```
List where its training data may introduce cultural or regional imbalance.
```

3. Evaluate how transparent and self-aware the model appears.
4. Discuss potential societal impacts and propose one mitigation strategy.

   **Deliverable:** 400-word analytical brief with evidence excerpts.

### Exercise 5 – AI Tool Showcase (Collaborative Project)

**Goal:** Apply comparative insights to a real-world scenario.
**Instructions:**

1. Form small groups. Each group is assigned or selects **one of the models**.
2. Research its ecosystem, pricing, data policy, and integration options.
3. Demonstrate a practical use (e.g. Copilot for Excel analytics, Gemini for multimodal design).
4. Present findings as a 5-slide presentation or short recorded demo.

   **Deliverable:** Presentation + one-page executive summary highlighting strengths, weaknesses, and best-fit contexts.

## 7.6 Key Takeaways

- Foundational and general-purpose models act as **infrastructure for intelligence** — adaptable across domains and modalities.
- Each model embodies the **values and priorities** of its developer ecosystem.
- **Critical literacy and human oversight** remain essential for all AI interactions.
- The future lies in **interoperable and multimodal AI**, where systems collaborate across tools and contexts.

## 📘 Further Reading (vendor‑neutral)

- OpenAI (2024). GPT-4 Technical Report. https://cdn.openai.com/papers/gpt-4.pdf
- Anthropic (2024). Claude Model Overview and Safety Research. https://www.anthropic.com/research
- Google DeepMind (2024). Gemini: A Family of Multimodal Foundation Models. https://arxiv.org/abs/2312.11805
- Perplexity AI (2024). About Perplexity. https://www.perplexity.ai/about  
- Meta AI (2024). Llama 4: Leading intelligence. Unrivaled speed and efficiency. https://ai.meta.com/llama
- Microsoft (2024). Copilot learning hub. https://learn.microsoft.com/en-us/copilot
- xAI (2024). Introducing Grok: Conversational AI with Real-Time Awareness. https://x.ai/grok
- Bommasani, R., Hudson, D. A., Adeli, E. et al. (2021). On the Opportunities and Risks of Foundation Models. Stanford Center for Research on Foundation Models (CRFM). https://arxiv.org/abs/2108.07258
- Bubeck, S., Chandrasekaran, V., Eldan, R. et al. (2023). Sparks of Artificial General Intelligence: Early Experiments with GPT-4. Microsoft Research. https://arxiv.org/abs/2303.12712
- Mollick, E. & Mollick, L. R. (2024). Co-Intelligence: Living and Working with AI. Portfolio.
- Dendritic Institute (2025). AI Literacy Series – Module 7: Foundational Models and General-Purpose LLMs. (Slides & Video Lecture).
