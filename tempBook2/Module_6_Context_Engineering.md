# Module 6: Context Engineering - Advanced AI Communication

Context engineering is the practice of **designing, structuring, and managing the broader environment** in which a large language model (LLM) processes information, not just the direct prompt.
While prompt engineering focuses on *how you phrase the instruction*, context engineering focuses on *what additional information surrounds and informs that instruction*.
It is sometimes called *“prompt engineering on steroids”* because it moves beyond single instructions into **systematic control of the model’s cognitive environment**.

## Learning Objectives

After completing this module, you will be able to:
- Define **Context Engineering** and explain its importance in guiding AI behavior and output quality.  
- Identify key components that shape AI context, including **role**, **audience**, **purpose**, **tone**, and **constraints**.  
- Design prompts that embed clear contextual cues to improve relevance, coherence, and ethical alignment.  
- Distinguish between **explicit** and **implicit** context in human–AI interaction.  
- Apply context engineering techniques to achieve desired outcomes across different domains and use cases.  
- Reflect on how context influences meaning, interpretation, and responsibility in AI-generated content.  

## 6.1 Why Context Matters?

LLMs generate answers based purely on the **input context window**: the prompt plus any surrounding data you provide. By carefully shaping this context, you can:
- **Bias the model toward desired outcomes**  
- **Reduce hallucination** by grounding responses in authoritative sources  
- **Adapt the model to specific roles**  
- **Create repeatable workflows** for consistency  

## 6.2 Key Techniques in Context Engineering

Context engineering integrates multiple techniques to shape how AI systems interpret inputs, maintain coherence, and generate relevant, high-quality outputs. Each technique contributes to a structured interaction framework that transforms a simple prompt into a rich, goal-oriented exchange.

1. **System Role Design** – Define the AI’s persona or purpose.  
   *Example:*  
   ```
   You are an experienced data storyteller helping a university explain research findings to a general audience. Use clear, engaging language and avoid technical jargon.
   ```

2. **Instruction Layering** – Combine multiple prompt patterns (e.g., role + format + goal).  
   *Example:*  
   ```
   Act as a policy analyst. Summarize this report in bullet points, then draft a 100-word executive summary emphasizing environmental impact.
   ```

3. **Contextual Priming** – Provide reference materials or examples to shape the model’s reasoning.  
   *Example:*  
   ```
   Here is an example of a strong abstract for a research paper. Use the same structure and tone to rewrite the following abstract.
   ```

4. **Retrieval-Augmented Generation (RAG)** – Dynamically inject external data into the prompt to enhance factual grounding.  
   *Example:*  
   ```
   Using the following retrieved text from a 2024 WHO report, summarize the three main health challenges related to AI in diagnostics.
   (Paste retrieved content or database snippet below.)
   ```

5. **Chained Prompts** – Break complex tasks into sequential, interdependent stages.  
   *Example:*  
   ```
   Step 1: List key challenges in AI ethics in higher education.
   Step 2: For each challenge, propose one institutional policy response.
   Step 3: Summarize the recommendations in a 150-word brief.
   ```

6. **Output Shaping** – Specify the desired tone, style, or format of the response.  
   *Example:*  
   ```
   Write the introduction as if for a university newsletter — friendly, professional, and limited to 120 words.
   ```

7. **Negative Context Engineering** – Explicitly define what should be avoided or excluded.  
   *Example:*  
   ```
   Summarize the benefits of generative AI in healthcare, but do not include examples related to patient data privacy or regulation.
   ```

8. **Multi-Modal Context Orchestration** – Combine multiple input types (e.g., text, image, or structured data).  
   *Example:*  
   ```
   Analyze the chart below showing AI model accuracy over time and write a paragraph explaining the trend. Reference the image in your response.
   (Insert chart or figure here.)
   ```

## 6.3 Prompt vs Context Engineering

| Aspect        | Prompt Engineering              | Context Engineering                             |
|---------------|---------------------------------|------------------------------------------------|
| Focus         | Wording of instruction          | Full environment around the instruction         |
| Scope         | Single prompt                   | Multi-layered input, documents, workflows       |
| Goal          | Better single response          | Consistent, domain-specific high-quality outputs|
| Analogy       | Writing a recipe                | Designing the entire kitchen and pantry setup   |

## 6.4 Example in Education and Learning

**Prompt Engineering Example:**  
```
Summarize this lesson plan in three bullet points.
```

Download the [Sample lesson plans](./Data/SampleLessonPlans.pdf). 

**Context Engineering Example:**  
```
System Role: You are an instructional designer specializing in technology-enhanced learning.

Reference Context: Here are three sample lesson plans from previous AI Literacy workshops [INSERT OR UPLOAD CONTENT].

Task: Evaluate the following lesson plan. Compare it to the reference cases and summarize in three bullet points.

Output: Provide a structured table with Strengths, Weaknesses, and Improvement Suggestions.
```

By embedding **role, reference materials, task, and output format**, the model produces more reliable and actionable results.

## 6.5 Example in Healthcare

**Prompt Engineering Example:** 
```
Summarize this patient case in three bullet points.
```

**Context Engineering Example:**  
```
System Role: You are a clinical data analyst supporting a hospital’s quality-improvement team.

Reference Context and Task: Review the following anonymized patient summary and compare it to current treatment guidelines provided in the reference file.

Output: Present your response in three bullet points organized under: Key Findings, Potential Risks, and Recommended Next Steps.
```

This demonstrates how adding context transforms a basic summarization task into a guided, responsible, and domain-specific analysis—producing output aligned with medical standards and professional use.

## Exercise 1: From Prompt Engineering to Context Engineering

**Part A – Prompt Engineering (Baseline)**  
Use a simple prompt to complete the task below:
```
Summarize the following startup idea in three bullet points:

Startup Idea: An AI-powered platform that helps local farmers predict crop diseases using satellite images and weather data.
```

**Part B – Context Engineering (Enhanced)**  
Expand the same task into a **context-engineered input** by adding:  
1. **System Role**  
2. **Reference Material**  
3. **Instruction Layering**  
4. **Output Shaping**  

*Example:*  
```
System Role: You are a venture capital analyst specializing in AgriTech startups.

Reference Context: Farmers face billions in losses annually due to crop diseases. Satellite-based solutions are an emerging trend in precision agriculture.

Task: Summarize the following startup idea. Compare it to typical AgriTech innovations and highlight market potential.

Startup Idea: An AI-powered platform that helps local farmers predict crop diseases using satellite images and weather data.

Output: Provide three bullet points under the headings:
- Value Proposition
- Market Fit
- Investment Potential
```

**Your Task:**  
1. Write your own **context-engineered version** of the baseline prompt.  
2. Compare the two outputs (baseline vs. context-engineered).  
3. Reflect: *What improvements did context engineering bring to the AI’s response?*

## 6.6 Personalized Assistants and Projects: Extending the GenAI Toolkit

Generative AI tools like ChatGPT, Perplexity and Claude provide powerful **general-purpose intelligence**, but professionals often need **domain-specific capabilities**. 
Two recent innovations — **Personalized Assistants** and **Projects** — enable you to move beyond using AI *as-is* and start **building tailored AI solutions**.

### 6.6.1 Personalized Assistants

**What are they?**  
Personalized assistants, such as *Custom GPTs* are personalized versions of foundational models (like GPT-4/5) that you configure with **specific instructions, data, and tools**. 
Think of them as your own AI partner that understands the context of your business.

**When to use them?**  
  - Automating repetitive interactions (e.g., customer support, investor FAQs).  
  - Acting as a *single-purpose agent* — a specialized helper for a narrow domain.  
  - Rapid prototyping of ideas that require direct user interaction.  

**How to create one:**  
1. **Define the role**: What is your model supposed to do (e.g., answer customer questions, analyze investor reports, explain a certain content)?  
2. **Set instructions**: Craft clear system messages and prompt templates. 
3. **Add knowledge**: Upload files, FAQs, or curated datasets to ground the model in your domain.  
4. **Integrate tools**: Connect APIs, code interpreters, or plugins when needed.  

**Strengths**: Always available, consistent tone/persona, easy to scale to many users.  

**Limitations**: Narrow focus, less suitable for managing complex or evolving datasets.  

**Sample Applications:**  
- Customer support assistant tailored to your product.  
- Investor relations bot answering FAQs about your startup.  
- Market research assistant for competitor and trend analysis.  
- Internal knowledge base for onboarding new team members.
- AI Teaching Assistant that explains topics at multiple difficulty levels.  
- Lesson Plan Generator aligned with curriculum standards.  
- Academic Writing Coach that reviews clarity, tone, and citation style.  
- Student Support GPT that answers course-related FAQs using syllabus materials.
- Patient Education Assistant that explains diagnoses and procedures in plain language.  
- Wellness Companion offering lifestyle guidance based on verified sources.

## Exercise 2: Create Your Own Personalized Assistant

**Objective:** Apply the concepts of **Context Engineering** and **Personalized Assistants** by creating a specialized AI assistant trained on a specific dataset.
**Task:** Use the dataset provided below for the **AI Literacy Program Assistant** to create your own personalized assistant.

Download the [Personalized_Assistant_Example](./Data/Personalized_Assistant_Example.pdf). 

Your assistant should be able to answer questions, summarize modules, and guide learners about the AI Literacy Program using the uploaded knowledge base.

**Steps**
1. **Define the Role**
   - Example: “You are a program support assistant for the FGCU AI Literacy course.”
2. **Upload the Knowledge Base**
   - Use the provided dataset titled *AI Literacy Program Assistant Knowledge Base*.
3. **Set Instructions**
   - Describe the assistant’s behavior, tone, and purpose.
   - Example: “Be friendly, informative, and professional. Always connect responses to learning goals.”
4. **Test Your Assistant**
   - Try prompts like:
     - “Summarize what students learn in Module 4.”
     - “Who developed the AI Literacy program?”
     - “What is the difference between Modules 5 and 6?”
5. **Evaluate Context Quality**
   - How does the assistant’s role, tone, and knowledge data affect output accuracy?
   - What improvements would you make to the system message or dataset?

### 6.6.2 Projects

**What are they?**  
Projects are collaborative **AI workspaces** that allow teams to combine **LLM interactions, files, data, and notes** into one structured environment. 
Instead of isolated chats, a Project acts as a **hub of AI-augmented workflows**.

**When to use them?**  
  - Organizing and curating research (market analysis, regulations, competitor benchmarking).  
  - Managing multi-step workflows (e.g., lean canvas, due diligence, product roadmap).  
  - Supporting team collaboration where everyone contributes and refines knowledge.  

**Core Components:**  
- **Knowledge base**: Upload business plans, reports, datasets.  
- **Model interactions**: Ask questions, generate summaries, or perform analysis on the shared material.  
- **Collaboration**: Teams can contribute, track, and refine insights in one place.  

**Strengths**: Structured, persistent, collaborative, source-grounded.

**Limitations**: Less dynamic for real-time interaction with external users; requires careful data curation.

**Sample Applications:**  
- Organizing all research for a business idea (e.g. market trends, competitors, regulations).  
- Running due diligence or compliance reviews.  
- Coordinating product roadmaps and investor pitch material.  
- Managing an MVP’s iterative development with AI assistance.
- Course companion to store syllabus, readings, and assignments to answer student questions and generate study guides.  
- Lesson plan designer that uses uploaded standards or rubrics to create structured lessons and activities.  
- Assessment builder to generate quizzes, rubrics, and feedback forms for instructors.
- Research grant assistant that uses previous proposals to draft new ones aligned with specific funding calls.

### 6.6.3 Personalized Assistants vs. Projects

Both **personalized assistants** (like Custom GPTs, Personas, or Copilots) and **projects** (structured workspaces such as OpenAI Projects, Claude Projects, or Perplexity Spaces) extend the power of foundational models. 
They serve different but complementary purposes.

#### When to Use Each

| Scenario | Use a **Personalized Assistant** | Use a **Project** |
|----------|----------------------------------|-------------------|
| **Customer-facing task** (answering FAQs, onboarding new users) | ✅ Yes | ❌ No |
| **Internal research & knowledge management** | ❌ No | ✅ Yes |
| **Rapid prototyping** (chatbot, idea validator) | ✅ Yes | ❌ No |
| **Team collaboration** (shared notes, multi-doc analysis) | ❌ No | ✅ Yes |
| **Automating repetitive workflows** | ✅ Yes | ❌ No |
| **Organizing documentation** (business model canvas, pitch prep, compliance files) | ❌ No | ✅ Yes |
| **Scaling a specific role** (legal assistant, marketing copywriter, technical explainer) | ✅ Yes | ❌ No |

### Discussion

- Use **Personalized Assistants** when your goal is to **simulate a role or automate a conversation**. They are like *agents you can design*: a customer service rep, an analyst, or even a coach.  
- Use **Projects** when your goal is to **structure knowledge, organize complexity, or collaborate as a team**. They are like a *digital office space* where people and AI work together on shared artifacts.  
- In practice, more sophisticated applications often combine both:  
  - A **Project** to organize market research and design the product.  
  - A **Custom GPT** as the product itself (e.g., a customer-facing assistant powered by that research).  

**Key Insight:** Assistants help you **execute tasks**, while Projects help you **organize work**. Together, they form the backbone of a GenAI-enabled workflow.

### 6.6.4 Similar Resources Across Platforms

The idea of customizing and structuring generative AI is spreading across different ecosystems. 
Below is a **comparative table** (as of October 2025) of how major platforms implement features equivalent to **Personalzied Assistants** and **Projects**:

| Platform / Model        | Equivalent to **Personalized Assistants** | Equivalent to **Projects** (persistent workspaces) | Entrepreneurial Use Cases |
|--------------------------|---------------------------------------------------------|-----------------------------------------------------|----------------------------|
| **OpenAI (ChatGPT)**    | Custom GPTs | Projects – organize chats, files, notes in one hub  | MVP prototyping, research collaboration |
| **Claude.ai (Anthropic)** | Artifacts | Projects – persistent context with files + notes    | Team-based document analysis, compliance reviews |
| **Perplexity.ai**       | No direct equivalent          | Spaces – save, organize, and share research threads | Market/competitor intelligence, curated knowledge bases |
| **xAI Grok**            | No direct equivalent         | Projects – thematic workspaces for structured tasks | Community engagement, startup branding assistants |
| **Google Gemini**       | Gems | Via NotebookLM         | Research + planning inside Google ecosystem |
| **Microsoft Copilot**   | Copilot GPT    | Copilot Pages is a similar feature       | Enterprise workflows, sales/pitch preparation |
| **Meta LLaMA**    | No direct equivalent                 | No direct equivalent | Not applicable |

### 6.6.5 Connecting to Our Course

- In **Prompt Engineering**, we explored generative AI as a tool for creativity and analysis.  
- With **Custom GPTs**, you learn how to **design your own AI-powered assistants**.  
- With **Projects** and their equivalents, you experience how AI can become a **shared workspace**, helping you manage complexity while building your solution.  
- Both features let you test assumptions, gather feedback, and iterate quickly with minimal cost.  

## Exercise 3: Personalized Assistants and Projects 

**Team Exercise**:  
  1. Create a **Personalized Assistant** that supports your startup idea (e.g., a customer FAQ bot or investor Q&A assistant).  
  2. Set up a **Project** (or equivalent) to organize your startup’s research and MVP documents.  
  3. Compare across platforms: What worked best? What were the limitations?  

By mastering these extensions of the GenAI toolkit, you will learn not just to use AI, but to **engineer AI-powered solutions** — a critical step in building innovative startups.

## Reflections

- Responsible use: data privacy, bias, hallucinations, transparency
- Examples of misuse and how to avoid them
- When *not* to use AI or when to rely on human judgment
- What did you learn about AI tools that surprised you?
- Which AI tasks are you most comfortable with?
- What task in your work would you most like to streamline with AI?
- What did you learn about prompt engineering?

## 📘 Further Reading

- *Context Engineering Guide*. https://www.promptingguide.ai/guides/context-engineering-guide
- LangChain (2025). *The rise of "context engineering"*. https://blog.langchain.com/the-rise-of-context-engineering/
- Lewis, P. et al. (2020). *Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks (RAG).* arXiv:2005.11401 https://arxiv.org/abs/2005.11401  
- Wei, J. et al. (2022). *Chain-of-Thought Prompting Elicits Reasoning in Large Language Models.* arXiv:2201.11903 https://arxiv.org/abs/2201.11903  
- Anthropic (2025). *Effective context engineering for AI agents*. https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents
- Dendritic Institute (2025). *AI Literacy Series – Module 6: Context Engineering.* (Slides & video lecture)

