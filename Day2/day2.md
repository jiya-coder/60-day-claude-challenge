## Day 2 — Prompt Engineering

### What I worked on
Today I explored how prompt structure changes the quality of Claude's output. I ran the same general topic — "explain prompt engineering" — through two very different prompts to see the difference for myself, instead of just reading about it.

### Prompts I entered

**Prompt 1 (basic):**
```
Create an image explaining Prompt Engineering
```

**Prompt 2 (engineered):**
```
You are an AI educator teaching complete beginners.
Explain Prompt Engineering in simple language.
Include:
- What Prompt Engineering is
- Why it matters when using AI tools like Claude
- One example of a weak prompt
- One example of an improved prompt
- Three practical benefits of writing better prompts
Also create a LinkedIn-ready image concept.
Image Requirements:
- Square LinkedIn post (1080x1080)
- Claude-inspired brown, beige and cream colors
- Professional and minimal design
- Main title: "Prompt Engineering"
- Show a visual comparison: Weak Prompt -> Basic Output, Engineered Prompt -> Better Output
- Modern AI and productivity-themed visuals
Output Format:
Section 1: Explanation
Section 2: Weak vs Improved Prompt Example
Section 3: Detailed Image Generation Prompt
```

### Comparing the two outputs

| | Prompt 1 (basic) | Prompt 2 (engineered) |
|---|---|---|
| **Explanation quality** | None — went straight to a visual with no written explanation | Full beginner-friendly breakdown: definition, why it matters, benefits |
| **Structure** | Single diagram, no sections | Clearly labeled Section 1 / 2 / 3, easy to scan and reuse |
| **Examples** | None given | Concrete weak prompt and improved prompt, with reasoning for why each works or fails |
| **Image design** | Generic SVG diagram, Claude's own default style and colors | Fully specified image brief — exact dimensions, brand colors, layout, typography, mood — ready to hand to an image generator |
| **Reusability** | One-off visual, not directly reusable elsewhere | Output is copy-paste ready for a LinkedIn post and an image-gen tool |

### Key learnings
- **Vague prompts get vague results.** Prompt 1 only said "create an image" — Claude had to guess the explanation, the structure, even whether an explanation was wanted at all. It defaulted to a single diagram.
- **Specifying format and sections forces organized output.** Asking for "Section 1 / 2 / 3" in Prompt 2 made the response easy to scan and directly usable, instead of one long block of text.
- **Giving constraints (colors, dimensions, tone, audience) removes guesswork.** The image brief in Prompt 2 was detailed enough to hand directly to a designer or AI image tool with no follow-up questions needed.
- **Asking for examples inside the prompt produces examples in the output.** Prompt 2 explicitly asked for "one weak prompt" and "one improved prompt" — and got exactly that, paired with reasoning, which Prompt 1 never produced because it was never asked for.
- **The biggest lesson: structure your ask the way you want the answer structured.** The output format mirrors the input format almost exactly.
