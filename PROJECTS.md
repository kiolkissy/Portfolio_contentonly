# Portfolio Projects

Content export from `src/lib/projects.ts` for transfer to another repo.

---

## 1. Query Suggestions × Copilot

- **Slug:** `query-suggestions-copilot`
- **Subtitle:** Adapting Bing's Query Suggestions for the AI era — bridging classic search and conversational Copilot
- **Category:** AI / Search Design
- **Year:** 2023
- **Thumbnail:** `/projects/query-suggestions-copilot.jpg`
- **Hero:** `/projects/query-suggestions-copilot.jpg`
- **Accent color:** `#E8614D`
- **Roles:** Product Design, AI/UX Design, Interaction Design, Design Strategy

### Challenge
When Bing launched its conversational AI, Query Suggestions — surfaces used by millions every day to type and explore — risked becoming irrelevant overnight.

### Process
_(To be filled in.)_

### Solution
_(To be filled in.)_

### Impact
_(To be filled in.)_

### Reflection
_(To be filled in.)_

---

## 2. SMS Organiser

- **Slug:** `sms-organiser`
- **Subtitle:** An AI-powered SMS application with smart classification features
- **Category:** Product Design
- **Year:** 2019
- **Thumbnail:** `/projects/sms-organiser.jpg`
- **Hero:** `/projects/sms-organiser.jpg`
- **Accent color:** `#4A90D9`
- **Roles:** Product Design, UX Design, Interaction Design

### Quote
> Going through SMS inbox has always been a pain as it is filled with mostly unwanted promotional SMS and thus we miss out on crucial information.

### Challenge
Users were overwhelmed by cluttered SMS inboxes — mixing personal messages with OTPs, promotions, and transactional updates. In India, SMS is not a medium that majority users care for, yet it carries critical information. Pushing this idea to stakeholders and aligning the thought process was a major hurdle we overcame.

### Problem points
- Inboxes flooded with unwanted promotional SMS
- Critical transactional information buried under clutter
- OTP authorization required 6 steps — open SMS, browse, open, copy, switch app, paste
- Multiple SMS from the same bank sent from different numbers

### Research questions
- Why do people use SMS apps?
- What do people look for in SMS inboxes?
- When do people use SMS?
- How can we make the SMS inbox better?

### Process
- Identified information workers as the star persona — users most engaged with transactional messages
- Mapped the SMS landscape in India into 5 categories: task-related, personal, promotional, notifications, and spam
- Evaluated 3 IA approaches: single view, two tabs, and individual category tabs — selected individual tabs for clarity
- Designed smart cards that convert task SMS into actionable information — train tickets, movie tickets, credit card bills, OTP codes
- Created card behaviors across touchpoints: lock screen, home page mini view, active card, expired states, and reminders

### Solution highlights
- **Organise** — Reorganised the SMS landscape optimised for information workers
- **Set Priority** — Determined interaction models for different SMS categories through user interviews
- **Showcase** — Converted SMS into contextual cards displayed at the right time and place

### Solution
An AI-powered SMS app that automatically classifies messages into smart categories with contextual reminder cards. We consolidated multiple SMS from the same provider into single threads using ML, reduced OTP authorization from 6 steps to 2, and converted task-related SMS into actionable information cards with dynamic behavior across lock screen, home page, and in-app views.

### Metrics
| Label | Value |
| --- | --- |
| Downloads | 100,000+ |
| Achievement | Won Microsoft Hackathon 2015 |
| Recognition | Best SMS app in India |
| OTP Steps | 6 → 2 |

### Impact
- Won Microsoft Hackathon 2015 in the outstanding category
- Received funding following hackathon pitch
- 100,000+ downloads post public launch
- Featured as best SMS app in the country by numerous publications

### Reflection
The challenge was making AI feel invisible. The best classification is one the user never has to think about — it just works.

### Key learning
Working alongside PMs and developers from initial concept through full-product launch taught me how business strategy and design execution are deeply interconnected.

---

## 3. Tech Help — Bing.com

- **Slug:** `tech-help-bing`
- **Subtitle:** Setup, support, and troubleshooting answers on Bing.com
- **Category:** UX Design
- **Year:** 2018
- **Thumbnail:** `/projects/tech-help.jpg`
- **Hero:** `/projects/tech-help.jpg`
- **Accent color:** `#7B61FF`
- **Roles:** UX Design, Information Architecture, Prototyping

### Challenge
Users searching for tech support on Bing were getting generic blue links instead of actionable, structured answers. The problem had two dimensions: users needed the right answers quickly, and content authors required an efficient framework to update solutions at scale.

### Problem points
- Paragraph-heavy instructions caused reading comprehension issues
- Repeated window switching between browser and file explorer created friction
- Product terminology confusion hindered understanding
- Users formulated identical problems in multiple ways
- Users unable to articulate problems clearly — relied on F1 help

### Process
- Analyzed top tech support queries and user intent patterns on Bing
- Designed structured answer cards combining images, glyph icons, and product nomenclature to reduce cognitive load
- Created multi-solution tab interface for near-intent queries phrased differently
- Built interactive carousel for category browsing and issue exploration
- Tested with real users to validate comprehension and task completion

### Solution
A rich answer experience on Bing.com that surfaces step-by-step visual guides with structured instructions, multi-solution tabs for varied query formulations, and interactive carousels for category browsing — reducing the need to click through to external sites while streamlining the author workflow.

### Metrics
| Label | Value |
| --- | --- |
| TCX Success Rate | Increased |
| DSAT Rate | Reduced |
| APSAT Score | Improved |

### Impact
- TCX (session) success rate increased significantly
- DSAT (negative feedback) rates reduced substantially
- APSAT (average positive satisfaction) improved across queries
- Scalable framework that streamlined content author workflows

### Reflection
Search is about intent, not keywords. Designing for Bing taught me to think about what people need, not just what they type.

### Key learning
Small iterative improvements yielded significant results. Carousel engagement remained unexpectedly low — device type and user task context significantly influence solution effectiveness. This led directly to the Contextual Help project.

---

## 4. Software Search & Download

- **Slug:** `software-search-bing`
- **Subtitle:** Software search and download experiences on Bing.com
- **Category:** Product Design
- **Year:** 2017
- **Thumbnail:** `/projects/software-search.jpg`
- **Hero:** `/projects/software-search.jpg`
- **Accent color:** `#2ECC71`
- **Roles:** Product Design, UX Design, User Research

### Challenge
Finding and downloading software through search was risky — users often landed on shady download sites with bundled malware. Users had to navigate version compatibility, OS requirements, and technical specifications with no trustworthy guidance from the search engine itself.

### Problem points
- Difficulty finding appropriate software for specific needs
- Challenge selecting best-suited options among alternatives
- Dependency on non-authoritative hosting platforms with malware risk
- Uncertainty about software usage post-download
- Windows unrecognized file dialogs led users to unmaintained pages

### Research questions
- When do users look for software?
- How do users decide which software to download?
- What competing software platforms exist?
- How to establish answer authority?

### Process
- Mapped the end-to-end software discovery and download journey across explicit, implicit, and research-mode queries
- Identified trust signals and safety concerns through user research on Bing and IE logs
- Designed verified publisher badges, direct download cards, and trust indicators
- Created distinct experiences for category search, name search, research mode, and file extension disambiguation
- Integrated with Windows OS suggestion system to eliminate intermediate pages

### Solution highlights
- **Category/task-based search** — exploratory mode with category pages and store integration
- **Software name search** — non-exploratory direct download with metadata and trust indicators
- **Research mode** — guidance for users who don't know what to search for
- **File extension disambiguation** — helping users when one extension maps to multiple file types

### Solution
A curated software search and download experience on Bing.com with verified publisher information, direct download links, clear safety indicators, and OS-level integration — handling everything from specific software queries to file extension confusion to exploratory category browsing.

### Metrics
| Label | Value |
| --- | --- |
| SBS Score | +5 vs competitor |
| Monthly DSQs | +21 million |

### Impact
- Download answers scored +5 in side-by-side comparisons against competitor search engines
- File extension experiences increased Bing Distinct Search Queries by 21 million monthly
- Integrated directly with Windows OS for seamless entry points
- Established trust through verified publisher badges

### Reflection
Trust is designed, not declared. Every pixel in this experience needed to communicate safety without the user having to think about it.

### Key learning
User trust is crucial and requires special attention. Strategic entry point integration with the OS drives significant impact beyond the search page itself.

---

## 5. Routofy

- **Slug:** `routofy`
- **Subtitle:** A visually interactive travel booking website
- **Category:** Interaction Design
- **Year:** 2016
- **Thumbnail:** `/projects/routofy.jpg`
- **Hero:** `/projects/routofy.jpg`
- **Accent color:** `#E8614D`
- **Roles:** Interaction Design, Visual Design, Prototyping

### Quote
> What are the opportunities and design challenges around Indian travel websites? We explored the possibility of making booking and planning a trip much more easier, enjoyable and intuitive.

### Challenge
Travel booking platforms were functional but lifeless — complex itineraries felt like spreadsheets, not journeys. As a team of 1 designer and 3 developers, our goal was to build a visual interactive website for planning a trip that captures the excitement of travel itself.

### Process
- Studied travel booking behaviors and pain points across Indian travel platforms
- Created user personas and journey maps to identify key friction points
- Designed visual route maps and interactive itinerary builders with slider controls for travel duration
- Built seat availability information display without needing to visit external booking sites
- Tested with frequent travelers to validate engagement and usability

### Solution highlights
- One-click travel route discovery from anywhere to everywhere
- Slider controls for adjusting travel duration — well received by users
- Seat availability without visiting external booking sites
- Frequent search logging for personalised results

### Solution
Routofy — a website to find the best way to travel from anywhere to everywhere in one click. Features visual interactive route planning with slider controls for duration, real-time seat availability, and a log of frequent searches to personalize results. The interactions complement the visual representation of flight, train, and bus combinations.

### Impact
- Visually engaging booking experience unlike existing platforms
- Interactive route visualization with multi-modal combinations
- Slider interactions praised for intuitive duration control
- Positive reception from the travel community

### Reflection
This project reminded me that utility and delight aren't opposites. The best functional experiences are the ones that make you feel something.

---

## 6. Bing Translator

- **Slug:** `bing-translator`
- **Subtitle:** A visual makeover of Bing translator answer experience
- **Category:** UX Design
- **Year:** 2018
- **Thumbnail:** `/projects/bing-translator.jpg`
- **Hero:** `/projects/bing-translator.jpg`
- **Accent color:** `#F39C12`
- **Roles:** UX Design, Visual Design, Interaction Design

### Challenge
The Bing translator answer was functionally correct but visually forgettable. The editable area was not intuitive, audio/swap/copy buttons were undersized, font scaling had issues, and the mobile experience became unusable when the keyboard appeared. Business goal: win against competitors in SBS scoring.

### Problem points
- Editable input area was not intuitive
- Audio, swap, and copy buttons were undersized
- Font scaling issues across input lengths
- Mobile experience broke completely when keyboard appeared

### Process
- Audited the existing translator against competitors with SBS framework
- Redesigned the visual language with modern typography and responsive spacing
- Implemented progressive font scaling: 40px → 32px → 24px → 18px based on content length
- Designed 6 interface states: default, edit, suggestive word, translated collapsed, translated expanded, desktop and mobile variants
- Optimised mobile layout to accommodate on-screen keyboard without breaking the UI

### Solution
A complete visual makeover of the Bing translator answer — intuitive editable area, properly sized interactive controls, responsive font scaling system, and a mobile-first layout that works seamlessly with on-screen keyboards. Every state was intentionally designed from default through translation completion.

### Metrics
| Label | Value |
| --- | --- |
| SBS Score | +5 vs competitor |

### Impact
- Achieved +5 SBS score against competitor translator
- Modernised visual design with responsive font scaling
- Resolved mobile keyboard UX completely
- Designed comprehensive state system across desktop and mobile

### Reflection
Sometimes the biggest impact comes from refining what already exists. A visual makeover isn't superficial — it changes how people feel about a product.

---

## 7. Contextual Help on Windows 10

- **Slug:** `contextual-help-windows`
- **Subtitle:** In-context help experiences for Windows 10 users
- **Category:** Product Design
- **Year:** 2017
- **Thumbnail:** `/projects/contextual-help.jpg`
- **Hero:** `/projects/contextual-help.jpg`
- **Accent color:** `#9B59B6`
- **Roles:** Product Design, UX Design, User Research

### Quote
> What device is the user using? What task are they performing? What software version do they have?

### Challenge
Windows users struggling with tasks had to leave their context to search for help — breaking their flow and often leading to frustration. Search engines didn't leverage contextual information like device type, current task, or software version. For identical queries and answers, satisfaction levels varied significantly — the missing element was user context.

### Problem points
- Users had to leave their workflow to search for help externally
- Difficulty formulating effective search queries
- Uncertainty about what and how to search
- Repetitive back-and-forth navigation without finding solutions
- Same query + same answer = different satisfaction levels depending on context

### Process
- Identified the most common help-seeking moments in Windows 10
- Discovered that users rely on 3 elements: primary title, source URL, and secondary metadata
- Found the key insight: satisfaction varies for identical query-answer pairs — context is the missing variable
- Identified data sources: user location, task intent, and all contextual device information
- Designed contextual help overlays and OS-integrated scenarios

### Solution highlights
- **Conversational search** — guided dialogue to narrow down specific issues
- **OS Settings integration** — dynamic top-queried questions aligned with Windows Settings pages
- **Error-based assistance** — non-deterministic entry points for contextual help
- **Trending issue notifications** for OS updates

### Solution
A contextual help system that surfaces relevant guidance within the user's current task using device context, location, and task intent. Includes conversational search interfaces, dynamic integration with Windows Settings pages, and future scenarios for error-based assistance and trending issue notifications — all without requiring users to leave their workflow.

### Impact
- In-context help without leaving the workflow
- Progressive disclosure from quick tips to detailed guides
- Enhanced relevance through device and OS context
- Paved the way for multi-entry point search from within the OS

### Reflection
The best help is the kind you don't have to ask for. Contextual design means being there at the right moment — not before, not after.

### Key learning
This project was the natural evolution of Tech Help on Bing — deeper impact required integrating help directly into user workflows rather than waiting for them to search.
