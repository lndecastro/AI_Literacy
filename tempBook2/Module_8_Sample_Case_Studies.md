# Module 8: Sample Case Studies and Applications of AI

Artificial Intelligence is transforming every sector of society — from education and healthcare to environmental management, business, and the arts.
This module provides **hands-on, ready-to-run case studies** where you can explore data, run code, and design prompts to experience AI-assisted analysis and creation in action.

> All datasets are **synthetic/anonymized** and for **educational use** only.

[⬇️ Download all case-study data (ZIP)](../Data/ai_literacy_case_studies.zip)

## Learning Objectives

After completing this module, you will be able to:

- Apply AI tools and prompt engineering techniques to real-world case studies.
- Run data analyses using the provided datasets for education, healthcare, environment, business, and arts.
- Evaluate how prompt design and context affect AI performance.
- Reflect on ethical, social, and environmental implications of AI applications.

## 🧑‍🏫 Case Study 1 — Education: Build an Instructional Design Personalized Assistant

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
4) Rewrite the learning objectives for clarity and alignment.
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

### A) Prompt

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

### B) LLM Analysis — Clinical Data Summary

Use an LLM to simulate the analytical reasoning of a healthcare analyst.

#### Optional Extension Prompts

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
Compare v1 and v2 of the Insights Report. What changed?
```
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

## 🌿 Case Study 3 — Environment: Water Quality Analysis Using a Hybrid PA + Project Approach

**Files:**

- environment/water_quality.csv

### A) Prompt

```
System role: You are an environmental data analyst.
Goal: Detect anomalies suggestive of potential algal bloom risk.

Task:
1) Review the sample data available in the file water_quality.csv (site, date, chlorophyll_a, temp_c, nitrate_mgL, phosphate_mgL).
2) Identify potential outliers or unusual trends based on chlorophyll_a variation by site.
3) Describe a simple rule-based approach (e.g., z-scores or thresholds) to flag anomalies.
4) Draft a concise management report: Summary | Sites of Interest | Recommended Next Checks.
```

### B) LLM Analysis — Environmental Data Review

Let the LLM interpret and describe the data qualitatively.

#### Optional Extension Prompts

1. **Policy Translation**

   ```
   Rewrite your management report for a non-technical audience, such as community stakeholders.
   Emphasize environmental impact and recommended preventive actions.
   ```

2. **Predictive Reasoning**

   ```
   Based on observed patterns, hypothesize environmental factors that might explain chlorophyll spikes.
   ```

3. **Visual Design Guidance**
   ```
   Suggest three types of visualizations that would best communicate this data to policymakers.
   ```

#### Reflection

> 1. What did the AI emphasize as the main risk indicators?  
> 2. How can human experts validate and contextualize these findings before action?

---

## 💼 Case Study 4 — Business: Customer Feedback Insights

**Files:**

- business/customer_feedback.csv

### A) Prompt

```
System role: You are a customer insights analyst.

Task:
1) I will paste a sample of customer_feedback.csv (product, feedback).
2) Cluster feedback into 3–5 themes with short labels.
3) Produce a table: Theme | Representative Quote | Suggested Action.
4) Write a 100-word executive summary describing key takeaways.
```

### B) LLM Analysis — Customer Insights Report

Use the LLM to generate structured market insights and practice clarity in summarization.

#### Optional Extension Prompts

1. **Sentiment Analysis**

   ```
   Classify each feedback item as Positive, Neutral, or Negative.
   Provide a summary table showing distribution by product.
   ```

2. **Persona Creation**

   ```
   Based on the themes identified, draft short user personas (e.g., "Budget-Conscious Buyer", "Tech Enthusiast")
   that reflect these segments.
   ```

3. **Strategic Recommendation**
   ```
   Summarize your insights into three actionable business recommendations.
   ```

#### Reflection

> 1. How did the AI’s clustering compare with your intuition as a human analyst?  
> 2. What elements of the prompt (role, structure, or examples) improved the clarity of the output?

---

## 🎨 Case Study 5 — Arts: Story Seeds to Short Scene

**Files:**

- arts/story_seeds.csv

### A) Prompt

```
System role: You are a creative writing coach.

Task:
1) Here are story seeds (character, trait, goal) from a CSV.
2) Pick one seed and outline a scene (setting, conflict, turning point, resolution beat) in ~120 words.
3) Keep tone grounded and sensory-rich.
4) End with two "next-scene" options for narrative continuation.
```

### B) LLM Analysis — Creative Generation Exercise

Use the LLM to develop a narrative scene and then reflect on tone, emotion, and voice.

#### Optional Extension Prompts

1. **Perspective Shift**

   ```
   Rewrite the same scene from a different character’s point of view.
   ```

2. **Style Transfer**

   ```
   Adapt the scene to a new literary style (e.g., mystery, sci-fi, historical fiction).
   ```

3. **Multimodal Prompt**
   ```
   Suggest an image prompt that visually represents the key moment in your story.
   ```

#### Reflection

> 1. How did prompt specificity affect the creativity and coherence of the AI’s output?  
> 2. What aspects of authorship remain uniquely human in AI-assisted storytelling?

---

## Submission & Reflection

- Submit your **prompts**, **AI outputs**, and a **short reflection (150–200 words)** for one or more case studies.
- Discuss how **prompt and context** shaped your results, and where **human judgment** was most critical.
- Highlight ethical and practical insights from using LLMs in each domain.

## Reflection

> 1. Which of these case studies feels most relevant to your field or future career?  
> 2. How might you apply similar principles in your own work or research?  
> 3. What challenges or safeguards would you need to ensure responsible AI use?

Reflect on how the lessons from these cases — transparency, context, and collaboration — can guide your personal or organizational approach to AI adoption.

---

## 📘 Further Reading

- World Economic Forum (2024). _Shaping the future of artificial intelligence: Reflections from the AI Governance Alliance._, https://www.weforum.org/stories/2024/06/ai-governance-alliance-future-of-ai/
- UNESCO (2023). _Guidelines for AI in Education and Research._, https://www.unesco.org/en/articles/guidance-generative-ai-education-and-research
- European University Association (2023). _Artificial Intelligence in Science. Challenges, Opportunities and the Future of Research._, https://www.eua.eu/news/member-and-partner-news/artificial-intelligence-in-science-challenges-opportunities-and-the-future-of-research.html
- Mollick, E. & Mollick, L. R. (2024). _Co-Intelligence: Living and Working with AI._, Portfolio.
- European Commission (2019). _Ethics Guidelines for Trustworthy AI._, https://digital-strategy.ec.europa.eu/en/library/ethics-guidelines-trustworthy-ai
- Dendritic Institute (2025). _AI Literacy Series – Module 8: Sample Case Studies and Applications of AI._ (Slides & video lecture)
