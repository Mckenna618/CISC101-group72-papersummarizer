### **Module 3: Guardrails Module**
- Detect missing/empty/<50-word sections.
- Enforce anti-hallucination rules.
- Apply source-faithfulness constraints (summaries must reflect actual text).
- Use a long-text chunking strategy for scalability.


evidence = "strict"

\\(These are anti-hallucination rules)
IF evidence = "strict":
    - The summarizer may ONLY include information directly found in the provided text.
    - No external inference, no embellishment, no assumed facts.
    - If the section does not provide enough detail, output:
      “The source text does not provide enough detail to summarize this section with strict evidence.”

IF a section has:
    - no text, or fewer than 50 words:
        Output one of the following standardized warnings:
        “Section skipped: no text was provided.”
        “Section too short: summary may be incomplete.”
