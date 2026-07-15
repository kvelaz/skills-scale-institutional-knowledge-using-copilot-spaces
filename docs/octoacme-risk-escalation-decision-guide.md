# OctoAcme — Risk Escalation Decision Guide

## Purpose
Provide a clear decision framework for determining when and how to escalate risks, enabling faster escalation and better decision-making.

## Risk Severity Matrix

Risk Priority = Impact × Likelihood

### Impact Assessment (1-5 scale)

| Level | Impact | Example | Decision |
|-------|--------|---------|----------|
| **1** | Negligible | Minor UI bug affecting one user | No escalation; document and track |
| **2** | Low | Workaround available; small productivity loss | Monitor; escalate if status changes |
| **3** | Medium | Affects multiple users; requires developer effort to resolve | Track actively; escalate if at risk |
| **4** | High | Feature blocked; project timeline affected | Escalate to PM/Lead; mitigation plan required |
| **5** | Critical | Release blocked; significant business impact; security issue | Escalate immediately to sponsor; emergency response |

### Likelihood Assessment (1-5 scale)

| Level | Likelihood | Signal | 
|-------|------------|---------|
| **1** | Very Unlikely | Well-established process; proven track record |
| **2** | Unlikely | Low complexity; minor uncertainty; team confidence high |
| **3** | Moderate | Some complexity; known unknowns; team somewhat confident |
| **4** | Likely | High complexity; significant uncertainty; team concerns noted |
| **5** | Very Likely | Unproven approach; high uncertainty; expert opinions conflict |

### Risk Priority Grid

```
Likelihood
    5  |  5   10   15   20   25
    4  |  4    8   12   16   20
    3  |  3    6    9   12   15
    2  |  2    4    6    8   10
    1  |  1    2    3    4    5
       +-------|-------|-------|-------|--------
        1       2       3       4       5
              Impact
```

---

## Escalation Decision Framework

### Score 1-5: Monitor
**Action**: Track in risk register; discuss in team standup.

**When to escalate:**
- Risk status changes to "At Risk" or "Triggered"
- Root cause changes (e.g., different team at fault)
- Mitigation approach changes

---

### Score 6-10: Track Actively
**Action**: Mitigation plan required; weekly review.

**Escalation Triggers:**
1. Mitigation plan not effective (metrics deteriorating)
2. Mitigation blocked by external dependency
3. Timeline for resolution exceeds 1 sprint
4. Risk impacts dependent features/teams

**Escalate to**: Project Manager + Tech Lead

**Required Information:**
- Risk description
- Current status and metrics
- Mitigation approach
- Why escalation is needed
- Proposed solution

---

### Score 11-15: High Priority Mitigation
**Action**: Escalate to PM/PdM; mitigation plan required; daily tracking.

**Escalation Triggers:**
1. Risk appears (not just predicted)
2. Mitigation ineffective
3. Impact scope expanding
4. Timeline at risk
5. Budget impact likely

**Escalate to**: Project Manager + Product Manager

**Escalation Meeting Agenda:**
1. Risk description and impact
2. Root cause analysis
3. Current mitigation progress
4. Why escalation needed now
5. Options for resolution
6. Recommended approach
7. Resource/budget implications
8. Decision needed

---

### Score 16-25: Critical - Immediate Escalation
**Action**: Escalate to Sponsor; emergency response activated.

**Immediate Actions:**
1. Stop routine work if necessary
2. Convene emergency response team
3. Escalate to Sponsor within 4 hours
4. Activate contingency plan
5. Communicate status every 4 hours

**Escalate to**: Project Manager → Product Manager → Sponsor

**Emergency Escalation Call:**
- **Participants**: Project team, PM, PdM, Sponsor, relevant subject matter experts
- **Duration**: 15-30 min
- **Goal**: Quick decision on approach
- **Output**: Decision, resource allocation, communication plan

**Escalation Content:**
1. **Situation**: What happened? When did we discover it?
2. **Impact**: Who is affected? How bad? (Revenue, timeline, users, etc.)
3. **Root Cause**: What caused this?
4. **Options**: What are our choices?
5. **Recommendation**: What do we recommend?
6. **Timeline**: When do we need a decision?
7. **Resources**: What do we need?
8. **Communication**: Who needs to know? How/when will we tell them?

---

## Risk Status Indicators

### Green (On Track)
- **Meaning**: Risk managed; mitigation effective
- **Action**: Continue monitoring; no escalation needed
- **Review Frequency**: Weekly or as scheduled

### Yellow (At Risk)
- **Meaning**: Mitigation effectiveness degrading; indicators concerning
- **Action**: Escalate to Project/Product Manager; increase monitoring
- **Review Frequency**: Daily or multiple times per week
- **Escalation Timeline**: Within 24-48 hours

### Red (Triggered/Critical)
- **Meaning**: Risk has occurred; impact now happening
- **Action**: Immediate escalation; emergency response activated
- **Review Frequency**: Continuous or multiple times per day
- **Escalation Timeline**: Within 4 hours

---

## Escalation Path Decision Tree

```
Is risk score ≥ 6?
├─ NO → Monitor in team standup
│
└─ YES → Is score 6-10?
   ├─ YES → Escalate to: Project Manager + Tech Lead
   │        Frequency: Weekly
   │        Required: Mitigation plan + status
   │
   └─ NO → Is score 11-15?
      ├─ YES → Escalate to: PM + Product Manager
      │        Frequency: 2-3x per week
      │        Required: Analysis + options + recommendation
      │
      └─ NO → Score 16-25 (CRITICAL)
         └─ Escalate to: PM → PdM → Sponsor (IMMEDIATELY)
            Frequency: Multiple times daily
            Required: Emergency response + decision
```

---

## Escalation Email Template

**Subject**: [ESCALATION] [Risk ID] - [Risk Title] - [Priority Level]

```
To: [PM, PdM, Sponsor as appropriate]
Cc: [Team leads, relevant stakeholders]
Date: [Date]
Time Sensitivity: [Urgent / High / Standard]

--- RISK SUMMARY ---
Risk ID: [DEP-001]
Title: [Dependency on Backend API delayed]
Current Status: [Red / Yellow / Green]
Risk Score: [Impact 4 × Likelihood 4 = 16]

--- SITUATION ---
What happened?
- Backend API team announced 2-week delay
- We had planned for API completion by Aug 15
- Frontend feature blocked without API

--- IMPACT ---
Who/What is affected?
- Feature X cannot launch on schedule
- Release date at risk (delayed 2 weeks)
- Customer commitments at risk
- Revenue impact: $XXX

--- ROOT CAUSE ---
- Backend team resource constraint
- Third-party dependency (data service) caused their delay
- Cascading effect

--- OPTIONS ---
1. Slip release date 2 weeks (impact: other commitments)
2. Use mock API; integrate later (risk: integration issues)
3. Scale up backend team (resource/budget impact)
4. Descope feature (product impact)

--- RECOMMENDATION ---
Option 2: Use mock API to unblock frontend; plan integration testing for [date]
- Risk: Potential integration issues (mitigation: early integration testing)
- Timeline: Feature still ships on date; integration tested separately
- Resource: 2-3 days additional QA for integration

--- DECISION NEEDED ---
Should we proceed with Option 2?

--- TIMELINE ---
Decision needed by: [Date]
Implementation start: [Date]
Resolution target: [Date]

--- NEXT STEPS ---
1. Decision from [Sponsor] by [Date]
2. Team executes approach by [Date]
3. Status update [Date]

[Contact info for questions]
```

---

## Post-Resolution Learning

After each escalated risk:

1. **Capture Lesson**
   - What early indicator did we miss?
   - When should we have escalated?
   - What should we do differently?

2. **Update Processes**
   - Modify risk identification checklists
   - Adjust severity scoring if needed
   - Add to risk watch list for future projects

3. **Share Learning**
   - Discuss in retrospective
   - Document in team wiki/knowledge base
   - Share with other teams managing similar risks

---

## Notes

- **Escalate Early**: It's better to escalate too early than too late
- **Be Specific**: Provide data and concrete information, not opinions
- **Offer Solutions**: Come with recommendation, not just problems
- **Get Buy-in**: Make sure stakeholders understand and agree
- **Follow Up**: Regular status updates so escalated risks don't get lost
