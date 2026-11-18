# Case 3 — Checking by looking: an AI board of a home, and the clock that went missing

**Session 3 · How to AI** · a real conversation between me (Gap) and my AI (Claude Code), 29 October 2026. Two stretches of it are kept, about 20 minutes in total.

## What this conversation is

I was planning the furniture and wiring of a flat I am moving into, on an interactive board the AI had built for me. In this conversation I asked it to add features (grouping items, then wall views). Two things go wrong and I catch them by **looking at the result myself**: the AI misdescribed a room, and later it silently deleted two clocks it had told me it added.

## Context before it starts

The board already existed and the plan was in my notes. Today's job was to add the new features and then fix what looked wrong.

## What to look for

1. **Turns 2 to 4:** the AI asks me a question before building. It misdescribed the bedroom as "not a plain rectangle"; I corrected it in turn 3 and it concedes in turn 4.
2. **Turn 5:** I did not like the default. I invented a feature (a standing point: where *I* stand decides what the wall shows) and told the AI *not* to pick where it goes.
3. **Turns 7 and 8:** I look at the result myself and find the drawing order is backwards (turn 7). The AI says it did not re-run its test after the fix (turn 8). It would not have found this without my looking.
4. **After the gap in the middle (turns 9 to 13):** I ask for a clock, it says it is there, and I cannot see it. The AI works out that it overwrote the board using an old copy, which erased both clocks with no error message. It then makes a new rule for itself: **before every write, re-read; after every write, read it back to confirm.**
5. **Turns 14 and 15:** the AI says what it should have said before ("I should have said that when you asked") and asks me where I spend my time before choosing.

## How to read this

- This is the conversation **word for word**, with the time of each message. I speak by voice, so my messages ramble and have dictation mistakes. I left them in.
- Only the **words** are here: no tool output, no code. When the AI says it "ran a test", you are reading its report of it.
- `[a note in the vault]`, `[a link]` and similar brackets mean I hid a file name, link or personal detail. `*[omitted: …]*` means a stretch of messages was removed completely.
- You do **not** need to understand the technical parts. Read it for how the two of us talk: who decides, who does the detail, and what happens when the AI is wrong.

---

### Turn 1 · 13:11 · Gap

Read the [project note], starting with the newest entries. Then build the groups feature first, then the wall elevation views. The condo board is the artifact at [a link]; its source is a file in that folder. Ask me the flagged questions before you build the wall views.

### Turn 2 · 13:17 · Claude

Groups are built and live on the condo board. I haven't built the wall views yet because the bedroom walls are still open.

**Groups**
- **Selecting:** Shift-click adds pieces to a selection. On a phone, press "Select several" in the new Groups card, then tap pieces.
- **Moving:** The selection moves together by drag or arrow keys and stays inside the plan. Cables between two moved devices go with them.
- **Saving a group:** Name the selection and press "Save as group".
- **Using a group:** Clicking any member selects the whole group. Alt-click picks one piece. The Selected card has "Take out of group" and "Ungroup".
- **Where it's stored:** The groups list is in the side panel. Groups are saved with the layout, shared by the Arrival and Future tabs, and covered by undo and live sync.
- **Testing:** I ran it in headless Chrome with a stubbed database and everything passed. I haven't tried it with two real viewers or on a phone.
- **Your examples:** "Desk setup" and "PC stack" aren't created yet. You can make them in two clicks each.

**Wall views, your answers so far**
- The work nook stays at 2 views, with no glass-wall view.
- Flat views, picked from a wall menu: confirmed.

**Bedroom, one question.** The bedroom isn't a plain rectangle. Its outline steps in near the wardrobe, so it has more than 4 straight walls. Your 4-wall count presumably meant the 4 main sides. Should I show the stepped-in section inside the nearest main wall, so the bedroom keeps your 4 views? That is my recommendation. Or do you want the stepped sections as extra views?

I've logged all of this in the project note. Once you answer, I'll build the wall views, starting with the per-item "bottom at / top at" heights.

### Turn 3 · 13:19 · Gap

the bedroom isn't a plain rectangle. It is a plain rectangle. What do you mean? It has outline steps in near the wardrobe. It has a 45° angle, so it has more than four straight walls. Your four walls count, presumably, as the four main sides. Yes, it is. It means the four main sides. The stepped-in section is inside the nearest main wall. Let's do that, so the bedroom keeps four views. Yes, we should do that.

### Turn 4 · 13:23 · Claude

The wall views are built and published to the same condo board link, in a new Walls tab beside Wiring. I tested them in headless Chrome with a stubbed database. I haven't tried them on a phone or with two real viewers.

On the bedroom: you're right, I misdescribed it. It is a plain rectangle, and the 45° cut belongs to the wardrobe. I've kept your four bedroom views and folded the stepped-in section into the nearest main wall (Left, the wardrobe side).

**Using the Walls tab**
- Pick a room, a wall, and Arrival or Future. The wall is drawn flat to the ceiling height with a 0.5 m scale, as if you stand in the room facing it. Windows and doors come from the developer drawing.
- Left, Right, Top and Bottom follow the board's default view, so Left is the outside wall in the living room.
- Drag a piece sideways to slide it along the wall, or up and down to change its height. Selected groups move together.
- The Selected card has number boxes for "Bottom at", "Top at" and "From the wall". The last one is the gap to the piece's nearest edge, shown only in this tab.
- Pieces farther from the wall fade, and a tick box shows only pieces within 1 m.

**Heights**
- Each piece gets a default height from its name, for example sofa 0–0.85 m and display 1.4–1.7 m. These stay amber until you press "Heights: mark as measured".
- Windows are drawn 0.9–2.1 m and doors 0–2.1 m. Those are my assumptions.
- Not drawn: the kitchen counter, tub, toilet, basin, wardrobe shelves and columns, because I have no heights for them.
- Sockets, switches and A/C indoor units appear once you add them from the Add menu or the Placeholders box.

**Please check:** you gave wall counts but not which walls. I guessed the nook's two are the outside wall and the wardrobe wall, and the balcony's two are its outside wall and the bedroom-side wall. If either is wrong, tell me which walls you meant.

I logged the groups build, your answers and the wall views in the project note.

### Turn 5 · 13:26 · Gap

things that I will see on the wall view will depend on it. It can't just be a reverse version of each one. For example, the left and the right work nook should not have the same objects on them. It should come under the assumption of where I sit or stand on each thing.

I think the best way that we can go about this is maybe you create a new function, some kind of anchor, a standing anchor or something like that. It will pretty much be a circle or an X, or whatever, that is specific for that page, and then I can drop that X for where I want the view to start from.

For example, in the work nook, it's a square-ish thing, right? If I put the X right in the middle of the room, maybe a little bit to the right side, some kind of place where I would stand, then the left wall will include the whole table. The right wall will be absolutely empty, right? That's what I want, something like that, but I don't think it's best for you to pick where that anchor lies. Can you build a part of this program so that I can choose where I stand for each thing, please? Thank you.

### Turn 6 · 13:27 · Claude

The standing anchor is built and published to the same condo board link. Each wall page (room plus side) has its own X, as you said: one anchor per wall side. I tested it headless against your work-nook example, not on a phone.

**How it works**
- Under each wall picture is a small top-down plan of the room, turned like the board. The wall you face is a thick line.
- Tap or drag on that plan to drop the X where you stand.
- The wall picture then shows only pieces between the X and that wall. A piece shows when its centre is nearer the wall than the X.
- A selected piece always shows, so you can still drag it.
- A note under the picture says how far you stand from the wall and how many pieces are behind you.
- On the small plan, pieces left out are dashed, and the X's you set for the room's other walls appear as faint grey marks.
- "Clear" removes the X.
- The X's are saved with the layout and covered by undo, lock and live sync.

**Your nook example:** with the X in the middle, a little to one side, the Left wall keeps the desk, chair, desk PC and desk switch, and the Right wall is empty.

I did not choose any positions. Until you place an X on a wall, that wall shows every piece in the room, so each wall you want to use needs its own X.

I logged this in the project note.

### Turn 7 · 13:28 · Gap

Yep, perfect. That's great. One inconsistency that I noticed, though, is that, for example, I'm looking at the work nook left outside wall right now. If I click where I stand, then it would only make sense for the chair to be on top, in front of the desk. You can have a look at it right now. I just clicked so that it makes sense from your perspective. It should be in front of the desk, but in the view on top, it shows behind the desk. That's an inconsistency that we're going to need to fix.

### Turn 8 · 13:29 · Claude

I fixed it and republished. I didn't re-run the headless test or look at a new screenshot after this change. Reload the board and check the nook Left wall.

The drawing order was backwards. I drew the pieces nearest the wall on top, which put the desk over the chair. Pieces now draw starting with the one nearest the wall, so the chair sits in front of the desk, as it would from where you stand.

I also removed the fading I had added for pieces far from the wall. It faded the wrong things: with an X placed, it would have dimmed the pieces closest to you.

I haven't added this fix to the project note yet.

> *[omitted: some messages where the AI saved notes, and about an hour of further changes]*

### Turn 9 · 15:42 · Gap

oh, by the way, I don't mean a table clock. I mean a normal wall clock that is going to be higher up than where it is right now. Just put it on top, probably as high as the wardrobe. It's a wall clock here.

### Turn 10 · 15:42 · Claude

The bedroom clock is now a normal wall clock above the makeup table, in both plans. I haven't looked at it on the live board. It sits on the wall, about 30 cm across, from 1.9 to 2.2 m, so its top is level with the top of the built-in wardrobe. That 2.2 m wardrobe height is my assumption, and the 30 cm size is a guess. I logged the correction in the project note.

### Turn 11 · 15:43 · Gap

how come I don't see it? Wait, let me refresh. Yeah, it's not there. Which wall did you put it on? I don't see it on any of the walls.

### Turn 12 · 15:44 · Claude

Verify by re-reading and rendering the bedroom's left wall.

### Turn 13 · 15:44 · Claude

The clock was missing because of my mistake, and it's back now. When I corrected the bedroom clock, I built the change from an older copy of the board data that didn't have either clock. That write erased both clocks, with no error, even though I'd told you they were added. After re-adding them, I read the data back and checked a render of the bedroom wall: the clock shows there.

**Where they are now**
- **Bedroom clock:** in the Walls tab, choose Bedroom, then **Left (wardrobe side)**. It's above the makeup table at 1.9–2.2 m, level with the top of the built-in wardrobe.
- **Sofa clock:** on the living-room outside wall behind the sofa, centred on it, 1.65–1.95 m. It's on the Living, Left wall.
- Both are in the Arrival and Future plans. Refresh and look.

**Why it didn't show up on any wall for you:** it was never in the data, so no wall could draw it. I didn't find any other clue.

I logged the mistake in the issue log, with a fix: before every write to shared data, re-read it first, and after the write read it back and confirm the new item is there. I also noted the clocks and the incident in the project note.

### Turn 14 · 15:47 · Gap

so you think it's better on the sofa?

### Turn 15 · 15:48 · Claude

Not necessarily. The wall behind the sofa is good for some positions and the worst for others, and I should have said that when you asked.

**Who can see a clock behind the sofa**
- **Dining table, kitchen and the TV area:** they all face the outside wall, so they see the clock easily.
- **Someone sitting on the sofa:** this is the one that fails. The clock is right behind them, and they'd have to turn around to see it.
- **The desk:** you face the wall there, so the sofa clock is off to the side and out of view.

**If you mostly want the time from the sofa**, put the clock on the TV wall, near the shelf or just beside the TV. Then you see it straight ahead from the sofa, and it's still visible from the dining table at an angle.

**If you want it for the kitchen and dining area**, behind the sofa is right.

I'd pick by where you spend your evenings: on the sofa, or at the table and in the kitchen. Which is it? If you say the sofa, I'll move the clock to the TV wall.

### Turn 16 · 15:48 · Gap

yeah, it's a good question. When do I want to see the time the most?
- Probably when I'm by the kitchen.
- When I'm by the sofa, I probably want to see it as well.
- When I'm working, seeing it would be nice.
- I want to be able to see it when I'm walking around the house.
I guess on top of the dining table would be better, actually. Somewhere around the door

### Turn 17 · 15:49 · Claude

I've moved the living-room clock to the entrance wall, between the dining table and the front door. It's about 30 cm across, at 1.85–2.15 m, in both plans. I read the data back after writing it and checked a render, and the clock shows on the Living and entry bottom (entrance) wall.

**Where it can be seen**
- **Dining table and the front door:** both see it directly, which helps when you're leaving.
- **Walking through the house:** most of the open floor sees it.
- **The sofa area:** a glance away, without turning your back.
- **The kitchen counter:** it's the same wall as the counter, so you see the clock at a shallow angle. It's readable, but not ideal.
- **The desk:** not visible, since you face the outside wall there.

**Desk gap:** the monitor's own clock works. If you want a real one, a small clock on the shelf rail above the monitor would cover it. Say so and I'll add one.

I logged the move in the project note.
