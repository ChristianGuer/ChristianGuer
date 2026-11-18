# Christian Guerrero

Software engineer and recent Computer Science graduate from James Madison University.
Most of what I build sits close to the machine or close to the data — a compiler, a
threaded network server, a recommendation engine that refuses to trust small samples.
Before that I spent three summers automating a school district's network, which is
where I learned that the best script is the one that replaces an afternoon of clicking.

Woodbridge, Virginia · English & Spanish

---

## Projects

### [decaf-compiler](https://github.com/ChristianGuer/decaf-compiler) · C

A compiler for Decaf, a C-like teaching language, taken from source text to allocated
machine-level code:

```
parsing  →  static analysis  →  ILOC codegen  →  register allocation
```

A hand-written recursive-descent parser builds a typed AST; a visitor pass enforces
type rules, scoping, and return agreement across nested symbol tables; code generation
emits ILOC against unlimited virtual registers; and the allocator maps those onto real
registers, spilling whichever value is used furthest in the future when it runs out.
Roughly 2,400 lines across the four phases, written with Mitch Kehoe.

### [mr-sqlite-sync](https://github.com/ChristianGuer/mr-sqlite-sync) · JavaScript · SQLite · Express · React

Syncs a player's *Marvel Rivals* match history into SQLite and recommends which hero
to pick against a given enemy team. The interesting part is statistical rather than
structural: raw win rates lie when the sample is small, so every score is Bayesian-
smoothed toward the player's global baseline, and the weight given to a specific
matchup scales with how many games actually back it — capped, so a 2-game fluke can
nudge a ranking but never decide it.

### [threaded-quiz-server](https://github.com/ChristianGuer/threaded-quiz-server) · C

A multithreaded TCP quiz server. One thread per client, a counting semaphore bounding
session capacity, and a mutex/condition-variable pair that holds early arrivals in a
lobby and releases them together, so every player sees each question at the same
moment. Session size isn't hardcoded — the first client to connect becomes the admin
and sets it during a handshake.

---

## Experience

**Network Service Intern** — Prince William County Schools · May 2023 – August 2025

- Wrote Python automation for network tasks, including DNS changes across district
  switches, cutting the manual work by about 85%
- Automated disabling unused switch ports district-wide, reducing attack surface
- Configured and deployed Cisco switches from the CLI across a network serving
  100+ schools
- Built replicated lab environments to test changes before they touched production
- Documented and presented the tooling to train technicians who'd maintain it

---

## Tools

**Languages** — C · Python · Java · JavaScript · SQL · Ruby · Shell · HTML/CSS
**Systems** — pthreads · sockets · compilers · SQLite · Linux
**Web** — Node · Express · React · Vite
**Network** — Cisco IOS · Meraki · SolarWinds · Tera Term

---

## Education

**B.S. Computer Science**, minor in Computer Information Systems
James Madison University · May 2026

Founding cohort member, Hispanic Professionals in STEM at JMU.

---

## Contact

[LinkedIn](https://www.linkedin.com/in/christianfguerrero)
