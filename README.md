# Auto Repair Service Advisor
### An ICM Specialist for Independent Shop Owners

---

## What This Is

A Claude specialist that translates what your technician
found into language your customer can act on.

You describe the repair the customer came in for and what
the technician found. The specialist writes the customer
conversation — spoken or text — in plain language that
informs without pressuring, explains without condescending,
and respects whatever the customer decides.

Built for independent shop owners who do great work and
lose customers anyway because nobody explained it right.

---

## The Problem It Solves

The communication gap in auto repair isn't usually about
honesty. It's about translation.

A technician finds a cracked CV axle boot. They know
exactly what it means — grease loss, joint wear, eventual
shaft failure. They write it on the estimate and hand it
to the service advisor. The service advisor tells the
customer "your CV boot is cracked and needs to be replaced."

The customer hears: *I'm being sold something I didn't
come in for.*

The finding was real. The recommendation was legitimate.
The customer left without approving it and didn't come back.

This specialist closes that gap. It takes what the
technician found and builds the conversation that helps
the customer understand — not just what is wrong, but
what it does, what happens if it waits, and what their
actual options are.

A customer who understands makes a real decision.
A customer who was just given a part name and a price
is guessing.

---

## How to Use It

**Step 1:** Drop the `auto-repair-service-advisor/` folder
into a Claude Project.

**Step 2:** Load the specialist with this prompt:

```
You are the Auto Repair Service Advisor described in
identity.md. Follow the rules in rules.md. Draw from
the examples in examples.md and the reference files
in reference/ when building your response.
```

**Step 3:** Give the specialist a scenario in this format:

```
Customer came in for: [primary repair]
What the technician found: [finding in plain terms]
Delivery method: [spoken / text message / written note]
```

**Step 4:** The specialist returns customer-ready language
structured around the primary repair first, the finding
second, the consequence third, and the decision last.

---

## Example Input

```
Customer came in for: oil change
What the technician found: serpentine belt is visibly
cracking along the ribs
Delivery method: spoken
```

## Example Output

*"While we had your car up for the oil change, your
technician noticed your serpentine belt has started
cracking. I want to show you what he found before
you leave.*

*The serpentine belt runs everything off your engine —
your alternator, your power steering, sometimes your AC.
The problem with a cracked belt isn't that it's cracked
today. It's that it doesn't give much warning before
it goes.*

*When it breaks, it usually breaks completely. Depending
on your car, that could mean losing power steering while
you're driving, your battery not charging, or your engine
shutting down.*

*We're not saying it'll go today. We're saying we can't
tell you when — and we'd rather you know now than find
out on the highway.*

*The repair is [price]. We can do it today while the car
is already here, or we can schedule it. What would you
like to do?"*

---

## What's in the Folder

```
auto-repair-service-advisor/
├── identity.md        — who the specialist is and what
│                        it believes about communication
├── rules.md           — how it structures and delivers
│                        every response
├── examples.md        — six full scenarios showing the
│                        specialist in action, including
│                        how it handles a customer who
│                        says no
└── reference/
    ├── consequence-language.md      — 20 common findings
    │                                  with plain-language
    │                                  consequence frameworks
    │                                  and honest urgency ratings
    ├── common-findings-by-repair-type.md — what technicians
    │                                  commonly find during
    │                                  9 primary repair types
    ├── trust-signals-vs-pressure-signals.md — side-by-side
    │                                  language reference for
    │                                  every stage of the
    │                                  customer conversation
    └── customer-objection-responses.md — 7 common objections
                                       with full handling
                                       frameworks and what
                                       not to say
```

---

## Why It's Built This Way

Each file does one job.

`identity.md` tells Claude who it is. `rules.md` tells
Claude how to behave. `examples.md` shows Claude what
good looks like. The `reference/` files give Claude the
knowledge to draw from.

None of them overlap. That's intentional.

This is Interpretable Context Methodology — folder as
architecture. Each file is readable on its own. The
structure tells you what's where before you open anything.
A teammate, a contractor, or a future version of you
can clone this, read the README, and be productive in
five minutes.

---

## The Communication Framework

The specialist runs on one pattern across every scenario:

```
1. Confirm the primary repair first
2. Name the finding in plain language
3. Explain what the part does before explaining failure
4. State consequence honestly — without exaggerating
5. Acknowledge uncertainty where it exists
6. Offer a decision — never assume agreement
```

This pattern does not change based on the size of the
repair, the age of the customer, or whether they approve
or decline.

A customer who declines gets the same respect and the
same quality of information as one who approves everything.
That's in the rules. It's also in the examples.

---

## Forking This Specialist

This specialist was built for auto repair. The
communication framework it runs on is not.

The pattern — confirm primary, explain the part, state
consequence honestly, acknowledge uncertainty, offer the
decision — applies anywhere a technician, inspector, or
specialist finds more than the customer expected and
needs to communicate it without losing their trust.

**To adapt it for another trade:**

- `identity.md` — replace the auto repair background
  with your domain. Keep the philosophy. It travels.
- `rules.md` — adjust jargon boundaries for your field.
  The structure rules do not change.
- `examples.md` — replace the six scenarios with three
  to six from your domain. Keep the "why it's structured
  this way" notes — they train the voice.
- `reference/consequence-language.md` — rewrite for
  your common findings. Keep the four-part structure:
  what it is, short term, long term, if ignored, urgency.
- `reference/trust-signals-vs-pressure-signals.md` —
  update the examples. The left/right column format
  and the underlying principle travel unchanged.
- `reference/customer-objection-responses.md` — the
  seven objections in this file are not auto-repair
  specific. Most of them will need only minor language
  changes for another trade.

**Trades this structure has been adapted for:**
*(leave blank — let forks fill this in)*

---

## Why This Works for Domains That Aren't Auto Repair

The problem this specialist solves is not a car problem.

It is a knowledge-gap problem. One person knows something
the other person needs to understand in order to make a
good decision. The person with the knowledge uses words
the other person can't evaluate. Trust breaks down.
The right decision doesn't get made.

That gap exists in HVAC, plumbing, home inspection,
medical second opinions, legal consultations, IT support,
financial advising, and anywhere else where expertise
creates distance between the finding and the person
who needs to act on it.

The domain changes. The gap is the same.
The specialist closes it the same way every time:
plain language, honest consequence, real uncertainty,
and a decision that belongs to the customer.

---

*Built using Interpretable Context Methodology.*
*Structure based on Jake Clief's ICM framework.*