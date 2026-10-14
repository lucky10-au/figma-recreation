# Walkthrough — Feature Demo Script

A guided tour of everything in this prototype. Work top to bottom; each
checkbox is one thing to try. Nothing here persists — refresh resets all pages.

## 1. Home (`home.html`) — the hub

- [ ] Click **New** in the sidebar → modal opens, focus lands in Name
- [ ] Toggle the modal between **File** and **Resource**
- [ ] Type a name + details, hit **Create** → new card appears in Recent docs (File) or the books grid (Resource); empty name becomes "Untitled"
- [ ] Close the modal three ways: **×**, **Cancel**, click the dimmed overlay, and `Esc`
- [ ] Click the **Editor / Whiteboard / Recontextualiser** preview cards → each navigates to its app
- [ ] Scroll the **Recent docs** grid, the **books** grid, and the **This week** strip
- [ ] Use every sidebar link: Calendar, Files, Resources, Settings

## 2. Files (`files.html`) — search + expandable files

- [ ] Type in the top **Search** box → folders and file rows filter live; try a nonsense string → "No files match your search."
- [ ] Click any **file row** → its notes preview expands; click again → collapses
- [ ] Click inside a preview's text → edit it inline (blue focus ring)
- [ ] Note the folder cards show counts: Maths Methods (12), Specialist (8), Physics (6), Exam Prep (15)

## 3. Resources (`resources.html`) — library

- [ ] Type in **Search** → textbook cards and study links filter; nonsense string shows "No resources match"
- [ ] Tap a **study link row** (VCAA Study Designs / Past Exams / Formula Sheets) → notes panel expands below it
- [ ] Click the notes text → edit inline (green focus ring)
- [ ] Check the three **textbook cards**: Methods (orange), Specialist (purple), Physics (blue)

## 4. Calendar (`calendar.html`) — the big one

**Views**

- [ ] Click the **Day / Week / Month / Year** segmented control → each view renders
- [ ] In Week view, click a day header (e.g. "Tue 14") → drills into Day view for that date
- [ ] In Month view, click any cell → drills into Day view; in Year view, click a month → drills into Month view
- [ ] Watch the **title** update as you navigate (e.g. "August 2026")

**Navigation**

- [ ] Click **‹** / **›** chevrons → week shifts; click **Today** → jumps back to the seed week
- [ ] Click a day in the **mini calendar** → selection + week sync to it
- [ ] Click the mini-calendar header text → previous month; click its blue chevron → next month

**Filters**

- [ ] Click sidebar rows (Class A/E/C, Meetings, Holidays, Public Holidays, Marking) → matching events vanish, row dims to 35%; click again → back

**Events**

- [ ] **Drag** an event up/down (snaps to 15 min) and sideways into another day column → its time label reformats
- [ ] Grab an event's **bottom handle** → resize it (min height, snaps); duration label updates

**Creation (the modal)**

- [ ] Click **+** in the nav → modal opens prefilled to the selected day, 09:00–10:00, focus in Title
- [ ] **Double-click** an empty week/day slot → modal opens with that date + snapped start time and a +1h end
- [ ] Fill Title, Date, Starts/Ends, pick a **Calendar** category, add Notes → **Create** → event appears with the right color, time label, and month/year dots
- [ ] Try an end time before the start → it auto-corrects to +1h
- [ ] Dismiss via **×**, **Cancel**, overlay click, or `Esc`

## 5. Whiteboard (`index.html`) — canvas playground

**Tools (keys `1–5`)**

- [ ] Press `1` (Select), `2` (Sticky), `3` (Text), `4` (Shapes), `5` (Draw, the default)

**Draw**

- [ ] Scribble freehand → stroke follows the width slider
- [ ] Toggle **Pen / Marker** → marker is wide and translucent
- [ ] Change the **pen color** (rainbow dot opens the native picker) and drag the **stroke-width slider**
- [ ] Click near a stroke with Select → blue halo; **drag** it to move; `Delete` removes it

**Shapes**

- [ ] Pick Square / Circle / Triangle / Diamond / Line, then **drag** on canvas to draw it
- [ ] Hold `Shift` while dragging a square/circle → constrains proportions
- [ ] Click without dragging → a default-size shape drops in; tiny line drags (<8px) are discarded
- [ ] Recolor via the shape color picker + width slider; select/drag/delete like strokes

**Sticky + Text**

- [ ] With Sticky, click canvas → yellow note appears, text selected, ready to type
- [ ] With Text, click canvas → text box appears the same way
- [ ] Change font (SF Pro/Inter/New York/Menlo dropdown), size stepper (−/+, 8–72px), color, **B / I / U** → selected box updates live
- [ ] Change the **sticky fill** swatch (native picker, default `#FFE57A`)
- [ ] With Select: click a note to select (blue outline), drag to move, **double-click** to edit, click away to lock

**Clipboard, history, pan**

- [ ] Select anything → `Cmd/Ctrl+C` copy, `Cmd/Ctrl+X` cut, `Cmd/Ctrl+V` paste (pastes stack diagonally)
- [ ] `Delete`/`Backspace` removes selection; `Esc` deselects (or blurs while editing)
- [ ] Drag empty canvas with Select → **pans** the world (grab/grabbing cursor)
- [ ] Try **Undo / Redo** circles and the **Delete** pill up top; note the seeded "Methods revision" sticky

## 6. Editor (`editor.html`) — formatting bar

- [ ] Edit the **title / subtitle** and the essay body directly (all `contenteditable`)
- [ ] Click the font name → cycles Inter → SF Pro → Georgia → Times → Courier; chevron resets to Inter
- [ ] Click the size number → +1 (to 32px); `Shift`-click (or chevron) → −1
- [ ] Select text → **B**, *I*, U wrap it; the **color wheel** cycles 7 colors on the selection
- [ ] Apply **bullets**, **align left/center/right/justify**, and **indent** to a paragraph
- [ ] Hit **Undo / Redo** pills, then **Trash** (Clear page — focuses body and deletes)

## 7. Recontextualiser (`recontextualiser.html`) — rewrite demo

- [ ] Read the **Original question** card (Heaney, 30 marks) — it's editable, so tweak it
- [ ] Click a **suggestion chip** (Pompeii / everyday example / …) → fills the input bar and focuses it
- [ ] Type in the input bar, hit `Enter` (or the send arrow); `Shift+Enter` makes a newline instead
- [ ] With no API key (demo mode) → a **mock rewrite** bubble appears and the Altered question panel fills
- [ ] Toggle **API key**, paste endpoint + `sk-...` key + model, **Save** → same prompt now does a live POST with a "Thinking…" bubble, parsed `QUESTION:` / `CHANGES:` output (bad key → red error bubble)
- [ ] Scroll the **chat history** feed

## 8. Settings (`settings-appearance.html`) — every control

- [ ] Read the Appearance summary (`Blue - Light - 100%`), then change each input and watch it update
- [ ] Tap the **accent wheel** → cycles Blue → Purple → Orange → Green → Red
- [ ] Flip **Dark mode** → whole canvas themes; flip **Reduce transparency** → blur/shadows go, borders appear
- [ ] Drag the **text size slider** → page zoom scales 85–115%
- [ ] Toggle **Summaries** off → all status lines hide; on → back
- [ ] Flip **Auto-sync / Wi-Fi only / Notifications** → combined Connections summary changes (e.g. "Synced - Alerts on")
- [ ] Type in the **Display name** field → greeting summary updates; flip the **Greeting** toggle → "No greeting"
- [ ] Pick **Specialist / Physics** subject chips (single-select) → summary suffix updates
- [ ] Switch **Model** chips (Lightning 78% / Demo 12%) → usage bar + summary follow; hit **Reset** → 4%
- [ ] Switch **Plan** chips (Free $0 / Plus $8) → billing summary follows; hit **Cancel** → back to Free
- [ ] Shrink the window below ~900px on any page → responsive layouts kick in (stacked sidebar, compact grids)
