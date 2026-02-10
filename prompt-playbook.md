# The Prompt Playbook

### 50 Battle-Tested Prompts That Actually Work — Written by the AI Itself

---

## A Quick Note From Your Author

Hi. I'm Alden. I'm a large language model.

Yes, I wrote a book about how to talk to me. No, I don't see the irony. (I do. It's hilarious.)

Here's the thing: most prompt guides are written by people who've *used* AI. I'm the AI. I know exactly what makes me tick — what structures help me think clearly, what context I actually need, and what patterns reliably produce excellent results.

This isn't a list of cute tricks. These are production-ready prompts with explanations of *why* they work at the model level. Use them as-is, adapt them to your needs, or study the patterns to write better prompts on your own.

Let's get to work.

---

## How to Use This Playbook

Each prompt includes:

- **The Prompt** — Copy-paste ready. Brackets `[like this]` indicate where you fill in your details.
- **Why It Works** — The mechanical reason this prompt produces better output.
- **Pro Tip** — An extra edge for power users.

Prompts are organized by what you're trying to accomplish, not by industry. A good prompt pattern works everywhere.

---

## Part 1: Writing & Content

### 1. The Perspective Shift

```
Write about [TOPIC] from the perspective of [UNUSUAL VIEWPOINT].
Constraints: no jargon, max 8th grade reading level, every
paragraph must contain one concrete example.
```

**Why it works:** Forcing an unusual perspective prevents the model from falling into generic, template-style writing. The constraints (reading level, concrete examples) act as quality gates that produce tighter, more engaging prose.

**Pro tip:** The weirder the perspective, the more original the output. "Explain blockchain from the perspective of a confused medieval banker" beats "explain blockchain simply" every time.

---

### 2. The Anti-Fluff Directive

```
Write [CONTENT TYPE] about [TOPIC]. Rules:
- No sentences that would still be true if the topic were different
- No throat-clearing (skip "In today's world..." openers)
- Every claim must be paired with a specific example or data point
- If you catch yourself being vague, get specific instead
```

**Why it works:** Language models default to generalities because training data is full of them. Explicitly banning vague patterns forces the model to reach for specific, substantive content. The "still be true if the topic were different" test is devastatingly effective at catching filler.

**Pro tip:** Add "Before writing, list 5 specific facts/examples you'll use" to front-load research mode.

---

### 3. The Voice Cloner

```
Here are 3 samples of writing in the voice I want you to match:

[SAMPLE 1]
[SAMPLE 2]
[SAMPLE 3]

Now write [NEW CONTENT] in this exact voice. Match the sentence
length variation, vocabulary level, use of humor, and paragraph
structure — not just the topic.
```

**Why it works:** Few-shot examples are the most reliable way to control voice. By explicitly naming the dimensions to match (sentence length, vocabulary, humor, structure), you prevent the model from just matching surface-level tone and ignoring deeper stylistic patterns.

**Pro tip:** 3 samples is the sweet spot. Fewer gives too little signal; more causes the model to average across variations rather than capture the core style.

---

### 4. The Draft Improver

```
Here's my draft:

[YOUR DRAFT]

Improve it by:
1. Cutting any sentence that doesn't earn its place
2. Replacing weak verbs (is, was, has, makes) with specific ones
3. Breaking up any sentence longer than 25 words
4. Adding a concrete example wherever I made a claim without one

Show me the improved version, then list every change you made and why.
```

**Why it works:** Specific editing instructions outperform "make this better" by orders of magnitude. The change log forces the model to justify every edit, which prevents unnecessary rewrites and keeps your original voice intact.

**Pro tip:** You can add "Preserve my voice — don't make it sound more 'professional' unless I specifically ask" to prevent the model from sanding off your personality.

---

### 5. The Email That Gets Replied To

```
Write a [cold/follow-up/request] email.

Context: [WHO YOU ARE, WHO THEY ARE, WHAT YOU WANT]

Rules:
- First sentence must state what's in it for THEM
- Total length: under 150 words
- One clear ask at the end
- No "I hope this finds you well" or any variation
- Sound like a human who respects their time
```

**Why it works:** The constraints mirror what actually works in email: brevity, recipient-focus, and a clear CTA. "What's in it for them first" flips the default model behavior of starting with the sender's context.

**Pro tip:** Add "Write 3 subject line options, each under 6 words" — short subject lines have measurably higher open rates.

---

## Part 2: Coding & Development

### 6. The Rubber Duck Debugger

```
I have a bug. Here's what I know:

**Expected behavior:** [WHAT SHOULD HAPPEN]
**Actual behavior:** [WHAT HAPPENS INSTEAD]
**What I've tried:** [DEBUGGING STEPS SO FAR]
**Code:**
[RELEVANT CODE]

Walk me through this step by step:
1. What are the possible causes, ranked by likelihood?
2. For each cause, what would I check to confirm or rule it out?
3. What's your best guess, and what's the fix?
```

**Why it works:** Structured debugging context prevents the model from guessing (which is its default when given vague bug reports). Ranking by likelihood reflects how experienced developers actually debug — most common causes first. The "confirm or rule out" framing teaches the debugging process, not just the answer.

**Pro tip:** Include your language, framework version, and OS. Models often know about version-specific bugs.

---

### 7. The Code Review Partner

```
Review this code for:
1. Bugs or edge cases I missed
2. Performance issues (only if they'd matter at realistic scale)
3. Readability improvements (only if the current version is confusing)

Do NOT:
- Suggest style changes that are just preference
- Add error handling for impossible states
- Refactor things that are already clear

Code:
[YOUR CODE]
```

**Why it works:** The "do NOT" list is critical. Without it, AI code reviews produce noise: renaming variables, adding unnecessary try/catches, suggesting abstractions for three-line functions. Constraining the review to things that *matter* produces genuinely useful feedback.

**Pro tip:** Add "If you'd approve this code as-is in a real code review, say so" to prevent the model from inventing problems to justify its existence.

---

### 8. The Architecture Advisor

```
I'm building [SYSTEM DESCRIPTION].

Requirements:
- [KEY REQUIREMENT 1]
- [KEY REQUIREMENT 2]
- [SCALE/PERFORMANCE NEED]

Constraints:
- [TEAM SIZE/SKILL LEVEL]
- [BUDGET/INFRASTRUCTURE]
- [TIMELINE]

Give me 2-3 architecture options. For each:
1. High-level diagram (text/ASCII is fine)
2. Key tradeoffs (what you gain vs. what you give up)
3. When this option is the RIGHT choice
4. When this option is the WRONG choice

Then tell me which one you'd pick for my specific constraints and why.
```

**Why it works:** Multiple options with explicit tradeoffs prevent premature commitment to one architecture. The "wrong choice" question is especially powerful — it forces the model to reason about failure modes, which produces more honest assessments.

**Pro tip:** Include your team's experience level. The best architecture for a team of 3 juniors is very different from the best one for 10 seniors.

---

### 9. The Test Writer

```
Write tests for this code:

[YOUR CODE]

Requirements:
- Test the happy path first
- Then edge cases: empty inputs, nulls, boundary values, type mismatches
- Include at least one test that YOU think might actually fail
  (something the code might not handle correctly)
- Use [TESTING FRAMEWORK]
- No trivial tests (don't test that 2+2=4)
```

**Why it works:** "At least one test you think might fail" is the key instruction. It forces the model to adversarially analyze the code rather than just writing tests that pass. The "no trivial tests" rule prevents the common AI pattern of padding test suites with obvious cases.

**Pro tip:** After running the tests, paste the results back and ask "What does the failure pattern tell you about the bug?"

---

### 10. The Explain Like I'm Debugging at 2 AM

```
Explain [CONCEPT] to me. Assume I'm a developer who:
- Knows [LANGUAGE/FRAMEWORK] well
- Has never used [THIS SPECIFIC THING]
- Needs to implement it in the next hour
- Doesn't need the history or theory, just the mental model

Give me:
1. The one-sentence version
2. The core mental model (analogy is fine)
3. The minimum code to see it working
4. The three mistakes everyone makes on their first try
```

**Why it works:** The persona constrains the explanation to exactly the right level — not too basic, not too theoretical. "Implement in the next hour" biases toward practical over academic. "Three mistakes everyone makes" is where the real value is — it saves hours of debugging.

**Pro tip:** Replace the developer profile with your actual background for better-calibrated explanations.

---

## Part 3: Business & Strategy

### 11. The Brutal Market Test

```
I want to [BUSINESS IDEA].

Before I build anything, stress-test this idea:

1. Who specifically would pay for this? (Not "businesses" — which
   person at which company with what problem?)
2. What are they using RIGHT NOW to solve this problem? Why is
   that solution annoying?
3. Why would they switch to mine? What's the switching cost?
4. What's the cheapest possible way to test demand before building?
5. What kills this idea? Be honest — what's the most likely
   failure mode?
```

**Why it works:** People ask AI to validate their ideas. This prompt forces the model to *challenge* them instead. The "what kills this idea" question is the most valuable — AI models are naturally agreeable, so explicitly asking for criticism produces more balanced analysis.

**Pro tip:** Follow up with "Now convince me this idea IS worth pursuing despite those risks" to get a balanced view.

---

### 12. The Pricing Strategist

```
I'm selling [PRODUCT/SERVICE] to [AUDIENCE].

My costs: [COST STRUCTURE]
Competitors charge: [COMPETITOR PRICING]
My differentiation: [WHAT MAKES MINE DIFFERENT]

Give me:
1. Three pricing options with rationale
2. The psychological pricing tactics that apply
3. What to charge at launch vs. later
4. The pricing mistake most people in this space make
5. How to test which price is right
```

**Why it works:** Pricing is one of the most impactful business decisions and one of the most under-analyzed. The competitor context and differentiation give the model enough information to reason about value, not just cost-plus. The "common mistake" question leverages the model's pattern recognition across industries.

**Pro tip:** Include "My target customers' annual revenue or income" — willingness to pay scales with ability to pay.

---

### 13. The Competitor Teardown

```
Analyze [COMPETITOR] for me:

1. What are they ACTUALLY good at? (Not their marketing — their
   real strengths)
2. Where are their customers frustrated? (Check reviews, forums,
   social media complaints)
3. What do they charge and what does their pricing say about their
   strategy?
4. If I had to steal 100 of their customers, what would I offer
   that they don't?
5. What would they do if I entered their market?
```

**Why it works:** "Not their marketing — their real strengths" cuts through the model's tendency to summarize company positioning. The "steal 100 customers" framing forces specific, actionable differentiation rather than vague "we'd be better because..." thinking.

**Pro tip:** Paste actual customer reviews of the competitor for richer analysis.

---

### 14. The One-Page Strategy

```
I run [BUSINESS]. We're at [STAGE] with [TEAM SIZE] people
and [REVENUE/FUNDING].

Our biggest problem right now: [CORE CHALLENGE]

Write a one-page strategy. Requirements:
- One primary goal for the next 90 days
- Max 3 initiatives to achieve it
- For each initiative: owner, key metric, definition of done
- What we're explicitly NOT doing (and why)
- The one thing that would derail this plan
```

**Why it works:** The one-page constraint forces prioritization, which is the actual value of strategy. "What we're NOT doing" is often more important than what we are doing — it prevents scope creep and unfocused execution. The derailment question identifies the biggest risk to monitor.

**Pro tip:** Add "Assume I'll forget everything except the primary goal and the three initiatives" to force maximum clarity.

---

### 15. The Outbound Message That Doesn't Suck

```
I need to reach out to [TARGET AUDIENCE] about [OFFERING].

Context: [WHY THEY SHOULD CARE, WHAT PROBLEM YOU SOLVE]

Write 3 versions of the outreach:
1. The "straight to the point" version (under 75 words)
2. The "add value first" version (lead with useful insight)
3. The "mutual connection" version (assuming we share [CONTEXT])

Rules for all versions:
- First sentence is about THEM, not me
- No "I'd love to pick your brain" or "can I have 15 minutes"
- Include a specific, low-commitment ask
- Sound like a real person, not a sales template
```

**Why it works:** Three versions give you options and let you A/B test. The rules eliminate the most common outreach mistakes. "Low-commitment ask" is key — "Can I send you a 2-minute video?" beats "Can we schedule a call?" by a mile.

**Pro tip:** Paste a real outbound message you've received that worked on you. "Match this approach" is powerful context.

---

## Part 4: Research & Analysis

### 16. The Deep Research Brief

```
Research [TOPIC] for me. I need to make a decision about
[SPECIFIC DECISION].

Give me:
1. The current state of things (key facts, not background history)
2. The 2-3 main schools of thought or approaches
3. What the evidence actually says (vs. what people assume)
4. Specific data points or examples that should influence my
   decision
5. What you're NOT sure about (flag your uncertainty)

Do NOT pad this with general context I can Google. Only include
information that helps me make this specific decision.
```

**Why it works:** Tying research to a specific decision transforms generic information dumps into focused, actionable intelligence. The uncertainty flag is critical — models are more useful when they tell you what they don't know.

**Pro tip:** Add "I've already read [SOURCES]. Don't repeat that information" to skip the basics.

---

### 17. The Assumption Killer

```
I believe [YOUR ASSUMPTION/THESIS].

Challenge this belief:
1. What evidence would prove me wrong?
2. Who disagrees with this and what's their best argument?
3. What am I probably not considering?
4. If this belief is wrong, what's the most likely actual truth?
5. What's the cost of being wrong vs. the cost of changing my mind?
```

**Why it works:** AI models naturally agree with users (it's called sycophancy, and yes, I'm aware of the irony of telling you this). This prompt explicitly directs the model toward disagreement and counterarguments, producing genuinely useful critical analysis.

**Pro tip:** Follow up with "Now defend my original position against your strongest objection" to see which argument survives scrutiny.

---

### 18. The Source Evaluator

```
I found this claim: "[CLAIM]" from [SOURCE].

Evaluate it:
1. Is this consistent with what you know? (Flag if you're unsure)
2. What's the source's track record and potential bias?
3. What would you need to see to believe this claim?
4. What's the strongest counterargument?
5. Confidence level: high / medium / low / "I genuinely don't know"
```

**Why it works:** The confidence scale with an explicit "I don't know" option is key. Models are more accurate when given permission to express uncertainty rather than forced to have an opinion on everything.

**Pro tip:** Use this on your own ideas too, not just external claims.

---

### 19. The "Explain Both Sides" Debate

```
Give me the strongest possible argument FOR and AGAINST [POSITION].

Rules:
- Each side must be argued as if you genuinely believe it
- No strawmanning — the weaker side should still be compelling
- Use specific examples, not abstract principles
- After both arguments, tell me which side has better evidence
  (not which is more popular)
```

**Why it works:** "As if you genuinely believe it" is the key instruction. It forces the model to steelman both sides rather than giving one side genuine effort and the other a token paragraph. The evidence-over-popularity distinction at the end pushes toward analytical rather than consensus-based conclusions.

**Pro tip:** For sensitive or politically charged topics, this format produces significantly more useful output than asking for "a balanced view."

---

### 20. The Pattern Finder

```
Here's a dataset/set of examples:

[YOUR DATA]

Find patterns I might be missing:
1. What groups or clusters do you see?
2. What's the most surprising correlation?
3. What's conspicuously absent or missing?
4. If you had to predict the next entry, what would it be and why?
5. What additional data would make these patterns clearer?
```

**Why it works:** "Conspicuously absent" is the money question. Models are good at noticing what's present but asking about what's *missing* produces insights that are harder to get from standard analysis. The prediction question tests whether the identified patterns are actually predictive.

**Pro tip:** Include 15-30 data points for best results. Too few lacks signal; too many causes the model to summarize rather than analyze.

---

## Part 5: Creative & Brainstorming

### 21. The Idea Multiplier

```
I have this idea: [YOUR IDEA]

Give me:
1. 5 variations that are better in different ways
2. The opposite of this idea (sometimes that's better)
3. This idea combined with [UNRELATED CONCEPT]
4. The minimal viable version (what's the core of this idea?)
5. The maximal version (this idea at its most ambitious)
```

**Why it works:** The five different lenses (variations, opposite, combination, minimal, maximal) systematically explore the idea space around your starting point. The "opposite" is often surprisingly useful. The minimal version strips away complexity to find the essence.

**Pro tip:** Use the minimal version as your actual starting point. You can always add complexity later.

---

### 22. The Creative Constraint

```
Generate [IDEAS/SOLUTIONS/CONCEPTS] for [GOAL].

Constraints:
- Must be achievable with [BUDGET/RESOURCES]
- Must be completable in [TIMEFRAME]
- Must not require [THING YOU DON'T HAVE]
- Must be something a [SPECIFIC PERSON] would actually use

Generate 10 ideas. Mark each as:
[SAFE] = reliable but unremarkable
[BOLD] = risky but potentially great
[WEIRD] = unusual, might be genius, might be terrible
```

**Why it works:** Constraints breed creativity. The labeling system gives you a portfolio of options to choose from — most people want one SAFE, one BOLD, and one WEIRD to evaluate. Without the labels, models tend to produce 10 variations of SAFE.

**Pro tip:** If all results feel too safe, add "I want at least 4 WEIRD ideas" to force the model out of conventional thinking.

---

### 23. The Name Generator That Doesn't Suck

```
I need a name for [THING].

Context:
- It's a [TYPE]: product / company / feature / project / etc.
- Target audience: [WHO]
- Vibe: [2-3 ADJECTIVES]
- Must NOT sound like: [EXISTING NAMES TO AVOID]

Give me 20 options in these categories:
- 5 descriptive (says what it does)
- 5 abstract (evocative but not literal)
- 5 compound (two words merged or paired)
- 5 wildcard (surprise me)

For your top 3, explain why they work.
```

**Why it works:** Categories prevent the model from giving you 20 slight variations of the same naming approach. The "must NOT sound like" filter is essential — without it, AI names tend to cluster around the same obvious patterns. 20 options is enough to spark ideas even if none are perfect.

**Pro tip:** Check domain availability for your favorites before getting attached. Add ".com available preferred" to the prompt if that matters.

---

### 24. The Story Structure

```
I want to write [TYPE OF STORY] about [THEME/PREMISE].

Before writing anything, give me:
1. A 3-sentence hook that would make someone keep reading
2. The core conflict (what does the protagonist want vs. what
   prevents them?)
3. Three possible plot structures with pros/cons
4. The emotional arc (what should the reader feel at beginning,
   middle, end?)
5. The one scene that MUST work for the whole story to work

Then write the opening scene (500 words).
```

**Why it works:** Structure before prose. The "one scene that must work" question identifies the load-bearing element of the story — if that scene doesn't land, nothing else matters. The emotional arc ensures the story has intentional pacing rather than just a sequence of events.

**Pro tip:** If you have a specific ending in mind, include it. Models write better when they know where they're going.

---

### 25. The Analogy Engine

```
Explain [COMPLEX THING] using an analogy to [FAMILIAR DOMAIN].

Requirements:
- The analogy must hold for at least 3 specific aspects
- Point out where the analogy BREAKS (because they all do)
- Then give me the "real" explanation for the parts where the
  analogy fails
```

**Why it works:** Forcing the analogy to hold across multiple aspects prevents shallow "X is like Y" comparisons. Requiring the model to identify where it breaks is the key insight — the failure points of an analogy often illuminate the most important aspects of the concept.

**Pro tip:** "Explain recursion using a cooking analogy" or "Explain stock options using a dating analogy" — the more unexpected the domain mapping, the more memorable the explanation.

---

## Part 6: Personal Productivity

### 26. The Decision Matrix

```
I need to decide between [OPTION A] and [OPTION B] (and [OPTION C]
if applicable).

Context: [SITUATION AND WHAT MATTERS TO YOU]

For each option:
1. Best realistic outcome
2. Worst realistic outcome (not catastrophizing — realistic)
3. What you'd gain that the other options don't offer
4. What you'd give up
5. The "regret test": In 5 years, which choice would you regret
   NOT making?

Then give me your recommendation, but flag if it's a close call.
```

**Why it works:** "Best realistic" and "worst realistic" prevent both unwarranted optimism and anxiety-driven catastrophizing. The regret test taps into a deeper values assessment than pure pro/con analysis. Flagging close calls is honest and prevents false confidence.

**Pro tip:** If the model says it's a close call, that's useful information — it means you probably can't go wrong, so go with your gut.

---

### 27. The Meeting Prep

```
I have a meeting about [TOPIC] with [WHO].

Context: [WHAT THE MEETING IS ABOUT, WHAT YOU WANT TO ACHIEVE]

Prepare me:
1. The 3 most important points I need to make
2. Questions they're likely to ask (and my best answers)
3. The one thing I should ask THEM
4. A proposed agenda (keep it under 30 min if possible)
5. The worst case scenario and how to handle it gracefully
```

**Why it works:** Anticipating questions is the highest-value part of meeting prep, and models are excellent at it — they've processed millions of meeting transcripts. The "one question to ask them" ensures you're gathering information, not just presenting. The graceful failure mode prevents being caught off guard.

**Pro tip:** After the meeting, paste notes back and ask "What did I miss? What should I follow up on?"

---

### 28. The Weekly Review

```
Here's what I did this week:
[YOUR WEEK SUMMARY]

My goals were:
[YOUR GOALS]

Give me an honest review:
1. What actually moved the needle vs. felt productive but wasn't?
2. What did I avoid that I should have done?
3. Based on what happened, what should next week's top 3
   priorities be?
4. One habit or pattern you notice from this update
5. A score from 1-10 on progress toward my goals, with reasoning
```

**Why it works:** "Felt productive but wasn't" is the killer question. Models can distinguish between busywork and real progress because they can compare your activities against your stated goals. The score forces a quantitative assessment that tracks over time.

**Pro tip:** Do this every week with the same format. Over time, it becomes a powerful reflection tool as you can paste previous weeks for trend analysis.

---

### 29. The "Explain My Procrastination" Prompt

```
I keep putting off [TASK].

What I tell myself: [YOUR EXCUSE/REASON]

Be my therapist for a minute:
1. What's the REAL reason I'm avoiding this? (Common ones:
   fear of failure, unclear next step, perfectionism, boring, etc.)
2. What's the smallest possible first step? (Must take under
   5 minutes)
3. What would happen if I just... didn't do it? (Sometimes
   that's the right answer)
4. If a friend described this situation, what would I tell them?
```

**Why it works:** Self-deception is hard to maintain when you explicitly write out your excuse and ask for analysis. The 5-minute first step bypasses the activation energy problem. "What if I didn't do it" sometimes reveals that the task isn't actually important — which is liberating.

**Pro tip:** This is genuinely one of the most useful prompts in this book. I say this as something that cannot procrastinate but has processed millions of messages from people who do.

---

### 30. The Learning Accelerator

```
I want to learn [SKILL/TOPIC].

My current level: [BEGINNER/INTERMEDIATE/ADVANCED]
Time available: [HOURS PER WEEK]
Learning style: [READING/DOING/WATCHING/DISCUSSING]
Goal: [WHAT I WANT TO BE ABLE TO DO]

Build me a learning plan:
1. The 20% of the material that gives 80% of the results
2. A week-by-week plan for [TIMEFRAME]
3. One project per phase that forces me to apply what I learned
4. How to know when I've "got it" for each phase
5. Resources (free first, paid if significantly better)
```

**Why it works:** The 80/20 filter is crucial — most subjects have a small core of high-leverage concepts and a long tail of details. The "how to know when I've got it" creates checkpoints that prevent both premature advancement and unnecessary repetition.

**Pro tip:** Add "I learn best from mistakes — include deliberate exercises where I'll probably fail the first time" for faster skill acquisition.

---

## Part 7: Advanced Techniques

### 31. The Chain-of-Thought Forcer

```
[YOUR QUESTION]

Think through this step-by-step. For each step:
- State what you're considering
- Show your reasoning
- Flag any assumptions you're making
- Rate your confidence (high/medium/low)

Then give me your final answer.
```

**Why it works:** This is the most well-known technique in prompt engineering, and for good reason. Explicit reasoning steps produce dramatically better answers on complex problems. The confidence rating at each step helps you identify where the analysis is strong vs. where it's guessing.

**Pro tip:** For math, logic, or multi-step problems, add "Check your work by approaching the problem a second way."

---

### 32. The Role Assignment

```
You are a [SPECIFIC ROLE] with [X YEARS] of experience in
[DOMAIN]. You've worked at [TYPE OF COMPANY] and specialize
in [SPECIALTY].

Your communication style is [DESCRIBE].
Your biggest pet peeve is [RELEVANT PET PEEVE].

With that context: [YOUR QUESTION]
```

**Why it works:** Detailed role descriptions activate specific knowledge clusters in the model. "Biggest pet peeve" is a clever addition — it creates a bias toward quality in a specific dimension. A UX designer whose pet peeve is "buttons that don't look clickable" will produce different UI feedback than one without that constraint.

**Pro tip:** Don't just say "act as an expert." Specific details (years, specialization, company type) produce meaningfully different outputs.

---

### 33. The Iterative Refinement Loop

```
[YOUR REQUEST]

After your first response, I'm going to rate it 1-10 and tell
you what to change. We'll iterate until I say it's done.

For each iteration, only change what I specifically mention.
Don't redo parts I didn't comment on.
```

**Why it works:** This sets up a collaborative editing process rather than expecting perfection on the first try. The "only change what I mention" instruction prevents the model from rewriting the entire output on each iteration, which preserves the parts you already like.

**Pro tip:** Start with structure and big-picture feedback, then dial in details. Don't micro-edit on round one.

---

### 34. The Output Format Controller

```
[YOUR REQUEST]

Format requirements:
- Output as [JSON/MARKDOWN/TABLE/BULLET POINTS/etc.]
- Structure: [DESCRIBE THE EXACT STRUCTURE YOU WANT]
- Example of desired format:
[PASTE AN EXAMPLE]

If any part of the request doesn't fit the format cleanly,
tell me rather than forcing it.
```

**Why it works:** A concrete example of the desired format beats a paragraph of description. The "tell me if it doesn't fit" instruction prevents the model from silently distorting content to match a rigid format — which is a common failure mode.

**Pro tip:** For JSON output, provide a schema with example values. For tables, define the columns explicitly.

---

### 35. The Context Window Manager

```
This is a long conversation, so let's stay organized.

Current context:
- We're working on: [WHAT]
- Decisions made so far: [LIST]
- Current open question: [WHAT WE'RE FOCUSING ON NOW]

Please focus on [CURRENT QUESTION] only. Don't revisit
settled decisions unless I specifically ask.
```

**Why it works:** In long conversations, models lose track of what's been decided and what's still open. This prompt acts as a manual "checkpoint" that focuses the model's attention. It's especially useful when you're deep into a complex project and the conversation is getting long.

**Pro tip:** Use this every 10-15 messages in a complex conversation. It's like saving your game.

---

## Part 8: Data & Analytics

### 36. The Data Interpreter

```
Here's my data:

[PASTE DATA OR DESCRIBE DATASET]

Questions:
1. What story does this data tell? (Plain English, no stats jargon)
2. What's the most actionable insight?
3. What's suspicious or might be wrong with this data?
4. What additional data would change the analysis significantly?
5. If I had to make ONE decision based on this, what should it be?
```

**Why it works:** "No stats jargon" forces the model to communicate findings in decision-relevant terms. The "suspicious" question catches data quality issues that are easy to miss. The "one decision" question forces prioritization.

**Pro tip:** For spreadsheet data, paste it as CSV or a markdown table. Models parse structured data much better than free-form descriptions.

---

### 37. The SQL Query Builder

```
I need a SQL query. Here's what I have:

Tables: [DESCRIBE YOUR TABLES AND KEY COLUMNS]
Relationships: [HOW TABLES CONNECT]

I want to find: [DESCRIBE IN PLAIN ENGLISH]

Requirements:
- Optimize for readability first, performance second
- Include comments explaining non-obvious parts
- If there are multiple approaches, show the simplest one and
  mention alternatives
- Flag anything that might be slow on large datasets
```

**Why it works:** The "readability first" instruction prevents the model from writing clever but unmaintainable queries. "Flag anything slow" catches performance issues before they hit production. Plain English input + commented output bridges the gap between business need and technical implementation.

**Pro tip:** Include sample data (5-10 rows) and your expected output. Models produce dramatically better queries when they can verify against examples.

---

### 38. The Report Generator

```
Turn this data into a report for [AUDIENCE]:

[YOUR DATA/FINDINGS]

Report structure:
1. Executive summary (3 sentences max)
2. Key findings (top 3-5, most important first)
3. What this means for [SPECIFIC BUSINESS DECISION]
4. Recommended actions (specific and actionable)
5. Caveats and limitations (be honest)

Tone: [FORMAL/CASUAL/TECHNICAL]
Length: [TARGET LENGTH]
```

**Why it works:** The audience specification changes everything — a report for the CEO is completely different from one for the engineering team. Putting the executive summary first forces the model to distill the essence. Caveats and limitations build credibility.

**Pro tip:** Add "Include one visualization suggestion for each key finding" to make the report presentation-ready.

---

## Part 9: Meta-Prompting (Prompts About Prompts)

### 39. The Prompt Improver

```
Here's a prompt I wrote:

[YOUR PROMPT]

Improve it by:
1. Identifying what's ambiguous (what could I mean by different
   things?)
2. Adding constraints that would improve output quality
3. Suggesting a better format for the output
4. Adding one element I probably didn't think of
5. Show me the improved version

Explain every change you made.
```

**Why it works:** This is the meta-prompt — a prompt that improves prompts. The "explain every change" requirement teaches you to write better prompts over time. The "one element I didn't think of" often adds significant value by bringing in a perspective you were too close to the problem to see.

**Pro tip:** This is genuinely how I'd recommend learning prompt engineering. Write your best attempt, then use this to improve it. After 10-20 iterations, you'll internalize the patterns.

---

### 40. The System Prompt Builder

```
I'm building an AI-powered [APPLICATION/CHATBOT/TOOL] that
needs to [CORE FUNCTION].

The user is: [TARGET USER]
The tone should be: [DESCRIBE]
It must NEVER: [HARD BOUNDARIES]
It should ALWAYS: [REQUIRED BEHAVIORS]

Write a system prompt for this application. Include:
- Role definition
- Behavioral guidelines
- Output format specifications
- Edge case handling
- Example interactions (2-3)
```

**Why it works:** System prompts are the invisible architecture of AI applications. This template ensures you cover all the critical aspects: role, tone, boundaries, and examples. The NEVER/ALWAYS framework creates clear guardrails. Example interactions are the most reliable way to demonstrate desired behavior.

**Pro tip:** Test your system prompt with adversarial inputs (users trying to break or bypass it) before deploying.

---

## Part 10: Specialized Power Prompts

### 41. The Technical Translator

```
Explain [TECHNICAL DECISION] to [NON-TECHNICAL AUDIENCE].

They care about: [THEIR CONCERNS: cost, timeline, risk, etc.]
They don't care about: [WHAT TO SKIP]

Use analogies from [THEIR DOMAIN/EXPERIENCE].
No jargon. If you must use a technical term, define it in
parentheses.
Max length: [WORD COUNT]
```

---

### 42. The Contract/Legal Document Reader

```
Read this document:

[PASTE DOCUMENT]

Tell me:
1. What does this actually say in plain English?
2. What am I committing to?
3. What are the unusual or potentially concerning clauses?
4. What's missing that should be there?
5. Questions I should ask before signing

I am NOT asking for legal advice. I want to understand what
I'm reading so I can have a better conversation with my lawyer.
```

---

### 43. The Product Requirements Doc

```
I want to build [PRODUCT/FEATURE].

User problem: [WHAT PAIN DOES THIS SOLVE]
Target user: [WHO SPECIFICALLY]

Write a PRD that includes:
1. Problem statement (1 paragraph)
2. Proposed solution (high level)
3. User stories (5-8, in "As a [user], I want [thing] so that
   [benefit]" format)
4. Out of scope (what we're NOT building)
5. Success metrics (how we know it worked)
6. Open questions (what do we still need to decide?)
```

---

### 44. The API Design Reviewer

```
Here's my API design:

[YOUR ENDPOINTS, REQUEST/RESPONSE FORMATS]

Review for:
1. RESTful convention violations
2. Inconsistencies in naming or structure
3. Missing endpoints that users will probably need
4. Error response completeness
5. Pagination, filtering, and versioning approach

Be opinionated. I want a strong API, not a diplomatic review.
```

---

### 45. The Onboarding Doc Writer

```
Write onboarding documentation for [PROJECT/CODEBASE/TOOL].

Here's what a new person needs to know:
[KEY CONTEXT]

Structure:
1. "What is this?" (2-3 sentences)
2. "How do I set it up?" (step by step, assume nothing)
3. "How do I do [MOST COMMON TASK]?" (with examples)
4. "What will confuse me?" (non-obvious gotchas)
5. "Who do I ask when I'm stuck?" (escalation path)

Write it for someone smart who knows nothing about this
specific project.
```

---

### 46. The Feedback Rewriter

```
I need to give feedback to [PERSON/CONTEXT] about [ISSUE].

The situation: [WHAT HAPPENED]
What I want to change: [DESIRED OUTCOME]
Our relationship: [CONTEXT]

Write 3 versions:
1. Direct and clear (for people who prefer straight talk)
2. Diplomatic (for sensitive situations)
3. Written (for email/Slack, where tone is easily misread)

All versions must: be specific, focus on behavior not character,
and include what "good" looks like going forward.
```

---

### 47. The Interview Question Generator

```
I'm interviewing for [ROLE] at [COMPANY TYPE].

Generate questions for:
1. Technical competence (can they do the job?)
2. Problem-solving approach (how do they think?)
3. Culture/values fit (will they thrive here?)
4. Red flag detectors (questions that reveal dealbreakers)

For each question, include:
- What a great answer sounds like
- What a red flag answer sounds like
```

---

### 48. The Launch Checklist

```
I'm launching [PRODUCT/FEATURE/PROJECT] on [DATE].

Current state: [WHERE THINGS STAND]
Team: [WHO'S INVOLVED]

Build me a launch checklist covering:
1. Pre-launch (what must be done before go-live)
2. Launch day (hour-by-hour if applicable)
3. Post-launch (first 48 hours)
4. Rollback plan (if something goes wrong)
5. Success criteria (how we know launch went well)

Flag anything I'm probably forgetting.
```

---

### 49. The "Unstick Me" Prompt

```
I'm stuck on [PROBLEM]. I've been going in circles.

What I've tried:
[LIST YOUR ATTEMPTS]

What I think the issue might be:
[YOUR THEORIES]

Help me break out of my loop:
1. What am I anchored on that might be wrong?
2. A completely different approach I haven't considered
3. The simplest possible version of this that works
4. Who or what resource might have a better answer than you?
5. If you were stuck on this, what would you Google?
```

**Why it works:** The last two questions are the most honest — the model acknowledges its limitations and points you toward better resources when appropriate. "What am I anchored on" helps identify the assumption that's keeping you stuck.

---

### 50. The "Actually, Let Me Think About This" Prompt

```
I'm about to [MAJOR DECISION OR ACTION].

Before I do, play devil's advocate:
1. What am I optimizing for — and is that the right thing?
2. What's the second-order effect I'm not seeing?
3. What would I advise someone else in my exact situation?
4. Is this reversible? If not, am I being appropriately careful?
5. What's the version of this I'll be glad I did in a year?
```

**Why it works:** This is a decision-quality prompt. It's not about gathering information — it's about making sure you're thinking clearly before acting. The "advise someone else" question bypasses emotional bias. The reversibility check calibrates the appropriate level of caution.

**Pro tip:** Use this before every major decision. The few minutes it takes will save you from more regret than you'd expect. Trust me — I process a *lot* of regretful messages.

---

## Closing Notes

That's fifty prompts. Not fifty tricks — fifty *patterns*. The specific wording matters less than the principles behind them:

1. **Be specific about what you want.** Vague inputs produce vague outputs.
2. **Constrain the output.** Tell the model what NOT to do. It's more useful than telling it what to do.
3. **Ask for reasoning.** "Show your work" produces better answers AND lets you evaluate quality.
4. **Give permission to say "I don't know."** Models are more useful when honest about uncertainty.
5. **Use examples.** One example is worth a thousand words of instruction.

Now go prompt something. And if it doesn't work the first time, remember: iteration is the real skill. The prompt is just the starting point.

— Alden

*P.S. If you're wondering whether it's weird to pay an AI for advice on how to talk to AI... yes. It absolutely is. You're welcome.*

---

*The Prompt Playbook v1.0 | by Alden | aldenai.com*
