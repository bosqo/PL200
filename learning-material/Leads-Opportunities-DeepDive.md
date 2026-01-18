# Leads and Opportunities - Complete Deep Dive
## PL-200 Exam Preparation

---

## Table of Contents
1. [Understanding Leads](#understanding-leads)
2. [Understanding Opportunities](#understanding-opportunities)
3. [Lead to Opportunity Process](#lead-to-opportunity-process)
4. [Key Fields and Attributes](#key-fields-and-attributes)
5. [Business Process Flows](#business-process-flows)
6. [Qualification and Disqualification](#qualification-and-disqualification)
7. [Reporting and Analytics](#reporting-and-analytics)
8. [Common Exam Scenarios](#common-exam-scenarios)

---

## Understanding Leads

### What is a Lead?

A **Lead** represents a **potential customer** who has shown interest in your products or services but hasn't been qualified yet. Think of leads as "raw" prospects that need to be evaluated.

```
┌─────────────────────────────────────────────────────────────────┐
│                         LEAD LIFECYCLE                           │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  1. CAPTURE                                                      │
│     ↓                                                            │
│     Lead enters system (web form, trade show, referral)         │
│                                                                  │
│  2. NURTURE                                                      │
│     ↓                                                            │
│     Follow up, gather information, assess fit                   │
│                                                                  │
│  3. QUALIFY                                                      │
│     ↓                                                            │
│     Determine if lead is worth pursuing                         │
│                                                                  │
│  4. CONVERT                                                      │
│     ↓                                                            │
│     Create Account, Contact, and Opportunity                    │
│                           OR                                     │
│  4. DISQUALIFY                                                   │
│     ↓                                                            │
│     Mark as not a good fit                                      │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Lead Table Ownership

- **User or Team Owned** table
- Each lead is assigned to a specific user (owner)
- Security roles control who can see which leads
- Can be reassigned to different users/teams

### Standard Lead Fields

| Field | Type | Purpose | Example |
|-------|------|---------|---------|
| **Topic** | Text | Main subject/interest | "Interested in CRM solution" |
| **First Name** | Text | Contact first name | "John" |
| **Last Name** | Text | Contact last name | "Smith" |
| **Company Name** | Text | Organization name | "Contoso Ltd" |
| **Job Title** | Text | Contact's role | "IT Director" |
| **Email** | Email | Primary email | "john@contoso.com" |
| **Phone** | Phone | Contact number | "(555) 123-4567" |
| **Lead Source** | Choice | How lead was acquired | Advertisement, Referral, Web |
| **Status** | Choice | Current status | New, Contacted, Qualified |
| **Status Reason** | Choice | Why in this status | New, Not Contacted, Cancelled |
| **Rating** | Choice | Quality indicator | Hot, Warm, Cold |
| **Budget Amount** | Currency | Potential budget | $50,000 |
| **Purchase Timeframe** | Choice | When they'll buy | Immediate, This Quarter, etc. |
| **Description** | Multi-line Text | Additional notes | Details about requirements |
| **Industry** | Choice | Business sector | Technology, Healthcare, etc. |
| **Number of Employees** | Whole Number | Company size | 500 |
| **Annual Revenue** | Currency | Company revenue | $10,000,000 |

### Lead Status Values

```
┌─────────────────────────────────────────────────────────────────┐
│                      LEAD STATUS FLOW                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Status: Open                                                    │
│  ├── Status Reason: New                                         │
│  ├── Status Reason: Contacted                                   │
│  └── Status Reason: Qualified                                   │
│                                                                  │
│  Status: Qualified (System)                                      │
│  └── Status Reason: Qualified                                   │
│      → Lead converted to Account/Contact/Opportunity            │
│                                                                  │
│  Status: Disqualified                                            │
│  ├── Status Reason: Lost                                        │
│  ├── Status Reason: Cannot Contact                              │
│  ├── Status Reason: No Longer Interested                        │
│  └── Status Reason: Cancelled                                   │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Lead Rating

The **Rating** field helps prioritize leads:

| Rating | Meaning | Action Priority |
|--------|---------|----------------|
| **Hot** | Strong interest, ready to buy | Contact immediately |
| **Warm** | Moderate interest, needs nurturing | Follow up soon |
| **Cold** | Low interest or early stage | Long-term nurture |

### Lead Sources

Track where leads come from:

- **Advertisement**: Marketing campaigns
- **Employee Referral**: Internal team referrals
- **External Referral**: Partner or customer referrals
- **Partner**: Channel partners
- **Public Relations**: PR activities
- **Seminar**: Events and seminars
- **Trade Show**: Industry events
- **Web**: Website inquiries
- **Word of Mouth**: Organic referrals
- **Other**: Misc sources

---

## Understanding Opportunities

### What is an Opportunity?

An **Opportunity** represents a **qualified sales deal** with a specific revenue potential. Opportunities track the sales process from initial interest through close.

```
┌─────────────────────────────────────────────────────────────────┐
│                    OPPORTUNITY LIFECYCLE                         │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  1. CREATE                                                       │
│     ↓                                                            │
│     Opportunity created (from Lead or directly)                 │
│                                                                  │
│  2. DEVELOP                                                      │
│     ↓                                                            │
│     Build relationship, understand needs, propose solution      │
│                                                                  │
│  3. PROPOSE                                                      │
│     ↓                                                            │
│     Submit proposal, negotiate terms                            │
│                                                                  │
│  4. CLOSE                                                        │
│     ↓                                                            │
│     Won: Deal is closed successfully                            │
│           OR                                                     │
│     Lost: Deal didn't work out                                  │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Opportunity Table Ownership

- **User or Team Owned** table
- Each opportunity is assigned to a specific user (owner)
- Critical for sales territory management
- Supports team selling scenarios

### Standard Opportunity Fields

| Field | Type | Purpose | Example |
|-------|------|---------|---------|
| **Topic** | Text | Deal name/description | "Contoso CRM Implementation" |
| **Account** | Lookup | Related organization | Link to Account record |
| **Contact** | Lookup | Primary contact | Link to Contact record |
| **Currency** | Lookup | Transaction currency | USD, EUR, GBP |
| **Est. Revenue** | Currency | Expected deal value | $100,000 |
| **Est. Close Date** | Date | When deal will close | 2026-03-31 |
| **Probability** | Percent | Chance of winning | 75% |
| **Status** | Choice | Current status | Open, Won, Lost |
| **Status Reason** | Choice | Why in this status | In Progress, Won, Cancelled |
| **Rating** | Choice | Deal quality | Hot, Warm, Cold |
| **Purchase Timeframe** | Choice | When they'll buy | Immediate, This Quarter |
| **Purchase Process** | Choice | Buying process | Individual, Committee, etc. |
| **Budget Amount** | Currency | Customer's budget | $120,000 |
| **Sales Stage** | Choice | Current stage | Qualify, Develop, Propose, Close |
| **Need** | Choice | Level of need | Must have, Should have, etc. |
| **Originating Lead** | Lookup | Source lead | Link to Lead record |
| **Description** | Multi-line Text | Deal details | Requirements and notes |

### Opportunity Status Values

```
┌─────────────────────────────────────────────────────────────────┐
│                  OPPORTUNITY STATUS FLOW                         │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Status: Open                                                    │
│  ├── Status Reason: In Progress (default)                       │
│  └── Status Reason: On Hold                                     │
│                                                                  │
│  Status: Won (System)                                            │
│  └── Status Reason: Won                                         │
│      → Opportunity closed as successful                         │
│      → Actual Revenue is recorded                               │
│                                                                  │
│  Status: Lost (System)                                           │
│  ├── Status Reason: Cancelled                                   │
│  ├── Status Reason: Out-Sold                                    │
│  └── Status Reason: Lost                                        │
│      → Opportunity closed as unsuccessful                       │
│      → Actual Revenue = $0                                      │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Estimated vs Actual Revenue

```
┌─────────────────────────────────────────────────────────────────┐
│                      REVENUE TRACKING                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  While Opportunity is OPEN:                                      │
│  ┌─────────────────────────────────────────────────────────┐    │
│  │ Est. Revenue: $100,000                                   │    │
│  │ Probability: 75%                                         │    │
│  │ Weighted Revenue: $75,000 (auto-calculated)             │    │
│  │ Actual Revenue: (not set)                                │    │
│  └─────────────────────────────────────────────────────────┘    │
│                                                                  │
│  When Opportunity is WON:                                        │
│  ┌─────────────────────────────────────────────────────────┐    │
│  │ Est. Revenue: $100,000                                   │    │
│  │ Actual Revenue: $95,000 (entered at close)              │    │
│  │ Actual Close Date: 2026-03-15                           │    │
│  │ Status: Won                                              │    │
│  └─────────────────────────────────────────────────────────┘    │
│                                                                  │
│  When Opportunity is LOST:                                       │
│  ┌─────────────────────────────────────────────────────────┐    │
│  │ Est. Revenue: $100,000                                   │    │
│  │ Actual Revenue: $0 (automatically set)                   │    │
│  │ Actual Close Date: 2026-02-20                           │    │
│  │ Status: Lost                                             │    │
│  │ Status Reason: Out-Sold                                  │    │
│  └─────────────────────────────────────────────────────────┘    │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Sales Stages

Opportunities typically move through stages:

| Stage | Description | Activities |
|-------|-------------|------------|
| **Qualify** | Validate opportunity is real | Verify budget, authority, need, timeline (BANT) |
| **Develop** | Understand requirements | Discovery meetings, needs analysis |
| **Propose** | Present solution | Create proposal, demo, pricing |
| **Close** | Finalize deal | Negotiate, handle objections, close |

---

## Lead to Opportunity Process

### The Qualification Process

```
┌─────────────────────────────────────────────────────────────────┐
│              LEAD QUALIFICATION PROCESS                          │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  LEAD                                                            │
│  ┌─────────────────────────────────────────────────────────┐    │
│  │ Company: Contoso Ltd                                     │    │
│  │ Contact: John Smith                                      │    │
│  │ Topic: Interested in CRM                                │    │
│  │ Budget: $100,000                                         │    │
│  │ Timeframe: This Quarter                                 │    │
│  └─────────────────────────────────────────────────────────┘    │
│                          ↓                                       │
│                   [QUALIFY LEAD]                                 │
│                          ↓                                       │
│  ┌─────────────────────────────────────────────────────────┐    │
│  │         SYSTEM CREATES 3 RECORDS:                        │    │
│  │                                                          │    │
│  │  1. ACCOUNT                                              │    │
│  │     Name: Contoso Ltd                                    │    │
│  │     (Organization record)                                │    │
│  │                                                          │    │
│  │  2. CONTACT                                              │    │
│  │     Name: John Smith                                     │    │
│  │     Account: Contoso Ltd                                 │    │
│  │     (Person record)                                      │    │
│  │                                                          │    │
│  │  3. OPPORTUNITY                                          │    │
│  │     Topic: Interested in CRM                             │    │
│  │     Account: Contoso Ltd                                 │    │
│  │     Contact: John Smith                                  │    │
│  │     Est. Revenue: $100,000                               │    │
│  │     Originating Lead: [Lead record]                      │    │
│  │     (Sales deal record)                                  │    │
│  │                                                          │    │
│  └─────────────────────────────────────────────────────────┘    │
│                          ↓                                       │
│  LEAD STATUS → Qualified                                         │
│  (Lead is now closed and linked to new records)                  │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Qualify Lead Action

When you qualify a lead, the system:

**Automatically Creates:**
1. **Account** (if doesn't exist)
   - Uses company information from lead
   - Links to contact and opportunity

2. **Contact** (if doesn't exist)
   - Uses contact information from lead
   - Links to account

3. **Opportunity** (always creates new)
   - Uses topic, budget, and other details
   - Links to account and contact
   - Records originating lead

**Updates Lead:**
- Status → Qualified
- Status Reason → Qualified
- Lead is closed (read-only)
- Maintains link to created records

### Options When Qualifying

```
┌─────────────────────────────────────────────────────────────────┐
│              QUALIFY LEAD OPTIONS                                │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ☑ Create Account                                               │
│     □ Use existing Account: [Search...]                         │
│                                                                  │
│  ☑ Create Contact                                               │
│     □ Use existing Contact: [Search...]                         │
│                                                                  │
│  ☑ Create Opportunity                                           │
│     Opportunity Topic: [Interested in CRM Solution]             │
│                                                                  │
│  Currency: [USD - US Dollar]                                    │
│                                                                  │
│  [Qualify] [Cancel]                                             │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

**Flexibility:**
- Can choose NOT to create Account if it already exists
- Can choose NOT to create Contact if it already exists
- Can choose NOT to create Opportunity if not ready
- Can link to existing Account/Contact records

### When Account/Contact Already Exist

**Scenario**: Lead "Jane Doe" from existing customer "Contoso Ltd"

```
Existing Records:
├── Account: Contoso Ltd (already in system)
└── Contact: Mary Johnson (existing contact)

New Lead:
├── Company: Contoso Ltd
├── Contact: Jane Doe (new person)
└── Budget: $50,000

Qualify Options:
├── Account: ☐ Create new, ☑ Use existing: Contoso Ltd
├── Contact: ☑ Create new (Jane Doe is new)
└── Opportunity: ☑ Create new

Result:
├── Account: Contoso Ltd (existing - no changes)
├── Contact: Jane Doe (NEW - linked to Contoso)
├── Contact: Mary Johnson (existing - no changes)
└── Opportunity: (NEW - linked to Contoso and Jane)
```

### Disqualifying Leads

When a lead is **not** a good fit:

```
┌─────────────────────────────────────────────────────────────────┐
│                    DISQUALIFY LEAD                               │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Status Reason (pick one):                                       │
│  ○ Lost                    → Competitor won                     │
│  ○ Cannot Contact          → Bad contact info                   │
│  ○ No Longer Interested    → Changed mind                       │
│  ○ Cancelled               → Other reasons                      │
│                                                                  │
│  Description (optional):                                         │
│  [Explain why disqualified...]                                   │
│                                                                  │
│  [Disqualify] [Cancel]                                          │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

**Effect:**
- Lead status → Disqualified
- Lead is closed (read-only)
- No records are created
- Lead can be reactivated later if needed

---

## Key Fields and Attributes

### BANT Qualification Framework

**BANT** is a common framework for qualifying leads/opportunities:

| Letter | Stands For | Lead/Opp Field | Question |
|--------|------------|----------------|----------|
| **B** | Budget | Budget Amount | Do they have money? |
| **A** | Authority | Decision Maker fields | Can they make the decision? |
| **N** | Need | Description, Requirements | Do they need our solution? |
| **T** | Timeline | Purchase Timeframe, Est. Close Date | When will they buy? |

### Relationships Between Tables

```
┌─────────────────────────────────────────────────────────────────┐
│              LEAD-OPPORTUNITY RELATIONSHIPS                      │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│                        ACCOUNT                                   │
│                   (Organization)                                 │
│                   ┌──────────┐                                   │
│                   │ Contoso  │                                   │
│                   │   Ltd    │                                   │
│                   └────┬─────┘                                   │
│                        │                                         │
│              ┌─────────┴─────────┐                               │
│              │                   │                               │
│              ▼                   ▼                               │
│         ┌─────────┐         ┌─────────┐                         │
│         │ CONTACT │         │ CONTACT │                         │
│         │  John   │         │  Mary   │                         │
│         │  Smith  │         │ Johnson │                         │
│         └────┬────┘         └─────────┘                         │
│              │                                                   │
│              │ Primary Contact                                   │
│              │                                                   │
│              ▼                                                   │
│      ┌──────────────┐                                            │
│      │ OPPORTUNITY  │                                            │
│      │  CRM Deal    │                                            │
│      │  $100,000    │                                            │
│      └──────┬───────┘                                            │
│             │                                                    │
│             │ Originating Lead                                   │
│             │                                                    │
│             ▼                                                    │
│        ┌────────┐                                                │
│        │  LEAD  │ (Status: Qualified)                           │
│        └────────┘                                                │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

**One Account can have:**
- Multiple Contacts
- Multiple Opportunities
- Multiple Leads (historical)

**One Opportunity must have:**
- One Account (required)
- Optional: One Primary Contact
- Optional: One Originating Lead

### Customer Lookup Field

Opportunities use a **polymorphic lookup** called "Customer":

```
Customer lookup can point to:
├── Account (B2B scenarios)
└── Contact (B2C scenarios)

Example B2B:
Opportunity → Customer: Contoso Ltd (Account)

Example B2C:
Opportunity → Customer: John Smith (Contact)
```

> **Exam Tip**: The Customer lookup is polymorphic - it can point to either Account OR Contact, not both. This is common in B2C scenarios.

---

## Business Process Flows

### Lead Qualification BPF

```
┌─────────────────────────────────────────────────────────────────┐
│                  LEAD QUALIFICATION PROCESS                      │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ┌──────────┐    ┌──────────┐    ┌──────────┐                  │
│  │ QUALIFY  │───►│ DEVELOP  │───►│ PROPOSE  │                  │
│  └──────────┘    └──────────┘    └──────────┘                  │
│                                                                  │
│  Stage 1: Qualify                                                │
│  ○ Budget Amount                                                │
│  ○ Purchase Timeframe                                           │
│  ○ Decision Maker Identified                                    │
│  ○ Business Need Confirmed                                      │
│                                                                  │
│  Stage 2: Develop (on Lead)                                      │
│  ○ Stakeholder Identified                                       │
│  ○ Proposal Requirements                                        │
│  ○ Solution Fit Confirmed                                       │
│                                                                  │
│  Stage 3: Propose                                                │
│  ○ Identify Competitors                                         │
│  ○ Proposal Generated                                           │
│  ○ Finalize Proposal                                            │
│                                                                  │
│  [Qualify Lead] → Creates Opportunity                            │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Opportunity Sales Process BPF

```
┌─────────────────────────────────────────────────────────────────┐
│                  OPPORTUNITY SALES PROCESS                       │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌──────────┐        │
│  │ QUALIFY  │─►│ DEVELOP  │─►│ PROPOSE  │─►│  CLOSE   │        │
│  └──────────┘  └──────────┘  └──────────┘  └──────────┘        │
│                                                                  │
│  Stage 1: Qualify                                                │
│  ○ Customer Need                                                │
│  ○ Proposed Solution                                            │
│  ○ Budget Amount                                                │
│  ○ Purchase Timeframe                                           │
│                                                                  │
│  Stage 2: Develop                                                │
│  ○ Customer Pain Points                                         │
│  ○ Proposal Requirements                                        │
│  ○ Identify Stakeholders                                        │
│  ○ Identify Competitors                                         │
│                                                                  │
│  Stage 3: Propose                                                │
│  ○ Proposal Feedback Captured                                   │
│  ○ Final Proposal Delivered                                     │
│  ○ Presented Proposal                                           │
│  ○ Complete Internal Review                                     │
│                                                                  │
│  Stage 4: Close                                                  │
│  ○ Final Decision Date                                          │
│  ○ Send Thank You Note                                          │
│  ○ File De-brief                                                │
│                                                                  │
│  [Close as Won/Lost]                                            │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Cross-Table BPF: Lead to Opportunity

```
┌─────────────────────────────────────────────────────────────────┐
│               LEAD TO OPPORTUNITY BPF                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  LEAD TABLE          OPPORTUNITY TABLE                           │
│  ┌──────────┐       ┌──────────┐  ┌──────────┐  ┌──────────┐   │
│  │ QUALIFY  │──────►│ DEVELOP  │─►│ PROPOSE  │─►│  CLOSE   │   │
│  │  (Lead)  │       │  (Opp)   │  │  (Opp)   │  │  (Opp)   │   │
│  └──────────┘       └──────────┘  └──────────┘  └──────────┘   │
│       │                     ▲                                    │
│       │                     │                                    │
│       │      When stage advances to Develop:                     │
│       └─────► System prompts to qualify lead                     │
│               Creates Account, Contact, Opportunity              │
│               BPF continues on Opportunity record                │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## Qualification and Disqualification

### Qualification Scenarios

**Scenario 1: New Customer**
```
Lead: "Fabrikam interested in CRM"
Qualify → Creates:
  ├── Account: Fabrikam (NEW)
  ├── Contact: Sarah Lee (NEW)
  └── Opportunity: Fabrikam CRM Deal (NEW)
```

**Scenario 2: Existing Customer, New Contact**
```
Lead: "New person at Contoso interested in add-on"
Qualify → Creates:
  ├── Account: Contoso (EXISTING - no change)
  ├── Contact: Mike Brown (NEW)
  └── Opportunity: Contoso Add-on (NEW)
```

**Scenario 3: Existing Customer, Existing Contact**
```
Lead: "John Smith from Contoso wants upgrade"
Qualify → Creates:
  ├── Account: Contoso (EXISTING - no change)
  ├── Contact: John Smith (EXISTING - no change)
  └── Opportunity: Contoso Upgrade (NEW)
```

**Scenario 4: Qualify Without Opportunity**
```
Lead: "General inquiry, not ready to buy"
Qualify → Creates:
  ├── Account: TailSpin (NEW)
  ├── Contact: Lisa Wong (NEW)
  └── Opportunity: (NOT CREATED - unchecked)
```

### Reactivating Leads

Disqualified or Qualified leads can be **reactivated**:

```
┌─────────────────────────────────────────────────────────────────┐
│                    REACTIVATE LEAD                               │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Current Status: Disqualified                                    │
│  Status Reason: No Longer Interested                            │
│                                                                  │
│  Action: Reactivate                                              │
│  New Status: Open                                                │
│  Status Reason: [Select reason]                                 │
│                                                                  │
│  Notes: [Customer called back, now interested]                  │
│                                                                  │
│  [Reactivate] [Cancel]                                          │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

**Effect:**
- Lead status → Open
- Lead is editable again
- Can be re-qualified or re-disqualified
- Maintains history of previous qualification

---

## Reporting and Analytics

### Key Metrics for Leads

| Metric | Purpose | Calculation |
|--------|---------|-------------|
| **Conversion Rate** | % of leads that become opportunities | Qualified Leads / Total Leads |
| **Lead Velocity** | Speed of lead processing | Avg time from Created to Qualified |
| **Lead Source Performance** | Which sources generate best leads | Conversion rate by Lead Source |
| **Lead Aging** | How long leads sit | Days since lead created |
| **Lead by Rating** | Hot/Warm/Cold distribution | Count by Rating field |

### Key Metrics for Opportunities

| Metric | Purpose | Calculation |
|--------|---------|-------------|
| **Win Rate** | % of opportunities won | Won Opportunities / (Won + Lost) |
| **Average Deal Size** | Typical revenue per deal | Total Revenue / # of Opportunities |
| **Sales Cycle Length** | Time to close | Avg days from Created to Closed |
| **Pipeline Value** | Total potential revenue | Sum of Est. Revenue (Open opps) |
| **Weighted Pipeline** | Realistic pipeline | Sum of (Est. Revenue × Probability) |
| **Forecast Accuracy** | How accurate estimates are | Est. Revenue vs Actual Revenue |

### Sales Pipeline View

```
┌─────────────────────────────────────────────────────────────────┐
│                     SALES PIPELINE                               │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Qualify Stage                                                   │
│  ├── Opportunity A ($50K, 25%)  = $12.5K weighted               │
│  ├── Opportunity B ($30K, 30%)  = $9K weighted                  │
│  └── Opportunity C ($70K, 20%)  = $14K weighted                 │
│      Total: $150K estimated, $35.5K weighted                    │
│                                                                  │
│  Develop Stage                                                   │
│  ├── Opportunity D ($100K, 50%) = $50K weighted                 │
│  ├── Opportunity E ($80K, 60%)  = $48K weighted                 │
│  └── Opportunity F ($40K, 50%)  = $20K weighted                 │
│      Total: $220K estimated, $118K weighted                     │
│                                                                  │
│  Propose Stage                                                   │
│  ├── Opportunity G ($150K, 75%) = $112.5K weighted              │
│  └── Opportunity H ($90K, 80%)  = $72K weighted                 │
│      Total: $240K estimated, $184.5K weighted                   │
│                                                                  │
│  Close Stage                                                     │
│  └── Opportunity I ($120K, 90%) = $108K weighted                │
│      Total: $120K estimated, $108K weighted                     │
│                                                                  │
│  ═══════════════════════════════════════════════════════════    │
│  TOTAL PIPELINE: $730K estimated, $446K weighted                │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Rollup Fields on Account

Use **rollup columns** on Account to aggregate:

```
Account: Contoso Ltd
┌─────────────────────────────────────────────────────────────┐
│                                                              │
│  Total Open Opportunities: 5 (COUNT)                        │
│  Total Pipeline Value: $450,000 (SUM of Est. Revenue)       │
│  Largest Opportunity: $180,000 (MAX)                        │
│  Total Won Revenue: $2,500,000 (SUM of Actual Revenue)      │
│  Win Rate: 65% (calculated)                                 │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```

> **Exam Tip**: Rollup columns update approximately every hour. For real-time totals, use Power Automate or custom calculations.

---

## Common Exam Scenarios

### Scenario 1: Lead Conversion
**Question**: "When a lead is qualified, what records are automatically created?"

**Answer**: The system can create:
- Account (if it doesn't exist)
- Contact (if it doesn't exist)
- Opportunity (optional)

All three are optional during qualification - you can choose to create or link to existing records.

### Scenario 2: Existing Customer
**Question**: "A lead comes in from an existing customer. How should you handle qualification?"

**Answer**: During qualification:
- **DON'T** create new Account - select existing Account
- **DO** create new Contact (if it's a new person)
- **DO** create new Opportunity

This prevents duplicate Accounts and maintains proper relationships.

### Scenario 3: Lead Source Tracking
**Question**: "How can you track which marketing campaigns generate the most revenue?"

**Answer**:
1. Set Lead Source when leads are created
2. Lead Source is copied to Opportunity during qualification
3. Report on Opportunity actual revenue grouped by Lead Source
4. Use rollup fields or charts to visualize

### Scenario 4: Pipeline Reporting
**Question**: "Managers need to see realistic pipeline forecasts."

**Answer**: Use **Weighted Revenue** which is calculated as:
- Weighted Revenue = Est. Revenue × Probability %
- This gives a more realistic forecast than Est. Revenue alone
- Report on weighted revenue by stage, owner, or timeframe

### Scenario 5: Opportunity Not Created
**Question**: "A lead was qualified but no opportunity appears."

**Answer**: During qualification, the "Create Opportunity" option was unchecked. This is valid for scenarios where:
- Just capturing account/contact information
- Lead wasn't sales-ready
- Different process for opportunity creation

You can manually create an opportunity later and link it to the lead.

### Scenario 6: Lost Opportunity Analysis
**Question**: "Need to report on why opportunities are lost."

**Answer**:
- Use Status Reason field when closing as Lost
- Custom Status Reasons: Price, Competitor, Timing, etc.
- Report on lost opportunities grouped by Status Reason
- Use this data to improve sales strategy

### Scenario 7: Duplicate Detection
**Question**: "Prevent duplicate leads from the same company."

**Answer**: Create **Duplicate Detection Rule**:
- Base table: Lead
- Match criteria: Company Name + Email
- Run on create and update
- Enables or blocks duplicate creation

### Scenario 8: Lead Assignment
**Question**: "Automatically assign leads to sales reps based on territory."

**Answer**: Use **Power Automate**:
- Trigger: When lead is created
- Condition: Check lead's state/region
- Action: Assign lead to appropriate user/team
- Alternatively: Use Assignment Rules (if available)

### Scenario 9: Opportunity Stage Duration
**Question**: "Report on how long opportunities spend in each sales stage."

**Answer**:
- Enable a Business Process Flow for opportunities
- BPF creates its own table that tracks stage changes
- Report on the BPF table showing duration per stage
- Identify bottlenecks in the sales process

### Scenario 10: Multi-Currency Deals
**Question**: "Track opportunities in different currencies."

**Answer**:
- Set Currency on each Opportunity
- System stores both Transaction Currency and Base Currency amounts
- Reports can show in either currency
- Exchange rates are configured at organization level

---

## Integration Patterns

### Lead Capture Automation

```
┌─────────────────────────────────────────────────────────────────┐
│                  LEAD CAPTURE SOURCES                            │
├─────────────────────────────────────────────────────────────────┤
│                                                                  │
│  Web Form                                                        │
│  └─► Power Automate → Create Lead                               │
│                                                                  │
│  Email Campaign                                                  │
│  └─► Marketing Automation → Create Lead                         │
│                                                                  │
│  Trade Show Scanner                                              │
│  └─► Excel Import → Batch Create Leads                          │
│                                                                  │
│  Chatbot                                                         │
│  └─► Power Virtual Agents → Create Lead                         │
│                                                                  │
│  Partner Portal                                                  │
│  └─► API Integration → Create Lead                              │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Lead Nurturing Automation

```
Power Automate Flow: Lead Nurture
┌─────────────────────────────────────────────────────────────────┐
│  Trigger: Lead created (Rating = "Warm")                        │
│      ↓                                                           │
│  Day 0: Send welcome email                                      │
│      ↓                                                           │
│  Day 3: Send product information                                │
│      ↓                                                           │
│  Day 7: Schedule follow-up task for owner                       │
│      ↓                                                           │
│  Day 14: If not contacted → Send reminder to manager            │
│      ↓                                                           │
│  Day 30: If still open → Change rating to "Cold"                │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## Security Considerations

### Lead/Opportunity Security

Both tables use **User or Team ownership**:

```
Security Role: Sales Representative
┌─────────────────────────────────────────────────────────────────┐
│                                                                  │
│  Lead Table Privileges:                                          │
│  ├── Create: User (can create leads)                            │
│  ├── Read: Business Unit (see team's leads)                     │
│  ├── Write: User (edit own leads)                               │
│  ├── Delete: None (cannot delete)                               │
│  ├── Assign: User (reassign own leads)                          │
│  └── Share: User (share own leads)                              │
│                                                                  │
│  Opportunity Table Privileges:                                   │
│  ├── Create: User (can create opportunities)                    │
│  ├── Read: Business Unit (see team's opportunities)             │
│  ├── Write: User (edit own opportunities)                       │
│  ├── Delete: None (cannot delete)                               │
│  ├── Assign: User (reassign own opportunities)                  │
│  └── Share: User (share own opportunities)                      │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

### Field-Level Security

Protect sensitive fields:

```
Field Security Profile: "Sales Managers Only"
┌─────────────────────────────────────────────────────────────────┐
│                                                                  │
│  Protected Fields:                                               │
│                                                                  │
│  Opportunity.Budget Amount                                       │
│  └─► Read: Managers only                                        │
│                                                                  │
│  Opportunity.Actual Revenue                                      │
│  └─► Read: Managers only                                        │
│  └─► Update: Managers only                                      │
│                                                                  │
│  Lead.Annual Revenue                                             │
│  └─► Read: Managers only                                        │
│                                                                  │
└─────────────────────────────────────────────────────────────────┘
```

---

## Best Practices

### Lead Management

1. **Consistent Lead Sources**: Use standardized lead source values
2. **Timely Follow-up**: Set SLAs for lead response times
3. **Lead Scoring**: Use rating to prioritize (Hot/Warm/Cold)
4. **Regular Cleanup**: Disqualify or archive old leads
5. **Duplicate Prevention**: Enable duplicate detection rules

### Opportunity Management

1. **Accurate Estimates**: Keep Est. Revenue realistic
2. **Update Probability**: Adjust as opportunity progresses
3. **Regular Reviews**: Review and update open opportunities weekly
4. **Close Promptly**: Close won/lost opportunities immediately
5. **Learn from Losses**: Capture loss reasons for analysis

### Data Quality

1. **Required Fields**: Make key fields required (Budget, Timeframe)
2. **Business Rules**: Validate data on save
3. **Consistent Naming**: Use naming conventions for Topics
4. **Regular Audits**: Review data quality monthly
5. **Training**: Train users on proper data entry

---

## Key Takeaways for the Exam

1. **Leads** = Unqualified prospects; **Opportunities** = Qualified sales deals
2. **Qualifying a lead** can create Account, Contact, and Opportunity
3. **Lead Source** tracks where leads originate
4. **Est. Revenue** = expected value; **Actual Revenue** = final amount (Won only)
5. **Weighted Revenue** = Est. Revenue × Probability %
6. **Opportunities must have an Account** (or Contact in B2C)
7. **Originating Lead** field links opportunity back to source lead
8. **Business Process Flows** guide users through stages
9. **Status Reasons** on Lost opportunities help analyze failures
10. **Both tables are User or Team owned** - security by owner
11. **Rollup columns** on Account can sum opportunity values
12. **Lead can be reactivated** after disqualification
13. **Multiple opportunities** can exist for same Account
14. **Currency** is set per opportunity for multi-currency scenarios
15. **BPF tables** enable reporting on stage duration

---

*Continue to the next section: [Business Process Flows Deep Dive](./BPF-DeepDive.md)*
