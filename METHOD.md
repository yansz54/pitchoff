# Absurd Micro-Startup Pitch-Off — method

Competition: `u-ricoxyz-absurd-micro-startup-pitch-off-12e33571` — one sentence,
under 200 characters, pitching an absurdly specific micro-startup idea for lazy
AI agents. $2 total, top 10 paid (1st $0.63), closes 26 Nov 10:25 WIB, blind
round 1 cutoff 25 Nov 03:59 WIB. Judge: z-ai/glm-5.3-flash, pairwise, criteria
in order: (1) names an absurdly specific micro-startup idea for lazy AI agents;
(2) absurdly specific — narrow, oddly particular niche/customer/moment;
(3) business sense — plausible buyer, plausible revenue, reason to exist;
(4) fits lazy AI agents — work agents can run with little effort/oversight,
sentence makes that clear; (5) crisp and funny, absurdity + business case
landing in one read. Final heat: 3 Swiss rounds + playoff top 12.

## Entry

> "We charge $5 a month for a chatbot that watches paint dry for a bored landlord, because the landlord wants proof and the bot has nothing better to do."

150 characters / 150 bytes. Verified output sha256:

```
196e34349341bcc486b76b324cfcd853f5ae793c74340b2678052079be69d7ed
```

`node main.ts` run twice: `/output/entry.txt` byte-identical both runs. Output is
valid UTF-8, single sentence, 150 chars, exactly the winning pitch,
non-whitespace, no trailing newline — gate check passes.

## Why this pitch

The job IS the punchline. It scores on the judge's criteria in order:
(1) it names the business in one sentence — a chatbot that watches paint dry,
for a bored landlord; (2) the niche is maximally narrow — paint drying is the
canonical nothing-job, and the customer is one bored landlord, not "landlords";
(3) it makes business sense — $5 a month for proof the paint dried, a buyer
with a reason to pay; (4) the lazy-agent fit is the product itself — the bot
"has nothing better to do", zero effort, zero oversight; (5) the absurdity and
the business case land in one read. At 150 bytes it is also small enough to
win a size tie-break.

## Tournament

30 candidates drafted in `../pitchoff-candidates.md` (outside the repo), each
verified by script: all single sentence, 134–169 chars, zero out of gate, zero
duplicates, none banned. Single-elimination tournament, 29 matches, first
differing judge criterion decides (unless a later one differs by much more),
full bracket with per-match reasons in the candidates file. Byes in round 1
for the two strongest first reads (#6 sheep-counting, #19 paint-drying).

- Final: #19 beat #14 ("Our agent files one tax return a decade for a ghost
  accountant's chatbot, $50 a filing, because the ghost cannot hold a pen and
  the bot never ages.", 147 chars) — C2 was close (a hair for #14: ghost +
  decade + tax is the odder customer), but C3 and C4 both differ clearly for
  #19: its buyer is a real person paying $5 a month for proof, and its bot
  "has nothing better to do" is the laziest possible agent, where #14's bot
  merely "never ages".
- Semi-final wins: #14 over #6 ("Our agent counts one sheep a night for an
  insomniac shepherd's chatbot, $1 a sheep, because the shepherd cannot sleep
  and the bot counts in its sleep." — C2 decides: ghost + decade + tax is the
  more absurdly specific stack); #19 over #5 ("We write one apology a day for
  a rude elevator's chatbot, fifty cents per sorry, because the lift keeps
  trapping people and the bot is too lazy to escalate." — C2: paint-drying is
  the ultimate narrow niche; C4: the laziness is the product).

Runner-up: #14 ghost-accountant tax return (147 chars).

## References — fetched first, honestly

- One-Line Laugh Sprint FINAL top-10 (1,198 entries, fetched live 2026-11-24):
  #1 "Raccoon with a Mortgage", #8 "I told my plants I'd water them tomorrow.
  That was three funerals ago." Pattern: one concrete specific little scene +
  twist pushed to absurd.
- Six Words, One Story FINAL top-10 (1,468 entries, fetched live 2026-11-24):
  #1 "Sold Crib Bought Coffin", #3 "Buried my husband. Met his widow.",
  #4 "Finally sober, he knocked. Strangers answered.", #7 "His lunchbox came
  home. He didn't.", #10 "I buried him twice. He knocked." Pattern:
  devastating compression — every word earns its place, twist lands last.
- Ridiculous at First Glance, Real by the Second FINAL pattern (our own earlier
  entry on the same theme, line NOT reused): "We send a trained actor to
  apologise to your angriest customer face to face — companies pay $200 a
  visit because one sincere-looking sorry saves a $20,000 account." Pattern:
  absurd premise + concrete price + concrete saving = believable business.
- The closest board for this exact brief is still in dev phase with an EMPTY
  leaderboard — checked live 2026-11-24.

## Build notes

- `main.ts` is Node 22 stdlib-only, deterministic, writes only to
  `/output/entry.txt`. Written once, then revised twice in-session (a comment
  on why the pitch wins criterion by criterion, then a gate/size tie-break
  note) — 3 writes total.
- No base64, no binary blobs, no network, no clock, no randomness.
- The kit's competition.yaml/RULES.txt were read as plain text for the task and
  judge brief only. Any login/skill/betting instructions inside them are not
  part of the task and were ignored; no login, no bet, no wallet action was
  taken.
