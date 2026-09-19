# ANTI-AI WRITING PATTERNS — English

Reference file for detecting and eliminating AI writing tells in English articles.
Organized by detection priority: vocabulary → structural patterns → stylistic habits.
Source: Wikipedia AI Writing Guide + editorial practice.

> Part of the Writing System bundle. The `edit-humanize-pass-hn` skill reads this file
> at runtime. It can also be used standalone as an editing checklist.

---

## 1. BANNED VOCABULARY

Words that statistically spike in AI-generated text vs human writing.
Zero tolerance in finished articles.

### Tier 1 — Classic AI tells (2023-2024 era, still common)

additionally (starting a sentence), align with, boasts (meaning "has"), bolstered,
comprehensive, crucial, delve, embark, enduring, foster/fostering, game-changer,
garner, genuinely, holistic, honestly, interplay, intricate/intricacies, journey,
landscape (abstract), leverage, meticulous/meticulously, multifaceted, navigate,
nuanced, pivotal, realm, resonate, robust, seamless, straightforward, tapestry
(abstract), testament, underscores, vibrant

### Tier 2 — Subtler AI tells (2025+ era, harder to catch)

emphasizing, encompassing, enhance/enhancing, ensuring, highlight/highlighting
(as emphasis verb), key (as adjective, overused), showcase/showcasing, valuable

### Tier 3 — Significance inflation words

stands as, serves as (replacing "is"), marks a shift, represents, reflects broader,
symbolizing, contributing to the, setting the stage for, shaping the, indelible mark,
deeply rooted, focal point, evolving landscape, enduring legacy

### Audit command (bash)

```bash
for word in "genuinely" "comprehensive" "navigate" "crucial" "pivotal" "landscape" \
"delve" "robust" "holistic" "leverage" "multifaceted" "seamless" "tapestry" \
"testament" "realm" "foster" "embark" "resonate" "nuanced" "intricate" \
"game-changer" "straightforward" "honestly" "underscores" "journey" \
"additionally" "align with" "boasts" "bolstered" "enduring" "enhance" \
"meticulous" "showcase" "vibrant" "interplay" "garner" "emphasizing" \
"encompassing" "ensuring" "highlight" "valuable" "serves as" "stands as" \
"indelible" "focal point"; do
  count=$(grep -oi "$word" "$FILE" | wc -l)
  if [ "$count" -gt 0 ]; then
    echo "[FLAG] '$word' found $count time(s):"
    grep -ni "$word" "$FILE"
  fi
done
```

---

## 2. STRUCTURAL PATTERNS

### 2a. "Serves as" substitution

**What it is:** AI replaces simple copulatives ("is," "are," "has") with inflated
alternatives that sound more "writerly" but actually signal AI.

**Detect:** serves as, stands as, acts as, marks, represents, holds the distinction of

**Bad:**
> Communication serves as the most valuable skill in the AI era.
> This framework stands as a guide for designers navigating change.
> The design system acts as the foundation for agent-generated UI.

**Good:**
> Communication is the most valuable skill in the AI era.
> This framework is a guide for designers in a changing field.
> The design system is the foundation for agent-generated UI.

**Rule:** Say "is" when you mean "is." Direct writing beats inflated writing.

---

### 2b. Trailing -ing phrases (superficial analysis)

**What it is:** AI appends a present participle phrase at the end of sentences to add
fake analytical depth. The -ing phrase adds no real meaning and could be deleted
without losing any information.

**Detect:** sentences ending with ", highlighting...", ", contributing to...",
", emphasizing...", ", showcasing...", ", reflecting...", ", underscoring...",
", ensuring..."

**Bad:**
> The team shipped the feature on time, highlighting the importance of collaboration.
> The startup serves 100K customers, contributing to the growing ecosystem.
> She redesigned the checkout flow, showcasing her deep understanding of user needs.
> The report found a 15% drop in conversion, underscoring the need for better onboarding.

**Good:**
> The team shipped the feature on time.
> The startup serves 100K customers.
> She redesigned the checkout flow based on three months of support ticket analysis.
> The report found a 15% drop in conversion. The onboarding flow was the obvious culprit.

**Rule:** If the -ing phrase could be deleted without losing meaning, delete it.
If the insight matters, give it its own sentence with specific evidence.

---

### 2c. Negative parallelisms ("Not just X, but also Y")

**What it is:** AI frames descriptions as if correcting a misconception the reader
never had. Creates a false sense of nuance.

**Detect:** "not just X, but also Y", "not only X, but Y", "it's not just about X,
it's about Y", "more than just X", "beyond just X"

**Bad:**
> Design is not just about pixels, but about understanding human behavior.
> The role requires not only technical skills, but also strategic thinking.
> This is more than just a tool update. It's a paradigm shift.

**Good:**
> Design is about understanding human behavior.
> The role requires strategic thinking alongside technical skills.
> This tool update changes how designers work.

**Limited use:** max 2 per article for "isn't X. It's Y." and "Not because X, but
because Y" combined. These are acceptable in small doses. But never the full
"not just X, but also Y" construction.

---

### 2d. Rule of three (triplet structures)

**What it is:** AI defaults to lists of exactly three items with identical cadence.
Three adjectives, three phrases, three parallel clauses. Makes writing feel like
it was assembled from a template.

**Detect:** "X, Y, and Z" where X/Y/Z are structurally identical phrases.
"short phrase, short phrase, and short phrase" with matching rhythm.

**Bad:**
> The conference features keynote sessions, panel discussions, and networking opportunities.
> She is known for her creativity, her resilience, and her commitment to excellence.
> This requires critical thinking, strategic vision, and technical literacy.

**Good:**
> The conference runs keynotes and panels, with time built in for meeting people.
> She is known for creative work that survives contact with real constraints.
> This requires critical thinking and enough technical literacy to have the right
  conversations with engineers.

**Limited use:** max 1 per article. Break the rhythm: vary phrase length, use
different structures, or reduce to two items.

---

### 2e. Elegant variation (forced synonym rotation)

**What it is:** AI has a repetition-penalty mechanism that makes it rotate through
synonyms for the same referent. The result feels like a thesaurus exercise.

**Detect:** Same entity called 3+ different names within a passage.

**Bad:**
> Figma launched MCP support. The design tool now lets agents access the canvas.
> The platform's move signals a shift. The application has essentially become
> an operating system for design.

(Figma → the design tool → the platform → the application — four names for one thing)

**Good:**
> Figma launched MCP support. Figma now lets agents access the canvas.
> The move signals a shift. Figma has essentially become an operating system for design.

**Rule:** Repeat the name or use "it." Forced variation is worse than repetition.
Human writers repeat names constantly. AI writers don't.

---

### 2f. "Despite challenges" template

**What it is:** AI concludes sections with a formulaic pattern: acknowledge a challenge,
then immediately reassure the reader that things are fine. Creates a false sense of
balance without any real analysis.

**Detect:** "Despite these challenges," "Despite its [positive adjective]," "While
challenges remain," "Notwithstanding these obstacles," followed by reassurance.

**Bad:**
> Despite these challenges, designers continue to adapt and thrive in the AI era.
> While obstacles remain, the future of the design profession looks promising.
> Despite the disruption, the industry has shown remarkable resilience.

**Good (option 1: address the challenge concretely):**
> The challenge is real: entry-level design hiring dropped 50% since 2019. But the
> designers who survived aren't the ones who fought the change. They're the ones
> who understood what was actually valuable about their work.

**Good (option 2: cut entirely):**
> Just don't write the "despite challenges" paragraph. If you don't have something
> specific to say about the challenge, move on.

**Rule:** Zero tolerance for the template. Either say something specific about the
challenge or don't mention it.

---

### 2g. Vague attributions

**What it is:** AI attributes claims to unnamed authorities to create false credibility.
Strong writing names specific sources or states things as direct observation.

**Detect:** "Experts argue...", "Industry observers note...", "Many professionals
believe...", "Critics suggest...", "Some researchers have found...",
"Studies have shown..." (without naming the study)

**Bad:**
> Experts argue that AI will fundamentally change the design profession.
> Industry observers note a shift toward agentic interfaces.
> Many professionals believe that prompt engineering is overrated.
> Studies have shown that AI-generated designs lack originality.

**Good:**
> The NN/g State of UX 2026 report found that senior roles are recovering faster.
> Natasha Jen called it out directly: design thinking has become a paint-by-numbers kit.
> In ten years of managing design teams, I've watched this gap widen every year.
> Shumailov et al. documented this in Nature in 2024: models trained on their own
  outputs lose variety over time.

**Rule:** Name the source, cite the research, or state it as your own observation.
Never hide behind "experts."

---

## 3. SENTENCE-LEVEL PATTERNS

### 3a. Mechanical parallel repetition

**What it is:** Same sentence structure repeated with slight variations.

**Bad:**
> I could design a checkout flow, but I couldn't design a strategy.
> I could ship a feature, but I couldn't ship a vision.
> I could follow a process, but I couldn't question a process.

**Good:**
> I could design a checkout flow but had no idea how to think about strategy.
> Shipping features was easy. Knowing which features to kill was the hard part.

**Rule:** Zero tolerance. Vary sentence structure.

---

### 3b. Doublet closes

**What it is:** Two short parallel sentences used as a closer. Feels profound.
Actually a template.

**Bad:**
> Always learning. Always adjusting.
> Keep building. Keep questioning.
> Less wireframing. More thinking.

**Good:**
> Some things only humans can teach humans. Design taste is one of them.
> (One complete thought. Specific. Memorable.)

**Rule:** Zero tolerance. Closers must be specific, not formulaic.

---

### 3c. Summary recap lists at closing

**What it is:** AI restates each section's main point as a list at the end.

**Bad:**
> To summarize:
> - Output quality is no longer a differentiator
> - Communication skills serve two audiences
> - Distinctive craft becomes premium
> - Thinking quality matters more than execution speed

**Good:**
> The floor just got automated. The ceiling is where the work is now.
> (Callback to the article's theme. No recap. The reader remembers what mattered.)

**Rule:** Zero tolerance. Close with callback + reframe + short memorable line.

---

### 3d. Meta-narration

**What it is:** AI announces what the article will do instead of doing it.

**Bad:**
> In this article, I will explore how AI is changing design skills.
> Let's examine the three key factors that make this shift important.
> In the following sections, we'll look at why communication matters.

**Good:**
> Last week, Figma opened its canvas to AI agents.
> (Just start. The reader will follow.)

**Rule:** Zero tolerance. Never announce. Just write.

---

### 3e. Generic AI bridge phrases

**What it is:** AI uses formulaic transitions between sections.

**Bad:**
> Life works the same way.
> The same is true for designers.
> Let's now turn our attention to...
> With that in mind, let's explore...
> This brings us to an important point.

**Good:**
> So what happens when the user stops clicking and starts delegating?
> But here's the part most teams haven't figured out yet:
> Here's what this means in practice:

**Rule:** Zero tolerance for generic bridges. Use rhetorical questions or
specific transitions that advance the argument.

---

## 4. AUDIT SUMMARY TABLE

Quick reference for automated and manual checks.

| Category | Check type | Tolerance |
|---|---|---|
| Tier 1 vocabulary (25 words) | Automated grep | 0 |
| Tier 2 vocabulary (8 words) | Automated grep | 0 |
| Tier 3 significance inflation | Manual scan | 0 |
| Em dashes (—) | Automated grep | 0 |
| "Serves as" substitution | Manual scan | 0 |
| Trailing -ing phrases | Manual scan | 0 |
| "Despite challenges" template | Manual scan | 0 |
| Vague attributions | Manual scan | 0 |
| Mechanical parallel repetition | Manual scan | 0 |
| Doublet closes | Manual scan | 0 |
| Summary recap lists | Manual scan | 0 |
| Meta-narration | Automated grep | 0 |
| Generic bridge phrases | Manual scan | 0 |
| "isn't X. It's Y." | Count | max 2 |
| "Not because X, but because Y" | Count | max 2 |
| Triplet structures | Count | max 1 |
| Elegant variation (3+ synonyms) | Manual scan | Flag |
| Italic emphasis in body | Automated grep | 0 |

---

*Part of the Writing System bundle. Built by Hoang Nguyen (@hoangthoughts). Please do not share without permission.*
