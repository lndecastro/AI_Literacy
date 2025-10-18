# Module 8 — Sample Case Studies and Applications of AI

Artificial Intelligence is transforming every sector of society — from education and healthcare to environmental management, business, and the arts.
This module provides **hands-on, ready-to-run case studies** where you can explore data, run code, and design prompts to experience AI-assisted analysis and creation in action.

> All datasets are **synthetic/anonymized** and for **educational use** only.

[⬇️ Download all case-study data (ZIP)](Data/ai_literacy_case_studies.zip)

## Learning Objectives

After completing this module, you will be able to:
- Apply AI tools and prompt engineering techniques to real-world case studies.
- Run data analyses using the provided datasets for education, healthcare, environment, business, and arts.
- Evaluate how prompt design and context affect AI performance.
- Reflect on ethical, social, and environmental implications of AI applications.

## 🧑‍🏫 Case Study 1 — Education: Course Companion & Lesson Plan Review

**Files (in the ZIP):**
- education/syllabus.txt
- education/rubric.txt
- education/lesson_plan.md

### A) Prompt
```
System role: You are an instructional designer for higher education.

Context files you can reference:
- Syllabus (excerpt): [paste the text from syllabus.txt]
- Writing Rubric (excerpt): [paste the text from rubric.txt]

Task:
1) Review the lesson_plan.md (pasted below) against the syllabus goals and the rubric criteria.
2) Summarize the lesson plan in 3 bullet points for students.
3) Produce a table with columns: Strengths | Weaknesses | Improvement Suggestions.
4) Write a 60-word student-facing overview.

Lesson Plan:
[Paste the contents of lesson_plan.md]
```

### B) LLM Analysis — Instructional Design Review

This activity demonstrates how context-aware prompting enables AI to act as an instructional design assistant.

#### Optional Extension Prompts

1. **Role Variation**
   ```
   Now act as a teaching assistant preparing for this class. 
   What materials should be ready, and what questions might students ask?
   ```

2. **Iterative Refinement**
   ```
   Based on your analysis, rewrite the lesson objectives so they align more clearly 
   with the syllabus goals and rubric criteria.
   ```

3. **Reverse Prompting**
   ```
   Analyze the output you just created. What kind of prompt would have generated it? 
   Suggest how changing the phrasing might alter the response.
   ```

#### Reflection
> How did the AI’s interpretation of rubric alignment compare to your own?  
> Which contextual elements (role, tone, or format) most affected the usefulness of the response?

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
[Paste the text from guideline.txt]

Task:
1) Read the following anonymized patient data from patient_records.csv (pasted below).
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
> How did contextualizing the task with the “clinical analyst” role affect the tone and precision of the response?  
> What limitations must remain explicit when using AI in healthcare communication?

---

## 🌿 Case Study 3 — Environment: Water Quality Early Warning

**Files:**
- environment/water_quality.csv

### A) Prompt
```
System role: You are an environmental data analyst.
Goal: Detect anomalies suggestive of potential algal bloom risk.

Task:
1) Review the sample data pasted from water_quality.csv (site, date, chlorophyll_a, temp_c, nitrate_mgL, phosphate_mgL).
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
> What did the AI emphasize as the main risk indicators?  
> How can human experts validate and contextualize these findings before action?

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
> How did the AI’s clustering compare with your intuition as a human analyst?  
> What elements of the prompt (role, structure, or examples) improved the clarity of the output?

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
> How did prompt specificity affect the creativity and coherence of the AI’s output?  
> What aspects of authorship remain uniquely human in AI-assisted storytelling?

---

## Submission & Reflection

- Submit your **prompts**, **AI outputs**, and a **short reflection (150–200 words)** for one or more case studies.  
- Discuss how **prompt and context** shaped your results, and where **human judgment** was most critical.  
- Highlight ethical and practical insights from using LLMs in each domain.

## Reflection

> Which of these case studies feels most relevant to your field or future career?  
> How might you apply similar principles in your own work or research?  
> What challenges or safeguards would you need to ensure responsible AI use?

Reflect on how the lessons from these cases — transparency, context, and collaboration — can guide your personal or organizational approach to AI adoption.

---

## 📘 Further Reading

- World Economic Forum (2024). *Shaping the future of artificial intelligence: Reflections from the AI Governance Alliance.*, https://www.weforum.org/stories/2024/06/ai-governance-alliance-future-of-ai/  
- UNESCO (2023). *Guidelines for AI in Education and Research.*, https://www.unesco.org/en/articles/guidance-generative-ai-education-and-research  
- European University Association (2023). *Artificial Intelligence in Science. Challenges, Opportunities and the Future of Research.*, https://www.eua.eu/news/member-and-partner-news/artificial-intelligence-in-science-challenges-opportunities-and-the-future-of-research.html  
- Mollick, E. & Mollick, L. R. (2024). *Co-Intelligence: Living and Working with AI.*, Portfolio. 
- European Commission (2019). *Ethics Guidelines for Trustworthy AI.*, https://digital-strategy.ec.europa.eu/en/library/ethics-guidelines-trustworthy-ai  
- Dendritic Institute (2025). *AI Literacy Series – Module 8: Sample Case Studies and Applications of AI.* (Slides & video lecture)
