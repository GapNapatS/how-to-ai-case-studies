# Case 1 — "Did you really watch it?" (the AI that said it watched a video)

**Session 3 · How to AI** · a real conversation between me (Gap) and my AI (Claude Code), 30 October 2026, about 1 hour 20 minutes of it kept.

## What this conversation is

I sent my AI an Instagram reel because I liked the idea in it. The AI described the reel confidently. Later I asked how it had managed to "watch" it, and it admitted it had not actually watched it: it had read the caption and one still picture, and guessed the rest. We then tested five tools that can really watch a video, kept the one that worked, and checked the reel again properly.

## Context before it starts

I was in the middle of other work with this AI. I had just bought a small table for my computer and was adjusting a plan for it. Then I sent the reel, and this conversation begins there.

## What to look for

1. **Turn 2:** the AI says plainly "I can't tell which idea you mean" instead of pretending. Then it lists the possible readings and asks.
2. **Turn 8:** I asked "how come I was able to get you to watch an Insta reel before?" and it says: *"I didn't actually watch the reel."* This is the moment that matters. I only got that answer because I asked.
3. **Turns 9 to 12:** I said "test all of it, find the best one". It tested five tools, reported which failed and why, and in turn 12 it separates what it saw from what it only read.
4. **Turns 16 to 18:** a tool install was blocked. Notice what the AI does and does not do, and how it checks that nothing was installed.

## How to read this

- This is the conversation **word for word**, with the time of each message. I speak by voice, so my messages ramble and have dictation mistakes. I left them in.
- Only the **words** are here: no tool output, no code. When the AI says it "ran a test", you are reading its report of it.
- `[a note in the vault]`, `[a link]` and similar brackets mean I hid a file name, link or personal detail. `*[omitted: …]*` means a stretch of messages was removed completely.
- You do **not** need to understand the technical parts. Read it for how the two of us talk: who decides, who does the detail, and what happens when the AI is wrong.

---

### Turn 1 · 22:24 · Gap

[link to an Instagram reel]
This aint a bad idea for our future build in the condo

### Turn 2 · 22:28 · Claude

I opened the link, but I can't tell which idea you mean for the condo.

The page redirected to the Reels feed and I couldn't play the video. The first reel shown is from [an account]. The caption says they built a reels-editing system with Claude Code. The video shows a "Sorting my Downloads folder" screen with a cloud of photo thumbnails being sorted into folders. The "bonus" is a photo and video organization lesson, and it's a paid course ("comment 'sort'").

I can't see a link to the condo build in that. A few readings seem possible:

1. **A photo/video sorter for the condo project.** It would sort the listing photos, site-visit photos and measurement shots, so they feed the board automatically.
2. **A visual sorting interface on the board.** You'd drag things into groups, like the thumbnail cloud.
3. **Claude Code controlling a physical device.** The feed also had a reel called "AI coded my LG TV", which is closer to the smart-home side.
4. **Something I couldn't see in the video itself.**

Which one is it, or what in the reel caught your eye? I haven't changed anything.

### Turn 3 · 22:32 · Gap

Yeah, the idea was that it sorts the videos and photos. Like, you know, like when you're working on, when you've been taking a lot of photos for a trip or something, and you have just a bulk of photos, you probably would want to go through and then slog through each one of them, finding which one's good, which one's bad, right? So, could be some kind of program built by Claude or... Oh! We're going to have a local LLM, right? It might not be the greatest one but that LLM can look at those photos and evaluate them. It can then look at it as a whole and sort them into different categories.

They're already going to be in categories, which is fine, but then it can group up photos of this style and that kind that go together (as for traveling to this place and that kind of thing). It can then pick out good photos, one with good context, to allow us to capture the whole story of what happened in a certain place.

All of that should probably be able to be done on a local LLM, right? We just need to make sure that we have specific rules for it and then when we have a proper rule it can take as long as it wants. Now we'll have a proper system.

We already planned something to go on with the photo dumping system that is in the vault. We had an idea where we put the SSD together and once we plug that in it just dumps all of the photos to be backed up into the hard drive. That idea was for a NAS system but we can also just dump it into the PC before we have a NAS system. Once it's there we can do all the sorting, all the picking, all the cherry-picking, making sure we're keeping the good photos and throwing away the bad ones.

Of course you can also ask us or me to confirm that these are bad photos. Can we delete? Something like that can be done too. Yeah that's not a bad idea. What do you think?

### Turn 4 · 22:33 · Claude

Good idea, and the PC you just ordered can probably run it. It also fits onto plans you already have: the vault has a note about a station that copies photos off the cards when you plug them in. Your idea is the step after that: once the photos are copied, sort them and pick the good ones.

**Why I think it works on your PC:**
- **Most of it doesn't need the LLM.** Spotting blurry, dark or near-identical shots and closed eyes can be done by small, fast programs. I'd guess a few thousand photos take minutes.
- **The LLM handles the judgement calls.** That means grouping by place and scene, describing each photo, and picking a set that tells the story of each place. A small vision model (around 7B) should fit the RTX 5060's 8GB. At a few seconds per photo, a trip is an overnight job, which suits your "it can take as long as it wants". When you swap in a bigger graphics card later, it gets faster and smarter.
- **Before the NAS exists, the photos can land on the PC**, as you said.

**Two cautions:**
- **"Good photo" is your taste, not a rule I can write down.** It would work best if you hand-pick the best shots from one past trip and the system learns from those, rather than from generic rules.
- **Don't build it all from scratch.** There's a free, self-hosted photo library called Immich that already groups photos by faces and finds duplicates. The custom part would be the culling and the story picks on top of it.

On deleting: rejects would go into a holding folder. You'd confirm the delete, and only after the backup has been checked. That matches the rule already in the note.

I've added this as an idea, not a decision, to the log in [a note in the vault]. That project stays parked as "someday" until the PC is built and the condo move happens.

### Turn 5 · 22:35 · Gap

Coolies. Then maybe all it does is toss bad photos. Identifying shit should be easier than identifying perfection. Oo self hosted photo library is a good idea, save that idea in our note.

### Turn 6 · 22:35 · Claude

Both are saved in [a note in the vault].

- **Reject-only culling:** the first version only flags bad photos (blurry, dark, duplicate, closed eyes, accidental shots). It never tries to pick the best. I agree with your reasoning, because spotting bad is easier and more reliable than judging great. Story picks can come later if the cull works. Rejects still go to a holding folder, and you confirm before anything is deleted.
- **Self-hosted photo library:** I noted Immich as the base, running on the PC now and the NAS later. The culling would sit on top of it instead of us building a library from scratch. I haven't installed or tested Immich, so the note says to check that it runs on the planned box first.

### Turn 7 · 22:39 · Gap

How come i was able to get you to watch insta reel before. Can you research how you can do that and if you find the perfect answer, save it.

### Turn 8 · 22:40 · Claude

I didn't actually watch the reel. I read the page in your own Chrome, where you're already logged in to Instagram. That gave me the caption, the account name and one still frame. I never heard the audio or saw the video play, so my first guess at the idea was partly a guess.

My plain `curl` attempt failed because Instagram puts a login wall in front of reels. Chrome worked because it uses your logged-in browser.

**How I could actually watch a reel (researched, not tested):**
1. **Download it** with yt-dlp, using your browser's login. It isn't installed on this Mac yet. Instagram reels generally need a logged-in session, and stale cookies cause "login required" errors. One [GitHub issue](https://github.com/yt-dlp/yt-dlp/issues/10462) warns that Instagram can detect yt-dlp and ban accounts, so a throwaway account is the cautious route.
2. **Pull frames and audio** with ffmpeg, which is already installed.
3. **Transcribe the audio** with whisper-cli, also installed and fast on your Mac. A reel is under a minute.
4. **I read the frames and the transcript** together.

Ready-made versions of these steps exist, such as [claude-watch](https://github.com/alexlarcheveque/claude-watch), [claude-video](https://github.com/bradautomates/claude-video) and [video-context-plugin](https://github.com/vusallyv/video-context-plugin). They're community projects, not from Anthropic, and I haven't vetted any of them.

I haven't found one perfect answer. The Chrome method works now but is shallow. The download method is the full one, but it needs yt-dlp installed, and it saves a video file and uses your Instagram login, so I want your yes first. I can test it on that same reel if you want.

I saved all of this, including the "untested" flag, in [a note in the vault] in the memory folder. It also has a line in the memory index.

### Turn 9 · 22:45 · Gap

You used to be able to in one of the previous conversation, so i know you can. We can test these Claude watch and Claude video and the plug ins. Test all of it. Find the best one and save that as a thing to watch videos from now on.

### Turn 10 · 22:52 · Claude

I tested all five video tools. One worked end to end, and I've built a script around it. I also added a step to the lecture procedure from the new reel.

## Watching videos

I ran each tool on the sorting reel. You were right that this worked before: an Oct 9 conversation downloaded a reel with plain yt-dlp, no login. This time I used the same approach. I also had to rebuild yt-dlp's broken pipx install.

| Tool | Result |
|---|---|
| claude-video (bradautomates) | Downloaded and framed the reel cleanly. Its transcript needs an API key, WhisperX, or Gemini, which uploads the video to Google. |
| claude-watch | Failed. Its video-format setting finds nothing on Instagram. |
| video-context-plugin | Failed. It uses an ffmpeg option the current version removed. |
| mathiaschu fork | Downloaded fine, then crashed on transcription. |
| video-reader | Frames worked, but its transcription script crashed on macOS. |

- **Winner:** claude-video for downloading and picking frames. I replaced its transcript step with your local whisper-cli, so no key is needed and nothing leaves the Mac.
- **Script:** `watch_video.sh` takes a link or file and prints frames to look at and a timestamped transcript. It worked on a speech reel and on the sorting reel. That reel has music only, so the script warns when whisper prints a stray credit line.
- **Memory:** saved in [a note in the vault], including why each loser lost. I copied claude-video into `~/Projects/claude-video`. I didn't read all of its code line by line, only the scripts I ran. The script uses no cookies and no Instagram login.

## The new reel and the lecture procedure

The reel is about a free tool called earshot. It gives Claude "ears": it turns sound into a picture and numbers. It also has a bank of sound effects made as code.

- **Not installed:** earshot needs PyTorch and about 1.1 GB of model downloads. I kept it as an option.
- **What I built instead:** `audio_sheet.sh` uses ffmpeg only, with no models. It saves one picture of the audio (spectrogram on top, waveform below). It also prints loudness and every silence of 1.5 seconds or more. I opened the picture on a 40-second test clip and it reads clearly.
- **Where it went:** new §9.3a in [a note in the vault], after the voice chain and before publishing. Claude reads the picture and numbers for level jumps, clipping, leftover beep markers, missed dead air and noise. Your ears still make the final call.
- **Not yet tested on a real lecture export:** the first real use will be your next recording. The note says to log anything the step missed.
- **Sound effects:** I wrote down that earshot's effects aren't for lectures, since your slides stay quiet. Tell me if you disagree.

Note: [a note in the vault] and the memory index also changed, and nothing is committed yet.

Sources: [earshot GitHub wiki](https://github.com/Leonxlnx/earshot/wiki), [earshot README](https://github.com/Leonxlnx/earshot), [claude-video](https://github.com/bradautomates/claude-video), [claude-watch](https://github.com/alexlarcheveque/claude-watch), [video-context-plugin](https://github.com/vusallyv/video-context-plugin).

### Turn 11 · 22:53 · Gap

So did you manage to watch the video?

### Turn 12 · 22:53 · Claude

Yes, I watched it properly this time, apart from the music, which I can't judge.

**The sorting reel (the one you sent first):**
- I downloaded it and looked at 3 frames taken 4 seconds apart. The tool also saved 13 frames at one per second, but I only looked at those 3.
- The on-screen text reads "Claude takes care of my photos after every trip".
- The laptop shows a page called "Sorting my Downloads folder", with a cloud of photo thumbnails flying into labelled folders.
- It sorts photos into categories such as selfies, food and cafés, nature, and work from home. It also sorts videos, and the counters show folders created and duplicates found.
- A "Sort" button is clicked, and the last frame says "want access? comment 'sort'".
- The clip is 12.7 seconds with no speech, only music. The transcript came back as a stray credit line, so there was nothing spoken to hear.

Everything I told you earlier about the reel came from the caption and one frame. Having now seen the frames, it matches. It sorts into categories and finds duplicates. It doesn't show anything about picking the best photos or throwing out bad ones. That part was your idea.

**The other two reels:**
- For the voice-chain reel, I read the full spoken transcript.
- For the earshot reel, I read the full spoken transcript, but I didn't look at its frames.

### Turn 13 · 22:54 · Gap

Awesome so now you can also understand sound in the lectures and you can also create sfx right? Using info from the latest reel

### Turn 14 · 22:54 · Claude

Only partly, and I'd rather be exact about which part.

**Understanding sound in lectures: partly, with what's built now.**
- **Speech:** yes. I transcribe it with whisper-cli, as I did on the reels.
- **Loudness and silence:** yes, as numbers.
- **Seeing the audio:** I can read a spectrogram picture and spot clipping, long silences, level jumps and leftover beep markers. I tested this on a 40-second clip, not yet on a real lecture export.
- **Not yet:** I can't judge how a sound sounds, such as "that cut sounds abrupt" or "that's a keyboard click". The reel's tool, earshot, is built for that, with labelled sound events and a sound-to-picture sync check. I haven't installed or tested it. It needs PyTorch and about 1.1 GB of downloads.

**Creating sound effects: not with what's installed now.**
- **earshot:** it ships 252 code-made effects (clicks, whooshes, dings) and lets Claude tweak them. That's the reel's real claim, but I haven't tested it.
- **Without earshot:** I could write simple tones and noise bursts with ffmpeg or Python. They'd be basic, and I couldn't check by listening that they sound good.

For your lectures, the use case I can see is a soft click or pop under the click animations in [a later step]. You've kept your slides quiet so far, so I haven't added one.

The next step is to install earshot in its own folder and test it on one real lecture clip and one effect. It uses about 1.1 GB and runs only on your Mac's CPU. Do you want me to try it?

### Turn 15 · 22:55 · Gap

Go on

### Turn 16 · 22:56 · Claude

I couldn't install earshot. The install command was blocked, and I haven't tried another way around it. Nothing has been installed, so the heavy part is still undone.

**What I was trying to do:** set up earshot in its own folder, `~/Projects/earshot`, so I could test it on one real lecture clip and one sound effect. The command created a Python 3.12 virtual environment there, then installed PyTorch and earshot into it from the internet. The default Python on your Mac is 3.15, which is too new for PyTorch, so I picked 3.12. The first use would also download about 1.1 GB of models.

**What did happen:** I cloned earshot's source code into `~/Projects/earshot` and read its package file. It lists only the usual audio and machine-learning libraries. A search of the code found no commands that run outside programs or make network calls. I haven't read every file.

**One thing to know before you decide:** your disk is 93% full, with about 16 GB free. PyTorch plus the models will take roughly 3 to 4 GB of that.

**Your options:**
1. **Allow it.** Add a permission rule for Bash commands in your Claude Code settings, then tell me and I'll run the install. Or run this yourself in a terminal:
   `cd ~/Projects/earshot && /opt/homebrew/bin/python3.12 -m venv .venv && .venv/bin/python -m pip install torch && .venv/bin/python -m pip install -e .`
2. **Skip earshot.** The ffmpeg spectrogram step is already in the lecture procedure. Sound effects stay out for now.

Which do you want?

### Turn 17 · 22:57 · Gap

it even deny my attempt

### Turn 18 · 22:57 · Claude

I'm not sure what happened on your side, and nothing has been installed. I just checked: there's no `.venv` folder in `~/Projects/earshot`, and your disk is unchanged.

What did you try, and what message came up? For example, a permission prompt you declined, or an error in a terminal. That tells me where it was blocked.

**You can skip Claude Code's permission system entirely.** Open the regular Terminal app on your Mac and paste this:

```
cd ~/Projects/earshot && /opt/homebrew/bin/python3.12 -m venv .venv && .venv/bin/python -m pip install torch && .venv/bin/python -m pip install -e .
```

It takes a few minutes and uses roughly 3 GB, from your 16 GB free. When it finishes, tell me. I'll run the earshot test on one lecture clip and one sound effect. The test downloads the roughly 1.1 GB of models the first time.

If you'd rather not spend the disk space, we can skip earshot. The spectrogram step already in the lecture procedure stays either way.

### Turn 19 · 22:58 · Gap

got it. it should be good soon. when its done downloading, get tested ok? probably 3 minutes left or so

### Turn 20 · 22:58 · Claude

I'm waiting in the background for the install to finish, checking every 10 seconds for up to about 9 minutes. As soon as PyTorch and earshot import cleanly, I'll start the test. It will run earshot on one lecture clip and make one sound effect.

### Turn 21 · 23:01 · Claude

The earshot install isn't finished yet. PyTorch is in, but the other audio libraries, such as numpy and librosa, are still downloading. I'm waiting in the background and will start the test as soon as they all load.

### Turn 22 · 23:08 · Claude

Earshot works. The test was on 60 seconds of a raw [lecture] recording, plus one sound effect. The recording was not a finished export.

**On the recording:**
- It correctly found speech, loudness (-20.9 LUFS, true peak -3.9) and a 10-second stretch of near-silence at 0:14 to 0:25. The ffmpeg picture would have shown that gap but not named it.
- It drew a labelled picture of the audio. I opened it and it reads clearly.
- **Its sound-event labels on speech are guesses.** It tagged speech as "chat message pop", "sub bass drop" and "funk music", and the tool calls these weak hints. Trust its loudness, gaps and sections, not its sound names on a voice.

**On sound effects:**
- It made a soft 0.09-second click from its bank of 252.
- Its own description of the click was "toggle switch click, cork pop, plastic snap". That's plausible but not firmly confirmed.
- I haven't added any effect to your slides. I can't judge by ear whether it sounds good. If you want a click under the [a later step] animations, you'd need to listen to it, and the test file is `click_soft.wav` in the scratchpad folder.

**Where it sits now:**
- Each call takes about 15 to 20 seconds.
- Your disk is down to about 14 GB free.
- I updated §9.3a of the lecture procedure, the memory note and today's run sheet. The note says to use the quick ffmpeg step as the routine check, and earshot when a cut sounds wrong.
- Neither audio check has been run on a finished lecture export yet. Your next recording is the first real use.
