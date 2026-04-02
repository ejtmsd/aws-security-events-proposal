# AWS Security Experience — Proposal Website
## Claude Code Build Brief

This file is the single source of truth for building `index.html`. Reference `styles.css` for the design system and `CREATIVE_DIRECTION.md` for aesthetic decisions. All content, component specs, image placeholder instructions, and build directives are below.

---

## Project Setup

- Output: single `index.html` file (vanilla HTML/CSS/JS, no build step, no framework)
- Fonts: load from Google Fonts — `Syne` (700, 800) for headings, `DM Sans` (300, 400, 500, 600) for body, `DM Mono` (400, 500) for labels, data, and code
- All styles from `styles.css` via `<link>` tag
- The interactive venue estimator (see Section 16) is self-contained vanilla JS, inlined in `<script>` at bottom of body
- Sticky top nav with smooth scroll to section anchors
- No external JS dependencies except Google Fonts

---

## Global Layout Rules

- Max content width: 1080px, centered, padding 0 24px
- Section vertical padding: 96px top/bottom (64px on mobile)
- All sections have `id` anchors matching the nav
- Image placeholders: `<div class="img-placeholder" data-label="[LABEL]">` — style as dark bordered boxes with centered label text. When the user drops an image file into the folder with the matching filename, it replaces the placeholder via `<img>` tag
- Image filenames are specified per section below

---

## Navigation

Sticky top bar. Left: 24 Seven Agencies wordmark (text, not image). Right: anchor links.

Links (text → anchor):
- Overview → `#overview`
- Experience → `#experience`
- Layers → `#layers`
- Production → `#production`
- Budget → `#budget`
- Case Study → `#case-study`
- About → `#about`

---

## Section 1 — Hero (`#hero`)

Full viewport height. Dark background with the proposal's blue-to-lavender gradient as a large diagonal overlay element (not a background fill — a positioned pseudo-element or div). 

**Content:**
```
Eyebrow label (DM Mono, small caps):
  Amazon Web Services · Proposal · February 2026

H1 (Syne 800, very large — 72px desktop / 44px mobile):
  Welcome to an
  Invite-Only AWS
  Security Experience

Subheadline (DM Sans 300, 22px):
  A Security Ops Simulation with Networking and World-Class
  Keynotes, for Security Execs — Produced by 24 Seven Agencies

CTA row:
  [View Proposal ↓]  (smooth scrolls to #overview)
  
Partner logos row (text-based, DM Mono, small, muted):
  The Sage Group  ·  SketchDeck  ·  Futureman
  A 24 Seven Company
```

**Image placeholder:**
- File: `hero-bg.jpg`
- Usage: full-bleed background image behind gradient overlay, `object-fit: cover`
- Placeholder label: `Hero Background — Event Photography`

---

## Section 2 — Document Overview (`#overview`)

Two-column layout: left column (40%) is a section label block, right column (60%) is content.

**Content:**
```
Section label (DM Mono, eyebrow):
  Document Overview

Intro paragraph:
  The AWS Security team is evaluating agency partners to help with turnkey event production. As part of this process, you've asked us how we might have produced the recent Gen-AI Security Symposium that took place in New York.

Subheading: Event Objectives

Numbered list:
  1. Deliver a differentiated boutique-style event for Data, IT, and Cybersecurity executives that positions AWS, alongside curated Partners, as the thought leader in Generative AI Security and Governance.
  2. Ability to reproduce the event in other locations.
  3. Produce a remarkable experience that leads to executives talking about AWS with their teams, and elevates their affinity to AWS Security Solutions.

Subheading: In This Proposal

List (styled as icon + text rows, use → arrow as icon):
  → Full experience walkthrough and attendee touchpoints
  → Event production logistics
  → Budget summary
  → Case study
```

---

## Section 3 — Executive Summary (`#executive-summary`)

Full-width image above, then two-column text below (50/50).

**Image placeholder:**
- File: `exec-summary.jpg`
- Placeholder label: `Executive Summary — Event Photography`
- Full content width, 480px tall, `object-fit: cover`

**Content:**
```
Section label: Executive Summary

Left column:
  This proposal reimagines the AWS Security Symposium as an immersive, invite-only security ops experience that combines a VR activity, audience participation moments leveraging our "command center" concept, conventional keynote sessions, and networking.

Right column:
  Pull quote (styled prominently, bordered left accent line):
    "People forget up to 70% of new information within 48 hours when learning is passive."
    — Ebbinghaus Forgetting Curve, reinforced by modern learning science

  Body text:
    The experience we propose replaces passive consumption with applied participation. Executives practice judgment under pressure using realistic scenarios, shared constraints, and AWS-native services. The result is stronger recall, shared mental models, and greater remarkability for AWS Security events.
```

---

## Section 4 — Strategic Rationale (`#strategic-rationale`)

Section label + intro, then a two-panel comparison card, then the "format mirrors real incidents" block.

**Content:**
```
Section label: Strategic Rationale

Intro:
  Senior security leaders lack safe environments to test their judgment with their peers across other organizations.

Comparison cards (side by side, styled as contrasting panels):

  LEFT PANEL — "Most executive events optimize for:" (muted, slightly faded style)
    · Awareness
    · Thought leadership
    · Brand exposure

  RIGHT PANEL — "Our experience optimizes for:" (accent/highlighted style)
    · Decision-making under uncertainty
    · Prioritization when tradeoffs are unavoidable
    · Coordination across incomplete information

Format mirrors real-world security incidents (3-column stat/fact cards):
  Card 1: "No one has full visibility"
  Card 2: "Time pressure forces imperfect choices"
  Card 3: "Outcomes depend on collaboration"

Closing line (large, centered, Syne):
  Executives leave with muscle memory. And with a good story to tell.
```

---

## Section 5 — Why This Approach Works (`#why-it-works`)

Three principle cards in a row. Each card has a number, principle name, and explanation.

**Content:**
```
Section label: Why This Approach Works

Intro:
  Traditional symposium formats rely on listening, note-taking, and post-event recall. These methods are poorly suited to complex, high-stakes domains like AI security. This experience applies three evidence-backed principles:

Principle Cards:

  01 / Active Recall Beats Passive Exposure
  Making decisions — even imperfect ones — dramatically improves retention versus listening alone.

  02 / Emotional Stakes Anchor Memory
  Time pressure, team dependency, and visible outcomes create recall anchors that slides do not.

  03 / Social Accountability Reinforces Learning
  Group progression and shared success or failure increase focus and commitment.

Closing emphasis line:
  The sum of these principles makes for a more remarkable experience.
```

---

## Section 6 — Audience & Format (`#audience`)

Left: specs as a clean data table. Right: image placeholder.

**Image placeholder:**
- File: `audience.jpg`
- Placeholder label: `Audience — Networking Photography`
- Height: 520px

**Content:**
```
Section label: Audience & Format

Spec rows (label → value, DM Mono labels):
  Audience Size      →  20–30 senior executives
  Target Roles       →  CIO, CISO, Chief Data Officer, Chief AI Officer, senior IT and security leaders
  Format             →  Invite-only, closed-door, no press, no recording
  Duration           →  One full day
  Optional           →  Evening reception or private dinner

Body text:
  The tone is intentionally restrained. The experience is serious, focused, and credible. Participation is required, but no individual is singled out or put on stage.
```

---

## Section 7 — Experience Architecture (`#experience`)

Section intro, then 3-layer summary cards (horizontal scroll on mobile). This is a hub that introduces the three layers before their dedicated sections.

**Content:**
```
Section label: Experience Architecture

Intro:
  Core symposium elements remain intact — keynote speakers, expert presentations, technical deep dives, partner perspectives, and executive networking. On top of this foundation, we introduce a 3-layer experience system that fundamentally changes how attendees engage with AI security concepts.

Layer cards (3 cards, visually bold, link-style to layer sections):

  Layer 01 · Command Center
  A private, invite-only web platform. The operational backbone of the event.
  → View details

  Layer 02 · Security Clearance
  DEFCON-style NFC badges. Clearance levels unlock as the room participates.
  → View details

  Layer 03 · Field Training
  Immersive VR security games tied directly to keynote content.
  → View details

Connecting note:
  Each layer is triggered directly by agenda content and speaker sessions. No layer exists in isolation.
```

---

## Section 8 — Layer 01: Command Center (`#command-center`)

Full-width image, then content below. Layer number badge visible.

**Image placeholder:**
- File: `command-center.jpg`
- Placeholder label: `Command Center — Platform Screenshot or Event Photo`
- Full width, 440px tall

**Content:**
```
Layer badge: 01
Section label: Command Center
Subheading: Private Interactive Platform

Intro:
  The Command Center is a private, invite-only web platform that acts as the operational backbone of the event. All attendees are onboarded before the symposium. Access is restricted to registered participants and approved AWS stakeholders.

The platform functions as:
  · A secure group chat for moderated discussion
  · A live polling and voting system during sessions
  · A mechanism for pushing prompts tied to speaker content
  · A real-time visualization layer for aggregate responses shown in the room

Body:
  Speakers use the platform to activate the audience during their sessions. Prompts are designed to force prioritization and judgment calls — not trivia or opinion polling. Moderators surface patterns, disagreements, and edge cases from responses and feed them back into the discussion.

  This creates a continuous feedback loop between content and audience, and demonstrates secure, AI-mediated communication in practice.
```

---

## Section 9 — Layer 02: Security Clearance (`#security-clearance`)

Image right, content left (50/50 reverse layout vs Section 8).

**Image placeholder:**
- File: `security-badge.jpg`
- Placeholder label: `Security Clearance Badge`
- Height: 560px, `object-fit: contain` (the badge product shot)

**Content:**
```
Layer badge: 02
Section label: Security Clearance

Intro:
  Each attendee receives a DEFCON-style badge at check-in. The badge is locked by default. It represents the attendee's security clearance level throughout the symposium.

Badge technology (horizontal tag list):
  Physical Buttons  ·  NFC  ·  LEDs  ·  Sensors  ·  Haptic Feedback

Body:
  Progression is driven by engagement. When the room reaches predefined thresholds — a percentage of attendees voting in a poll or completing a discussion prompt — clearance levels unlock for everyone.

  Badges notify individual attendees when new challenges or Field Training modules become available. This directs flow without relying on stage announcements or manual coordination.

  The badge serves as a physical representation of security by design. It turns abstract security principles into a tangible artifact that evolves throughout the event.
```

---

## Section 10 — Layer 03: Field Training (`#field-training`)

Full-width image, then content + scenario grid.

**Image placeholders:**
- File: `field-training-vr.jpg` — Placeholder label: `Field Training — VR Headset Photo` — Full width, 440px
- File: `field-training-team.jpg` — Placeholder label: `Field Training — Team Collaboration` — Half width, 360px (sits alongside scenario list)

**Content:**
```
Layer badge: 03
Section label: Field Training
Subheading: Interactive VR Security Game

Intro:
  Field Training is the most immersive component of the symposium. We evolve the VR game Keep Talking and Nobody Explodes into an AI security-themed experience customized for AWS. Teams of four to five rotate through during the day, or participate in a full group breakout.

How It Works — 3-column layout:

  The Challenge
  One team member wears a VR headset and faces a virtual device composed of AI security modules that must be defused under time pressure. That participant cannot solve the challenge alone.

  The Collaboration
  Other team members hold physical instruction manuals customized with AWS services, security concepts, and decision logic. They cannot see what the VR participant sees. Success depends entirely on communication, prioritization, and trust under pressure.

  The Outcome
  When a team completes or fails a scenario, results feed back to the Command Center leaderboard — sparking discussion around which strategies worked, which failed, and why.

Scenarios grid (5 cards, icon + label):
  ⬡ AI model vulnerabilities and failure modes
  ⬡ Cloud infrastructure breach containment
  ⬡ Identity and access management threats
  ⬡ Data exfiltration prevention
  ⬡ Adversarial attack mitigation

Closing note (muted, italic):
  The experience is designed to be high pressure but not performative. No individual carries the success or failure of the team.
```

---

## Section 11 — How the Three Layers Work Together

Narrative section — no image. Dark background panel (alternate surface color). Full-width callout style.

**Content:**
```
Section label: The Layers in Action

Scenario narrative (styled as a step-by-step sequence — use numbered steps with connecting visual lines):

  Step 1 — KEYNOTE TRIGGER
  A speaker introduces the concept of "AI model poisoning" during a keynote.

  Step 2 — COMMAND CENTER ACTIVATES
  The platform immediately pushes a live poll: "Which AWS service would you deploy first to detect this threat?" Attendees vote and discuss in the secure chat.

  Step 3 — SECURITY CLEARANCE UNLOCKS
  Collective participation reaches the threshold. Badge LEDs shift from red to yellow across the room, signaling a clearance level upgrade.

  Step 4 — FIELD TRAINING TRIGGERED
  Individual badges vibrate: "You have unlocked VR Module 3: Model Integrity Breach."

  Step 5 — DEBRIEF FEEDS BACK
  Teams complete or fail the scenario. Results push to the Command Center leaderboard. Discussion resumes — grounded in live data from the room.

Closing emphasis:
  The result is keynote content that is immediately tested, applied, gamified, and socially reinforced — through three complementary channels working in concert.
```

---

## Section 12 — Speaker Sessions (`#speaker-sessions`)

Brief section. Light treatment.

**Content:**
```
Section label: Speaker Sessions

Body:
  The venue will be set up for speaker sessions alongside the VR activity. Speaker sessions serve as a critical draw for invited executives and strategic partners — invitees will look for top-tier names and logos on the event invite. All speaker content is designed to integrate directly with the three experience layers.
```

---

## Section 13 — Lead Management & Executive Journey (`#lead-management`)

Two-column: Base Services (left) and Optional Upgraded Services (right). Use accordion or tab toggle to handle content depth.

**Content:**
```
Section label: Lead Management & Executive Journey

Intro:
  We manage the executive journey from invitation through post-event handoff — ensuring disciplined communication, accurate attendance tracking, and structured transfer to AWS sales stakeholders.

BASE SERVICES (always included):

  Invitation & Registration
  · Secure, agency-managed registration landing page
  · Automated RSVP confirmation with calendar invite (.ics)
  · Automated reminder cadence (7-day and 24-hour)
  · Real-time RSVP tracking dashboard
  · Data capture aligned to AWS-required fields
  · Secure data storage and deletion policy

  AWS Stakeholder Coordination
  · Kickoff alignment email to AWS sales stakeholders
  · Final confirmed attendee list shared 72 hours prior

  Onsite Attendance Capture
  · Digital check-in with attendance tracking
  · Reconciliation of RSVP vs actual attendance

  Post-Event Communication
  · Thank-you email within 24 hours
  · Secure CSV handoff for Salesforce upload

OPTIONAL: Executive Sourcing & Upgraded Lead Management

  Targeted Executive Sourcing
  · Curated target account list (1,000–1,200 executive contacts)
  · Contact enrichment and quality control
  · Coordination with AWS sales for priority account alignment
  · Speaker and partner co-invite amplification

  Multi-Touch Outreach Cadence
  · Initial invite + two additional reminder emails
  · 48-hour logistics confirmation
  · Segmented messaging for priority accounts
  · LinkedIn InMail for high-value contacts (up to 100)

  Post-Event Meeting Conversion Enablement
  · Attendee preview list to AWS sellers (48 hours prior)
  · "Sorry we missed you" no-show outreach
  · Two-touch follow-up for unbooked attendees
  · 7-day post-event conversion summary

  Data Governance
  · Role-based access controls
  · Secure CSV delivery in AWS-approved format
  · Data deletion policy on request
```

---

## Section 14 — Turnkey Production Deliverables (`#production`)

Numbered list, 6 categories. Use an expandable accordion per category on mobile. On desktop, show all expanded.

**Content:**
```
Section label: Turnkey Event Production Deliverables

1. Experience & Content Strategy
  · Event narrative and thematic framing aligned to AWS Security priorities
  · Agenda architecture and session sequencing
  · Integration of speaker content with experiential systems
  · Scenario design tied to real AWS security use cases
  · Run-of-show development mapped to system triggers
  · Speaker briefing documents
  · Moderator runbooks and facilitation guides
  · Presentation template for AWS speakers
  · Event landing page designed and copywritten

2. Experience Systems
  · Command Center live chat and polling platform
  · Security Clearance badge system (30 units)
  · Field Training VR simulation modules
  · System configuration and pre-event testing
  · On-site technical setup and support
  · Post-event system debrief and insights capture

3. Base Lead Management Services
  · Secure RSVP registration environment setup
  · Invitation drafting and email copy
  · Initial invite deployment + one reminder
  · RSVP tracking and approval workflow
  · Automated calendar invite upon confirmation
  · Kickoff alignment email to AWS sales stakeholders
  · Final attendee list 72 hours prior
  · Digital onsite check-in and reconciliation
  · Thank-you email within 24 hours
  · Secure attendee data export for Salesforce

4. Optional: Upgraded Lead Management Services
  · Two additional reminder emails
  · 48-hour pre-event logistics confirmation
  · Attendee preview list 48 hours prior
  · Seller outreach prompt email
  · Pre-event stakeholder briefing summary
  · "Sorry we missed you" to no-shows
  · Meeting conversion tracking (7-day readout)
  · High-touch meeting scheduling assistance

5. Production & Operations
  · Venue sourcing and negotiation
  · Space planning and layout design
  · AV coordination and technical production management
  · Dedicated Wi-Fi coordination
  · Catering and hospitality planning
  · Vendor management (AV, fabrication, print)
  · Budget tracking and cost reconciliation
  · Night-before load-in planning
  · On-site staffing: Executive producer, 3 event staff, 1 additional facilitator

6. Data Governance & Reporting
  · Role-based access controls
  · Secure attendee list transfer
  · Data deletion policy execution if needed
  · No AWS internal systems access if required
  · Internal AWS post-event readout:
    — Attendance metrics
    — Participation patterns
    — Qualitative executive insights
```

---

## Section 15 — Outcomes & Repeatability (`#outcomes`)

Two parts: success metrics, then the repeatability/economics argument.

**Content:**
```
Section label: Outcomes & Repeatability

Success indicators (4 horizontal cards):
  · Executive recall and post-event feedback
  · Depth and consistency of participation throughout the day
  · Post-event engagement with AWS Security resources
  · Internal AWS assessment of format effectiveness

Repeatability block (large callout panel, dark surface):

  Heading: Built to Scale

  Body:
    This format is intentionally built as a reusable executive enablement system. Core experience components are designed once and redeployed with minimal modification — allowing future events to focus on logistics rather than reinvention.

    The initial event carries the highest development investment. Subsequent deployments benefit from lower marginal cost, faster setup, and increased operational confidence.

    Over time, this positions the AWS Security Symposium not as a one-off activation, but as a scalable tactic within AWS Security's engagement playbook.

Attendee Sourcing Assumptions (data table):
  Label                              Value
  Registration target                90 event registrants
  In-room target                     30 attendees
  Executive contact list size        1,000–1,200 targeted contacts
  Expected registration rate         8–10% from curated outreach
  Invite amplification               AWS partners co-leveraged

Meeting Conversion Target (bold callout stat):
  40% follow-up meeting conversion within 30 days
  ≈ 12 post-event sales meetings from a 30-person audience

Assumptions note (small, muted):
  Assumes AWS participation onsite, pre-aligned target account prioritization, and timely post-event outreach ownership by AWS sales teams.
```

---

## Section 16 — Services Budget Summary (`#budget`)

Clean table section, dark surface.

**Content:**
```
Section label: Services Budget Summary

Budget table:

  Category                                             First Event    Repeat Events
  ─────────────────────────────────────────────────────────────────────────────────
  Experience Systems                                   $40,000        $10,000
    Command Center platform                            $12,000
    Security Clearance badges (30 units)               $20,000
    Field Training VR simulation + custom scenarios    $8,000

  Content & Production Services                        $39,000        $39,000–$71,000

  Optional: Executive Sourcing & Upgraded              $32,000        $32,000
  Lead Management

  ─────────────────────────────────────────────────────────────────────────────────
  All-In Total (with upgraded lead mgmt)               $111,000
  All-In Total (without upgraded lead mgmt)            $79,000
  Repeat events (range)                                               $49,000–$81,000

  Excludes venue and F&B costs.

Note block (muted, italic):
  A conventional symposium without experience systems, with base lead management, is available for ~$40,000 excluding venue and food costs.
```

---

## Section 17 — Estimated Venue & Hospitality Costs (`#venue-costs`)

**This section contains the interactive JavaScript estimator. Build it as a fully self-contained component.**

### Static intro (always visible):

```
Section label: Estimated Venue & Hospitality Costs

Intro paragraphs:
  The following ranges reflect directional planning estimates for venue, food and beverage, and technical requirements for a 30-person executive symposium. Pricing varies meaningfully depending on timing and location — particularly during Black Hat week in Las Vegas, where venue demand, service minimums, and labor costs increase.

  These estimates are based on current Las Vegas market benchmarks and comparable executive-level events. Final costs will be validated through a formal venue RFP process once date, footprint, and experience requirements are confirmed.

  The goal of this model is to provide transparent planning guardrails while maintaining flexibility as venue selection is finalized.
```

### Static reference table (shown above the interactive section):

```
                  Black Hat Low   Black Hat High   General Event Low   General Event High
Subtotal — Venue     $10,000        $25,000              $3,000             $20,000
Subtotal — F&B       $12,740        $24,050             $11,180             $19,500
Subtotal — Fees       $8,400        $19,700              $6,300             $13,600
TOTAL                $31,140        $68,750             $20,480             $53,100
```

### Interactive Regional Estimator Component

Label this section with a divider and heading: **"Regional Cost Estimator — Other Markets"**

Subtext: Select a region to see directional venue and hospitality estimates relative to the Las Vegas baseline.

#### Component behavior:
- Region selector: pill/tab buttons, one selected at a time
- On selection: cost breakdown animates/updates to show Low and High estimates
- Show: Venue / F&B / Extra Fees / Total rows
- Show: "vs. Las Vegas General Event" delta (colored green if cheaper, amber if similar, red if more expensive)
- Show: "Generate Market Context" button that calls Anthropic API for 3-sentence market rationale
- All Regions bar chart at bottom (sortable by low estimate)

#### Region data (apply multipliers to LV General baseline: Venue $3k/$20k, F&B $11,180/$19,500, Extra $6,300/$13,600):

```javascript
const BASE = {
  venue: { low: 3000, high: 20000 },
  fb:    { low: 11180, high: 19500 },
  extra: { low: 6300, high: 13600 }
};

// multipliers: [low_multiplier, high_multiplier]
const REGIONS = [
  {
    id: "lv-blackhat",
    label: "Las Vegas",
    sublabel: "Black Hat Week",
    flag: "🎰",
    multipliers: { venue: [3.33, 1.25], fb: [1.14, 1.23], extra: [1.33, 1.45] },
    note: "Premium demand / conference week pricing",
    color: "#f59e0b"
  },
  {
    id: "lv-general",
    label: "Las Vegas",
    sublabel: "General Event (Baseline)",
    flag: "🎰",
    multipliers: { venue: [1.0, 1.0], fb: [1.0, 1.0], extra: [1.0, 1.0] },
    note: "Baseline reference",
    color: "#6b7280",
    isBaseline: true
  },
  {
    id: "tier1-us",
    label: "Tier-1 US City",
    sublabel: "NYC · SF · DC · Chicago · Boston",
    flag: "🏙️",
    multipliers: { venue: [2.0, 2.5], fb: [1.25, 1.45], extra: [1.3, 1.5] },
    note: "Premium urban market — venue scarcity drives cost",
    color: "#3b82f6"
  },
  {
    id: "tier2-us",
    label: "Tier-2 US City",
    sublabel: "Austin · Denver · Nashville · Atlanta",
    flag: "🌆",
    multipliers: { venue: [0.9, 1.3], fb: [0.95, 1.15], extra: [0.9, 1.1] },
    note: "Growing event markets with competitive pricing",
    color: "#10b981"
  },
  {
    id: "london",
    label: "London",
    sublabel: "United Kingdom",
    flag: "🇬🇧",
    multipliers: { venue: [2.0, 2.8], fb: [1.3, 1.6], extra: [1.4, 1.7] },
    note: "High labor costs and premium venue demand",
    color: "#8b5cf6"
  },
  {
    id: "western-europe",
    label: "Western Europe",
    sublabel: "Paris · Amsterdam · Frankfurt · Zurich",
    flag: "🇪🇺",
    multipliers: { venue: [1.4, 2.0], fb: [1.2, 1.5], extra: [1.2, 1.5] },
    note: "Strong service standards, elevated F&B minimums",
    color: "#06b6d4"
  },
  {
    id: "southern-europe",
    label: "Southern Europe",
    sublabel: "Barcelona · Madrid · Lisbon · Milan",
    flag: "🌅",
    multipliers: { venue: [0.8, 1.4], fb: [0.9, 1.2], extra: [0.85, 1.15] },
    note: "High-quality venues at competitive rates",
    color: "#f97316"
  },
  {
    id: "latam",
    label: "Latin America",
    sublabel: "Mexico City · São Paulo · Bogotá",
    flag: "🌎",
    multipliers: { venue: [0.5, 0.85], fb: [0.65, 0.9], extra: [0.6, 0.85] },
    note: "Significant cost reduction vs US markets",
    color: "#ec4899"
  },
  {
    id: "apac1",
    label: "APAC Tier-1",
    sublabel: "Singapore · Tokyo · Sydney · Hong Kong",
    flag: "🌏",
    multipliers: { venue: [1.3, 2.0], fb: [1.1, 1.5], extra: [1.15, 1.4] },
    note: "World-class executive venues, premium pricing",
    color: "#14b8a6"
  },
  {
    id: "apac2",
    label: "APAC Tier-2",
    sublabel: "Bangkok · Kuala Lumpur · Manila",
    flag: "🏝️",
    multipliers: { venue: [0.4, 0.75], fb: [0.55, 0.8], extra: [0.55, 0.75] },
    note: "Substantial savings, strong hospitality infrastructure",
    color: "#84cc16"
  },
  {
    id: "middle-east",
    label: "Middle East",
    sublabel: "Dubai · Riyadh · Abu Dhabi",
    flag: "🕌",
    multipliers: { venue: [1.1, 1.8], fb: [1.05, 1.4], extra: [1.1, 1.5] },
    note: "World-class facilities, government hospitality minimums",
    color: "#fbbf24"
  }
];
```

#### Anthropic API call for market context button:

```javascript
// When user clicks "Generate Market Context" for a selected region:
const response = await fetch("https://api.anthropic.com/v1/messages", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({
    model: "claude-sonnet-4-20250514",
    max_tokens: 1000,
    messages: [{
      role: "user",
      content: `You are helping build a venue and hospitality cost estimator for a 30-person executive security symposium being pitched to AWS. Write a concise 3-sentence market context note for hosting this event in: ${region.label} (${region.sublabel}). Cover: (1) what drives venue and hospitality pricing in this market, (2) one logistical or operational consideration for an executive audience, (3) one strategic advantage or tradeoff compared to a US event. Be specific and direct. No filler.`
    }]
  })
});
const data = await response.json();
const text = data.content?.find(b => b.type === "text")?.text || "";
```

Cache the result per region in a JS object so the API is only called once per region per session.

#### Component layout structure:

```
[Region selector — horizontal pill buttons, wrapping]

[Selected region panel]
  Region name + flag + sublabel
  Total range (large, colored)
  
  Breakdown table:
    Row: Venue       [low bar]  $X – $Y
    Row: F&B         [low bar]  $X – $Y
    Row: Extra Fees  [low bar]  $X – $Y
    ─────────────────────────────────
    Row: TOTAL (bold)           $X – $Y
  
  vs. Las Vegas General callout (green/amber/red)
  
  [Generate Market Context] button → loading → 3-sentence text

[All Regions — Ranked by Low Estimate]
  Horizontal bar chart, all 11 regions, clickable to select
```

---

## Section 18 — Case Study (`#case-study`)

Dark alternate background. Image gallery + text.

**Image placeholders:**
- File: `case-study-hero.jpg` — full width, 420px tall — label: `LifeWave Experience Center — Hero`
- File: `case-study-1.jpg` — 1/3 width — label: `LifeWave — Interactive Kiosks`
- File: `case-study-2.jpg` — 1/3 width — label: `LifeWave — Immersive Environment`
- File: `case-study-3.jpg` — 1/3 width — label: `LifeWave — Product Display`

**Content:**
```
Section label: Case Study

Heading:
  Transforming a Welcome Center into an Immersive Spaceship for LifeWave

Client badge: Futureman · A 24 Seven Company

Body:
  Futureman, a 24 Seven Agency, partnered with LifeWave, a global health company, to design a flagship Experience Center for high-value customers. The objective was to replace one-way presentations with an immersive, self-directed environment that allowed visitors to control their depth of learning while reinforcing LifeWave's innovation narrative.

  The experience unfolded as a structured, multi-room journey — combining shared moments such as a founder welcome delivered via a life-size, language-localized hologram and an immersive brand storytelling environment, with hands-on product exploration through interactive kiosks and a forward-looking roadmap space.

  The program required close integration across physical design, digital platforms, content, and live operations — with an emphasis on reliability and clarity rather than spectacle alone.

Relevance callout (bordered panel):
  This experience was designed as a reusable system, with modular content and interaction models that scale across audiences, regions, and future deployments — the same architectural principle underlying our proposal for AWS Security.
```

---

## Section 19 — About 24 Seven Agencies (`#about`)

**Image placeholder:**
- File: `work-collage.jpg` — full width, 400px — label: `24 Seven Work Portfolio`

**Content:**
```
Section label: About 24 Seven Agencies

Headline (Syne):
  One Partner. Every Discipline.

Body:
  24 Seven Agencies is an integrated group of three specialized agencies — Futureman, SketchDeck, and Markacy — designed to support complex work that requires tight coordination across strategy, creative, technology, and execution.

  We regularly operate as an extension of internal teams, owning programs end to end while reducing vendor sprawl and operational overhead. Our model combines senior-led strategy, on-demand creative and production capacity, and dedicated technical and operational teams — allowing us to scale up or down without sacrificing quality or control.

  For AWS, this means a single accountable partner that can design the experience, build the systems, produce the assets, and run the event with the rigor and reliability expected in high-stakes environments.

3-stat row (large numbers, DM Mono):
  200+     In-house dev      Direct access
  creatives  & AI innovation  to talent via
  & marketers                  24 Seven

Client logo row (text-only, DM Mono, small, spaced out, muted):
  amazon  ·  Google  ·  McDonald's  ·  Spotify  ·  ADP  ·  Salesforce  ·  Microsoft  ·  Snapchat

Agency logos (text-based):
  The Sage Group  ·  SketchDeck  ·  Futureman
  A 24 Seven Company
```

---

## Footer

```
Left: sketchdeck.com
Center: © 2026 24 Seven Agencies. All rights reserved.
Right: Prepared for Amazon Web Services · February 2026
```

---

## Implementation Notes for Claude Code

1. **Image placeholder style**: dark `#0d1128` background, `1.5px dashed #2a3560` border, centered label in `DM Mono` 11px `#3a4a7a`. When actual image file exists in folder, wrap in `<img>` tag instead. Use `data-placeholder-file="filename.jpg"` attribute on every placeholder div.

2. **Interactive estimator**: build as a self-contained `<div id="venue-estimator">` with all JS in a `<script>` block at bottom of `<body>`. No external dependencies. Use CSS transitions for number updates (brief fade). Fetch API for the Anthropic call. Handle loading and error states gracefully.

3. **Smooth scroll**: all nav links use `scroll-behavior: smooth` on `html`. Active section tracking via `IntersectionObserver` — highlight nav item when section is in view.

4. **Mobile**: single-column below 768px. Nav collapses to hamburger. Region selector wraps. Tables scroll horizontally.

5. **Accessibility**: semantic HTML (`<main>`, `<section>`, `<nav>`, `<article>`). All images have `alt` text. Color contrast minimum AA. Focus states visible.

6. **Performance**: no unused JS. Font preconnect in `<head>`. Images lazy-loaded.

7. **Do not** include a back-to-top button, cookie banner, or any decorative elements not specified above.

8. **Section alternation**: odd sections use `--bg` (`#07091a`), even sections use `--bg-2` (`#0d1128`). The three-layers-in-action section (Section 11) always uses a distinct dark surface (`--surface`). Case study always uses `--bg-2`.
