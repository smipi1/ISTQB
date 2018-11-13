# ISTQB Foundation

## Fundamentals of testing

_Error_ (mistake) -> _Defect_ (fault, bug) -> _Failure_ (incident)

_Errors_ are caused by:
- Stress
- Process
- Hard skills
- Architecture

Not all _Defects_ result in _Failure_

_Failures_ are resolved by _Debugging_ the Defect

_Failures_ result in _Improvements_ to reduce _Errors_ on resolution

## Why is testing necessary

### Role of testing

- Measure quality (defects found)
- Helps reduce the risk
- Increase confidence
- Contribute to quality
- Required by law or industry-specific standards
- Contractual requirement

### No risk? No test!

- Tests balance risk
- No need to make tests where there is no risk

## What is testing

### What is testing?

- Planning & Control
- Analysis of Test Basis
- Design tests
- Execute tests (static and dynamic)
- Check results
- Evaluate exit criteria
- Reporting
- Finalizing / Completing

- **Testing is a process**
- **Testing now also is a carreer path**

**Testing is not the same as debugging**

### Testing objectives

- Finding defects
- Gain confidence
- Preventing defects
- Provide information

### ISTQB Definition

> The process consisting of all lifecycle activities, both
> - static, and
> - dynamic
> Concerned with
> - planning,
> - preparation, and
> - evaluation of software products and related work products
> To
> - determine that they satisfy specified requirements,
> - demonstrate the they are fit for purpose, and
> - detect defects

## Testing principles

- Tests show presence of defects, not the absence
- Exhaustive testing is impossible
  - Use risk-based testing instead
- Early testing
  - Early validation of documentation, requirements and user story definition
- Defect clustering
- Pesticide paradox
  - Revise test cases regularily
- Testing is context dependent
  - Approach required depends on the area of application
- Absence of defect fallacy

## The fundamental test process

```
> Plan > Analysis & Design > Implement & Execution > Evaluate&Report > Closure >
>                            (R)eplanning & Control                            >
```

### Planning

- Define objectives and strategy of test
- Define exit criteria

### Analysis & Design

- Review test basis
- Analyze the test items
- Create test situations / cases
- Identify test env / infra
- Identify test data
- Create traceability

### Implementation & Execution

- Finalizing test cases / data
...

### Evaluate & Report

...

### Closure

- Finalizing testware
- Handover testware to maintenance
- Determine lessons learned
- Use data to improve test maturity

## Psycology of testing

> Dr Jekyll & Mr Hyde

- Independence
- Objectives clear
  - If you expect defects, you'll find them
- Common goal
- Tester destructive / constructive?
- Bad an unwanted news
- Communication
- Relationship with developer

# Testing throughout the Software Lifecycle

## Software development models

Testing is part of any software lifecycle

## Traditional waterfall model

## Common V-model

```
       User Requirements <----Test Activity----> Acceptance test
                       \                         /
    Software Requirements <---Test Activity---> System Test
                        \                       /
      Global/System Design <--Test Activity--> Integration Test
                         \                     /
Detailed Design / Comp. Req <-Test Activity-> Component Test
                          \                   /
                                Coding
```

## Test levels

### Component testing

Test objective
- Separate modules
- Isolation (stubs / drivers)
- Functional and non-functional
Test object
- ...
Test basis
Others?
- Almost always automated

### Integration testing

Test objective
- Interfaces
- Interaction
Test objects
- Subsystems
Test basis
- Global design / system design
- Architectural design
Other characteristics
- Can be more levels
- ...

### System Testing

Test objective
- Complete system
- Final env / HW
Test objects
- Operational / maintenance process
- Business process
- User process
Test basis
- User requirements
- Business process
Other characteristics
- Mostly validation
- Responsibility of customer or user
- Contractual

## Forms of Acceptance Testing

- User acceptance testing
- Operational acceptance testing
- Contract acceptance testing
- Regulation AT
- Alpha testing
- Beta (Field) testing

## Test Types

- Functional
- Non-functional (...ilities)
- Structural testing (Thinking before testing)
- Confirmation (re-testing)
- Regression (Validating un-touched functionality)
- Maintenance (Everything above, but executed by maintenance dept)

### USI 25010 (ISO 9126)

- Functional testing
  - Functionality
- Non-functional testing
  - Reliability
  - Usability
  - Efficiency
  - ...

## Static techniques

Any form of testing when the code is not running

Mostly applied on the left-side of the V-model:
- Review,
- Static analysis,
- Compiler

Dynamic testing on the right-side of the V-model

## Review types

- Informal
- Walkthrough (formal)
  - Talk through the requirements
  - Author guides the peers through work product
  - Audience from different disciplines (marketing, management, ...)
- Technical (formal)
  - Same as walkthrough, but:
  - Audience from technical disciplines
- Inspection (most formal)
  - Very formal process with defined steps

Why?
- Early defect detection
- Improve development productivity
- Fewer defects during dynamic testing
- Earlier found = cost savings

## Cost of defects

Found earlier = cheaper to fix

60% of defects are created before implementation

## Inspection process - Activities

- Planning
  - Involves a moderator (not the author)
- Kick-off
- Individual preparation
  - Potentially with KPI's (E.g. 1 h / 5 pages, resulting in re-kickoff if non-compliant)
- Review meeting
  - Involves a scribe to collect additional remarks
  - Discuss most critical defects found
  - Triggers discovery of more defects
- Rework
  - Author resolves remarks
- Follow-up
  - Moderator checks up on author

## inspection process - Participants

- Moderator
- Author
- Reviewers
- Scribe
- Manager

## Static analysis by tools

- Find defects in SW
- No code executed
- Finds defects, not failures
- Analyze source code
- Mostly used by developers

## Typical checks

- Style guide
- Standards
- Undefined behavior
- Frequent defects or error
- Generate quality metrics

# Test design techniques

## Traceability

Test design provides traceability between User Requirements and Acceptance Test

## Test development process

- Formal or informal
- Preceded by test analysis + def configionts
- Lead to test cases / data
- Types
  - Spec-based (Black-box)
  - Structure-based (White-box)
  - Experience-based
- Test case
  - Precondition
  - Input values
  - Expected results
  - Postcondition
- Multiple test cases combined in Test Procedure

## Categories of test design techniques

### Specification-based (Black Box)

Input ->        DUT      -> Output
         (Specification)

### Equivalence Partitioning (EP)

- About input grouping resulting in same outputs
- Most used
- Applicable to all levels of testing
- Used without realizing
- Divide (partition) inputs in groups that are (considered) the same

Process:
- Identify input attributes
  - Find inputs that affect the outputs
- Divide inputs into valid and invalid classes (Equivalence classes)

Identify test cases: Steps
- Create compltely valid test case(s)
- Create test cases with only one invalid EC at a time
- Create one completely valid test case

### Boundary Value analysis

- Test the boundary values of each partition
- Large number of defects hide there

### Decision Table Testing (DTT)

- Cause / Effect graphinc
- All combinations are tested (#TC = 2^N, N = #conditions)
- Very time consuming
- Very formal

### State transition testing

- Test a state-machine
- Needs a state diagram / table
- Formal technique
- Much used in embedded- and technical software
- 0-switch covers all single transitions from one state to another
- 1-switch covers two subsequent transitions after each other
- N-switch covers N+1 subsequent transitions after each other

### Use Case Testing

Use Cases:
- Describe interaction between actor(s) and system
- Defined in terms of an actor
- Have pre- and post conditions
- Mostrly also describe alternative / exceptional flows

Use Case Testing:
- Sys and Acc tests
- Validation
- Usability
- No formal coverage

## Test coverage

- % of testing performed
- Lots of measurements
  - Statemen
  - Decision
  - Condition (Not Foundation coverage)
  - Requirement
- Establish confidence
- Automatic measuring with tools
- Drawback: Only measures items that have been written

## Statement coverage

- % of code executed during test
- Says nothing about the depth of testing (Not all branches need to be triggered)

## Decision coverage

- What is a decision?
  - if statement
  - loop control statements
  - case
  - all decision outcomes resolved

## Experience based techniques

### Error guessing (fault attacks)

- Complements other techniques
- Need desctructive mindset
- Need domain knowledge
- No rules
- Not objective
- Not formal (unstructured)

### Exploratory testing

- Hands-on approach
- Minimal planning, maximal execution
- Based on charter
  - Bullet-list of areas of interest
  - Time-limit
  - 2 persons (advised): Driver + Logger
- Need destructive mindset
- Need domain knowledge
- Semi-formal (more structured)
- Logging during execution
- Learning

## Choosing test techniques


