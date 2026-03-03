# Technical Debt — A Metaphor Almost Nobody Gets Right

tags: "Classics Collection", "technical debt", "AI", "architecture", "Martin Fowler", "Ward Cunningham"

Continuing the "Classics Collection" series. Today's protagonists — Martin Fowler and Ward Cunningham — and a metaphor that has dominated our industry's discussions, even though most of us understand it incorrectly.

"We have too much technical debt." That sentence is said at every retrospective. Everyone nods. But ask five people in the room what exactly they mean by it — and you'll get five different answers. Ugly code. Missing tests. An old framework. Quick workarounds. Everything we should have done differently. Everyone uses the same metaphor, but everyone is talking about something different.

And that's the problem — because this metaphor has a very specific meaning.

## Cunningham Wasn't Talking About Bad Code

Ward Cunningham introduced the concept of technical debt in 1992, describing the WyCash system [1]. And this is where most of the industry takes a wrong turn — because Cunningham **was not talking about messy code**. He was talking about something far more subtle.

A team wrote code as best they could, based on what they understood about the business domain at that time. Then they learned more — and the same code, previously good, became misaligned with their current understanding of the problem. That gap — between the code and the current knowledge of the domain — is technical debt in Cunningham's sense.

The financial metaphor is deliberate. Debt is not evil in itself. Companies take on loans because they allow faster growth — provided they have a repayment plan. In a 2009 interview, Cunningham said it directly: it was about a conscious tradeoff, not about writing sloppy code and calling it "debt" [2].

## Fowler's Quadrant — Not Every "Debt" Is Debt

Fowler in 2009 took this chaotic terminology and imposed order on it [3]. Two axes — deliberate/reckless and prudent/inadvertent — give four completely different situations. And only when you distinguish between them does talking about "technical debt" start to make sense.

![Fowler's Technical Debt Quadrant](/blog/fowlers-quadrant.svg)

**Deliberate-Prudent:** "We must ship now and deal with the consequences." The team knows what they're simplifying and has a repayment plan. This is debt in Cunningham's sense — and it's the only debt worth consciously taking on.

**Deliberate-Reckless:** "We don't have time for design." The team knows they're doing it wrong, but does it anyway. No repayment plan. This isn't debt — it's negligence with intent. Using the word "debt" here is a euphemism that makes it easier to live with that fact.

**Inadvertent-Prudent:** "Now we know how we should have done it." The team learned something new — about the domain, about patterns, about architecture — and sees that earlier code, though written in good faith, doesn't fit the current understanding. An unavoidable cost of learning. Every system has it.

**Inadvertent-Reckless:** "What's layering?" The team doesn't know they're doing it wrong because they don't know good practices. This isn't debt — it's a lack of competence. It's cured by education and mentoring, not by "repayment."

## And Then AI Came Along

I have the impression that the AI agent era complicates each of these quadrants in new ways.

An agent generating code doesn't go through a phase of learning the domain, doesn't gradually build intuition about why a client does something a certain way. It produces code that formally meets requirements — but doesn't carry the full domain understanding that Cunningham considered the core of a conscious tradeoff. Inadvertent-Prudent debt appears immediately, because the code from day one reflects a shallow understanding of the problem.

Deliberate-Reckless debt — "we don't have time for design" — takes on a new dimension when code generation is instantaneous. Since "you can just ask the agent," the temptation not to invest in architecture is greater than ever. I suspect that's exactly what we're observing — nobody plans architectural tradeoffs, because a tradeoff implies you're thinking about architecture at all.

And Inadvertent-Reckless debt? Here AI creates dynamics that didn't exist before. A person who doesn't understand design patterns gets a tool that generates code looking professional — but can't evaluate whether that code is good. The agent reproduces patterns from a repository with complete consistency, without a moment of reflection. If the repository is full of broken windows, the agent takes that as the norm and adds more.

![How AI Changes Each Debt Quadrant](/blog/ai-quadrant.svg)

## Why It's Worth Talking About This Precisely

McKinsey estimates that technical debt accounts for about 40% of IT balance sheets [4]. Besker, Martini and Bosch calculated that 25% of developer effort is wasted on problems caused by technical debt [5]. One quarter of a team's time — not building new things, but navigating the maze of complexity we created ourselves.

In an era where code is produced faster than ever, those numbers can only grow. Unless we start using the language that Cunningham and Fowler gave us — not as an academic curiosity, but as an everyday tool. When "we have too much technical debt" comes up in a discussion, the correct response isn't "let's plan a refactoring sprint"; the correct response is: "What kind of debt? Did we plan it? Or do we simply have a mess?"

---

#### Sources:

* [[1] Ward Cunningham, "The WyCash Portfolio Management System", OOPSLA 1992](http://c2.com/doc/oopsla92.html)
* [[2] Ward Cunningham, "Debt Metaphor" (video, 2009)](https://www.youtube.com/watch?v=pqeJFYwnkjE)
* [[3] Martin Fowler, "Technical Debt Quadrant" (2009)](https://martinfowler.com/bliki/TechnicalDebtQuadrant.html)
* [[4] McKinsey, "Tech Debt: Reclaiming Tech Equity"](https://www.mckinsey.com/capabilities/mckinsey-digital/our-insights/tech-debt-reclaiming-tech-equity)
* [[5] Besker, Martini, Bosch, "Technical Debt Cripples Software Developer Productivity" (2018)](https://www.researchgate.net/publication/325790190)
