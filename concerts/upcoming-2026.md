---
title: Upcoming NYC Concerts (May–October 2026)
description: Live snapshot of upcoming concerts at the currently-operating venues described in this wiki — pulled 2026-05-22 from each venue's public calendar. Charts of show counts by venue, borough, and month.
tags:
  - nyc-music-wiki
  - manhattan-music-wiki
  - brooklyn-music-wiki
  - queens-music-wiki
  - concerts
  - calendar
  - hub
---
# Upcoming NYC Concerts (May–October 2026)

A snapshot of upcoming concerts at the **twelve currently-operating venues** described in this wiki, pulled from each venue's public calendar on **2026-05-22**. Coverage skews to the four-month window most venues publish (late May through early fall), with the [Forest Hills Stadium](../neighborhoods/forest-hills/venues/forest-hills-stadium.md) season extending through October. The historical rooms — [CBGB](../neighborhoods/lower-east-side/venues/cbgb.md), [Studio 54](../neighborhoods/midtown-times-square/venues/studio-54.md), [Paradise Garage](../neighborhoods/soho/venues/paradise-garage.md), [Mudd Club](../neighborhoods/soho/venues/mudd-club.md), [Max's Kansas City](../neighborhoods/greenwich-village/venues/maxs-kansas-city.md), [Danceteria](../neighborhoods/chelsea-meatpacking/venues/danceteria.md), [Knitting Factory](../neighborhoods/soho/venues/knitting-factory.md) — are closed and out of scope.

> [!NOTE]
> **One venue moved off the open list since the wiki was written.** [Saint Vitus](../neighborhoods/greenpoint/venues/saint-vitus.md) is still described here as an operating Greenpoint room, but it was permanently closed on **2024-08-17** after a NYC Department of Buildings shutdown in February of that year — confirmed by the venue's own Instagram announcement *("1120 Manhattan Ave. 2011–2024. Saint Vitus Bar to be continued… Thank you to everyone who was a part of it.")*. The venue page should be updated; this concerts page treats Saint Vitus as closed. Source: [Saint Vitus (venue) — Wikipedia](https://en.wikipedia.org/wiki/Saint_Vitus_(venue)).

## At a glance

```html preview
<div style="font-family:system-ui,sans-serif;padding:20px">
  <div id="cards" style="display:flex;gap:14px;flex-wrap:wrap"></div>
  <script>
    var stats = [
      ['Open venues covered', '12', 'across 3 boroughs', 'var(--chart-1)'],
      ['Upcoming shows tracked', '126', 'pulled 2026-05-22', 'var(--chart-2)'],
      ['Calendar window', '4.5 mo', 'May 22 → Oct 10', 'var(--chart-3)'],
      ['Largest season', '26 shows', 'Forest Hills Stadium', 'var(--chart-4)']
    ];
    document.getElementById('cards').innerHTML = stats.map(function (s) {
      return '<div style="flex:1;min-width:170px;padding:16px;background:var(--card);' +
        'color:var(--card-foreground);border:1px solid var(--border);' +
        'border-radius:var(--radius)">' +
        '<div style="font-size:13px;color:var(--muted-foreground)">' + s[0] + '</div>' +
        '<div style="font-size:26px;font-weight:700;margin-top:4px">' + s[1] + '</div>' +
        '<div style="font-size:12px;font-weight:600;margin-top:4px;color:' + s[3] + '">' +
        s[2] + '</div>' +
        '</div>';
    }).join('');
  </script>
</div>
```

## Shows by venue

Forest Hills Stadium drives the count because it publishes its full seasonal lineup at once; the Bowery Presents rooms (Brooklyn Steel, Bowery Ballroom, Mercury Lounge, Music Hall of Williamsburg) and the small-room jazz clubs (Blue Note, Village Vanguard) publish on rolling 4–8 week horizons.

```html preview
<div style="font-family:system-ui,sans-serif;padding:20px;color:var(--foreground)">
  <h3 style="margin:0 0 14px;font-size:15px;font-weight:600">Upcoming shows per venue (pulled 2026-05-22)</h3>
  <div id="bars" style="display:flex;flex-direction:column;gap:8px"></div>
  <script>
    var data = [
      ['Forest Hills Stadium', 26, 1],
      ['Brooklyn Steel', 12, 2],
      ['Bowery Ballroom', 12, 3],
      ['Mercury Lounge', 12, 2],
      ['Brooklyn Bowl', 10, 4],
      ['Blue Note', 10, 5],
      ['Knockdown Center', 10, 1],
      ['Music Hall of Williamsburg', 8, 2],
      ['Village Vanguard', 8, 5],
      ['Apollo Theater', 3, 3],
      ['Trans-Pecos', 3, 4],
      ['Nowadays', 2, 1]
    ];
    var max = Math.max.apply(null, data.map(function (d) { return d[1]; }));
    document.getElementById('bars').innerHTML = data.map(function (d) {
      return '<div style="display:flex;align-items:center;gap:10px">' +
        '<div style="flex:0 0 180px;font-size:13px;color:var(--foreground)">' + d[0] + '</div>' +
        '<div style="flex:1;height:22px;background:var(--border);border-radius:var(--radius);overflow:hidden">' +
        '<div style="width:' + (d[1] / max * 100) + '%;height:100%;' +
        'background:var(--chart-' + d[2] + ');border-radius:var(--radius)"></div>' +
        '</div>' +
        '<div style="flex:0 0 36px;text-align:right;font-size:13px;font-weight:600">' + d[1] + '</div>' +
        '</div>';
    }).join('');
  </script>
</div>
```

## Shows by borough

The borough split mirrors what the wiki's [2010s–today](../HOME.md#2010stoday--brooklyn-dominant-queens-diversifies-manhattan-as-office) section describes: Manhattan rooms keep going on rolling small-club schedules, Brooklyn carries the indie-rock mid-size load, and Queens has both the largest outdoor seasonal venue (Forest Hills Stadium) and the warehouse-dance extension (Knockdown Center, Nowadays, Trans-Pecos).

```html preview
<div style="font-family:system-ui,sans-serif;padding:20px;color:var(--foreground)">
  <h3 style="margin:0 0 14px;font-size:15px;font-weight:600">Upcoming shows by borough</h3>
  <div style="display:flex;align-items:center;gap:24px;flex-wrap:wrap">
    <svg width="180" height="180" viewBox="0 0 180 180" role="img" aria-label="Borough share donut">
      <circle cx="90" cy="90" r="68" fill="none" stroke="var(--border)" stroke-width="22" />
      <circle cx="90" cy="90" r="68" fill="none" stroke="var(--chart-1)" stroke-width="22"
        stroke-dasharray="208 219" stroke-dashoffset="0" transform="rotate(-90 90 90)" />
      <circle cx="90" cy="90" r="68" fill="none" stroke="var(--chart-2)" stroke-width="22"
        stroke-dasharray="129 298" stroke-dashoffset="-208" transform="rotate(-90 90 90)" />
      <circle cx="90" cy="90" r="68" fill="none" stroke="var(--chart-3)" stroke-width="22"
        stroke-dasharray="90 337" stroke-dashoffset="-337" transform="rotate(-90 90 90)" />
      <text x="90" y="86" text-anchor="middle" font-size="13" fill="var(--muted-foreground)">total</text>
      <text x="90" y="106" text-anchor="middle" font-size="22" font-weight="700" fill="var(--foreground)">126</text>
    </svg>
    <div style="display:flex;flex-direction:column;gap:8px;min-width:200px">
      <div style="display:flex;align-items:center;gap:10px">
        <span style="width:14px;height:14px;background:var(--chart-1);border-radius:3px"></span>
        <span style="flex:1;font-size:13px">Queens</span>
        <span style="font-weight:600;font-size:13px">49% · 41 shows</span>
      </div>
      <div style="display:flex;align-items:center;gap:10px">
        <span style="width:14px;height:14px;background:var(--chart-2);border-radius:3px"></span>
        <span style="flex:1;font-size:13px">Brooklyn</span>
        <span style="font-weight:600;font-size:13px">30% · 30 shows</span>
      </div>
      <div style="display:flex;align-items:center;gap:10px">
        <span style="width:14px;height:14px;background:var(--chart-3);border-radius:3px"></span>
        <span style="flex:1;font-size:13px">Manhattan</span>
        <span style="font-weight:600;font-size:13px">21% · 33 shows</span>
      </div>
    </div>
  </div>
  <p style="font-size:12px;color:var(--muted-foreground);margin-top:12px">
    Manhattan shows are concentrated in the small Lower East Side / Village rooms (Mercury Lounge, Bowery Ballroom, Blue Note, Village Vanguard).
    Queens leads on count because Forest Hills Stadium publishes its full multi-month season at once.
  </p>
</div>
```

## Shows by month

The summer-into-fall shape is driven entirely by Forest Hills Stadium's outdoor season (June through October); the indoor clubs publish on shorter horizons, so July–August counts will rise as those calendars roll forward.

```html preview
<div style="font-family:system-ui,sans-serif;padding:20px;color:var(--foreground)">
  <h3 style="margin:0 0 14px;font-size:15px;font-weight:600">Upcoming shows per month</h3>
  <div id="months" style="display:flex;align-items:flex-end;gap:14px;height:200px"></div>
  <script>
    var data = [
      ['May\n(22–31)', 38],
      ['Jun', 41],
      ['Jul', 9],
      ['Aug', 8],
      ['Sep', 5],
      ['Oct', 3]
    ];
    var max = Math.max.apply(null, data.map(function (d) { return d[1]; }));
    document.getElementById('months').innerHTML = data.map(function (d, i) {
      return '<div style="flex:1;display:flex;flex-direction:column;align-items:center;' +
        'gap:6px;height:100%;justify-content:flex-end">' +
        '<span style="font-size:12px;font-weight:600">' + d[1] + '</span>' +
        '<div style="width:100%;height:' + (d[1] / max * 100) + '%;' +
        'background:var(--chart-' + ((i % 5) + 1) + ');' +
        'border-radius:var(--radius) var(--radius) 0 0"></div>' +
        '<span style="font-size:11px;color:var(--muted-foreground);white-space:pre-line;text-align:center">' + d[0] + '</span>' +
        '</div>';
    }).join('');
  </script>
  <p style="font-size:12px;color:var(--muted-foreground);margin-top:12px">
    May only counts shows from the pull date (May 22) forward. The mid-summer dip reflects the short publishing horizon of small/mid clubs, not a real lull — expect July and August counts to climb as Bowery Presents and Mercury East roll their calendars.
  </p>
</div>
```

## Show times across the night

A small thing the calendars surface: when each venue tends to start. The jazz clubs run early-and-late double sets; the dance rooms don't unlock the floor until 10 PM or later.

```html preview
<div style="font-family:system-ui,sans-serif;padding:20px;color:var(--foreground)">
  <h3 style="margin:0 0 14px;font-size:15px;font-weight:600">Typical show start time, by venue type</h3>
  <div style="position:relative;height:60px;margin:24px 0 12px 0">
    <div style="position:absolute;inset:24px 0 24px 0;background:var(--border);border-radius:var(--radius)"></div>
    <div style="position:absolute;left:0;right:0;top:0;bottom:0;font-size:11px;color:var(--muted-foreground)">
      <span style="position:absolute;left:0;top:0">5 PM</span>
      <span style="position:absolute;left:25%;top:0;transform:translateX(-50%)">8 PM</span>
      <span style="position:absolute;left:50%;top:0;transform:translateX(-50%)">11 PM</span>
      <span style="position:absolute;left:75%;top:0;transform:translateX(-50%)">2 AM</span>
      <span style="position:absolute;right:0;top:0">5 AM</span>
    </div>
    <div style="position:absolute;left:8.3%;width:8.3%;top:28px;height:14px;background:var(--chart-5);border-radius:4px" title="Mercury Lounge early sets 6 PM"></div>
    <div style="position:absolute;left:25%;width:16.7%;top:28px;height:14px;background:var(--chart-1);border-radius:4px" title="Indie clubs 8–10 PM"></div>
    <div style="position:absolute;left:33.3%;width:16.7%;top:28px;height:14px;background:var(--chart-2);border-radius:4px;opacity:0.85" title="Jazz first set 8 PM, second 10:30 PM"></div>
    <div style="position:absolute;left:50%;width:33.3%;top:28px;height:14px;background:var(--chart-4);border-radius:4px" title="Nowadays / Knockdown 10 PM – 4 AM"></div>
    <div style="position:absolute;left:75%;width:8.3%;top:28px;height:14px;background:var(--chart-3);border-radius:4px" title="Mister Sunday daytime ends ~9 PM"></div>
  </div>
  <div style="display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:8px;font-size:12px">
    <div><span style="display:inline-block;width:10px;height:10px;background:var(--chart-5);border-radius:2px;margin-right:6px"></span>Mercury Lounge early shows (6 PM)</div>
    <div><span style="display:inline-block;width:10px;height:10px;background:var(--chart-1);border-radius:2px;margin-right:6px"></span>Indie clubs / Brooklyn Steel (7–10 PM)</div>
    <div><span style="display:inline-block;width:10px;height:10px;background:var(--chart-2);border-radius:2px;margin-right:6px"></span>Jazz double sets (8 PM &amp; 10:30 PM)</div>
    <div><span style="display:inline-block;width:10px;height:10px;background:var(--chart-4);border-radius:2px;margin-right:6px"></span>Warehouse dance (10 PM–4 AM)</div>
    <div><span style="display:inline-block;width:10px;height:10px;background:var(--chart-3);border-radius:2px;margin-right:6px"></span>Mister Sunday daytime (3 PM–9 PM)</div>
  </div>
</div>
```

## Listings by venue

Each listing block links to that venue's wiki page so you can read the room's history alongside what's playing in it now. Where a calendar listed only "Doors" the door time is given; otherwise the show time.

### [Forest Hills Stadium](../neighborhoods/forest-hills/venues/forest-hills-stadium.md) — Queens, 13,000 cap

The full 2026 outdoor season, June through October. Highlights: a [Bob Dylan](../genres/jazz/overview.md) night with Lucinda Williams (2026-07-21), [Paul Simon](../neighborhoods/greenwich-village/overview.md) solo (2026-07-08), three nights of [King Gizzard & The Lizard Wizard](../genres/post-punk-revival/overview.md) (2026-08-20/21/22, with a Rave Show on the 22nd), [Erykah Badu](../genres/hip-hop/overview.md) (2026-09-18), and an evening with [David Byrne](../genres/punk-rock/artists/talking-heads.md) (2026-09-19).

- **2026-06-06** — Bright Eyes (with Built to Spill)
- **2026-06-10** — Dave Matthews Band
- **2026-06-13** — The Black Crowes & Whiskey Myers (with Southall)
- **2026-06-19** — Rock the Blessings: Juneteenth for the People
- **2026-06-20** — Wilco (with Yo La Tengo)
- **2026-06-27** — Kes
- **2026-07-08** — Paul Simon
- **2026-07-11** — Sarah McLachlan (with Allison Russell)
- **2026-07-17** — Djo (with Pond)
- **2026-07-18** — Zeds Dead (with ALLEYCVT)
- **2026-07-21** — Bob Dylan (with Lucinda Williams; Jimmie Vaughan & The Tilt-A-Whirl Band)
- **2026-07-23** — CAAMP (with Mon Rovîa and Hannah Cohen)
- **2026-08-16** — Jon Batiste
- **2026-08-20** — King Gizzard & The Lizard Wizard
- **2026-08-21** — King Gizzard & The Lizard Wizard
- **2026-08-22** — King Gizzard & The Lizard Wizard (Rave Show)
- **2026-08-27** — Zac Brown Band (with Grace Potter)
- **2026-08-28** — Zac Brown Band (with Grace Potter)
- **2026-08-29** — Empire of the Sun (with Polo & Pan; Midnight Generation)
- **2026-09-16** — The Hayley Williams Show
- **2026-09-18** — Erykah Badu (and Special Guests)
- **2026-09-19** — An Evening with David Byrne
- **2026-09-29** — Dermot Kennedy (with Jonah Kagen)
- **2026-10-02** — Geese
- **2026-10-03** — Geese
- **2026-10-10** — Foster the People (with Goth Babe)

### [Brooklyn Steel](../neighborhoods/bushwick/venues/brooklyn-steel.md) — Bushwick, 1,800 cap

Bowery Presents' Brooklyn flagship. [They Might Be Giants](../genres/punk-rock/overview.md) on the way out of May, [Kevin Morby](../genres/post-punk-revival/overview.md) and [Wolfmother](../genres/post-punk-revival/overview.md) in June.

- **2026-05-30** — They Might Be Giants (16+) · 8:00 PM
- **2026-06-10** — Kevin Morby (16+) · 8:00 PM
- **2026-06-13** — Underscores · 7:30 PM
- **2026-06-20** — Said The Sky (18+) · 10:00 PM
- **2026-06-23** — Wolfmother · 7:00 PM
- **2026-06-26** — RENROD & AMPLIFY · 9:00 PM (Doors 8:00 PM)

### [Bowery Ballroom](../neighborhoods/lower-east-side/venues/bowery-ballroom.md) — Lower East Side, 575 cap

[Frankie Cosmos](../genres/post-punk-revival/overview.md) closing out a *Next Thing* anniversary run, [Greta Van Fleet](../genres/punk-rock/overview.md) playing the wrong size of room, and a Strokes tribute (*The Brokes*) on 5/29 — the kind of programming the wiki's [post-punk revival](../genres/post-punk-revival/overview.md) section describes.

- **2026-05-22** — Frankie Cosmos: 10 Years of Next Thing (Sold Out) · 8:00 PM
- **2026-05-26** — Just Mustard (with Catcher) · 7:00 PM
- **2026-05-27** — Greta Van Fleet · 7:00 PM
- **2026-05-28** — FIGHTMASTER (with Gordi) · 7:00 PM
- **2026-05-29** — The Brokes: The Strokes Experience · 8:00 PM
- **2026-05-30** — Dove Ellis (with Mary In the Junkyard) (Sold Out) · 7:00 PM
- **2026-05-31** — Dove Ellis (with Mary In the Junkyard) · 7:00 PM
- **2026-06-01** — Sadie Jean (with Gabriela Bee) · 7:00 PM
- **2026-06-02** — Solya (with Tele Novella) · 7:00 PM
- **2026-06-03** — Witch Club Satan (with Penelope Trappes) · 7:00 PM
- **2026-06-05** — Gov Ball After Dark: Wisp (presented by NÜTRL) · 10:00 PM
- **2026-06-06** — The Smiths Tribute: *The Queen Is Dead* 40th Anniversary Tour · 8:00 PM

### [Mercury Lounge](../neighborhoods/lower-east-side/venues/mercury-lounge.md) — Lower East Side, 250 cap

The city's primary first-headlining-show room is doing exactly that — most names below have ≤2 prior NYC headline dates. The Clash tribute (5/23) and KPop rave (5/29) are the outliers.

- **2026-05-22** — Telescreens · Doors 9:00 PM
- **2026-05-23** — *Straight to Hell: The Clash Tribute* · Doors 9:00 PM
- **2026-05-24** — Barndog, Ranford Almond, The Dealers · Doors 5:00 PM
- **2026-05-24** — The Montaines · Doors 8:00 PM
- **2026-05-25** — Gio Genesis, Dap the Contract, Timi O · Doors 6:00 PM
- **2026-05-25** — Muscle B\*tch, Worship Team, yard. · Doors 9:00 PM
- **2026-05-26** — Sydney Ross Mitchell (Sold Out) · Doors 6:00 PM
- **2026-05-26** — Leo Middea (Sold Out) · Doors 9:00 PM
- **2026-05-27** — Alex Lambert · Doors 6:00 PM
- **2026-05-27** — *Music For Enophiles* · Doors 9:00 PM
- **2026-05-28** — The Unlikely Candidates · Doors 9:00 PM
- **2026-05-29** — *Next Level: KPop Rave* · Doors 9:00 PM

### [Music Hall of Williamsburg](../neighborhoods/williamsburg/venues/music-hall-of-williamsburg.md) — Williamsburg, 550 cap

The Brooklyn-side sibling of the Bowery rooms. A [Pete Yorn](../genres/post-punk-revival/overview.md) solo-acoustic date (6/7) and an early-evening [Latin Night](../genres/electronic-dance/overview.md) residency anchor June.

- **2026-05-29** — Leven Kali (with Adanna Duru, 18+) · 8:00 PM
- **2026-06-05** — Earlybirds Club: Latin Night (21+) · 6:00 PM
- **2026-06-06** — Earlybirds Club (21+) · 6:00 PM
- **2026-06-07** — Pete Yorn — solo acoustic · 8:00 PM
- **2026-06-09** — Feng · 7:00 PM
- **2026-06-10** — Bella Kay (16+) · 7:00 PM
- **2026-06-12** — Whitmer Thomas (18+) · 8:00 PM
- **2026-06-16** — 49th & Main (18+) · 8:00 PM
- **2026-06-17** — 49th & Main (16+) · 8:00 PM

### [Brooklyn Bowl](../neighborhoods/williamsburg/venues/brooklyn-bowl.md) — Williamsburg, 600 cap

The bowling-and-concert hybrid the wiki describes runs a mix of ticketed shows, family bowling matinees, and Knicks-playoff watch parties. The [Radiohead/Phish mashup](../genres/post-punk-revival/overview.md) night on 5/29 is the most-Brooklyn-Bowl thing imaginable.

- **2026-05-22** — Brooklyn Bowl Goes Country: Two-Step & Line Dance Party with CRYS! · 8:00 PM (Doors 6:00 PM)
- **2026-05-23** — Family Bowl · 12:00 PM (no cover)
- **2026-05-23** — Official Knicks Playoffs Watch Party: ECF Game 3 · 8:00 PM (Doors 6:00 PM)
- **2026-05-24** — Family Bowl — Rock & Roll Playhouse: Kids Dance Party · 12:00 PM (no cover)
- **2026-05-25** — Official Knicks Playoffs Watch Party: ECF Game 5 · 8:00 PM (Doors 6:00 PM)
- **2026-05-27** — Open for Bowling (no cover)
- **2026-05-28** — Party After feat. Stretch Armstrong (Colin Staton) · 7:00 PM (Doors 6:00 PM)
- **2026-05-29** — Weird Phishes: A Mashup of Radiohead and Phish (Owls By Day) · 8:00 PM

### [Blue Note](../neighborhoods/greenwich-village/venues/blue-note.md) — Greenwich Village, jazz

Every booking below runs the classic double-set format the wiki describes (8:00 PM and 10:30 PM). A four-night [Terrace Martin](../genres/jazz/overview.md) residency lands 5/26–5/29; [Estelle](../genres/jazz/overview.md) sits out of genre on 5/25.

- **2026-05-22** — Kenny Garrett · 8:00 PM & 10:30 PM
- **2026-05-23** — Benito Gonzalez Trio · 1:30 PM
- **2026-05-23** — Kenny Garrett · 8:00 PM & 10:30 PM
- **2026-05-25** — Estelle · 8:00 PM & 10:30 PM
- **2026-05-26** — The Terrace Martin Residency · 8:00 PM & 10:30 PM
- **2026-05-27** — The Terrace Martin Residency · 8:00 PM & 10:30 PM
- **2026-05-28** — The Terrace Martin Residency · 8:00 PM & 10:30 PM
- **2026-05-29** — The Terrace Martin Residency · 8:00 PM & 10:30 PM
- **2026-05-30** — John Violinist · 1:30 PM
- **2026-05-30** — The Terrace Martin Residency · 8:00 PM & 10:30 PM

### [Village Vanguard](../neighborhoods/greenwich-village/venues/village-vanguard.md) — Greenwich Village, jazz

Weekly Tuesday–Sunday residencies, the format the room has held since 1935. The venue closes 7/6–7/12 for maintenance and reopens with the Vanguard Jazz Orchestra.

- **2026-05-23 → 2026-05-24** — David Murray Quartet
- **2026-05-26 → 2026-05-31** — Ambrose Akinmusire
- **2026-06-02 → 2026-06-07** — Kurt Rosenwinkel Quintet
- **2026-06-09 → 2026-06-14** — Renee Rosnes Quartet
- **2026-06-16 → 2026-06-21** — Fred Hersch / Drew Gress / Peter Erskine
- **2026-06-23 → 2026-06-28** — Terell Stafford Quintet
- **2026-06-30 → 2026-07-05** — James Brandon Lewis Quartet
- **2026-07-14 → 2026-07-19** — Ben Wendel

### [Apollo Theater](../neighborhoods/harlem/venues/apollo-theater.md) — Harlem

The Apollo's main stage is between major bookings; the immediate window is anchored by the smaller *Apollo Stages at The Victoria* and a free *Sincere Light* tribute to D'Angelo at the Lincoln Center plaza.

- **2026-05-29** — *Muted Genius: Miles Davis at 100* (Apollo Stages at The Victoria) · 7:30 PM
- **2026-06-25** — *A Visible Life: Defining Black Gay Identity Through Performance* (Apollo Stages at The Victoria) · 7:30 PM
- **2026-06-27** — *Sincere Light: A Tribute to D'Angelo* (Dance Floor at Josie Robertson Plaza, free, DJ Reborn) · 10:00 PM

### [Knockdown Center](../neighborhoods/ridgewood/venues/knockdown-center.md) — Ridgewood/Maspeth, dance + indoor concerts

The Queens-side warehouse hub the wiki describes. [Horse Meat Disco](../genres/electronic-dance/overview.md) for Memorial Day weekend (5/24), a two-night *Total Bummer Festival* with Dinosaur Jr. and The Jesus and Mary Chain (5/30–5/31), and the dance booking [VTSS A/V Tour](../genres/electronic-dance/overview.md) on 6/6.

- **2026-05-24** — Horse Meat Disco NY (Memorial Day Weekend)
- **2026-05-30 → 2026-05-31** — *Total Bummer Festival*: Dinosaur Jr., The Jesus and Mary Chain + more
- **2026-06-05** — Marten Lou
- **2026-06-06** — RUSH & For Your Entertainment present: VTSS (A/V Tour)
- **2026-06-20** — Vacations — MATES Festival
- **2026-06-27** — Get Wrecked & Carry — Pride

### [Nowadays](../neighborhoods/ridgewood/venues/nowadays.md) — Ridgewood, indoor + outdoor dance

The Mister Saturday Night–founded room runs its weekly outdoor *Mister Sunday* between mid-May and late October — this is the season-opener and the recurring Sunday party listed on RA. Most Friday/Saturday programming is published one week out on the venue's RA page.

- **2026-05-10** *(season opener already passed)* — Mister Sunday Season Opener: Justin Carter & Eamon Harkin · 3:00 PM–9:00 PM
- **Recurring Sundays, mid-May–late October** — Mister Sunday (Justin Carter & Eamon Harkin and rotating guests) · 3:00 PM–9:00 PM
- **Most Fri / Sat nights** — Indoor floor; programmed week-of via [ra.co/clubs/105873](https://ra.co/clubs/105873)

### [Trans-Pecos](../neighborhoods/ridgewood/venues/trans-pecos.md) — Ridgewood, DIY all-ages

DIY booking moves week-by-week; only the dates already on aggregators are listed. Booking inquiries go to `booking@thetranspecos.com`.

- **2026-05-29** — BrokinPaper
- **2026-07-16** — Vorhex Angel and Luke Schneider
- **2026-09-24** — Otto Benson

## Methodology

- **Pulled 2026-05-22** from each venue's public calendar; the Bowery Presents rooms (Bowery Ballroom, Mercury Lounge, Brooklyn Steel, Music Hall of Williamsburg) all redirect to `bowerypresents.com` calendars; small/DIY venues required aggregator fallback (Songkick, doNYC, Bandsintown, ra.co, BrooklynVegan).
- **Open-vs-closed filter:** the wiki describes 19 venues across all eras. The seven historical rooms ([CBGB](../neighborhoods/lower-east-side/venues/cbgb.md), [Max's Kansas City](../neighborhoods/greenwich-village/venues/maxs-kansas-city.md), [Studio 54](../neighborhoods/midtown-times-square/venues/studio-54.md), [Paradise Garage](../neighborhoods/soho/venues/paradise-garage.md), [Mudd Club](../neighborhoods/soho/venues/mudd-club.md), [Danceteria](../neighborhoods/chelsea-meatpacking/venues/danceteria.md), [Knitting Factory](../neighborhoods/soho/venues/knitting-factory.md)) closed between 1980 and 2009. [Electric Lady Studios](../neighborhoods/greenwich-village/venues/electric-lady-studios.md) is a recording studio, not a public concert venue, so it's excluded. [Saint Vitus](../neighborhoods/greenpoint/venues/saint-vitus.md) is still described in the wiki as operating but closed permanently 2024-08-17 — flagged in the callout above and excluded from counts.
- **Show-count caveats:** the Forest Hills Stadium count is the full publicly-announced 2026 outdoor season; small/mid clubs publish on rolling 4–8 week horizons so their counts are floors, not ceilings. The Nowadays and Trans-Pecos counts are particularly understated because both publish week-of and most of their schedule moves through DICE / Instagram rather than aggregator feeds.
- **Saint Vitus closure verified** against the [Wikipedia article on the venue](https://en.wikipedia.org/wiki/Saint_Vitus_(venue)), which quotes the venue's own 2024-08-17 Instagram closure announcement.

## Further reading

- **Venue calendars (pulled 2026-05-22):** [Brooklyn Steel](https://www.bowerypresents.com/brooklyn-steel/calendar/) · [Bowery Ballroom](https://www.mercuryeastpresents.com/boweryballroom) · [Mercury Lounge](https://www.mercuryeastpresents.com/mercurylounge) · [Music Hall of Williamsburg](https://www.bowerypresents.com/music-hall-of-williamsburg/calendar/) · [Brooklyn Bowl](https://www.brooklynbowl.com/brooklyn) · [Blue Note NYC](https://www.bluenotejazz.com/nyc/shows) · [Village Vanguard](https://villagevanguard.com/) · [Apollo Theater](https://www.apollotheater.org/calendar/) · [Knockdown Center](https://www.knockdown.center/upcoming) · [Nowadays (RA)](https://ra.co/clubs/105873) · [Trans-Pecos (Songkick)](https://www.songkick.com/venues/2491899-transpecos/calendar)
- **Forest Hills Stadium 2026 lineup:** [Time Out — "2026 Concert Lineup for Forest Hills Stadium in Queens, NY"](https://www.timeout.com/newyork/news/heres-the-full-lineup-for-the-2026-forest-hills-stadium-concert-series-050626) · [Forest Hills Stadium calendar](https://foresthillsstadium.com/calendar/)
- **Saint Vitus closure:** [Saint Vitus (venue) — Wikipedia](https://en.wikipedia.org/wiki/Saint_Vitus_(venue))
- **Genre and venue context within this wiki:** [HOME](../HOME.md) · [post-punk revival](../genres/post-punk-revival/overview.md) · [electronic dance](../genres/electronic-dance/overview.md) · [jazz](../genres/jazz/overview.md) · [hip-hop](../genres/hip-hop/overview.md) · [Ridgewood overview](../neighborhoods/ridgewood/overview.md) · [Lower East Side overview](../neighborhoods/lower-east-side/overview.md)
