# What If AI Didn't Change the Rules of the Game, It Just Sped It Up?

tags: "Classics Collection", "architecture", "AI", "software evolution", "Barry Boehm", "Martin Fowler", "Simon Wardley"

Boehm showed decades ago that the cost of change grows exponentially with project phase [1]. Fowler documented how architecture breaks down when you're not looking — slowly, imperceptibly, like a river undermining its bank [2]. Wardley drew maps of component evolution from the Pioneer experiment through the mature Product to Commodity [3]. Each of them said something different, but all pointed to one thing: evolution is inevitable. The only question is whether you'll lead it consciously.

Today we observe something unsettling. Most developers using AI become, inadvertently, Pioneers in Wardley's sense — we build custom solutions to problems that already have product-grade answers, because AI generates code faster than we have time to ask: "does this already exist somewhere?"

On Wardley's map we should be operating in the Product or Commodity zone, yet we behave like a startup in permanent Genesis mode.

I also have the strong impression that systems are no longer going through an evolution phase. The normal lifecycle is intense development, then refactoring and maturing, then stable maintenance. Projects written by agents mature differently: intense development, followed almost immediately by maintenance. The evolution phase disappears — not because we've solved the technical debt problem, but because code accumulates so fast there's no time to tend it. The system ends up in the ICU before its first birthday.

The question isn't "should we use AI." It's: are we building the right culture and processes to protect ourselves from the dangers that wise people warned us about long ago? The speed at which new features emerge is impressive, but the speed at which systems erode is alarming.

(Yes, I use long dashes "—" because I was doing it even before LLMs.)

---

#### Sources:

* [[1] Barry Boehm, "Software Engineering Economics"](https://www.academia.edu/108567971/B_W_Boehm_software_engineering_economi)
* [[2] Martin Fowler, "Is High Quality Software Worth the Cost?"](https://martinfowler.com/articles/is-quality-worth-cost.html)
* [[3] Simon Wardley, "Wardley Maps"](https://learnwardleymapping.com)
