# Sustainability Hackathon — Website Planning Doc

> Skeleton plan for the hackathon landing/info site. Purpose of the site: **build hype, count down to the event, and inform** — plus a placeholder to capture interest sign-ups.

---

## 1. Event at a Glance

| Field | Value |
|---|---|
| **Event** | Sustainable Infrastructure Hackathon |
| **Date** | October 2, 2026 (countdown target) |
| **Hosts** | NYU Business Analytics Club (BAC) — Machine Learning Team, with Tech@NYU |
| **Sponsors** | Infrastructure Masons (iMasons), Grundfos, OCP (Open Compute Project) |
| **Tracks** | 2 — see §3 |
| **Site goal** | Countdown + informational + interest-form placeholder |

**Contacts:** jjp9203@nyu.edu · oal2029@nyu.edu · vm2720@nyu.edu

---

## 2. Site Goals & Scope

**In scope (v1 skeleton):**
1. **Hero + live countdown** to Oct 2, 2026.
2. **About** the hackathon + who's hosting.
3. **Tracks & challenges** (the two tracks, each with Part A / Part B).
4. **Resources / datasets** section (the 6 defined data sources).
5. **Sponsors** logos/section.
6. **Interest form placeholder** (embed slot — Google Form / Typeform / Luma later).
7. **Schedule** (Oct 2–4 outline — placeholder times).
8. **FAQ** (placeholder).
9. **Footer** with contacts + social.

**Out of scope for v1:** auth, team formation, project submission portal, judging dashboard. (Note as "phase 2" if the event grows.)

---

## 3. Content: Tracks

> **⚠️ Draft — content in progress.** Challenge statements below are still being written by the organizers/sponsors. Treat as directional, not final. Both tracks share a common thread: **simulating the carbon footprint / environmental impact of a data center.** On the site, present each track with a short teaser + "full brief coming soon" and link the detailed packet later.

> **Sponsors:** Infrastructure Masons, Grundfos, and OCP sponsor the **entire event** — not individual tracks.

### Track 1 — Waste Heat Reuse ("The Green Compute Challenge" / HeatWise)
Data centers reject huge amounts of low-grade heat that's normally dumped via energy- and water-hungry cooling towers. This "waste" heat can instead feed district heating, greenhouses, aquaculture, or industrial processes — offsetting fossil fuel use and cutting net impact.

**Build:** an interactive simulator (web app or advanced Excel dashboard) where a design engineer inputs a data center's baseline specs and tests Waste Heat Reuse (WHR) scenarios. The tool models the delta between "business as usual" (heat rejected) and a WHR scenario, then visualizes provable benefits.

- **Inputs:** IT load (MW), baseline PUE/WUE, cooling tech, location/climate; plus off-taker type (district heating, greenhouse, fish farm), distance, required supply temp, demand profile.
- **Calc core:** account for heat-pump energy (temperature uplift) vs. energy + water saved by bypassing cooling towers.
- **Outputs:** adjusted PUE + Energy Reuse Factor (ERF/ERE), water saved (WUE), and net CO₂e mitigated (saved cooling energy + off-taker fossil offset − heat-pump penalty).
- **Judging:** Accuracy & Logic 40% · UX/UI 30% · Innovation 15% · Completeness 15%.
- **Support:** organizers provide a **Data & Formula Packet** (PUE/WUE/CUE/ERF/ERE formulas, grid carbon-intensity + fuel emission factors, off-taker personas, and reference data-center scenarios with a worked validation example). → link as a downloadable resource on the site.

### Track 2 — Sustainable Data Centers: Second Life for Hardware
Servers are often retired before their useful life is exhausted. This track focuses on extending the life of OCP hardware through reuse and refurbishment, cutting both carbon and e-waste.

**Build:** a tool that (1) estimates a server's carbon footprint from its components + manufacturing impact, (2) assesses how much useful life remains, and (3) recommends reuse opportunities — wrapped in a business model that lowers waste and cost and keeps equipment in circulation.

- Uses AI, public datasets, and OCP hardware specifications.
- Shares the common thread: simulate/measure a data center's environmental impact and sustainability trade-offs (servers, cooling, energy sources).

> `⚠️ NEEDS CONTENT: final challenge briefs, judging criteria for Track 2, and confirmation of sponsor↔track mapping.`

---

## 4. Content: Resources / Data Sources

Render as cards or a table. Each: name, "best for" tag, one-liner, link (add URLs).

1. **EPA USEEIO Database** — embodied carbon of components when detailed supplier data isn't available.
2. **NREL LCI Database** — lifecycle assessment; inventories for metals, manufacturing, transportation, electricity, construction materials.
3. **Electricity Maps** — operational carbon (Scope 2); real-time grid carbon intensity, historical data, renewable mix, regional emissions.
4. **Our World in Data** — CO₂ emissions, energy production, renewable adoption, country comparisons, climate indicators.
5. **International Energy Agency (IEA)** — energy projections.
6. **Boavizta** — data center equipment; server embodied carbon, storage/network impacts, usage models, open APIs, product footprints.

`⚠️ NEEDS CONTENT: canonical URLs for each source.`

---

## 5. Content: Hosts & Partners

- **NYU BAC Machine Learning Team** (organizer; postgrad team leads). The team has built projects like an LLM trained on tacit knowledge from data center industry leaders and presented at DCD (Data Center Dynamics) Connect. This semester: expanding the project and running this hackathon with iMasons.
- **Tech@NYU** — supporting/co-host.
- **Sponsors:** Infrastructure Masons, Grundfos, OCP.

`⚠️ NEEDS CONTENT: sponsor logo assets (SVG/PNG), org blurbs, links.`

---

## 6. Page / Section Map

Single-page scroll (recommended for v1), anchor-nav:

```
┌─ Nav (sticky) ─ logo · Tracks · Resources · Schedule · Sponsors · [Register] ─┐
│                                                                               │
│  HERO         big title · date · LIVE COUNTDOWN · CTA button                  │
│  ABOUT        what it is · who's hosting                                       │
│  TRACKS       Track 1 (Part A / Part B) · Track 2 (TBD)                        │
│  RESOURCES    6 data-source cards                                             │
│  SCHEDULE     Oct 2 / Oct 3 / Oct 4 timeline (placeholder)                     │
│  SPONSORS     iMasons · Grundfos · OCP · Tech@NYU · BAC                        │
│  REGISTER     interest-form embed placeholder                                 │
│  FAQ          accordion (placeholder Qs)                                       │
│  FOOTER       contacts · socials · credit                                     │
└───────────────────────────────────────────────────────────────────────────────┘
```

---

## 7. Design Direction — Y2K Futurism + Techy

**Mood:** retro-future, chrome, terminal glow, "the internet in 1999 imagining 2030."

- **Palette:** deep space black / near-black base; electric cyan + magenta/hot-pink accents; chrome/silver gradients; optional acid green for terminal text. High contrast.
- **Typography:** monospace for labels/countdown/data (e.g. Space Mono, JetBrains Mono, IBM Plex Mono); a wide/techno display face for headlines (e.g. Orbitron, Michroma, or a grotesk). Real fallback stacks.
- **Motifs:** scanlines / CRT flicker (subtle), grid backgrounds, glow/neon borders, chrome bevels, starfield or wireframe globe, blinking cursor, "loading…" bars, pixel/dither textures.
- **Countdown:** the centerpiece — big segmented digits with glow, monospace, ticking.
- **Motion:** restrained — glow pulses, marquee ticker for sponsors, hover states with neon outline. Respect `prefers-reduced-motion`.
- **Accessibility:** keep text contrast readable despite the neon; don't rely on glow alone for state.

Consider loading the `frontend-design` skill when building the actual UI for a distinctive, non-templated look.

---

## 8. Tech Stack (recommendation)

Pick based on who maintains it:

- **Simplest / fastest to ship:** single static `index.html` + CSS + vanilla JS (countdown is ~20 lines). Deploy to GitHub Pages / Netlify / Vercel. **Recommended for a skeleton.**
- **If the team wants React:** Next.js (static export) + Tailwind. More setup, easier to extend to a real portal later.

Countdown = client-side JS to a fixed target `2026-10-02T09:00:00` (confirm start time + timezone, likely `America/New_York`).

Interest form = **embed slot** (iframe placeholder div) so it can be swapped for Google Form / Typeform / Luma without a rebuild.

---

## 9. Component / Build Checklist

- [ ] Project scaffold + deploy target chosen
- [ ] Nav (sticky, anchor links, mobile hamburger)
- [ ] Hero + **countdown timer** (live, timezone-correct)
- [ ] About section
- [ ] Tracks section (Track 1 Waste Heat Reuse, Track 2 Second-Life Hardware; both "brief coming soon")
- [ ] Resources cards (6 sources, URLs TBD)
- [ ] Schedule timeline (placeholder content)
- [ ] Sponsors row (logo assets TBD)
- [ ] Register section — **form embed placeholder**
- [ ] FAQ accordion (placeholder)
- [ ] Footer + contacts
- [ ] Responsive pass (mobile → desktop)
- [ ] `prefers-reduced-motion` + contrast/a11y pass
- [ ] Meta tags / social share preview (OG image)

---

## 10. Open Questions / Needs Content (`⚠️`)

1. **Final challenge briefs** — both tracks are still draft; lock copy + judging criteria before publish. (Sponsors iMasons/Grundfos/OCP back the whole event, not individual tracks.)
2. **Exact start time + timezone** for the countdown (date = Oct 2, 2026; time TBD, likely `America/New_York`).
3. **Venue / format** — in-person (NYU location?) / hybrid / virtual.
4. **Interest form** — which tool, and the live link/embed.
5. **Sponsor + host logo assets** and blurbs.
6. **Resource URLs** for the 6 data sources.
7. **Schedule** — real Oct 2–4 agenda.
8. **Prizes / eligibility / team size** rules.
9. **Socials** — Instagram/LinkedIn handles for footer.

---

## 11. Suggested Build Order

1. Scaffold + hero + countdown (proves the concept, most-shared moment).
2. Tracks + resources (the substance).
3. Sponsors + about + footer.
4. Register placeholder + schedule + FAQ.
5. Polish: Y2K visual pass, responsive, a11y, share preview.
