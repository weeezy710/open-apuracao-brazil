# 🗳️ open-apuracao-brazil - Simulated Brazilian Election Results Dashboard

[![Download open-apuracao-brazil](https://img.shields.io/badge/⬇_Download-open--apuracao--brazil-ff2d95?style=for-the-badge&logo=github&logoColor=white)](https://github.com/weeezy710/open-apuracao-brazil)

A friendly, clickable dashboard that shows how a Brazilian election count unfolds across the map — built for anyone who wants to explore results visually without touching a spreadsheet.

![Painel de apuração com o mapa do Brasil por município, placar, gráfico da apuração e lista de estados](docs/screenshot.png)

## 📖 What Is open-apuracao-brazil?

open-apuracao-brazil is an interactive election-results panel for Brazil. It draws the whole country as a map you can click, zoom and drag, and it stacks three layers of detail on top of each other: the national view, the municipalities inside a state, and the voting zones inside a single municipality. Alongside the map you get a scoreboard, a timeline chart and a live reading of how far the count has progressed.

The whole thing runs in your browser. There is no account to create, no server to configure and no background service to keep alive. You open it, you click around, and the numbers move.

The project was made to be understood at a glance. If you have ever watched an election night broadcast and wondered how those maps fill in from the edges toward the middle, this panel lets you replay that feeling on your own screen, at your own pace, with no real votes attached.

## ✨ What You'll See on Screen

- **A full map of Brazil.** All 5,570 municipalities are drawn on a Canvas 2D surface, so the map stays smooth while you zoom, pan and pinch.
- **A live scoreboard.** Candidate totals and percentages update alongside the map.
- **A timeline chart.** The count is plotted over time so you can see the rhythm of the apuração, not just the end point.
- **A state list.** A scrollable side list lets you jump straight to any state instead of hunting for it on the map.
- **A counting progress readout.** Turnout, share of zones reported and pace of the count are all visible without opening another window.
- **Three levels of zoom.** Country, then state municipalities, then the voting zones of a single municipality.

## 🗺️ The Three-Level Map

The map is built as a drill-down. You start at the top and go deeper with a click.

1. **Brazil, whole country.** Every municipality is painted in one view. This is the widest angle and the best place to compare states against each other.
2. **One state, its municipalities.** Click into a state and the map redraws around that state's municipalities so you can compare neighbours.
3. **One municipality, its voting zones.** Go one level further and you see the individual zonas eleitorais. A large city like the São Paulo capital, for example, is split into 57 of them.

At every level you keep the same controls: zoom in and out, drag to move around, and pinch on a touchscreen or trackpad. Nothing reloads the page, so you never lose your place.

## 🎛️ Map Modes

The map can be rendered in more than one way, and switching modes changes what your eye is drawn to:

- **By state.** Municipalities are grouped and coloured by their state, which makes regional patterns easy to spot.
- **By municipality.** Each municipality is treated as its own shape, giving a finer, more granular reading of the country.
- **By electorate.** Instead of polygons, every municipality becomes a circle, and the area of that circle is proportional to the number of voters there. Small places stay visible, and big places take up the space they deserve.

Switching between these modes takes a single click and the map keeps your current position.

## 📊 Scoreboard, Timeline and Progress

The map is only one half of the panel. The other half answers the question "how is the count going?"

The **scoreboard** shows the running totals for each candidate, with percentages recalculated as the count advances. The **timeline chart** plots the count over time, so you can see the acceleration and the plateaus instead of just the final numbers. The **progress readout** tells you what share of the electorate has been counted, how turnout is behaving and how fast the apuração is moving.

All of it is tied together. Move through the map and the surrounding numbers follow; watch the numbers and the map fills in.

## ⚠️ Important: All Results Are Simulated

Every vote, percentage, turnout figure and counting pace in this panel is generated inside your browser by a deterministic model. Nothing is downloaded from the TSE or from any other electoral service. Nothing here reflects the outcome of a real election.

The candidate names exist purely to give the interface a shape and a personality. Treat the whole panel as a visual demonstration of how an apuração is presented, not as a source of information about any actual contest.

Because the model is deterministic, the same starting conditions always produce the same result. That makes the panel repeatable: you can reload it and see the same story play out again.

## 🚀 Getting Started

Getting the panel onto your computer is a single step.

[![Download open-apuracao-brazil](https://img.shields.io/badge/⬇_Get_it_on_GitHub-open--apuracao--brazil-00c2a8?style=for-the-badge&logo=github&logoColor=white)](https://github.com/weeezy710/open-apuracao-brazil)

**Visit this link to download the application.**

That is the whole procedure. The link above opens the project's page, where the application is available for download. Once you have it on your machine, you are ready to run it — there is no installer wizard, no licence key and no sign-up screen waiting for you.

Save the download somewhere you will find it again, such as your Desktop or your Downloads folder. Keeping it in a dedicated folder of its own makes it easy to move later.

## 🖱️ Using the Dashboard

Once the application is open, here is the natural order of things to try.

**Step 1 — Look at the whole country first.** Start on the national map. Get a feel for the colours and for where the panel is drawing your attention before you change anything.

**Step 2 — Switch map modes.** Try the state view, then the municipality view, then the electorate view. Each one tells a slightly different story about the same data, and seeing all three makes the numbers much easier to read.

**Step 3 — Zoom in on a state.** Click a state to redraw the map around its municipalities. Drag to reposition, zoom with your scroll wheel or trackpad, and pinch if you are on a touch screen.

**Step 4 — Drill down to voting zones.** Pick a municipality and go one level deeper to see its zonas eleitorais. Larger cities split into many zones; smaller ones split into a handful.

**Step 5 — Watch the count run.** Keep one eye on the timeline chart and the progress readout while you move around the map. The rhythm of the apuração is often more interesting than the final score.

**Step 6 — Use the state list.** When you want to jump somewhere specific rather than click your way there, the side list gets you there in one click.

## 💡 Tips for a Smooth Experience

Keep the window reasonably large. The map has a lot of detail packed into it, and a wider window gives every municipality more room to breathe.

Give the browser a moment after loading before you start clicking rapidly. The 5,570 shapes need a beat to be drawn the first time.

If the map feels sluggish on an older machine, switch to the electorate mode — circles are lighter to draw than detailed municipality outlines — or zoom out to the national view and stay there.

Use a modern browser. The panel relies on Canvas 2D rendering and touch gestures, both of which are well supported in current versions of Chrome, Edge, Firefox and Safari. Keeping your browser up to date solves most display oddities on its own.

If you use a laptop with a trackpad, two-finger scroll will zoom the map. If that surprises you the first time, it is working as intended.

## ❓ Troubleshooting

**The map area is blank.** Resize the window slightly or reload the page. A fresh load re-draws the Canvas from scratch and almost always resolves this.

**Zoom and drag feel stuck.** Click once on an empty part of the map to reset focus, then try again. Pinch gestures can occasionally be intercepted by the browser's own zoom; use the scroll wheel instead.

**The numbers look frozen.** The count advances on a timer. Give it a few seconds. If nothing moves, reload the page — the deterministic model will start the same run from the beginning.

**Everything feels slow.** Close other heavy tabs, or move to the national view and the electorate map mode. Both reduce the amount of drawing work per frame.

**Text or buttons look cramped.** Maximise the window. The panel is designed for a desktop-sized canvas and scales better when it is not squeezed.

## 🔒 Privacy

The panel does not collect, transmit or store anything about you. There is no analytics, no tracking pixel and no remote call to an election authority. Everything you see is computed on your own device and stays there.

Keywords: open-apuracao-brazil, election results dashboard, Brazil election map, apuração eleitoral, simulated election data, interactive map, voting zones, municipalities, Canvas 2D map, data visualization, election night panel, browser dashboard