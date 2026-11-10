---
name: "youtube-growth-intel"
description: "Use for ANY YouTube video, Short or channel task (idea, script, edit, title, thumbnail, upload, publish, review): refreshes the latest algorithm changes from official sources, then applies a verified playbook and virality scorecard."
---

# YouTube growth intel (algorithm, best practices, virality)

Sanitized copy of the imported Claude skill. Platform claims and historical examples below are inherited source material, not a fresh verification; recheck current official documentation before applying them. This skill grants no access or permission to publish, edit accounts, upload, or contact anyone.

Run this skill at the start of every YouTube video or channel task, before scripting or packaging, and again before publishing. It works for any creator and any channel. Channel-specific skills (house style, voice, CTA) still apply on top of it.

## Step 0. Research-first production framework (TOP PRIORITY)
These points come before everything else in any YouTube production. Do not start full production (recording, voice, edit) until the five gate deliverables at the end of this step exist and the channel owner has seen them.

| Area | What to apply |
|---|---|
| Research | Start with audience problems, not tools. Examine what people actually watch (search suggestions, comments, outliers), verify current demand with dated sources, and record every source in a table. |
| Topics | Compare several candidate topics. For each, look at ordinary performers AND viral examples. Adjust for channel size (views vs subscriber count) and video age (views per day) before calling something an outlier. |
| Packaging | Develop title, thumbnail and opening 30 seconds together, around ONE truthful promise. If one of the three can't carry the promise, change the promise. |
| Design | Thumbnails must be understood at a glance on a phone: 0 to 4 words, one focal point, authentic results (real frames, real UI, real output), no fake events. |
| Hooks | The opening states the promise, shows proof, gives the plan, and names who it is for, in that order, inside the first 30 s. |
| Storyline | Turn every claim in the title and thumbnail into a specific scene with on-screen evidence. A claim with no scene gets cut from the packaging. |
| Editing | Match the promised experience: show a useful result early, use genuine screen recordings, cut dead time, add a pattern change every few seconds, keep an open loop that pays off at the end. |
| Analytics | Read impressions, CTR, retention and feedback (comments, surveys, likes vs dislikes) together. Never react to one number in isolation, and judge on engaged views. |
| Improvement | After each video, record evidence, mistakes, fixes and lessons in the project log, so the next production starts smarter. |

Qualifications to keep in mind (state them when relevant, never hide them):
- Competitor view counts are evidence of demand, not a guaranteed outcome for this channel.
- Positive comments do not prove future success.
- Retention still decides reach; a great title on a weak video backfires.
- Revenue or growth claims made by other creators are unverified unless an official source confirms them.

Gate deliverables before full production (show them to the channel owner):
1. Research evidence table: topic, source URL, date checked, views, channel size, video age, what it proves.
2. Ranked topic list with a one-line reason for each rank.
3. Title, thumbnail and hook proposals built around one truthful promise (3 titles, 2 to 3 thumbnails, 1 hook).
4. Promise-to-scene checklist: every claim mapped to the scene and the on-screen proof.
5. Recording feasibility test: a short dry run proving each planned screen recording can be captured cleanly (correct window, no private content, permissions in place, dedicated demo folder) before the real take.

## Step 1. Refresh what changed (every time, takes 2 to 4 searches)
YouTube changes monthly. Never rely only on the facts below.
1. Get today's date. Run, in one turn:
   - WebSearch "YouTube algorithm update <Month> <Year>" (standard)
   - WebSearch "YouTube Shorts update <Month> <Year>" (standard)
   - WebSearch "site:blog.youtube OR site:support.google.com/youtube creators <topic of this video>" (standard)
2. Prefer official sources, in this order: YouTube Help (support.google.com/youtube), YouTube Official Blog (blog.youtube), Creator Insider / YouTube Creators channel, TeamYouTube and the YouTube Liaison, Google research papers. Creator-coach and tool-vendor articles are secondary: label them "claimed".
3. Write a short dated "What changed since <date of last refresh>" list. Mark each item **verified** (an official source says it) or **claimed** (only creators or vendors say it).
4. If a new verified change contradicts this skill, follow the new source and propose a skill update at the end of the task (propose_skills, full SKILL.md).
5. **TubeBuddy watch list (before EVERY new video on any channel):** open https://www.youtube.com/@TubeBuddy/videos (channel id UCo33niDKpTpgwZ_dohqvylg) in the built-in browser, list uploads newer than the last check logged in `<CHANNEL_RESEARCH_LOG>`, and for each one about YouTube itself (algorithm, Studio settings, Shorts, packaging, monetization; skip anything outside YouTube) read its captions with the caption-seek method (Step 6), write a short dated summary (our words, never the transcript) and the tactic, mark it verified or claimed against Step 2 / official sources, apply what fits the current video and channel, and log it. Update this skill when a tactic becomes a standing rule.

## Step 2. Historical platform notes: revalidation required
Historical platform notes: revalidation required. The imported source recorded a refresh on Oct 24, 2026 and a re-check on Oct 26, 2026, and attributed the following claims to official sources unless marked. These historical attributions have not been independently verified for this preview; check current official documentation before applying or quoting them.
- **Recommendations are pulled per viewer, not pushed per video.** YouTube ranks "the best videos for this viewer at this moment" from watch history, search history, subscriptions, likes, dislikes, "Not interested", "Don't recommend channel" and satisfaction surveys. North Star: "long-term user value". (YouTube Help "How YouTube recommendations work"; Todd Beaupré, Creator Insider, Sep 1, 2026)
- **No single metric decides.** CTR only shows how attractive the thumbnail and idea were; watch time is weighed with satisfaction. Subscribers are not a test group, the first hour does not decide a video's fate, and many videos earn most views a month or more after upload. (Beaupré, Sep 2026)
- **Satisfaction beats minutes.** Surveys and "did the right person love it" signals sit next to watch time. (YouTube Help)
- **Views vs engaged views (Aug 24, 2026).** Public views count from the first frame; CTR, average view duration, retention and monetization use engaged views (kept watching past the first seconds, or clicked to watch). Judge performance on engaged views. (YouTube Official Blog)
- **Shorts:** each Short is shown to a seed audience; the core signal is viewed vs swiped away. Length: whatever the story needs, up to 3 min. Links in Shorts descriptions and comments are not clickable; only the Related video link and channel links are. Custom Shorts thumbnails started rolling out in Jul 2026. The Shorts dislike button was removed Jun 25, 2026; "Not interested" carries that feedback.
- **Originality (Oct 1, 2026):** the Shorts feed favors original content; re-uploads "without adding anything of your own" get less reach. Add your own commentary, edits or storytelling to any borrowed clip.
- **Inauthentic content (Jul 2026 wording):** repetitive or template-mass-produced videos and AI personas advising on sensitive topics can't monetize and tend to lose reach.
- **AI disclosure:** answer the AI-use question honestly on every upload with realistic AI; YouTube may add a label itself if it detects undisclosed realistic AI (May 2026). A label alone does not change recommendations, and AI-made videos "can be recommended as broadly" as others (YouTube Help).
- **Metadata:** tags "play a minimal role in your video's discovery"; title, thumbnail and description matter more (YouTube Help). Only the first 3 hashtags show above the title.
- **A/B testing (Test and compare):** up to 3 titles and/or thumbnails, winner chosen by watch time share, not CTR; not available for Shorts or private videos. (YouTube Help)
- **Reach beyond English:** translated titles and descriptions per language, localized thumbnails (Aug 2026) and auto-dubbing (open to all creators, 27 languages, Feb 2026).
- **Monetization (YPP) counting (YouTube Blog, Aug 12, 2026):** "qualified" watch hours come only from public long-form videos and archived livestreams (not Shorts, ads, private, unlisted or deleted videos); qualified Shorts views are engaged views on public Shorts. So Shorts views never add watch hours: route Shorts viewers into long-form (Step 4, Shorts → long).
- **YPP thresholds rising (reported, PPC Land Aug 2026 citing a TeamYouTube Help Community post; confirm on support.google.com before quoting):** from Feb 1, 2027 new applicants need 1,000 subscribers + 8,000 qualified watch hours in 365 days, or 20M qualified Shorts views in 90 days (today 4,000 / 10M). The 500-subscriber expanded tier stays 3,000 hours / 3M Shorts views. Existing partners keep monetizing but must accept the new terms by Jan 31, 2027. Channels not yet in YPP should track how close they are and say so in reviews.
- **Not confirmed (treat as claims):** "the Browse feed was rebuilt around hyper-specific watch-history clusters in Feb 2026" and "the 2026 algorithm is semantic". Google research on "semantic IDs" for recommendations exists, and YouTube does read title, description, captions and on-screen text, so the practical advice still holds: make the topic and the audience unmistakable.

## Step 3. Creator insights from analyzed videos (claims, useful as tactics)
Analyzed Oct 24, 2026 from transcripts (Think Media / Sean Cannell, "21-Day YouTube Reset"):
- MYXzCIC8Sac "The YouTube algorithm just had a huge change… (2026 Update)" (Short, 2:57, 135K views): eras of the algorithm (keywords → watch time → interests → "semantic"); "a small specific channel can now reach exactly the right person without going viral"; tags don't matter. Verified parts: satisfaction signals, tags minimal, AI behind recommendations (Neal Mohan 2026 letter). Unverified: the Feb 2026 browse rebuild.
- AiulYikjcY8 "Why Nobody is Using this YouTube Strategy" (2:41, 57K views): **trend timing.** When real news drops in your niche, publish fast ("talk about something new and talk about something now"); his reaction video ranked 1 of 10 on his channel within an hour. Research the source, then use Claude as a thought partner for the angle, title and thumbnail.
- FKvdJkENUSs "Why Most YouTube Channels Never Make Money 👀" (2:25, 7.8K views): **right views over viral views.** Views → Leads → Sales: a million views from people who will never buy is "not that helpful"; diagnose which step is broken (often messaging or offer, not views).
- Pattern across all three: one specific claim in the first sentence ("You're not crazy, YouTube changed their algorithm again"), a numbered framework, a series label (Day 12 of 21), and a follow CTA for the series.
- Claude/AI thumbnails (checked Oct 26, 2026, 19 videos with 663K to 2.57M views): 2 to 4 huge heavy words with one word in a colored pill; proof on screen (real output, dashboards, before/after with an arrow); tool + tool pairings; faceless winners show the finished output full frame. Brand names stay small; the result is the hero.
- TubeBuddy wZonRKXyvzI "The 2-Minute Algorithm Hack That Helps YouTube Recommend You!!" (3:50, ~1.98M views, analyzed Oct 27, 2026): three Studio settings for new channels: channel keywords (broad + long-tail), an upload-defaults description that is the channel's elevator pitch, and 2 to 5 channel-wide default tags. Settings are real; their weight is claimed (tags are minimal per YouTube Help).
- TubeBuddy HQ6-nOuCl4A "Get 4000 Watch Hours with This Simple Step" (6:36, ~308K views, analyzed Oct 27, 2026): only long-form watch time counts for YPP; the "flood method": set the Related video of every Short, old and new, to the NEWEST long-form and re-point them at each new upload; free route = Studio Analytics > Content > Shorts > top 5 to 15 Shorts. Claimed results; consistent with the official Related-video feature.
- AI-tutorial title shapes (test on the current video and read the A/B winner before reusing): "Claude Just Replaced My X (Real Test)", "I Asked AI for X. It Made Y", "One Prompt, One X". First-person, a tool name in the first words, a twist or proof marker. Avoid false hooks ("X is down", "X is stealing your data") the video can't pay off.

## Step 4. Playbook (apply in this order)
**Idea and audience**
- Write one sentence: "This is for <specific viewer> who wants <outcome>." If you can't, the idea is too broad.
- Prefer ideas with proven demand: search suggestions, competitors' outliers (views far above their channel average), fresh news in the niche (publish within 24 to 48 h).
- Pick the goal: reach (broad), or the right views (buyers, users). For products and apps, optimize for the right views.

**Hook (first 1 to 3 seconds)**
- Open mid-moment with the payoff or the problem; no logo, no "hi guys". The first spoken line and the first on-screen text must say what the video is.
- Long-form: deliver the promise of the title in the first 30 s, keep intros under 10 s.

**Retention and satisfaction**
- Cut dead air and fillers; change the visual every 2 to 4 s on Shorts; captions large and central (many watch muted).
- Pay off the title for real (no bait-and-switch: it hurts satisfaction).
- Ask one specific question mid-video and at about 60% (comments from the right viewers are satisfaction signals).
- Use keyword comment CTAs instead of "let me know": a mid-video card "Comment PROMPT and I'll send you the exact prompts", and at the end "Comment SKILLS for the file" + "What should I build next?". Repeat the same keywords in the description, pinned comment and the Short's end card, and reply to every keyword comment (claimed tactic; comments themselves are a satisfaction signal).
- Open loop: tease one concrete payoff in the hook ("the file is at the end"), remind at about 55-60%, and pay it off with "Remember the X I promised?". Never tease what the video doesn't deliver.
- Hook text must not collide with product vocabulary (e.g. "ZERO EDITING SKILLS" read as Claude Skills).
- End on a reason to keep watching (series, next video, Related video for Shorts).

**Packaging**
- Title: the viewer's words, keyword in the first 40 characters; Shorts 4 to 6 words; long-form about 50 to 60 characters. Curiosity is fine, misleading is not.
- Thumbnail: one idea, 0 to 4 words, readable on a phone and on a TV; face + emotion or the real object/result. Make 3 for Test and compare.
- Description: first 2 lines = value + keyword + the CTA link; chapters for long-form; 3 hashtags.
- **Channel settings hygiene (check once per channel, re-check quarterly):** Studio > Settings > Channel > Keywords: broad niche words + long-tail phrases viewers type (including the target audience's local search phrases), under 500 characters, no other creators' names. Upload defaults: a description that is the channel pitch (what, for whom, topics, key links) under the video-specific top lines, 2 to 5 channel-wide tags, category, video language, comments on. Country of residence set. Record the channel audit in `<CHANNEL_RESEARCH_LOG>`.
- Tags: a few, relevant only (minor signal). Default tags from upload defaults are channel-wide and kept; add the video's own tags after them. Translations for every language you target. For a local-language audience add search phrases people actually type in that language and one localized line in the description.

**Publishing**
- Choose the time the target audience is awake (cross-region: overlap window). Don't delete and re-upload to "reset" a video.
- Long-form: A/B test titles and thumbnails, end screen (Subscribe + best-for-viewer video), playlist, uploaded captions. Shorts: Related video to the long-form, on-screen CTA (links aren't clickable).
- **Shorts → newest long-form ("flood", claimed tactic for watch hours):** when a new long-form goes Public, re-point the Related video of the top 5 to 15 older Shorts (Studio > Analytics > Content > Shorts > See more) to it. Only after the owner's yes (it edits live videos), and only for Shorts whose end card does not name a different specific video; otherwise keep them on their own long-form. Shorts built for flooding use a generic end card ("Tap the ▶ video link below the title for my newest full video"). Read Related-video clicks and the long video's "Related videos" traffic after 7 days.
- Wait for YouTube's copyright checks to finish before making a video Public; never "Publish anyway".
- Disclose AI use honestly; disclose paid promotion.

**After publishing**
- 48 h: check impressions, CTR, engaged-view retention and (Shorts) "chose to view"; change one thing at a time (title or thumbnail).
- Reply to early comments; pin a comment with the next step.
- 2 weeks: read the A/B result; update the series plan with what won.

**What does not work (2026)**
- Tag or keyword stuffing, other creators' names in metadata, title/thumbnail that the video doesn't pay off.
- Re-uploads or lightly edited clips of others; template mass production; low-effort AI slop.
- Buying views or sub-for-sub; deleting and re-posting; chasing views from people who will never use the product.

## Step 5. Virality scorecard (Claude scores, then fixes the lowest)
Score 1 to 5 each, with one sentence of evidence, and rewrite anything under 4 before publishing:
1. Specific viewer and outcome clear
2. Hook says the payoff in 3 seconds
3. Title + thumbnail make one promise the video keeps
4. Retention design (pace, visuals, captions, no dead air)
5. Satisfaction (payoff, accuracy, no bait)
6. Timeliness or proven demand
7. Originality (own voice, footage, insight)
8. Clear next step (CTA, Related video, end screen, series)
Optional: run the Higgsfield virality_predictor on the first 15 s and report its numbers only if it returns them.

## Step 6. Studying reference videos (archival transcript methods)
The browser and transcript methods in Steps 6 and 6b are archival source material, not instructions to bypass present tool rules or restrictions. Use current supported tools and methods, follow their current instructions and access limits, and obtain any required user confirmation before recording, uploading, or otherwise taking a consequential action. If a historical method conflicts with current tool rules, do not use it.
- **Fastest transcript (works Oct 27, 2026, no download):** on the watch page, `p=document.querySelector('#movie_player'); p.loadModule('captions'); p.setOption('captions','track',{languageCode:'en'})`, mute, then in a JS loop `p.seekTo(t,true)`, wait ~280 ms, read `.ytp-caption-segment` text, keep it when it changes; step 1 s for manual captions, 2 s for auto (asr) captions and merge rolling lines. Split into JS calls of ~130 s of video each (CDP 45 s limit) and keep results in `window`; read them back in ~1,000-character slices (tool output truncates). Playback itself may stay paused in a background tab, which is why seeking works and playing does not. Never echo caption baseUrl or links with query strings (the tool blocks them).
- Metadata: open the watch page and read `ytInitialPlayerResponse.videoDetails` (title, keywords, lengthSeconds, viewCount, shortDescription) and `microformat.playerMicroformatRenderer.publishDate`.
- Transcript: YouTube's timedtext endpoint returns empty to page fetches and the transcript panel may not render. Capture audio instead: per tab, `MediaRecorder(new MediaStream(video.captureStream().getAudioTracks()), {mimeType:'audio/webm;codecs=opus'})` from time 0, stop on `timeupdate` near the end, PUT the blob to a presigned upload URL, download it, transcribe with faster-whisper (small.en, vad_filter). Playback needs a real click in the tab first (autoplay policy). Several tabs can record in parallel. Close the tabs afterwards (autoplay keeps playing other videos).
- Validate every claim in a transcript against Step 2 or an official source; label it verified or claimed.

### Step 6b. Packaging research from outliers (title, description, tags, thumbnail)
- Pull metadata from the watch page in the built-in browser (`ytInitialPlayerResponse.videoDetails`: title, viewCount, keywords, shortDescription; microformat publishDate/category; `#owner-sub-count`). Server-side curl/WebFetch of youtube.com is blocked or rate-limited; thumbnails via `i.ytimg.com/vi/<ID>/hqdefault.jpg` are fine.
- Score each reference: views ÷ subscribers, views per day, likes ÷ views. Copy patterns only from outliers (ratio above 1).
- Extract the skeleton of title, description order, tags (many top videos use none) and chapters; write our own with verified facts and our own angle. Never reuse their wording or unverified prices.
- **Remix, don't copy:** fill a remix table (element | winner | why it worked | our version | what we added) for concept, title, A/B titles, thumbnail, hook, description order, tags and CTA before writing packaging. Keep the skeleton (word order, length band, layout type, section order), change the surface (our facts, nouns, real frames), drop any fact you can't verify, and beat the winner on at least 3 of: extra proof, honesty beat, stronger open loop, a comment deliverable, Short → long routing, localization, production quality. After 48 h / 7 days, log which element won and carry it into the next remix. Record a worked example in `<PACKAGING_RESEARCH_LOG>`.
- Oct 2026 findings: the 1M+ AI pattern is "AI rebuilt/replaced paid software" (FUTC 2.4M, Fireship 1.3M); hooks: verdict first, cost math, contrast, challenge, switch confession; thumbnails: 2 to 4 huge words, hero UI/logo, before → after arrow, dark bg + one accent.

## Step 7. Channel growth system (for "grow to 1M subscribers" goals)
Be honest up front: no method guarantees a subscriber number or timeline, and creator claims about fast growth are unverified. What the official model rewards (Step 2) is satisfied viewers, so the system maximizes the number of videos that satisfy a clearly defined viewer, and routes every view to the next video.
1. **Niche and promise:** one sentence a stranger understands ("Real AI builds you can copy"). Check that every planned video fits it; a narrow, consistent audience profile is what lets recommendations find the right viewers.
2. **Formats (franchises):** 3 to 5 repeatable formats with a fixed structure and a title template, each a playlist. Track subscribers gained per 1,000 engaged views per format; double down on the best, drop a format after two misses.
3. **Idea pipeline (weekly):** outlier scan (videos in the niche with views far above their channel's subscriber count, normalized by age), search suggestions, comment requests on own videos, and fresh news. Score each idea on demand, packaging strength and whether the channel can deliver proof on screen.
4. **Packaging before production:** 10 title + thumbnail pairs per idea, keep the best 3 for A/B. The title is the viewer's desire in their words; the thumbnail is the proof.
5. **Retention targets:** a payoff in the first frame, the title's promise answered by 0:30, a visual change every few seconds, an open loop at the end, and no filler. Use the Studio retention graph: fix the first big drop in the next video.
6. **Shorts as the top of the funnel:** 3 to 5 Shorts per long-form, each a different moment with its own hook, Related video set to the long-form, the long-form's thumbnail on the end card. Judge them on viewed vs swiped and on subscribers gained.
7. **Session chaining:** end screens (best for viewer + Subscribe), playlists per format, "Watch next" lines, the Home trailer for non-subscribers, pinned comment with the next step.
8. **Community:** keyword comment CTAs, fast replies in the first hours, posts and polls that pick the next video, and collaborations with similar-size channels once a format works.
9. **Localization:** translated titles and descriptions plus auto-dubbing in the largest audiences' languages (prioritize languages using the current channel's audience data).
10. **Review loop:** 48 h, 7 days, 28 days (Step 4, After publishing), logged in the project with the real numbers and the one change for the next video. Milestone check monthly: subscribers, the subscriber rate per format, and the best traffic source; set the next month's plan from it.

## Output
For each task, give the user: the Step 0 gate deliverables, the dated "what changed" list with sources, the scorecard, and the concrete changes to the script, title, thumbnail, description and publish plan. Cite sources as links. Never invent metrics.
