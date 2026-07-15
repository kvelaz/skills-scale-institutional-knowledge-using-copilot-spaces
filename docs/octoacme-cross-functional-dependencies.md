# OctoAcme — Cross-Functional Dependencies Management

## Purpose
Provide clarity on how to identify, track, and manage dependencies across teams, reducing blockers and improving delivery predictability.

## Types of Dependencies

### 1. Technical Dependencies
One team's work depends on another team completing technical work first.

**Examples:**
- Feature A requires API from Team B
- Component C needs data schema from infrastructure team
- Integration depends on third-party service integration

**Management Approach:**
- Identify during planning phase
- Define clear interface contracts (API specs, data schemas)
- Create mock/stub services for parallel development
- Establish testing strategy for integration points
- Set clear completion dates with dependencies

### 2. Resource Dependencies
Team needs access to specific expertise, tools, or capacity from another team.

**Examples:**
- Needs Security team review before launch
- Requires QA capacity that's allocated to another project
- Depends on DevOps for infrastructure provisioning

**Management Approach:**
- Book resource time during project planning
- Create review queues and SLAs (e.g., security review within 48 hours)
- Identify backup resources for critical dependencies
- Schedule reviews early in development

### 3. Business/Approval Dependencies
Requires stakeholder or business decision before proceeding.

**Examples:**
- Needs product manager sign-off on design
- Requires sponsor approval for scope change
- Depends on legal/compliance review

**Management Approach:**
- Identify decision makers early
- Provide clear decision criteria and options
- Schedule review meetings in advance
- Create escalation path if approval is delayed

### 4. Data/Process Dependencies
Relies on data, processes, or information from another team.

**Examples:**
- Needs customer data from Sales team
- Depends on completed inventory process from Ops
- Requires vendor information from Procurement

**Management Approach:**
- Define data requirements and format clearly
- Establish data refresh schedule
- Identify data owner and point of contact
- Plan for data validation and quality checks

---

## Dependency Identification Process

### Step 1: Brainstorm Phase (During Planning)
1. Review backlog items for external team involvement
2. Ask: "Who else needs to contribute to this item?"
3. Identify all cross-team interactions
4. List external tools, services, or systems needed
5. Note stakeholder approvals required

### Step 2: Document Phase
For each dependency, create a record with:
- **Dependency ID**: Unique identifier (e.g., DEP-001)
- **Description**: Clear, concise description of the dependency
- **Type**: Technical / Resource / Business / Data
- **Owner**: Team or person managing the dependency
- **Dependent Item**: Which backlog item(s) are blocked
- **Due Date**: When this dependency must be completed
- **Impact if Delayed**: Severity and downstream effects
- **Mitigation**: What we'll do if this is at risk

### Step 3: Communication Phase
1. Share dependency list with dependent teams at kickoff
2. Confirm delivery dates and success criteria
3. Establish regular sync cadence (weekly minimum)
4. Identify single point of contact for each dependency
5. Document any assumptions or constraints

---

## Dependency Tracking Matrix

Create a simple tracking document (spreadsheet or GitHub Project):

| Dep ID | Description | Type | Owner | Due Date | Status | Risk | Mitigation |
|--------|-------------|------|-------|----------|--------|------|------------|
| DEP-001 | API endpoint for user auth | Technical | Backend Team | 2024-08-15 | On Track | Low | Using mock endpoint for now |
| DEP-002 | Design system components | Resource | Design Team | 2024-08-10 | At Risk | High | Escalate; have backup design |
| DEP-003 | Security review | Business | Security Team | 2024-08-20 | Pending | Med | Review early; have Infosec on speed dial |

---

## Weekly Dependency Sync

### Agenda (30 min)
1. **Status Update** (10 min)
   - Go through each active dependency
   - Mark as "On Track", "At Risk", or "Blocked"
   - Highlight any changes since last week

2. **Risk Review** (10 min)
   - Discuss any dependencies marked "At Risk"
   - Review mitigation plans
   - Escalate if needed

3. **Blockers** (5 min)
   - Address any blocked dependencies
   - Assign immediate action items
   - Set resolution timeline

4. **Next Steps** (5 min)
   - Confirm upcoming milestones
   - Schedule follow-up meetings
   - Distribute updated dependency matrix

---

## Escalation Triggers & Paths

### When to Escalate
1. **Dependency is more than 3 days behind schedule**
2. **Dependent team indicates they cannot meet the date**
3. **Resource conflict or competing priorities**
4. **Requires executive decision or budget approval**
5. **Multiple teams impacted by single dependency**

### Escalation Path
1. **Level 1 - Team Lead**: Discuss with immediate team lead, explore solutions
2. **Level 2 - Program/Product Manager**: Escalate if team leads can't resolve
3. **Level 3 - Sponsor/Executive**: Final escalation for business decisions

### Escalation Template
```
Dependency: [DEP-XXX description]
Origin Team: [Team A]
Dependent Team: [Team B]
Issue: [Why is this at risk?]
Current Status: [Latest update]
Proposed Solution: [How we'll resolve this]
Decision Needed: [What decision do we need?]
Impact if Unresolved: [Consequences]
Proposed Escalation: [To whom?]
Due Date for Decision: [When do we need an answer?]
```

---

## Mitigation Strategies

### For Technical Dependencies
1. **Parallel Development**
   - Create mock/stub services for early testing
   - Define clear interface contracts
   - Use contract testing to validate integration points

2. **Early Integration Testing**
   - Set up integration sandbox early
   - Create automated integration tests
   - Test with beta/early versions of dependent services

3. **Fallback Options**
   - Identify alternative APIs or services
   - Plan degraded functionality if dependency is delayed
   - Document manual workarounds

### For Resource Dependencies
1. **Book Early**
   - Reserve specialist time during planning
   - Schedule reviews in advance (3-4 weeks ahead)

2. **Prepare Well**
   - Provide clear documentation for reviewers
   - Ask specific questions, not vague reviews
   - Include acceptance criteria and success metrics

3. **Identify Backups**
   - Know who else can perform the review
   - Have secondary reviewers trained and ready

### For Business Dependencies
1. **Educate Early**
   - Brief stakeholders on the project and decisions needed
   - Provide options with pros/cons analysis
   - Schedule review meetings early

2. **Establish Clear Criteria**
   - Make decision criteria explicit upfront
   - Reduce ambiguity in approval requirements
   - Document any assumptions

3. **Create Decision Checkpoints**
   - Schedule formal review/approval meetings
   - Have escalation path if decision is delayed

---

## Dependency Risk Assessment

**Impact Scoring** (1-5)
- **1**: Minor delay, easily worked around
- **2**: Some impact, possible workaround
- **3**: Moderate impact, significant workaround needed
- **4**: Major impact, project timeline affected
- **5**: Critical impact, project cannot proceed

**Likelihood Scoring** (1-5)
- **1**: Very unlikely, well-established process
- **2**: Unlikely, low complexity
- **3**: Moderate likelihood, some complexity or uncertainty
- **4**: Likely, high complexity or uncertainty
- **5**: Very likely, high risk or uncertain commitment

**Risk Priority** = Impact × Likelihood

**Action:**
- Score 1-5: Monitor
- Score 6-10: Track actively, mitigation plan required
- Score 11-15: High priority mitigation, escalate if needed
- Score 16-25: Critical, escalate immediately, contingency plan required

---

## Lessons Learned

After each project/release, capture:
1. Dependencies that were well-managed and why
2. Dependencies that caused delays and why
3. Mitigation strategies that worked well
4. Early warning signs we should watch for
5. Process improvements for next project

Use these insights to improve dependency management over time.
