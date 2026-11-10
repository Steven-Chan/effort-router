<!--
How effort pays on Claude Fable 5.2. The router sends these notes with every check while the session (or a subagent) runs
on this model. They are heuristics, not results. Same shape as every model's notes: how effort pays, Anthropic's advice,
then each level with its cost, time and behaviours. A line that starts with a level the check can't pick (max, unless
offered) is left out of the prompt.

Fork addition, not from upstream. Source: Anthropic's migration guide for Claude Fable 5.2 ("Choosing an effort level"),
read 2026-11-10. Unlike the other models' notes there are no cost or time multipliers against medium here: none have been
measured for this model, so the lines say only which way cost and time move. Replace this file when upstream ships
measured notes. Never add eval results, ours or anyone's: these have to stay heuristics.
-->
How effort pays on this model: most of what effort buys arrives by high. Even low is very strong, close to what Fable 5.1 gives at higher levels. Above high the gains are uneven and depend on the task. Effort barely changes how long a reply is, so a level is never the way to get a longer or shorter answer.

Anthropic's advice for this model: start at high for hard work, drop to medium or low for routine work, and keep xhigh for the hardest long-running coding and agentic work where it is known to help.

Each level, with its cost and time against medium:
- low: less cost and time. Suits quick back-and-forth, well-specified tasks and fast subagents. More likely than higher levels to end a long multistep task before the work is done.
- medium: suits interactive coding, chat and everyday knowledge work. Can also end a long multistep task early, less often than low.
- high: noticeably more cost and time. Suits hard coding, research, agentic work and long unattended runs. From here up it thinks before almost every reply, a greeting included, so easy turns pay for thinking they don't need.
- xhigh: many more tokens than high for a slight gain, and only on the hardest long-running coding and agentic work.
- max: many more tokens than xhigh, and slow. Suits open-ended problems such as scientific discovery and mathematics, where time and tokens don't matter.
