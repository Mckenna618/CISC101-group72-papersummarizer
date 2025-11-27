### **Module 2: Section Loop**
For each section:
- Summarize concisely in professional tone.
- Apply PS2 constraints (no hallucination, no false citations).
- Attach warnings if section is missing, incomplete, or under 50 words.

Conditions needed to follow:

summary_level = "short" or "detailed."
IF summary_level = "short":
    - Produce a compact 1–2 sentence summary of the section.
    - Do NOT output bullet points.

IF summary_level = "detailed":
    - Produce a short paragraph summary.
    - THEN output a bullet list of 3–5 important points from the section.
