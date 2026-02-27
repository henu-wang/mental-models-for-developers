# Mental Models for Developers

A curated collection of mental models specifically relevant to software developers, engineering managers, and technical leaders. These thinking frameworks help you write better code, design better systems, make better technical decisions, and navigate your career more effectively.

## Why Mental Models Matter for Developers

Software development is fundamentally a decision-making activity. Every day you make dozens of choices: which architecture to use, how to name variables, when to refactor, whether to build or buy, how to prioritize a backlog, and when to ship. The quality of these decisions determines the quality of your software and your career.

Mental models are simplified representations of how things work. They help you reason about complex situations, predict consequences, and avoid common mistakes. The best developers do not just know programming languages -- they have rich collections of mental models that guide their thinking.

For building and maintaining your own library of decision rules as a developer, [KeepRule](https://keeprule.com) provides a platform for codifying the principles that guide your technical and career decisions.

## Core Mental Models

### 1. First Principles Thinking

Break problems down to their fundamental truths rather than reasoning by analogy. When someone says "we should use microservices because Netflix does," first principles thinking asks: What are the actual constraints of our system? What problems are we trying to solve? What are the trade-offs of different architectural approaches for our specific situation?

**Application**: Before adopting any technology, framework, or pattern, articulate the specific problem you are solving and evaluate options against your actual constraints rather than industry trends.

### 2. Second-Order Thinking

Consider not just the immediate consequences of a decision but the consequences of those consequences. Adding a cache improves performance (first order) but introduces cache invalidation complexity, potential stale data bugs, and additional infrastructure to maintain (second order).

**Application**: For every technical decision, ask "And then what?" at least twice. Map out the cascade of effects before committing.

### 3. Reversibility (Two-Way Doors)

Distinguish between decisions that are easy to reverse and those that are not. Choosing a variable name is highly reversible. Choosing a database is much less so. Calibrate the time you spend deciding to the reversibility of the decision.

**Application**: Make reversible decisions quickly and invest analysis time in irreversible ones. Most day-to-day coding decisions are far more reversible than developers treat them.

### 4. Pareto Principle (80/20 Rule)

Roughly 80% of effects come from 20% of causes. In software: 80% of users use 20% of features. 80% of bugs come from 20% of the code. 80% of performance problems come from 20% of the code paths.

**Application**: Focus optimization, testing, and refactoring effort on the critical 20%. Profile before optimizing. Measure before improving.

### 5. Technical Debt as Financial Debt

Ward Cunningham's original metaphor: technical debt is like financial debt. It lets you move faster now in exchange for future payments (interest). Some debt is strategic and worthwhile. Unmanaged debt compounds and eventually consumes all capacity.

**Application**: Take on technical debt deliberately with a repayment plan. Track it explicitly. Distinguish between strategic debt (conscious trade-offs) and reckless debt (shortcuts due to laziness or ignorance).

### 6. Conway's Law

Organizations design systems that mirror their communication structures. If three teams work on a compiler, you will get a three-pass compiler.

**Application**: Before debating architecture, look at team structure. If you want a particular architecture, organize teams accordingly. Recognize that organizational problems often manifest as technical problems.

### 7. Goodhart's Law

When a measure becomes a target, it ceases to be a good measure. If you measure developers by lines of code, you get verbose code. If you measure by number of tickets closed, you get ticket splitting.

**Application**: Be extremely careful about what metrics you optimize for. Use multiple metrics. Watch for gaming behavior. Measure outcomes rather than outputs when possible.

### 8. Occam's Razor

The simplest explanation is usually the correct one. When debugging, the most common cause of the bug is usually a simple mistake, not a compiler bug or hardware failure.

**Application**: When diagnosing problems, start with the simplest hypotheses. Check the obvious things first. "When you hear hoofbeats, think horses, not zebras."

### 9. The Map Is Not the Territory

Models, diagrams, and documentation are approximations of reality. The codebase is the truth. Architecture diagrams become outdated. Documentation lies. Tests specify behavior that may have drifted.

**Application**: When models and reality disagree, trust reality. Keep models useful but do not confuse them with the actual system. Verify assumptions against running code.

### 10. Leverage Points

Small changes in the right places can produce large effects. In software, these leverage points include shared libraries, database schemas, API contracts, and developer tooling. Changes to these high-leverage points ripple through the entire system.

**Application**: Identify and invest in high-leverage improvements. A better deployment pipeline benefits every team. A well-designed API contract prevents coordination costs. Focus your energy where the multiplier effect is greatest.

## Decision Models for Common Developer Situations

### Build vs. Buy
Ask: Is this a core competency that differentiates us? If yes, build. If no, buy or use open source. Even if building seems cheaper now, account for ongoing maintenance, opportunity cost, and the expertise required.

### When to Refactor
Refactor when the cost of working around the existing design exceeds the cost of improving it. Use the "rule of three": write it once, notice the duplication, and refactor on the third occurrence. Do not refactor code that works and is not actively being modified.

### When to Ship
Ship when the software solves the core problem, even if it is not perfect. "If you are not embarrassed by the first version of your product, you have launched too late." Perfect is the enemy of good, especially in environments with fast feedback loops.

### When to Optimize
First, measure. Never optimize without profiling data. Then optimize the bottleneck, not the code you find most interesting. Premature optimization is the root of all evil, but mature optimization of proven bottlenecks is essential engineering.

## Building Your Personal Decision Framework

The most effective developers build their own collection of decision rules that they refine over time. These rules encode lessons learned from experience, mistakes, and study. Examples:

- "Never deploy on Friday"
- "If a code review exceeds 400 lines, split the PR"
- "If I am stuck for more than 30 minutes, ask for help"
- "Always write tests for business logic, skip them for glue code"

You can organize and evolve these rules using [KeepRule](https://keeprule.com), creating a personal engineering handbook that grows with your experience.

## Recommended Reading

- "The Pragmatic Programmer" by Hunt and Thomas
- "A Philosophy of Software Design" by John Ousterhout
- "Thinking in Systems" by Donella Meadows
- "The Art of Action" by Stephen Bungay
- "Staff Engineer" by Will Larson

## Contributing

Contributions welcome. Share additional mental models relevant to software development via pull request.

## Resources

- [KeepRule - Decision Rules for Developers](https://keeprule.com)
- Charlie Munger's Mental Models approach
- Farnam Street Mental Models collection

## License

MIT License
