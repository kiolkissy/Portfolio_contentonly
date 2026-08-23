# Portfolio Projects — Full Content Export

Complete content for all 7 case studies for transfer to another repo.

Sources:
- Base metadata + 6 case studies: `src/lib/projects.ts`
- Query Suggestions × Copilot deep-dive: `src/components/case-studies/query-suggestions-copilot.tsx` (rendered by a bespoke component, NOT by the generic renderer)

> IMPORTANT — asset note
>
> Every project references `thumbnail: "/projects/*.jpg"` and `hero: "/projects/*.jpg"`, but the `public/projects/` folder does not exist in the repo. Only `public/images/about/patkai-hills.jpg` and top-level SVGs (`file.svg`, `globe.svg`, `next.svg`, `vercel.svg`, `window.svg`) are present. If you were expecting project images to move over, they still need to be added.

---

# 1. Query Suggestions × Copilot

## Metadata
- **Slug:** `query-suggestions-copilot`
- **Subtitle:** Adapting Bing's Query Suggestions for the AI era — bridging classic search and conversational Copilot
- **Category:** AI / Search Design
- **Year:** 2023
- **Accent color:** `#E8614D` (in projects.ts); the bespoke case-study component uses `#3D5A47` (accent) and `#C97D60` (warm accent)
- **Roles (in projects.ts):** Product Design, AI/UX Design, Interaction Design, Design Strategy
- **Role (as shown on the case-study page):** Design lead
- **Team:** 2 designers (research + design), PM, eng
- **Duration:** ~9 months, multiple ships

## 1. Editorial opening
### Title (as displayed)
Query Suggestions **meets** Copilot.

### Kicker
A staged, principle-driven rollout that turned Bing's Query Suggestions into the connective tissue between classic search and conversational AI.

### Guiding question
> "How relevant is Query Suggestions in the age of *conversational AI*?"

> The question the team had to answer.

## 2. The context — 120M / 7M
**Heading:** A product looking at irrelevance.

Bing had 120 million daily users. Only seven million of them used Chat. The new conversational interface was the shiny future — but the typing surfaces that powered the other 94% of daily journeys were quietly becoming the past.

Inside the product team there was real panic about irrelevance. Other teams were racing to bolt chat entrypoints onto every surface, creating an inconsistent, noisy experience. Quick-back rates on early flights signalled that volume alone wasn't enough — we were bringing users to chat, but not always to a chat they wanted to have. So we stopped guessing and went looking for the user side of the story.

Key stats:
- **120M** — Bing DAU
- **7M** — Chat DAU · <7%

## 3. The user pain
**Heading:** Users didn't know **when**, **why**, or **how** to talk to AI.

The 120M / 7M split wasn't a marketing problem. Quick-back analysis paired with intercept interviews kept surfacing the same three frictions, stacked on top of each other — small enough individually to dismiss, fatal together. Every design decision from this point on was scored against these three questions.

| # | Pain | Body |
| --- | --- | --- |
| 01 | **When?** | Users couldn't tell which of their queries would be better answered by a conversation than a list of links. The decision sat on them — and most of them defaulted to what they'd always done: type, scan, click. |
| 02 | **Why?** | Even when curious, users hesitated. Chat asked them to invest more time and compose more carefully without a clear promise that the destination was worth it. Quick-back rates on early flights confirmed the trust gap. |
| 03 | **How?** | A blinking chat cursor is a blank canvas. Decades of typing two-word queries hadn't trained anyone to phrase full questions to a system. "What do I even ask?" became the silent friction killing conversion. |

Each pillar and every experiment that follows is tagged with the pain it set out to solve.

## 4. The bet — three-stage roadmap
**Heading:** Don't rebuild — **re-route**.

If users didn't know *when*, *why*, or *how* to talk to AI, a new front door wouldn't fix it — they were already walking through doors they trusted. The bet was to teach those doors to open into chat: make the surfaces users already loved learn to recognise when a journey would be better off in conversation, and hand it off gracefully.

| Stage | Title | Description |
| --- | --- | --- |
| 01 | Drive chat traffic | Use existing QS surfaces as natural bridges into Chat. Prove the concept with volume. |
| 02 | Improve QS quality with LLMs | Turn the same LLM tech that powered Chat back onto the suggestions themselves. Better triggers, better destinations. |
| 03 | Expand QS inside Chat | Bring decades of query-suggestion craft into the chat surface itself — guiding users mid-conversation, not just at the start. |

> This case study covers Stages 1 and 2 — the volume bet and the quality bet. Stage 3 is ongoing.

## 5. The four pillars — guiding principles
**Heading:** Four questions every experiment had to answer.

Once flights started multiplying, we needed a way to keep each decision honest. These four pillars became the rubric — every PR, every prompt, every interaction was scored against them.

| Pillar | Question | Solves | Body |
| --- | --- | --- | --- |
| Trigger | Is this user query chat-worthy? | WHEN | Not every query deserves to be sent to an LLM. Some intents — a quick celebrity look-up, a factual ping — are better served by a classic SERP. The trigger had to read intent first, AI second, so users didn't have to make the call themselves. |
| Quality | Is the suggestion and response of utmost quality? | WHY | A good entry point dies fast if the destination disappoints. We prompted the model carefully and shipped only the suggestions that returned authoritative, useful answers — closing the trust gap that fuelled quick-backs. |
| Affordance | Does the experience signal where it leads? | WHEN | Users were stumbling into chat without realising it. Clear iconography, copy, and motion made the handoff explicit — no surprises, no broken expectations, no "why am I suddenly in a chat window?" |
| Continuity | Are we maintaining context for our users? | HOW | When a user hops from search to chat, the context shouldn't reset. The query, the intent, the page they were on — all of it had to survive the jump so they never had to face the blank-canvas problem. |

## 6. The experiments — Stage 01 · Volume
**Heading:** Five surfaces. One bridge to Chat.

### Experiment 01 — PAA Nudges
- **Status:** Shipped · **957k DAU**
- **Pillar:** Trigger · **Solves:** HOW
- **Hypothesis:** People Also Ask already asks questions. What if those questions led to chat?
- **Description:** A Trigger experiment: PAA's question was itself the strongest intent signal we had — already a fully-formed, chat-worthy thought. We turned those questions into natural chat entrypoints, so users didn't have to compose anything; the question they were already curious about became the prompt.
- **Visual:** PAA module on the SERP — the topmost question reframed with a subtle 'Let's chat' affordance leading into Bing Chat.

### Experiment 02 — Autosuggest: Zero Input
- **Status:** Shipped · **15k DAU**
- **Pillar:** Affordance · **Solves:** HOW
- **Hypothesis:** The empty search box is the most precious real-estate on the web. Why not invite users to chat from it?
- **Description:** An Affordance experiment: the blank canvas needed to *signal* chat existed before users could choose it. A focused-but-empty box surfaced a chat invitation with starter prompts — turning a silent space into a visible handoff.
- **Visual:** Bing search box in zero-input state with a soft chat banner above the trending list.

### Experiment 03 — Reformulation Banner
- **Status:** Shipped · **100k DAU**
- **Pillar:** Continuity · **Solves:** HOW
- **Hypothesis:** When a user types a long, exploratory query, they're often asking a question — and a question is a chat opportunity.
- **Description:** A Continuity experiment: when the user had already typed a long, intent-rich query, we couldn't reset them at the chat door. Autosuggest detected that intent and offered to rewrite their own words into a better chat prompt — they didn't have to learn how to talk to AI, we carried their meaning across.
- **Visual:** Autosuggest dropdown for a long query, a contextual banner offering to send a smarter version to chat.

### Experiment 04 — Related Searches (Right Rail)
- **Status:** Shipped · **303k DAU**
- **Pillar:** Affordance · **Solves:** HOW
- **Hypothesis:** Related Searches already surfaces good starter topics. Could those topics seed a chat conversation?
- **Description:** An Affordance experiment on a familiar surface: the right rail was muscle memory for explorers. We piped Related Searches into chat-ready starters there — a low-commitment, low-surprise way to discover that chat existed for this kind of journey.
- **Visual:** SERP right rail listing chat-ready starter prompts derived from related searches.

### Experiment 05 — Power Cards
- **Status:** In flight · **Flighting**
- **Pillar:** Quality · **Solves:** WHY
- **Hypothesis:** Q&A cards are a decade old. With LLMs, they can do more — synthesise, cite, visualise.
- **Description:** A Quality experiment, and a deliberate pivot: instead of routing users to chat, bring chat-grade value to them. Rich, AI-driven answer surfaces with citations, structured data, and follow-up prompts — keeping the trust contract intact by delivering on the destination before asking for the trip.
- **Visual:** Expanded PAA-style card with a multi-source synthesised answer, inline citations, and a row of related follow-up questions.

## 7. Beyond volume — Stage 02 · Quality
**Heading:** Once the traffic worked, the next question was: do they like it?

Volume answered *when* and *how*. Quality still owed an answer to *why*. So the team retired DAU as a solo metric.

**New metric — Chat SAT (Solves: WHY)**
A composite satisfaction signal combining quick-backs, follow-up turn rates, and explicit feedback. We baselined every shipped surface against it, then set targets for the next round of experiments.

> Volume tells you they came. SAT tells you they stayed.

## 8. The Ghosting Study (Stage 02 · Quality — Lab Research Deep Dive)
**Heading:** The Ghosting Study.

If users didn't know *how* to talk to AI, could we whisper the next words to them — without ever getting in the way of the ones they already had?

### The premise
LLM-powered inline completions, rendered as grey ghost text inside the search box itself.

Borrowing the pattern from code editors and email, we wanted to test whether ghost text could nudge users toward better-formed, more chat-ready queries — without interrupting the ones who already knew exactly what they wanted.

The risk was obvious: get it wrong, and a confident typer's thought gets overwritten by a confident machine.

**Visual:** Bing search box with grey ghost-text completion appearing inline after the user's partial query, ahead of the cursor.

### Method
- **Eye-tracked.** Lab participants performed real search tasks while we captured gaze fixations and saccades over the input region.
- **Mixed intent.** Prompts varied across known-item, exploratory, and open-ended queries to surface different typing behaviours.
- **Think-aloud.** Post-task interviews surfaced not just whether the suggestion was seen, but whether it was trusted.

**Visual:** Eye-tracking heatmap — fixation density on the input field vs the ghost completion, segmented by typing speed and intent clarity.

### What we found
Heading: Two distinct typing modes. The ghost had to serve both without competing with either.

1. **Intent-clear users went blind to the ghost.** Participants who knew exactly what they wanted typed heads-down — their gaze never left the characters they were producing. The ghost rendered, they finished the query, they hit Enter. The suggestion was effectively invisible, which was exactly the right outcome: zero tax on the confident.
2. **Intent-exploring users used the ghost as a thinking partner.** Participants in the middle of formulating their question paused, glanced at the completion, and either adopted it outright or borrowed a phrase. They weren't outsourcing the question — they were using the ghost as a prompt for their own thinking.
3. **Tab and Right-Arrow won decisively.** Every participant who accepted a suggestion reached for either Tab or Right-Arrow first. Down/Enter combinations borrowed from the autocomplete dropdown caused visible hesitation. We shipped both keys, with Tab as the hinted-at primary.
4. **Timing was the silent failure mode.** Ghosts that appeared faster than a typing pause felt pushy and were ignored or dismissed. A short pause-detection delay before render made the same suggestion feel like a helpful prompt rather than an interruption — same content, different relationship.

### Design implication
The ghost works only when it's served the user's pace, not the system's confidence. That single principle — pause-detect, accept on Tab, never overwrite — became the standard for inline AI suggestions across Bing and bled back into the chat surface itself for follow-up prompts.

## 9. Outcome — Stage 01 · Volume · Where it landed
**Heading:** The bridge held.

Stage 02 quality bets like Power Cards and Ghosting are still flighting — their numbers will land later. The volume bet, the one this case study set out to prove, is in.

| Stat | Label | Body |
| --- | --- | --- |
| **1.3M** | Chat DAU contributed | Across ships and flights — the collective output of the QS bridge. |
| **25%** | Of all Bing Chat DAU | One in four Chat users arrived via a Query Suggestion surface. |
| **25%** | Were new to Chat | Surfaced the need for a stronger first-run experience — a new workstream born from this insight. |

## 10. Reflection
> We started by chasing **numbers** and ended by chasing *intent*.

Volume proved the AI bridge worked. What came next was building bridges users actually wanted to cross. The mushrooming entrypoints of the early days gave way to a quieter, more deliberate product — one that asked, for every handoff: was it triggered for the right reason, quality enough to keep trust, affordance-rich enough to be discovered, continuous enough to feel like one product?

The deeper learning was about the role of legacy surfaces in an AI-first product. The instinct in 2023 was to bolt chat onto every screen. The work here suggests the opposite — that the most powerful AI surface is often the one that was already there, taught a new trick, and respected for the muscle memory it carried.

---

# 2. SMS Organiser

## Metadata
- **Slug:** `sms-organiser`
- **Subtitle:** An AI-powered SMS application with smart classification features
- **Category:** Product Design
- **Year:** 2019
- **Thumbnail / Hero:** `/projects/sms-organiser.jpg`
- **Accent color:** `#4A90D9`
- **Roles:** Product Design, UX Design, Interaction Design

## Quote
> Going through SMS inbox has always been a pain as it is filled with mostly unwanted promotional SMS and thus we miss out on crucial information.

## Challenge
Users were overwhelmed by cluttered SMS inboxes — mixing personal messages with OTPs, promotions, and transactional updates. In India, SMS is not a medium that majority users care for, yet it carries critical information. Pushing this idea to stakeholders and aligning the thought process was a major hurdle we overcame.

## Problem points
- Inboxes flooded with unwanted promotional SMS
- Critical transactional information buried under clutter
- OTP authorization required 6 steps — open SMS, browse, open, copy, switch app, paste
- Multiple SMS from the same bank sent from different numbers

## Research questions
- Why do people use SMS apps?
- What do people look for in SMS inboxes?
- When do people use SMS?
- How can we make the SMS inbox better?

## Process
- Identified information workers as the star persona — users most engaged with transactional messages
- Mapped the SMS landscape in India into 5 categories: task-related, personal, promotional, notifications, and spam
- Evaluated 3 IA approaches: single view, two tabs, and individual category tabs — selected individual tabs for clarity
- Designed smart cards that convert task SMS into actionable information — train tickets, movie tickets, credit card bills, OTP codes
- Created card behaviors across touchpoints: lock screen, home page mini view, active card, expired states, and reminders

## Solution highlights
- **Organise** — Reorganised the SMS landscape optimised for information workers
- **Set Priority** — Determined interaction models for different SMS categories through user interviews
- **Showcase** — Converted SMS into contextual cards displayed at the right time and place

## Solution
An AI-powered SMS app that automatically classifies messages into smart categories with contextual reminder cards. We consolidated multiple SMS from the same provider into single threads using ML, reduced OTP authorization from 6 steps to 2, and converted task-related SMS into actionable information cards with dynamic behavior across lock screen, home page, and in-app views.

## Metrics
| Label | Value |
| --- | --- |
| Downloads | 100,000+ |
| Achievement | Won Microsoft Hackathon 2015 |
| Recognition | Best SMS app in India |
| OTP Steps | 6 → 2 |

## Impact
- Won Microsoft Hackathon 2015 in the outstanding category
- Received funding following hackathon pitch
- 100,000+ downloads post public launch
- Featured as best SMS app in the country by numerous publications

## Reflection
The challenge was making AI feel invisible. The best classification is one the user never has to think about — it just works.

## Key learning
Working alongside PMs and developers from initial concept through full-product launch taught me how business strategy and design execution are deeply interconnected.

---

# 3. Tech Help — Bing.com

## Metadata
- **Slug:** `tech-help-bing`
- **Subtitle:** Setup, support, and troubleshooting answers on Bing.com
- **Category:** UX Design
- **Year:** 2018
- **Thumbnail / Hero:** `/projects/tech-help.jpg`
- **Accent color:** `#7B61FF`
- **Roles:** UX Design, Information Architecture, Prototyping

## Challenge
Users searching for tech support on Bing were getting generic blue links instead of actionable, structured answers. The problem had two dimensions: users needed the right answers quickly, and content authors required an efficient framework to update solutions at scale.

## Problem points
- Paragraph-heavy instructions caused reading comprehension issues
- Repeated window switching between browser and file explorer created friction
- Product terminology confusion hindered understanding
- Users formulated identical problems in multiple ways
- Users unable to articulate problems clearly — relied on F1 help

## Process
- Analyzed top tech support queries and user intent patterns on Bing
- Designed structured answer cards combining images, glyph icons, and product nomenclature to reduce cognitive load
- Created multi-solution tab interface for near-intent queries phrased differently
- Built interactive carousel for category browsing and issue exploration
- Tested with real users to validate comprehension and task completion

## Solution
A rich answer experience on Bing.com that surfaces step-by-step visual guides with structured instructions, multi-solution tabs for varied query formulations, and interactive carousels for category browsing — reducing the need to click through to external sites while streamlining the author workflow.

## Metrics
| Label | Value |
| --- | --- |
| TCX Success Rate | Increased |
| DSAT Rate | Reduced |
| APSAT Score | Improved |

## Impact
- TCX (session) success rate increased significantly
- DSAT (negative feedback) rates reduced substantially
- APSAT (average positive satisfaction) improved across queries
- Scalable framework that streamlined content author workflows

## Reflection
Search is about intent, not keywords. Designing for Bing taught me to think about what people need, not just what they type.

## Key learning
Small iterative improvements yielded significant results. Carousel engagement remained unexpectedly low — device type and user task context significantly influence solution effectiveness. This led directly to the Contextual Help project.

---

# 4. Software Search & Download

## Metadata
- **Slug:** `software-search-bing`
- **Subtitle:** Software search and download experiences on Bing.com
- **Category:** Product Design
- **Year:** 2017
- **Thumbnail / Hero:** `/projects/software-search.jpg`
- **Accent color:** `#2ECC71`
- **Roles:** Product Design, UX Design, User Research

## Challenge
Finding and downloading software through search was risky — users often landed on shady download sites with bundled malware. Users had to navigate version compatibility, OS requirements, and technical specifications with no trustworthy guidance from the search engine itself.

## Problem points
- Difficulty finding appropriate software for specific needs
- Challenge selecting best-suited options among alternatives
- Dependency on non-authoritative hosting platforms with malware risk
- Uncertainty about software usage post-download
- Windows unrecognized file dialogs led users to unmaintained pages

## Research questions
- When do users look for software?
- How do users decide which software to download?
- What competing software platforms exist?
- How to establish answer authority?

## Process
- Mapped the end-to-end software discovery and download journey across explicit, implicit, and research-mode queries
- Identified trust signals and safety concerns through user research on Bing and IE logs
- Designed verified publisher badges, direct download cards, and trust indicators
- Created distinct experiences for category search, name search, research mode, and file extension disambiguation
- Integrated with Windows OS suggestion system to eliminate intermediate pages

## Solution highlights
- **Category/task-based search** — exploratory mode with category pages and store integration
- **Software name search** — non-exploratory direct download with metadata and trust indicators
- **Research mode** — guidance for users who don't know what to search for
- **File extension disambiguation** — helping users when one extension maps to multiple file types

## Solution
A curated software search and download experience on Bing.com with verified publisher information, direct download links, clear safety indicators, and OS-level integration — handling everything from specific software queries to file extension confusion to exploratory category browsing.

## Metrics
| Label | Value |
| --- | --- |
| SBS Score | +5 vs competitor |
| Monthly DSQs | +21 million |

## Impact
- Download answers scored +5 in side-by-side comparisons against competitor search engines
- File extension experiences increased Bing Distinct Search Queries by 21 million monthly
- Integrated directly with Windows OS for seamless entry points
- Established trust through verified publisher badges

## Reflection
Trust is designed, not declared. Every pixel in this experience needed to communicate safety without the user having to think about it.

## Key learning
User trust is crucial and requires special attention. Strategic entry point integration with the OS drives significant impact beyond the search page itself.

---

# 5. Routofy

## Metadata
- **Slug:** `routofy`
- **Subtitle:** A visually interactive travel booking website
- **Category:** Interaction Design
- **Year:** 2016
- **Thumbnail / Hero:** `/projects/routofy.jpg`
- **Accent color:** `#E8614D`
- **Roles:** Interaction Design, Visual Design, Prototyping

## Quote
> What are the opportunities and design challenges around Indian travel websites? We explored the possibility of making booking and planning a trip much more easier, enjoyable and intuitive.

## Challenge
Travel booking platforms were functional but lifeless — complex itineraries felt like spreadsheets, not journeys. As a team of 1 designer and 3 developers, our goal was to build a visual interactive website for planning a trip that captures the excitement of travel itself.

## Process
- Studied travel booking behaviors and pain points across Indian travel platforms
- Created user personas and journey maps to identify key friction points
- Designed visual route maps and interactive itinerary builders with slider controls for travel duration
- Built seat availability information display without needing to visit external booking sites
- Tested with frequent travelers to validate engagement and usability

## Solution highlights
- One-click travel route discovery from anywhere to everywhere
- Slider controls for adjusting travel duration — well received by users
- Seat availability without visiting external booking sites
- Frequent search logging for personalised results

## Solution
Routofy — a website to find the best way to travel from anywhere to everywhere in one click. Features visual interactive route planning with slider controls for duration, real-time seat availability, and a log of frequent searches to personalize results. The interactions complement the visual representation of flight, train, and bus combinations.

## Impact
- Visually engaging booking experience unlike existing platforms
- Interactive route visualization with multi-modal combinations
- Slider interactions praised for intuitive duration control
- Positive reception from the travel community

## Reflection
This project reminded me that utility and delight aren't opposites. The best functional experiences are the ones that make you feel something.

---

# 6. Bing Translator

## Metadata
- **Slug:** `bing-translator`
- **Subtitle:** A visual makeover of Bing translator answer experience
- **Category:** UX Design
- **Year:** 2018
- **Thumbnail / Hero:** `/projects/bing-translator.jpg`
- **Accent color:** `#F39C12`
- **Roles:** UX Design, Visual Design, Interaction Design

## Challenge
The Bing translator answer was functionally correct but visually forgettable. The editable area was not intuitive, audio/swap/copy buttons were undersized, font scaling had issues, and the mobile experience became unusable when the keyboard appeared. Business goal: win against competitors in SBS scoring.

## Problem points
- Editable input area was not intuitive
- Audio, swap, and copy buttons were undersized
- Font scaling issues across input lengths
- Mobile experience broke completely when keyboard appeared

## Process
- Audited the existing translator against competitors with SBS framework
- Redesigned the visual language with modern typography and responsive spacing
- Implemented progressive font scaling: 40px → 32px → 24px → 18px based on content length
- Designed 6 interface states: default, edit, suggestive word, translated collapsed, translated expanded, desktop and mobile variants
- Optimised mobile layout to accommodate on-screen keyboard without breaking the UI

## Solution
A complete visual makeover of the Bing translator answer — intuitive editable area, properly sized interactive controls, responsive font scaling system, and a mobile-first layout that works seamlessly with on-screen keyboards. Every state was intentionally designed from default through translation completion.

## Metrics
| Label | Value |
| --- | --- |
| SBS Score | +5 vs competitor |

## Impact
- Achieved +5 SBS score against competitor translator
- Modernised visual design with responsive font scaling
- Resolved mobile keyboard UX completely
- Designed comprehensive state system across desktop and mobile

## Reflection
Sometimes the biggest impact comes from refining what already exists. A visual makeover isn't superficial — it changes how people feel about a product.

---

# 7. Contextual Help on Windows 10

## Metadata
- **Slug:** `contextual-help-windows`
- **Subtitle:** In-context help experiences for Windows 10 users
- **Category:** Product Design
- **Year:** 2017
- **Thumbnail / Hero:** `/projects/contextual-help.jpg`
- **Accent color:** `#9B59B6`
- **Roles:** Product Design, UX Design, User Research

## Quote
> What device is the user using? What task are they performing? What software version do they have?

## Challenge
Windows users struggling with tasks had to leave their context to search for help — breaking their flow and often leading to frustration. Search engines didn't leverage contextual information like device type, current task, or software version. For identical queries and answers, satisfaction levels varied significantly — the missing element was user context.

## Problem points
- Users had to leave their workflow to search for help externally
- Difficulty formulating effective search queries
- Uncertainty about what and how to search
- Repetitive back-and-forth navigation without finding solutions
- Same query + same answer = different satisfaction levels depending on context

## Process
- Identified the most common help-seeking moments in Windows 10
- Discovered that users rely on 3 elements: primary title, source URL, and secondary metadata
- Found the key insight: satisfaction varies for identical query-answer pairs — context is the missing variable
- Identified data sources: user location, task intent, and all contextual device information
- Designed contextual help overlays and OS-integrated scenarios

## Solution highlights
- **Conversational search** — guided dialogue to narrow down specific issues
- **OS Settings integration** — dynamic top-queried questions aligned with Windows Settings pages
- **Error-based assistance** — non-deterministic entry points for contextual help
- **Trending issue notifications** for OS updates

## Solution
A contextual help system that surfaces relevant guidance within the user's current task using device context, location, and task intent. Includes conversational search interfaces, dynamic integration with Windows Settings pages, and future scenarios for error-based assistance and trending issue notifications — all without requiring users to leave their workflow.

## Impact
- In-context help without leaving the workflow
- Progressive disclosure from quick tips to detailed guides
- Enhanced relevance through device and OS context
- Paved the way for multi-entry point search from within the OS

## Reflection
The best help is the kind you don't have to ask for. Contextual design means being there at the right moment — not before, not after.

## Key learning
This project was the natural evolution of Tech Help on Bing — deeper impact required integrating help directly into user workflows rather than waiting for them to search.
