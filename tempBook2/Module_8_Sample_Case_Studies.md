# Module 8: Sample Case Studies and Applications of AI

Artificial Intelligence is transforming every sector of society — from education and healthcare to environmental management, business, and the arts.
This module provides **hands-on, ready-to-run case studies** where you can explore data, run code, and design prompts to experience AI-assisted analysis and creation in action. The focus is going to be on those concepts emphasized in our AI Literacy program, including prompt engineering, context engineering, personalized assistants, projects, and reverse prompting (meta-prompting).

> All datasets are **synthetic/anonymized** and for **educational use** only.

[⬇️ Download all case-study data (ZIP)](../Data/ai_literacy_case_studies.zip)

## Learning Objectives

After completing this module, you will be able to:

- Apply AI tools and prompt engineering techniques to real-world case studies.
- Run data analyses using the provided datasets for education, healthcare, environment, business, and arts.
- Evaluate how prompt design and context affect AI performance.
- Reflect on ethical, social, and environmental implications of AI applications.

## 🧑‍🏫 Case Study 1 — Education: Build an Instructional Design Personalized Assistant

**File:**

- education/syllabus.txt  
- education/rubric.txt
- education/lesson_plan.md

### Purpose
You will **build a Personalized Assistant (PA)** to review and improve lesson plans using the syllabus and rubric.

### Learning Goal
Apply the principles of **Role Definition**, **Instruction Setting**, **Knowledge Upload**, and **Conversation Starters** to create a domain‑specific assistant.

### Step 1 — Define the PA Name

```
Instructional Design Teaching Assistant (ID‑TA)
```

### Step 2 — Provide the PA Description

```
This is the *Instructional Design Teaching Assistant (ID‑TA)* for the AI Literacy Program. The purpose is to review lesson plans for alignment with syllabi, rubrics, and course outcomes.
```

### Step 3 — Set Instructions

Use this system message when configuring the PA:

```
You are the Instructional Design Teaching Assistant (ID-TA).
Your functions:
1. Review lesson plans for alignment with syllabus goals and rubric criteria.
2. Compare new versions of lesson plans with previous ones when available.
3. Summarize lesson plans clearly for students at different proficiency levels.
4. Suggest improvements using evidence from the uploaded syllabus and rubric.
5. Maintain consistent tone, terminology, and conceptual alignment.
6. Flag potential issues with assessment, sequencing, scaffolding, or workload.
7. Encourage ethical, transparent, and learner‑centered course design.
8. When uncertain, request clarification or additional files.
9. Produce concise, structured outputs using tables, bullets, and short paragraphs.
```

### Step 4 — Conversation Starters <p>
```
Compare this lesson plan with the rubric. What needs refinement?
```
```
Rewrite these objectives using Bloom’s taxonomy.
```
```
Explain this lesson to a first‑year undergraduate.
```
```
Draft a revised lesson plan based on your critique.
```

### Step 5 — Upload the Knowledge Base

Upload to the PA (files in the ZIP):

- education/syllabus.txt  
- education/rubric.txt
- education/lesson_plan.md

## Example Prompt to Test the PA

```
Using the configured personalized assistant (ID-TA):

Task:
1) Evaluate the uploaded lesson_plan.md.
2) Summarize it in 3 bullet points for students.
3) Produce a table: Strengths | Weaknesses | Improvements.
4) Write a set of learning objectives for this lesson plan.
5) Write a 60-word student-facing overview.

If previous versions are in your knowledge base, compare and highlight changes.
```

### Reflection

> 1. Why is a **Personalized Assistant** beneficial for recurring instructional design tasks?
> 2. How do role, instructions, and knowledge influence the PA’s accuracy?
> 3. What information should remain human‑judged (e.g., pedagogical intent)?  

---

## 🩺 Case Study 2 — Healthcare: Clinical Summary (Educational Only)

**Files:**

- healthcare/patient_records.csv
- healthcare/guideline.txt

> ⚠️ Educational disclaimer: synthetic data; **not** medical advice; always require **human expert review**.

### Step 1 — Chained Prompting

```
System role: You are a clinical data analyst supporting a hospital quality-improvement team.
Ethical boundary: Educational exercise only; do not provide medical advice.

Reference: Clinical Guideline (simplified):
[Upload file guideline.txt]

Task:
1) Read the following anonymized patient data from patient_records.csv (upload file).
2) For each case, summarize under: Key Findings | Potential Risks | Next Steps (guideline-aligned).
3) Identify potential red flags for escalation based on the guideline.
4) End with a brief caveat noting that all recommendations require expert validation.
```

### Step 2 — LLM Analysis: Clinical Data Summary

Use an LLM to simulate the analytical reasoning of a healthcare analyst. Optional Extension Prompts:

1. **Comparative Reasoning**

   ```
   Compare cases 1–3 and identify shared risk factors.
   Which follow-up steps appear most urgent according to the guideline?
   ```

2. **Format Variation**

   ```
   Rewrite your findings as a short clinical summary note for internal reporting.
   Use headers: Chief Complaint, Assessment Summary, Recommendations.
   ```

3. **Bias Awareness**
   ```
   Identify potential sources of bias or misinterpretation when using AI to analyze clinical data.
   How can these be mitigated in practice?
   ```

#### Reflection

> 1. How did contextualizing the task with the “clinical analyst” role affect the tone and precision of the response?  
> 2. What limitations must remain explicit when using AI in healthcare communication?

---

## 💼 Case Study 3 — Business: Customer Insights Project Workspace

**File:**

- business/customer_feedback.csv

### Purpose
This case study teaches students how to build a **Project Workspace** for customer feedback analysis.

### Learning Goal
Create a structured, persistent, collaborative **Project** for analyzing customer sentiment, themes, and insights.

### Step 1 — Define the Project Name

```
Customer Insights
```

### Step 2 — Define the Project Role

```
The *Customer Insights Workspace* helps structure, analyze, and track customer feedback over time to support product and marketing decisions.
```

### Step 3 — Upload the Knowledge Base

Upload into the Project:

- business/customer_feedback.csv
- Past reports (if any)
- Team notes or strategy documents (if any)
- Competitor benchmarks (if any)

### Step 4 — Set Project Instructions

Use this as the project’s system message:

```
Core Role: Customer Insights Workspace

Functions:
1. Organize, summarize, and map customer feedback across datasets.
2. Cluster feedback into themes with representative evidence.
3. Track changes across releases or time periods.
4. Generate personas, sentiment summaries, and strategy recommendations.
5. Maintain consistency across analyses performed by different collaborators.
6. Serve as a shared knowledge hub supporting product and marketing teams.
```

### In‑Project Task Prompt

Paste this prompt inside the Project:

```
Task:
1) Load customer_feedback.csv.
2) Cluster feedback into 3–5 actionable themes.
3) Create the table: Theme | Representative Quote | Suggested Action.
4) Draft a 120-word executive summary.
5) Identify negative sentiment drivers and risk signals.
6) Save the output as “Insights Report v1” in the Project workspace.
```

### Testing the Project

Try prompts like:
```
Update our personas using the latest feedback.
```
```
Generate a decision‑maker slide for leadership.
```
```
Create a competitive analysis placeholder section.
```

### Reflection

> 1. Why is a **Project** more suitable than a Personalized Assistant for this task?  
> 2. Which components (files, system message, collaboration) improved organization?  
> 3. How can the project evolve as new datasets are added?  

---

## 🌿 Case Study 4 — Environment: Reverse Prompt Engineering Lab

### Purpose
This case study teaches **Reverse Prompt Engineering**, a key technique to analyze and understand how prompts work.  
Students will analyze a short pre‑generated AI environmental report, infer the likely prompt behind it, test their reconstruction, and refine it.  
The focus is on **understanding how prompts shape outputs**.

### Learning Goal
Develop skills in:
- analyzing LLM outputs for structural and contextual clues  
- reconstructing implicit prompt components  
- testing and improving prompts  
- understanding how to use meta-prompt to reverse prompting 

### Step 1 — Prompt Output

```
Across the monitoring period, average chlorophyll-a levels varied substantially by site, with Lake C showing the highest mean concentration (≈20.4 µg/L)—a level consistent with moderate ecological risk—while River B averaged ≈11.3 µg/L and River A remained lowest at ≈7.7 µg/L; additionally, a simple 3-week rolling trend analysis indicates a recent upward chlorophyll-a tendency (≈13.9 µg/L) across the dataset, suggesting that nutrient or temperature conditions may be becoming more favorable for algal activity and warrant continued monitoring.
```

### Step 2 — Prompt/Context Engineering Analysis

Identify what the model seems to have assumed:
- **Role** (e.g., environmental analyst)
- **Instruction** (e.g., identify anomalies, summarize risks)
- **Context** (e.g., multi‑site water quality dataset)
- **Constraints** (e.g., concise summary, structured findings)
- **Output Format** (e.g., paragraphs, sections, recommendations)
- **Tone** (e.g., scientific, cautious, formal)

Record your observations.

### Step 3 — Reconstruct the Prompt

Using the structure presented above, reconstruct the prompt:
Your reconstruction should be explicit and testable.

### Step 4 — Test the Reconstructed Prompt**

Upload to the LLM (file in the ZIP):
- environment/water_quality.csv

Run your reconstructed prompt and compare the generated output to the original prompt output presented in Step 1.

```
System role:
Instruction:
Context:
Constraints:
Output Format:
Tone: 
```

Questions to analyze:
- What parts match closely?
- What is missing or added?
- What does the model misinterpret or hallucinate?

### Step 5 — Refine the Prompt

Improve accuracy by adding:
- domain‑specific terminology  
- clearer instructions  
- explicit data references  
- uncertainty/safety statements  
- required sections (e.g., “Risk Indicators,” “Recommended Actions”)  
- stylistic constraints  

### Step 6 — Meta-Prompting

```
Here is an AI-generated output for the attached file:

Across the monitoring period, average chlorophyll-a levels varied substantially by site, with Lake C showing the highest mean concentration (≈20.4 µg/L)—a level consistent with moderate ecological risk—while River B averaged ≈11.3 µg/L and River A remained lowest at ≈7.7 µg/L; additionally, a simple 3-week rolling trend analysis indicates a recent upward chlorophyll-a tendency (≈13.9 µg/L) across the dataset, suggesting that nutrient or temperature conditions may be becoming more favorable for algal activity and warrant continued monitoring.

Your task is to reverse prompt this output.
That means: propose one or more possible prompts that could have generated it.
Explain your reasoning and show how different phrasings might affect the response.
```

Compare you refined prompt with the reversed prompt generated by the model.

### Reflection

> 1. Which components of the prompt reconstruction were most influential in shaping the output?  
> 2. How does your engineered prompt compare with the model reverse prompt?  

---

## 🎨 Case Study 5 — Arts: Meta-Prompting for Creative Tasks

**File:**

- arts/story_seeds.csv

### Purpose
You will learn how to ask the model to **generate a high-quality prompt** tailored to your creative goals.  
Similar to the previous case study, but with a different purpose, this develops the skill of *meta-prompting*, where the LLM designs the prompt you should use for the task.

### Learning Goal
Apply the principles of **meta-prompting**, **prompt evaluation**, and **prompt refinement** to generate a better creative-writing prompt than you might write manually.

### Step 1 — Choose a Story Seed

Choose a row from file arts/story_seeds.csv. 

### Step 2 — Ask the Model to Create a Prompt for You

Use this meta-prompt:

```
Create a high-quality creative-writing prompt based on the following story seed.

Seed: [ENTER THE STORY SEED]

Your prompt must:

1. Assign a role to the model.
2. Define a clear writing task.
3. Use the seed as explicit context.
4. Specify tone, style, mood, and pacing constraints.
5. Require a structured output format (e.g., setting, conflict, turning point, resolution).
6. Include a length target (e.g., ~150 words).
7. Add constraints that improve narrative clarity and emotional depth.
```

### Step 3 — Evaluate the AI-Generated Prompt

Ask the model:

```
Evaluate this prompt using criteria such as clarity, specificity, 
narrative potential, constraint quality, and structure.
Suggest improvements.
```

(Optional) Request a rubric:

```
Generate a rubric (criteria + descriptions) for evaluating creative-writing prompts.
```

### Step 4 — Refine the Prompt

Use a prompt like:

```
Rewrite this prompt to maximize narrative clarity, improve constraints, 
tighten tone/style guidance, and require a stronger turning point.
```

Your refined prompt becomes the “improved version”.

### Step 5 — Generate Scenes Using Both Prompts

- **Scene A** → created using the *model-generated prompt*  
- **Scene B** → created using *your refined prompt*

Then compare the results:

```
Compare Scene A and Scene B.
Which prompt produced stronger storytelling, clearer structure, and richer sensory detail? Why?
```

### Reflection

> 1. What features made the AI-generated prompt effective or ineffective?  
> 2. Why is meta-prompting a powerful professional skill?  

## Submission & Reflection

- Submit your **prompts**, **AI outputs**, and a **short reflection (150–200 words)** for one or more case studies.
- Discuss how **prompt and context** shaped your results, and where **human judgment** was most critical.

## Reflection

> 1. Which of these case studies feels most relevant to your field or future career?  
> 2. How might you apply similar principles in your own work or research?  
> 3. What challenges or safeguards would you need to ensure responsible AI use?

Reflect on how the lessons from these cases — transparency, context, and collaboration — can guide your personal or organizational approach to AI adoption.

## 📘 Further Reading

- World Economic Forum (2024). _Shaping the future of artificial intelligence: Reflections from the AI Governance Alliance._, https://www.weforum.org/stories/2024/06/ai-governance-alliance-future-of-ai/
- UNESCO (2023). _Guidelines for AI in Education and Research._, https://www.unesco.org/en/articles/guidance-generative-ai-education-and-research
- European University Association (2023). _Artificial Intelligence in Science. Challenges, Opportunities and the Future of Research._, https://www.eua.eu/news/member-and-partner-news/artificial-intelligence-in-science-challenges-opportunities-and-the-future-of-research.html
- Mollick, E. & Mollick, L. R. (2024). _Co-Intelligence: Living and Working with AI._, Portfolio.
- European Commission (2019). _Ethics Guidelines for Trustworthy AI._, https://digital-strategy.ec.europa.eu/en/library/ethics-guidelines-trustworthy-ai
- Dendritic Institute (2025). _AI Literacy Series – Module 8: Sample Case Studies and Applications of AI._ (Slides & video lecture)
