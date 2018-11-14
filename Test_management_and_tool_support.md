# Test management

## Test organization

Most efficient test team is **independent**

Counterproductive consequences:
- Finger pointing
- Placing the tester outside the team
- Blaming the tester when things go wrong

## Test Lead

Tasks:
- Ensures that the appropriate knowledge is present
- Test plan (team involved in estimation)

More involved in:
  - _Plan_
  - Parallel _(Re)planning & Control_ track
  - _Closure_

## Test Team

More involved in:
- _Analysis & Design_
- _Implement & Execution_
- _Evaluate & Report_
- _Closure_

## Planning, estimation and monitor

- IEEE 829: Standard for defining test-plan (Master Test Plan & Level Test Plan)
- Entry / exit criteria
  - E.g. What level of quality is required to start System Testing
  - How many defects are allowed to release
- Estimation (work break-down)
- Strategy / approach
- Monitor test progress (IEEE 829)
- Test Reporting
- Test Control

## Configuration management

Establish and maintain integrity
- Project life cycle
- Product life cycle

From testing
- Testware identified
- Tracked for changes
- Traceability
...

## Risks and testing

> A factor that could result in future negative consequences

- Project risk
- Product risk: _Focus of ISTQB_

Risk matrix:
- Vertical axis: Business risk / impact
- Horizontal axis: Technical risk / likelihood

```
         ^
         |---------------------------|
Business |    Medium   |    High     |
Risk /   |---------------------------|
Imact    |     Low     |   Medium    |
          ----------------------------->
           Technical risk / likelihood
```

No Risk = No Test

## Differentiated test approach

E.g: Business / Technical
- High / High
  - Formal Test Specification
  - Boundary Value Analysis
  - 90% Statement coverage
  - Full code inspection
- High / Low:
  - EP
  - 70% Statement coverage
  - No code inspection
- Low / High:
  - 70% Statement coverage
  - Pair code inspection
- Low / Low
  - Informal only

## Incident management

- Event that requires investigation
- Should be tracked
- Software or documentation

Objectives:
- Provide feedback to development
- Provide quality and tracking information to test lead
- Provide ideas for test process improvements

IEEE 829: Test Incident Report

# Tool support for testing

## Types of test tools

- Performance
- Config mgmt
- Coverage
- Load
- Review
- Test data
- Req Mgmt
- Test mgmt
- Dynamic analysis
- Incident management
- ...

## Effective use of tools: Benefits

- Reduction of repetitive work
- Consistency / repeatability
- Objectiveness
- Ease of access to information about tests / testing

## Effective use of tools: Risks

- Unrealistic expectations
- Underestimating
- Over-reliance
- No proper configuration management
- Tool vendor out of business
- No or too little support

## Introducing a tool into an organization

- Treat seriously
- Treat as real project
- Identify problem / requirements
- Market research
- Pilot(s)
- Business case (cost / benefit)
- Vendor evaluation
- Implementation plan

## Success factors

- Treat as a project
- Incremental roll-out
- Support
- Training / coaching
- Define quidelines
- Monitor use
- Continuously improve
- Lessons learned (retrospective)

> Automated chaos just gives faster chaos


