---
name: "tech-with-sas-video"
description: "Sanitized archival copy of the Tech with Sas video production workflow for planning, scripting, editing, packaging and authorized publishing; configure your own accounts and assets."
---

# Tech with Sas video production

Use this for long-form videos and Shorts in the Tech with Sas production style. Configure your own authorized channel. Run audience and growth research first (section 11b), then section 3b before packaging.


> SANITIZED COPY OF IMPORTED SOURCE — PRIVATE PREVIEW
> This preserves the source production workflow and much of its wording, with private material removed or replaced. It is not the unredacted original, a fresh installation, or a current-capability validation. Referenced helper scripts, voice assets and companion skills are not bundled. Historical timings, prices, platform limits, quality claims, model names and UI behavior require current verification before use.
>
> Configure your own authorized channel, public display name, voice, brand assets, demo workspace, GitHub owner, approved links, publishing settings and growth goals. Placeholders are not usable credentials or approvals. No source-owner permission, consent, account state or installation approval transfers to the reader. Obtain applicable authorization for recordings, uploads, public changes, external sharing, installations, account access and deletion. Do not bypass restrictions. Fulfill comment-delivery promises only with an authorized deliverable and response plan.

## 0. Standing rules (never break)
- **VOICE GUARDRAIL (hard rule):** every narration line uses the creator's own recorded voice or an explicitly authorized voice clone. Configure `<AUTHORIZED_VOICE_ID>` and `<AUTHORIZED_VOICE_TYPE>` in your own account before generating. Verify every audio generation uses that setting. Use the same authorized voice when patching a video; never mix narrator clones within one video. Transcribe the final mix and check for unintended voices or banned content. Other speakers may appear in real recordings, never as substituted narration.
- **NAME GUARDRAIL (hard rule):** configure `<PUBLIC_DISPLAY_NAME>` and `<PRIVATE_TERMS_TO_REMOVE>` with the creator. Check voice, captions, titles, descriptions, tags, filenames and every source frame. Replace or mute private names, inpaint fixed UI labels when appropriate, blur other disclosures, then re-check the final render and transcript for zero private-term matches.
- **UPLOAD QUALITY GUARDRAIL (hard rule):** long-form masters at 2560x1440 or higher, Shorts at 1080x1920 or higher (prefer 2160x3840). See section 6, QC.
- **CLEAN VOICE:** narration must be clear and professional, with no "um"s, no dead pauses and no background noise. See section 11a.
- No company names, employer, location, nationality or race in the video, title, description or hooks. Blur or cover company branding and real people's personal details in screen recordings.
- No promises of a weekly cadence or free giveaways. "Comment SKILLS and I'll send them" is fine.
- Never publish a cut that still has placeholder cards while the title, description or chapters promise those scenes. Either record the scene, recaption the card to real content, or remove the promise.
- Never claim something was recorded when it only ran unattended: a render that ran with nobody recording is real output but not footage.
- No fabricated metrics. Every number on screen must come from a real screen, a tool result or the user.
- No em-dashes in any copy.
- It must feel recorded by a person, not AI generated: the creator’s own voice, real screen captures, the creator’s own photos, and restrained motion.
- Animated icons for agents and tools must be original designs. Never redraw third-party logos.
- Publishing, visibility changes, scheduling, community posts and pinned comments each need the creator’s explicit go-ahead.
  - Claude cannot post comments or pins, and cannot permanently delete videos. The safety check may also block some visibility changes even with the creator’s yes. Hand the creator the exact steps instead of retrying.
- Phone or identity verification in YouTube is the creator’s to do, never Claude's.
- Disclose AI use honestly: the voice clone, AI motion on photos, and "screen captures are real".
- Every long-form plan includes a Short (section 10) and the right CTA (section 9b). The job is not done until both videos are live and linked (section 11 checklist).
- **SHORT → LONG TAP-THROUGH:** every Short that has a long-form ends with an end card that sends viewers to the long video, AND the long video is set as the Short's **Related video** so there is a real tappable link. The on-screen words and the voice must describe where that link really is: YouTube shows the Related video as a "▶ <long title>" link **below the Short's title** (bottom-left, over the video on mobile, under the player on desktop), never "above". Required wording: "Tap the ▶ video link below the title" with an arrow pointing down-left; never "tap above" or "link in the description" (Shorts description links are not clickable). YouTube has no autoplay from a Short into a long video; this link is the official tap-through. Keep that bottom-left area free of captions during the end card. Validation V1-V4 in section 10a must pass before the Short is published, and again after.
- **ASK BEFORE ANY CHANGE:** never change a live video’s visibility, replace it, or edit its metadata without current authorization. Before replacing a public video, ask whether the old link has been shared anywhere.
- **PRIVACY GUARDRAIL:** before rendering, check every photo and clip for vehicle license plates, house numbers, street or city signs, and anything else that reveals where he lives. Blur plates in the source photo (pixelate + Gaussian), then re-check the rendered frame.
- **Hindi on screen:** every Hindi or Hinglish line in the voice gets an English translation on screen (smaller, quoted, under the Hindi text), for viewers who don't speak Hindi.
- **Review first:** show the creator the script and frame sheets for both formats (16:9 and 9:16) before the final render.

## 0b. PRE-PUBLISH VALIDATION GATE
Before ANY upload, publish, visibility change or metadata edit, fill this table and show it to the creator in one message. Wait for the creator’s explicit "yes" to that table. Do not infer any row from an earlier task, a file name or "what makes sense".

| Check | Value | How to verify |
|---|---|---|
| Platform | YouTube long-form / YouTube Short / Instagram Reel / X / LinkedIn | Taken from the creator’s words in THIS request; if he names a platform but the file was built for another, stop and ask |
| Channel / account | `<AUTHORIZED_CHANNEL_NAME>` + `<AUTHORIZED_CHANNEL_ID>` | Read the account identity immediately before uploading |
| Exact file | full path + version (e.g. <APPROVED_VIDEO_VERSION>.mp4) | ffprobe |
| Which cut | "YouTube version" = the 16:9 cut built for YouTube; "Instagram/Reel version" = the 9:16 social cut. Never swap one for the other | Match the creator’s wording to the file's intended platform |
| Format fits platform | Short: vertical or square, 3 min or less. Long-form: 16:9, 1440p+. Reel: 9:16, 90 s or less | ffprobe width, height, duration |
| If format and platform conflict | e.g. he says "publish as a Short" but the YouTube cut is 16:9 | STOP and ask: upload as long-form, re-cut vertical, or both. Never quietly substitute another cut |
| Creator content requirements | List every requirement in the current request | Check frames and transcript for each; show a frame sheet |
| Banned items | Private details, rejected assets, disallowed branding, placeholder cards | Frame sheet + OCR |
| Title / description / tags | final text | Show it |
| AI-use box | Current content-appropriate disclosure, confirmed with the creator and platform requirements | Read the radio state back after saving |
| Visibility | Private until he approves the table, then what he asked for | oEmbed: 200 public, 403 private |
| Short → long tap-through (every Short) | end card says "Tap the ▶ video link below the title" + down-left arrow; VO matches; Related video = LONG_ID | Section 10a V1-V4: end-card frame viewed, transcript grep, Studio Related video, curl onTap url |
| Signature (every new Tech with Sas video and Short) | burned-in lockup at 0.2-3.2 s and the last ~4 s only, per 0g | frames at 1.5 s, middle, duration-2 s, last frame |

After uploading: read back the channel name on the public page (oEmbed author_name), the visibility, the AI-use radio and the title, and report them. If anything differs from the table, report the mismatch and obtain authorization before changing visibility.
If unsure about ANY row, ask. Asking costs one message; a wrong public upload costs the creator’s trust.

## 0c. Research-first production framework
Production rule: these points come before everything else in any YouTube production. Do not start full production (recording, voice, edit) until the five gate deliverables at the end of this section exist and the creator has seen them.

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

Gate deliverables before full production (show them to the creator):
1. Research evidence table: topic, source URL, date checked, views, channel size, video age, what it proves.
2. Ranked topic list with a one-line reason for each rank.
3. Title, thumbnail and hook proposals built around one truthful promise (3 titles, 2 to 3 thumbnails, 1 hook), plus the 3b remix table.
4. Promise-to-scene checklist: every claim mapped to the scene and the on-screen proof.
5. Recording feasibility test: a short dry run proving each planned screen recording can be captured cleanly (correct window, no private content, permissions in place, dedicated demo folder) before the real take. Verify the actual screen state with authorized tools; never enter a password.

## 0d. Screen-recording safety
- Do every demo inside a throwaway folder (e.g. <LOCAL_ASSET_PATH> or <LOCAL_ASSET_PATH>) with fictional or public data only; never run a demo from a GitHub or work folder, even if Terminal opens there by default. Everything the demo creates stays in that folder so he can delete it after.
- Never send keystrokes (System Events) to Terminal or other windows: Answer prompts inside the demo process itself (an expect wrapper around the CLI), or ask the creator to click.
- Open the demo in a NEW full-screen window that covers everything else, then take a screenshot and check it is clean (no other sessions, tabs, notifications, macOS permission dialogs) BEFORE starting the recorder. If anything private shows, discard the take (move it to raw-recordings/_discard) and tell the creator.
- Every recorder runs with a hard cap (ffmpeg -t 600) and a PID file; stop it with SIGINT by that PID.
- Do not answer macOS privacy or permission dialogs; they are the creator’s decision. Never type the creator’s password.
- Raw desktop recordings never go to external services; only cropped, privacy-checked frames or finished renders may be hosted (e.g. on Higgsfield) to move them between machines.
- Frame privacy check before export: scan frames for house address, map location, phone numbers, bank or card numbers, SSN, date of birth, vehicle plates, emails and other PII; blur only that region (not the whole frame) and re-check the rendered frame.
- **CLEAN UP AFTER EVERY RECORDING:** as soon as a recording or video build is finished, close everything Claude opened for it on the authorized recording computer: Chrome tabs and windows (Claude in Chrome tabs_close), Terminal windows started for the demo (close by the window id or tty you recorded when opening it), recorder/ffmpeg/dev-server processes (kill by the PID files), Docker containers for the demo (`docker compose down` in the demo folder), and VS Code windows opened for it. Keep a list of every tab id, window id and PID you open (e.g. <LOCAL_ASSET_PATH>) so cleanup is exact. Never close windows or tabs Claude didn't open (the creator’s own Claude Code sessions and Terminal work stay); if unsure whether something was opened by Claude, ask. Report what was closed.
- **DELETE GUARDRAIL:** Claude may delete ONLY the single demo repo it created for the current video, never any other repo, folder or GitHub resource.
  1. Name the demo repo `<slug>-demo-YYYYMMDD`, put the marker `<DEMO_MARKER>` in its GitHub description, and clone it only inside the demo folder.
  2. Right after creating and cloning, run `demo_guard.sh register <owner/repo> <clone path>` (script in the project: <REVIEWED_GUARD_SCRIPT>, copied to the demo folder). It stores the repo's GitHub node id, created_at, first commit SHA and the real clone path in a read-only manifest.
  3. Run `demo_guard.sh snapshot before` (every other GitHub repo of the account and its orgs with pushedAt/updatedAt, plus every local git repo under ~ outside the demo folder).
  4. Never run `gh repo delete`, `rm -rf` or `git push --force` by hand. Deletion only through `demo_guard.sh delete`: it re-verifies owner, name pattern, node id, created_at, marker, first commit and path (inside the demo folder, not a symlink, not ~ or /), refuses wildcards, shows a dry run, and needs the manifest's one-time confirm token.
  5. Double confirmation: show the creator the dry-run output (exact repo, node id, folder) and wait for the creator’s explicit yes in chat before running with the token.
  6. After deleting, `compare before after` must report no other GitHub repo changed and no other local repo added or removed; report that result to the creator. If any check fails: stop, delete nothing, tell the creator.
  7. Never edit, push to, archive or change settings of any repo other than the demo repo, at any time during the video work.

## 0e. GitHub-repo build videos: configuration and safeguards
Obtain the current creator’s own authorized settings and any required approvals. Prior source-owner permissions do not apply.
- **Repo vetting:** use only a PUBLIC repo whose code can be scanned before install. Reject private, paid or invite-only repos and say why in the video. Prefer an OSI license (MIT/Apache), commits within the last ~3 months, a pinned stable release tag (never main/canary). Scan BEFORE any install: gitleaks (secrets), osv-scanner on the lockfile (dependencies), semgrep (code), npm audit --omit=dev, trivy (built image). Any high or critical finding = do not install, do not use; pick another repo or have Claude build one from current official releases with exact pinned versions, then re-scan to 0 high/critical. Test-fixture secret hits (mocks, test keys) are false positives; check each.
- **Wording:** configure `<PRIVATE_TERMS_TO_REMOVE>` and permitted product names with the creator. Check voice, titles, descriptions, tags, on-screen text, repo and folder names.
- **Honest limits segment (mandatory in these videos):** say plainly it is a starting point for trying things out and for small teams (5 to 10 people) instead of buying licences, NOT a full SaaS replacement; real hosted multi-tenant SaaS needs a scalable backend, highly available database, data isolation by design, backups, monitoring and alerting, SOC 2 / GDPR work. Only include a production-service CTA if it is true and authorized by the creator. Also give the pros and cons of the reference video's product, using facts only from the video and the seller's own pages.
- **Security warning card (mandatory, on screen + voice + description):** "Any repo you download from GitHub can contain malicious code. Ask Claude to scan it first. If the scan finds security issues, do not proceed. Run it in an isolated environment, never in production or where you keep confidential data. Security scans reduce risk but cannot prove code is safe."
- **GitHub owner:** configure `<AUTHORIZED_GITHUB_OWNER>` and repo visibility with the creator. Demo names use `<slug>-demo-YYYYMMDD`. Never create, publish, modify or delete repositories without applicable authorization. Follow the deletion safeguards in 0d; source-owner approvals do not transfer.
- **Recording computer:** use `<AUTHORIZED_RECORDING_COMPUTER>` and `<DEMO_DIR>`. Verify installed tools, screen-capture support and permissions. Obtain any required installation or permission approvals. Do not route around a denied operation.
- **Recording method:** one continuous screen recording (no screenshots stitched into video): `ffmpeg -f avfoundation -capture_cursor 1 -framerate 30 -i "0:none"` with a PID file and a hard cap. Before recording: open a NEW full-screen demo window, capture one test frame, check it shows no other windows, notifications or private text , then start. Launch Claude Code (Opus 5.5) in a fresh Terminal window via `osascript -e 'tell app "Terminal" to do script "cd <demo> && claude --model claude-opus-5-5 --allowedTools ..."'` (never keystrokes into existing windows); browser steps in a clean Chrome window via Claude in Chrome. Flow on camera: clone → scan → install → configure → run → app opens in a NEW tab → create organization → clients/tenants → enable features → show them working (forms, chat, charts). Do one unrecorded rehearsal first so the take doesn't break. Keep raw footage on the authorized recording computer; verify retained copies before cleanup. Never read big media through read_media_file (it floods the context); stage files and view scaled frames instead.
- **Cleanup + delete:** after the video is uploaded, run the CLEAN UP and DELETE GUARDRAIL rules in 0d; report what was closed and the compare result.
- **Format:** faceless, <AUTHORIZED_CREATOR_VOICE_OR_NAME> voice, about 10 minutes, motion graphics in the channel style (dark, cyan/violet, step bar), never copying another creator's look, script or claims; extra features beyond the reference video so it isn't a copy. Use the reference video only for structure and demand evidence (use only authorized source media, transcriptions and contact sheets).

## 0f. Repo-build video lessons
- **Demo API keys:** never paste or print keys. Obtain the creator’s own authorized secure setup. Keep any approved configuration out of recordings and version control; do not create or expand persistent access without the required approval.
- **Clean screen while recording:** use authorized window controls to show only the demo. Verify the intended window stays in front throughout each take; discard takes exposing private information.
- **Verify every take before editing, with text, not big images:** `<LOCAL_ASSET_PATH> <video> 6` (what is on screen every 6 s), `findtext.py <video> a b step <regex>...` (time + bbox of words, used for zoom targets and blur boxes), `ocr_scan.py <video> 2` (secrets, real name, emails, notifications: must be 0 before export). All run on the authorized recording computer with Apple Vision; nothing leaves it.
- **Blur that really hides:** plain boxblur left the macOS "Data Access Blocked" banner OCR-readable. Pixelate first: `crop → scale=24:8 → scale back → boxblur=8:3 → overlay`, then re-run ocr_scan. Blur seeded sample emails in contacts tables the same way.
- **Honesty when combining takes:** if footage comes from two recordings, never say "one continuous recording" in voice, cards or description; say "real screen recordings". "One run" is fine only for what Claude actually did in one session.
- **Edit location:** edit only on an authorized computer, outside temporary demo directories that may be removed. Respect denied folder access; obtain authorization rather than using another route around it.
- **Moving small files:** Mac ⇄ container goes through Higgsfield: `media_upload` → curl PUT with `If-None-Match: *` → `media_confirm` → curl the cloudfront URL on the other side. Each presigned URL costs about 3k tokens, so batch files in one `media_upload` call and put the PUTs in one script.
- **Images in context:** `read_media_file` echoes the full base64 (a 30 KB jpg ≈ 20k tokens). Keep QC sheets under 15 KB, or download to the container and use Read (no base64 echo).
- **Render hygiene:** `render_long.sh` must `rm -f render.log` before rendering, or a wait loop sees the old RENDER_DONE and grabs a stale file. Kill renders by exact PID (`ps -eo pid,args | awk '/comp.py render/ && !/awk/'`), never a broad pkill.
- **Pacing check:** `ffmpeg -vf "scale=320:180,freezedetect=n=0.001:d=3"` lists static stretches; speed those source ranges up (6x for waiting/generation) and add a slow 3% push on cards.
- **Captions from whisper:** fix mishearings before burning (LIFE→LIVE, TOOK→TO, "5 .5"→5.5, "go high level"→GOHIGHLEVEL).
- **Voice:** use `<AUTHORIZED_VOICE_ID>`. Do not EQ or compress clean clone lines; only level them. Music: a cool lo-fi bed (98 BPM, Am9-Fmaj9-Cmaj9-G6/9) ducked by sidechain, final -14 LUFS.
- **Retention kit that worked:** result-first hook with kinetic words on VO word times, an open loop ("one catch") paid off near the end with 2 reminder chips ("STILL COMING: THE ONE CATCH"), step bar + progress line, callouts timed to words, zoom-dissolve between segments, a "which would you set up first? Comment" question mid-video, "COMMENT PROMPT" + Like/Subscribe pop right after the best moment, end card with PROMPT / SKILLS / SCALE.

## 0g. VIDEO SIGNATURE
Every NEW Tech with Sas long-form video and Short carries the creator’s signature burned into the video file, so it stays even if someone rips and re-uploads the video.
- **What:** use `<AUTHORIZED_LOGO_ASSET>` + `<PUBLIC_CHANNEL_NAME>` + `<PUBLIC_HANDLE>`, on a dark glass pill with a violet-to-cyan border.
- **When:** ONLY at the start (0.2 to 3.2 s) and at the end (the last ~4 s, ending 0.2 s before the last frame). Never in between. 0.35 s fade with a 14 px upward slide in and out.
- **Where:** 16:9 long-form: 26% of frame width, bottom-left, 3.5% side margin, 5% bottom margin (clear of the end-screen elements, which go top/right). 9:16 Shorts: 62% of width, top-centre at 9% height (clear of the Shorts UI and the tap-through arrow at bottom-left).
- **How:** use your own reviewed signature compositor and authorized assets. The source signature kit is not included. Apply it as the LAST video step on the final master, after captions and end card are burned, then re-run the quality guardrail (1440p/2160p master at crf 17-18).
- **Check before upload (add to 0b table):** extract frames at 1.5 s (signature visible), at the middle (no signature), at duration minus 2 s (signature visible) and at the very last frame (faded out); look at them. On Shorts also confirm the signature does not cover the hook panel or the tap-through end-card arrow.
- **Not for old videos:** do NOT re-render or re-upload videos already published to add it. Old videos only carry the channel watermark.
- **Channel watermark:** configure your own authorized logo and display timing in Studio; do not infer prior account state.
- **Brand assets:** supply your own authorized logo files. Private source assets and brand-history records have been removed.

## 1. Channel positioning (MKBHD lesson: keep the main thing the main thing)
- Promise: "Real AI builds you can copy: Claude, agents and automation, shown on screen. Honest results: what worked, what broke, what it cost."
- Audience: India-first, English with light Hinglish in descriptions only ("AI se content kaise banaye"). Targets creators and builders searching for Claude, MCP, AI video, AI content creation and automation.

## 2. Series (each is a playlist and a Home-tab shelf)
| Series | Format | Title template |
|---|---|---|
| Start Here | trailer, intro, best-of | n/a |
| Claude AI & AI Content Creation | tool tests and setup guides | `[Tool] Setup: [verdict]` or `I Let Claude [do X] 🤯` or `Claude Just Replaced My [Job] (Real Test)` |
| AI Agents & Automation, Built in Public | builds end to end, with cost and time | `I Built [X] With Claude: [verdict]` or `[Model] Just Replaced [Tool] ([No Monthly Fee], [proof tag])` |
| AI Explained | one concept in 5 to 8 min | `[Thing] Explained: [one-line hook]` |
| Tool Impressions | first 48 hours with a tool | `[Tool] Impressions: [2-5 word verdict]!` |
| Tech on the Road | outdoor, travel or camping gear and AI in the field | `[Gear/Trip] Test: [verdict]` |
| Revisited | 3 to 6 months later, honest follow-up | `[Tool] Revisited: [verdict]` |

Create a new series playlist only once it has a video. Annual tentpole: "AI Tools of the Year" (December). Franchise ideas for growth are in section 11b.

## 3. Titles (MKBHD restraint plus Indian search intent)
- Default: `[Thing] [Review|Impressions|Setup|Explained]: [2-5 word opinion]`. The opinion goes in the title.
- About 1 in 4 should be a curiosity or problem title: "Claude Has a Problem", "WTF is MCP?", "I Let Claude AI Fix My YouTube Channel 🤯".
- Put the primary keyword in the first 40 characters. At most one emoji, and no ALL CAPS clickbait.
- Optional keyword tail after a pipe for search, for example "| AI Content Creation 2026".
- Write 3 options and recommend one.
- **Suspense titles (the creator asks for these on product demos):** research the top videos on the topic first, then write a curiosity title that stays true to what is on screen, e.g. "AI Caught Cheating in a Job Interview?! (I Built This AI)". Back the claim with a real frame. Never invent an event that the video does not show.

## 3a. Viral packaging research (run before writing any title, description or tags)
1. **Collect references:** the reference video he gives plus 6 to 12 videos with 1M+ views on the same topic (WebSearch). Note: exact-topic videos may be small (GoHighLevel-with-Claude videos were all under 160K); the 1M+ pattern was the wider "AI rebuilt/replaced paid software".
2. **Read real metadata:** use a current supported browser or connector to read title, views, duration, tags, description, publication date, category, subscriber count and likes. Do not route around blocked or rate-limited access. Close research tabs after.
3. **Judge performance, not raw views:** views ÷ subscribers (above 1 = outlier), views per day, likes ÷ views.
4. **Thumbnails:** curl `https://i.ytimg.com/vi/<ID>/hqdefault.jpg` using an authorized tool, make one contact sheet (6 tiles, under 45 KB) and look. Oct 2026 pattern of 1M+ AI videos: 2 to 4 huge words (white or yellow highlight box), one hero object/UI/logo, before → after arrow or "X → Y", dark background with one bright accent, face optional.
5. **Extract the formula, not the words:** title skeleton (e.g. "[Model] Just Replaced [Tool] [cost hook] (No Subscription)"), description order (link lines → one bold claim with an arrow → "In this video I…" paragraph → teaser of a hidden cost/catch → keyword chapters → disclaimer → 3 hashtags), tag usage (often none), chapter wording.
6. **Write ours:** same skeleton, our true facts, our extra angle (e.g. "Scanned First", "Honest Verdict"). Verify any price on the vendor's own page before putting it in a title; if not verifiable, use "No Monthly Fee". Keep the creator’s banned words out (<PRIVATE_TERM>, <PRIVATE_TERM>) even when the reference uses them. Record the reference numbers in the upload pack.
7. **Hooks that drive 1M+ AI videos:** verdict first ("this exceeded my expectations"), cost math then cancel ("$20, $100… I cancelled them all"), contrast/metaphor, challenge ("can I recreate this with AI?"), switch confession. Pick one and open with the real result on screen.

## 3b. Proven-winner remix
Goal: start from a video that is ALREADY outperforming, keep what made it work (concept, design, title shape, description order), then change and polish it with our true facts and one extra angle, so each video starts from proof and ends better than the reference. Never copy wording, thumbnails, claims or prices; copy the structure.

**Step 1. Find the winner (built-in browser, 3a steps 1-3).** Pick 1 primary reference + 2-3 backups on the same topic, judged by views ÷ subs (>1), views/day and likes ÷ views, not raw views. Record the numbers.

**Step 2. Fill this remix table before writing anything** (keep it in the upload pack):

| Element | Reference winner | What made it work | Our remix | What we added / polished |
|---|---|---|---|---|
| Concept | `<REFERENCE_CONCEPT>` | `<EVIDENCE>` | `<OUR_CONCEPT>` | `<IMPROVEMENT>` |
| Title | `<REFERENCE_TITLE>` | `<STRUCTURE>` | `<OUR_TITLE>` | `<TRUTHFUL_ANGLE>` |
| A/B titles | `<REFERENCE_VARIANTS>` | `<OBSERVATIONS>` | `<OUR_VARIANTS>` | `<TEST>` |
| Thumbnail | `<REFERENCE_LAYOUT>` | `<OBSERVATIONS>` | `<OUR_REAL_FRAME>` | `<IMPROVEMENT>` |
| Hook (0-30 s) | `<REFERENCE_HOOK>` | `<OBSERVATIONS>` | `<OUR_HOOK>` | `<PROOF>` |
| Description | `<REFERENCE_ORDER>` | `<OBSERVATIONS>` | `<OUR_DESCRIPTION>` | `<VALUE>` |
| Tags | `<REFERENCE_TAGS>` | `<OBSERVATIONS>` | `<OUR_TAGS>` | `<RELEVANCE>` |
| CTA | `<REFERENCE_CTA>` | `<OBSERVATIONS>` | `<OUR_CTA>` | `<AUTHORIZED_DELIVERABLE>` |

**Step 3. Polish rules (each remix must beat the reference on at least 3):** a proof the reference lacks (scan result, real numbers on screen); an honesty beat (limits, cost, what broke); a stronger open loop paid off near the end; an extra deliverable for keyword comments (prompt, skill file); a Short that routes to the long video; Hinglish line + tags; better production (1440p, voice, music bed, zoom-dissolves, kinetic text).

**Step 4. Keep the skeleton, change the surface:** same title word order and length band (55-70 chars), different nouns and tag; same thumbnail layout type, our own real frame and words; same description section order, our own text. If a fact in the winner can't be verified (a price, a claim), drop it rather than copy it.

**Step 5. Close the loop:** at 48 h and 7 days read CTR, 0:30 retention, engaged views and the A/B winner (watch-time share) for the remix; write in the log which element beat or lost to the reference, and carry the winning title shape and thumbnail type into the next remix. The next video starts from the best of: the original winner + our A/B winner.

**Next-video candidates in the same proven shape (AI replaces paid software):** "Claude Opus 5.5 Just Replaced <Calendly / Zapier / Canva / Linktree-style tool> (No Monthly Fee)", each with a public scanned repo or a Claude-built app, the same remix table, and the same Short → long routing. Avoid any tool name the creator has banned (<PRIVATE_TERM>, <PRIVATE_TERM>).

## 4. Thumbnails (product-first, minimal)
- Use the dark channel background (11,13,18) with ONE saturated accent: cyan (79,209,232), violet (139,124,246) or orange (240,128,60) on warm videos.
- The real UI or object is the hero, oversized and close-cropped. Use 0 to 4 words in Inter Display Black.
- His face is optional and secondary. Measured expression, never fake shock.
- 1280x720 JPG, readable at phone size. Make 3 variants for YouTube Test and Compare.
- Making variants from an existing thumbnail: cover the old text by filling each row with that row's left-edge pixel colour up to the UI panel, then draw new Inter Display Black text; check that no line runs into the panel.
- Verify custom-thumbnail eligibility on your own account. Any required identity or phone verification is for the creator to perform.
- **What viral Claude/AI thumbnails do:** 2 to 4 huge heavy words with ONE word in a colored pill; real proof on screen (the finished output, before/after, a dashboard); a curved arrow from before to after; faceless winners show the finished output full frame. Our version: white text with a soft shadow, one orange or cyan pill, warm glow behind the hero object. Reference builders: <LOCAL_ASSET_PATH> and <LOCAL_ASSET_PATH> on the authorized recording computer.
- Readable words beat brand names: keep the product name small (it is in the title and description); the result is the hero.
- Each thumbnail is paired with ONE title for Test and Compare, and the pair makes one promise (e.g. "CLAUDE MADE MY AD" + "Claude Just Replaced My Video Editor (Real Test)").
- Check every thumbnail by viewing the JPG: nothing cropped, no stray UI artifacts from the source frame, text never over a busy area.

## 5. Script (bold-line method)
- Write in script.md. **Bold lines** are on-camera or key VO beats. Plain lines are VO over screens or b-roll.
- Structure:
  1. Cold open of 8 to 12 s: the single most surprising real result in one or two sentences.
  2. Promise of about 10 s: what you will know by the end. Tease the end payoff and deliver it for real.
  3. A 2 s branded sting (Tech with Sas wordmark in cyan) or none. Never a long intro.
  4. Context, then hands-on, then what it's good at, then what broke, then cost and time, then who it's for, then the verdict.
  5. CTA of about 20 s, said once and chosen per section 9b. Add "Comment SKILLS" and an authorized CTA.
- **Hook system:**
  - First frame = the finished result, not the tool. First line says what you will see, e.g. "I asked Claude to build a real video ad for my app."
  - On-screen hook overlay in 3 beats: a bold claim ("NO EDITOR. NO DESIGNER. JUST CLAUDE"), the proof ("Claude built, voiced and uploaded it"), and the open loop ("the skill file is at the end").
  - Avoid hook words that collide with product terms: "ZERO EDITING SKILLS" read as Claude Skills, so it was changed.
  - Open loop: promise one concrete payoff at the end (a file, a reveal, a result) and mention it again at about 55-60% ("stay till the end, because...") and open the payoff with "Remember the X I promised?".
- **Comment engagement (the creator wants comments to drive the algorithm):** use keyword comments, never vague "let me know":
  - Mid-video (about 55-60%) a full-screen card with VO: "Want the exact prompts I typed? Comment PROMPT below and I'll send them to you."
  - End card: "Comment SKILLS for the skill file" + "What should Claude build for you next?" + Like / Subscribe.
  - Same keywords in the description, the pinned comment and the Short's end card, so one action works everywhere. He replies to every keyword comment (Claude cannot post comments).
- **Subscribe ask:** once, right after the biggest value moment, with a reason ("for more real Claude builds"), never a cadence promise.
- **Short scripts:** the last line always sends viewers to the long video using the link's real position: "Tap the video link below the title to watch it all."
- Keep framing under 60 s before the first real segment. Cut any sentence that doesn't add information.
- Say honesty out loud: what failed and what it cost. Disclose if a tool was provided free.
- Read it aloud for flow. Target 140 to 160 words per minute.

## 6. Production pipeline
Working dir: <LOCAL_ASSET_PATH> with shots/, clips/, vo/, vo/clean/, gfx.py, comp.py, build.py, audio.py, music.py (reference: <LOCAL_ASSET_PATH> and <LOCAL_ASSET_PATH>).

### Voice (your own authorized voice, see the guardrail)
- Historical source voice pipeline: Higgsfield `generate_audio`, model text2speech_v2, variant elevenlabs, with your own `<AUTHORIZED_VOICE_ID>` and `<AUTHORIZED_VOICE_TYPE>`; await the resulting job. Verify current API support, pricing and voice authorization before use.
- Write lines for energy: short sentences, one idea each, "you" language, a question or number every few lines. 140 to 160 words per minute.
- For remastering an old recording:
  - Keep the creator’s real voice and clean it.
  - Re-voice only broken, new or must-change lines in the same clone the video already uses, matched in tone and loudness.
  - Place each new line at the original line's start time so it stays in sync with the visuals; use atempo of 1.1 or less if a line overruns.
  - If the original narration wasn't the creator’s voice, re-voice all of it in <AUTHORIZED_CREATOR_VOICE_OR_NAME>.
- Generate one file per script section. On a 429 error, retry once.
- Clean every line with this ffmpeg chain (not for <AUTHORIZED_CREATOR_VOICE_OR_NAME> clone lines, which stay unprocessed except leveling, see 0f):
```
highpass=f=75,equalizer=f=120:t=q:w=8:g=-10,equalizer=f=180:t=q:w=8:g=-8,afftdn=nr=12:nf=-50:tn=1,deesser=i=0.35,equalizer=f=250:t=q:w=1.2:g=-2,equalizer=f=3500:t=q:w=1.5:g=2.5,equalizer=f=9000:t=h:w=0.7:g=1.5,acompressor=threshold=-20dB:ratio=3:attack=8:release=120:makeup=3,silenceremove=start_periods=1:start_threshold=-50dB,loudnorm=I=-16:TP=-1.5:LRA=7
```
- Get word timestamps with faster-whisper small.en and save them to vo/words.json. Decode with ffmpeg into a numpy array; passing a file path fails on this PyAV version. Drive overlays and cuts from word times. When the same word appears twice, use `after=<time>`.

### Visuals
- Screens: real screenshots or recordings (Chrome, Studio, Claude), shown in a browser_frame or phone_frame with a slow 3 to 5% Ken Burns push.
- Photos: the creator’s own photos, animated with Kling 3.0 pro on Higgsfield (`generate_video`, model kling3_0, mode pro, sound off, start_image role). That is 8.75 credits per 5 s. Prompt for subtle, realistic motion only.
- Upload media with `media_upload`, then curl PUT with `If-None-Match: *`, then `media_confirm`.
- Graphics (gfx.py): Inter fonts, BG 11,13,18, CYAN 79,209,232, VIOLET 139,124,246 and a green accent. Elements: chip, step_row, headline, lower_third, browser_frame, phone_frame, like_chip, subscribe_button. Keep on-screen text to 3 to 6 words, never full sentences.
- Fixing text baked into an old video: build a mask of the text pixels, dilate it, then cv2.inpaint (TELEA) and redraw the new text with PIL. Track moving panels with cv2.matchTemplate on a nearby static line, and scale the redraw alpha by the original text brightness so fades still match. Reference: <LOCAL_ASSET_PATH>
- Retention: smooth transitions between chapters, zoom-ins on small UI, original animated agent icons, an audible music bed, and an end payoff teased early.
- **Transitions (he asked for professional ones):** zoom-dissolve, not hard cuts. In the demo compositor (<LOCAL_ASSET_PATH>): `tblend(old,new,k)` pushes the old frame in by 3-4% while fading and settles the new one from a slight zoom, 0.5 s, eased. Use it on step cards (XF=0.5) and on in-app screen switches, detected by a mean abs diff above 14 on a 96x54 gray thumbnail of the camera view, with a 2.5 s cooldown, applied to the content area only so the header and chrome stay still.
- **Story or patent inserts** (e.g. a 29 s card sequence): build 2560x1440 cards with PIL, add a 3% Ken Burns via zoompan, crossfade cards with `xfade`, and time card switches to the voice line's pauses (`silencedetect=n=-35dB:d=0.25`).
- Compositor (comp.py): PIL and numpy frames piped to ffmpeg libx264 (preset fast, crf 17, 30 fps, 1920x1080, `-threads 1`). Use bbox-cropped overlays and a static-frame cache. Kill stray renders by exact PID (section 11a), never `pkill -f` on a broad name.
- End card: the last 14 s, per section 9b.

### Music and mix
- He wants the music clearly audible and light/upbeat, not slow. Default bed: <LOCAL_ASSET_PATH> (synth, 112 BPM, Cmaj7-Am7-Fmaj7-G7, plucked arpeggio, warm pad, soft kick and shaker, light reverb; 68.6 s loop). For a "cool" feel use the lo-fi bed in 0f. Higgsfield has no general music model, so synthesize or use a licensed track. Never a famous song.
- Mix: loop the bed (`aloop=loop=-1:size=2147483647`), volume 0.30, fade in 1.5 s / out 3 s, then `sidechaincompress=threshold=0.05:ratio=2.5:attack=80:release=600` keyed by the voice (light ducking keeps it audible), then `amix normalize=0`, then two-pass `loudnorm I=-14:TP=-1.5:LRA=11`. The old 0.20 + ratio 7 setting ducked the bed to near silence.
- Remix from the clean voice-only stem (e.g. <CLEAN_VOICE_STEM>); check a stem has no music by its quiet-gap level (about -60 dBFS).

### Screen-recording edit
- Edit on the creator’s Mac with ffmpeg 8 (libx264, xfade); raw recordings never leave the Mac. Build graphics (PNG frames, chips, cards) and the audio mix in the container, ship them as a zip via Higgsfield media_upload, curl them down on the authorized recording computer, and run a generated build_long.sh there.
- Segment model: every scene is its own MP4 (screen / phone / card). Screen: crop the clean recording area (e.g. crop=1440:810:240:150), scale to 2240x1260 inside a browser_frame PNG at (160,150) on a 2560x1440 canvas; speed long waits 6-8x then return to 1x for the payoff. Vertical renders go into a phone_frame (hole 698x1240 at 931,100). Cards get a slow zoompan push.
- Join segments with xfade 0.5 s (alternate zoomin and fade), and put a synthesized whoosh (band-pass noise sweep, 0.7 s, sin² envelope, -13 dB) 0.2 s before each transition. Place each VO line 0.35 s after its segment start.
- Rebuild only changed segments (REBUILD set) and re-run the xfade join; a 3.5 min 1440p join takes a few minutes. Recaptioning a card (e.g. a placeholder into real content) is a one-segment rebuild.
- Chapters come from the segment start times in timeline.json; regenerate them whenever the cut changes.
- HTML ads/trailers made by Claude render to MP4 with Playwright on the authorized recording computer (CDP Page.startScreencast frames, then ffmpeg concat at 30 fps). On the Mac, Playwright lives in the npx cache: set NODE_PATH to that node_modules.
- QC on the authorized recording computer: `ffmpeg -i final.mp4 -vf "fps=1/12,scale=320:180,tile=6x3" -frames:v 1 qc.jpg` (about 100 KB) and view that one JPG; never read big images or videos through read_media_file (it floods the context).
- **Showcase insert:** to prove "you can do this too", add a 15-20 s "MADE THE SAME WAY" section near the end with 3-4 clips from one of the creator’s finished videos, a link pill "youtu.be/<ID> · link in the description", one VO line, and the link in the description. Long video only. Pick clips with a 3 s timestamped contact sheet and check every frame: no vehicles/plates, no location signs.
- Review link: PUT the finished render (never raw footage) from the Mac to a Higgsfield presigned URL with `-H "If-None-Match: *"`, media_confirm, then send the creator the cloudfront URL.

### QC and validation before publishing (mandatory)
- Make a preview frame sheet every 15 to 30 s and look at it.
- Transcribe the final render and check it against the banned list: weekly or Monday promises, free offers, company or employer names, location, real PII.
- Confirm the voice guardrail.
- Check: no song footage, no placeholder cards, all numbers true, captions in sync, about -14 LUFS, and audio peaks under -1 dBTP.
- Shorts: run section 10a V1 and V2 on the rendered file before uploading.
- Build captions_en.srt from words.json in phrases of up to 42 characters. Transcribe EVERY VO line into words.json first, offset each line by its timeline start, and fix proper nouns and whisper errors (<EXAMPLE_PRODUCT> not <EXAMPLE_PRODUCT>, chat not chart, Claude Code, Shorts/Reels, Higgsfield, PROMPT, SKILLS).
- **UPLOAD QUALITY GUARDRAIL (hard rule):** never upload a long-form below 1440p. YouTube serves its better VP9 encode only to 1440p+ uploads, and a 720p master plays in low quality by default.
  - Final long-form: `scale=2560:1440:flags=lanczos,unsharp=5:5:0.6:5:5:0.0`, libx264 crf 17, high profile, -g 60, +faststart, AAC 320k 48 kHz.
  - Shorts: 1080x1920 minimum at crf 18 or better; upscale to 2160x3840 the same way when the source allows.
  - ffprobe the final file before uploading: check the resolution and that the bitrate is reasonable.
  - After publishing, verify on the watch page: `document.querySelector('#movie_player').getAvailableQualityLevels()` must list hd1440 (long) or hd2160 (Short).

## 7. Description template (short top, rich bottom)
```
[product videos only, line 1: 👉 Try <Product>: https://<product>]
⚡ <N>-sec version: https://youtube.com/shorts/<SHORT_ID>
💬 Comment "PROMPT" and I'll send you the exact prompt.

[1-2 line bold claim restating the result, primary keyword early, cost arrow if true ("Monthly fee → $0")]

["In this video I..." paragraph: what Claude does, step by step, with the proof numbers]

[teaser: the one catch / hidden cost, paid off in the video]
[Hinglish search line: AI se ___ kaise banaye? ...] 🚀

[warning or safety box when relevant]

💬 Comment "PROMPT" for the exact prompts, "SKILLS" for the skill file (or a video-specific keyword). I reply to every comment.

[the exact prompt / checklist, when the video promises one]

[Optional creator-authorized product or contact links: `<APPROVED_PUBLIC_URLS>`]

🎬 [showcase line + https://youtu.be/<ID>, when there is one]

⏱ Chapters
0:00 ...   (first must be 0:00, at least 3 chapters, each at least 10 s, keyword-led)

🔔 Subscribe for more real Claude builds: https://www.youtube.com/@TechWithSas?sub_confirmation=1

AI disclosure: ...
Views are my own and do not represent any employer.

#ClaudeCode #[Topic] #[Audience]
```
- Test every URL before publishing (section 9b). Never link a Private video in a public description.

## 8. Tags
Use 15 to 25 tags, broad to specific: tool names (claude ai, claude code, claude skills, claude in chrome), the task (ai video ad, ai youtube automation, ai video editing), Hinglish (claude ai kaise use kare, ai se video kaise banaye, claude ai hindi, ai tools in hindi), format (faceless youtube channel, youtube shorts ai), and the brand (tech with sas). Never use other creators' names.
- Lead with the exact primary keyword ("claude ai"), then the specific topic, then India/Hinglish, then format tags, then the channel name.
- Keep the joined list under about 420 characters (limit 500).
- Add a "🇮🇳 Hindi/Hinglish:" search line to the description on every upload.

## 9. Publishing in YouTube Studio (archival source workflow)

All DOM selectors, JavaScript interaction sequences, capture methods, upload bridges and timing limits below and elsewhere are historical source notes, not verified current capabilities or executable instructions. Use current supported tools and UI controls with the reader’s own permissions. Do not use injection, prototype overrides, inaccessible-file bridges or alternate routes to bypass a restriction. Stop and hand off unsupported operations.
0. Obtain authorized source files through current supported downloads, connectors or an upload from the creator. Do not work around denied file access.
1. Select `<AUTHORIZED_CHANNEL_NAME>` and verify `<AUTHORIZED_CHANNEL_ID>` against the 0b table immediately before upload.
2. Upload through the currently supported authorized file-upload tool or Studio interface; do not inject files or override browser APIs to bypass restrictions.
   - The video ID is in the dialog's link (`ytcp-uploads-dialog a` text youtu.be/<ID>) as soon as the upload starts.
   - YouTube can't replace a video file in place, so a fix means a new upload (see the replacement order in section 11). He deletes old videos himself.
3. Fill the title and description and upload the thumbnail through supported tools; read the values back.
4. Tags: inspect current upload defaults, keep only relevant authorized tags, add video-specific tags without duplicates, and read back the chips and character count.
5. Settings: playlist, audience classification, AI-use disclosure, paid promotion, category and language must match the actual content and the creator’s current authorized settings. Read them back before publishing.
6. A/B test (long-form only): use the current supported Title and thumbnail testing interface, if available, with three approved pairs. Verify the saved test. Historical source behavior: changing the title can end a running test; check current behavior before editing.
7. Video elements step:
   - **Captions:** use the current supported Subtitles → Upload file → With timing flow. Verify a manual track on the watch page. If unsupported or blocked, give the creator the SRT; never override browser APIs to force file access.
   - **End screen:** Add → template "1 video, 1 subscribe" (Video: Best for viewer + Subscribe, last 20 s) → Save.
8. Visibility: Private by default when the content carries any risk; Public only after the creator’s go-ahead. **Wait for checks before Public:** publishing while "Checking N%" shows "We're still checking your content... you may get a strike" → click Go back, never "Publish anyway". Poll with short JS calls (each under 45 s; a longer await loop hits the CDP timeout and freezes the call) until "Checks complete. No issues found.", then select PUBLIC and click #done-button. The share dialog "Video published" confirms it.
9. **Publish order that worked:** long-form fully set (details, tags, playlist, AI use, A/B, captions, end screen) → Public → upload the Short with line 1 "▶️ Watch the FULL video: https://youtu.be/<LONG_ID>" → Short Public → Short edit page: find the button whose text starts "Related video" → pick the long video's tile → Save → run section 10a → long edit page: insert "⚡ <N>-sec version: https://youtube.com/shorts/<SHORT_ID>" after the Hinglish line (caret placed with a DOM Range at the end of that text node, then insertText; replacing an ID: select its exact range) → Save. Use the Short's real length. **When both are uploaded Private first** (the creator’s "keep it private for now"): the Related video picker lists only Public videos, so the long video can't be picked yet; set the Short's line 1 link and the long's "⚡ <N>-sec version" line now, and when he says publish: long Public → Short Related video = long (Save) → Short Public → A/B test on the long → 10a V3-V4.
10. Verify from outside: oEmbed 200 for both (author_name Tech with Sas); section 10a V4; watch page quality levels, manual caption track, chapters, `shortDescription` contains the Short ID. The watch page can show any A/B title variant; check the ID, not the title. Pause or close tabs after (autoplay). Fetch other watch pages from a youtube.com tab (same origin); container curl to youtube.com gets 429 after a few requests.
11. Home tab: trailer (non-subscribers) is the strongest hook video; featured video (returning) is the newest. "Change video" sits under the trailer section's ⋮ menu. Dragging sections doesn't work through automation.
12. Pinned comments: draft one for the long video AND one for the Short and give them to the creator to post and pin himself (Claude's comment posting and pinning are blocked). Templates:
    - Long: `Comment "SKILLS" and I'll send you the exact Claude skill file from this video 👇` / `Want the prompts I typed? Comment "PROMPT".` / `What should Claude build for you next?`
    - Short: `Full video (<one-line payoff>): tap the ▶ video link below the title 👆` / `Comment "SKILLS" for the skill file. What should Claude make next?`
    - Pin: open the video, post from the channel account, ⋮ on the comment → Pin. Reply to keyword comments within the first couple of hours. Verify after the creator posts: `#pinned-comment-badge` on the first comment thread.
13. Cross-link older videos: their "Watch next" lines and end screens point to the new video (ask first; they are live).

## 9 notes learned Oct 23-24, 2026
- Higgsfield upload rejects files around 670 MB (HTTP 502). Re-encode to about 9 Mbps 1440p (`-b:v 9M -maxrate 12M -bufsize 18M`) and upload that.
- Shorts have no A/B Test & Compare option. Test Short titles manually by swapping after 48 h.
- Fixing one shot in a finished long-form: render only the affected time ranges, then overlay them on the final with `setpts=PTS-STARTPTS+t0/TB` and `overlay=enable='between(t,t0,t1)'` in one re-encode.
- Visibility changes on a video with a running experiment show "This stops your current experiment"; after Continue, re-open Studio content to confirm the new visibility saved. Visibility on an edit page: the "Edit video visibility status" button → PRIVATE/PUBLIC radio → Done → Save.
- **Translations:** title + description in Hindi (and for <EXAMPLE_PRODUCT> also Bangla, Telugu, Marathi, Tamil, Spanish, Portuguese (Brazil)). Host a translations.json on Higgsfield, fetch it in Studio, then per language: Languages page → Add language → click the exact item → the Title and description dialog → insertText into its two #textbox → Update. Do 2-3 languages per JS call (CDP 45 s timeout).
- **Scheduling:** use the creator’s chosen date, time and time zone. Verify the current UTC offset and daylight-saving conversion. Schedule follow-up validation only with authorization.
- **Built-in buttons:** Like and Subscribe are always in the player; long-form can add a clickable Subscribe end-screen element (no Like element); Shorts have no end screens, so a drawn Like/Subscribe row is only a visual nudge.
- **Tags vs hashtags:** "only 3 tags" usually means the 3 description hashtags shown above the title; the real tags are in Show more.
- **Edit-page visibility via JS:** click the `ytcp-icon-button` inside `ytcp-video-metadata-visibility` (clicking the element itself does nothing), then `tp-yt-paper-radio-button[name=PUBLIC]`, Done, then `ytcp-button#save`. Save the Related video change before opening the visibility dialog. A/B on a published video: the "A/B Testing" button on the edit page → Title and thumbnail → the dialog has 3 file inputs (slot 1 needs the current thumbnail again) → Set test → Save.
- **No < or > in descriptions:** YouTube rejects them; write "[your repo]" instead of "<repo>".

## 9c. Other-channel material
[Removed: unrelated channel, founder biography, product claims, private account settings and production history.]

## 9a. Reposting a video from another of the creator’s channels (e.g. <EXAMPLE_PRODUCT>)
- Never touch the original: leave it published as it is.
- **Capture:** obtain the creator’s authorized original or supported download. Historical captureStream/MediaRecorder methods are archival, not instructions to bypass access restrictions.
- **Branding and PII scan:** tesseract plain + CLAHE passes at 2 s steps in the background; blur each hit for ±1.6 s; filter false hits ("cognitive", "recognition"); mute a spoken company name with a word-level volume=0.
- **Rebuild:** a 15 s preview of the best moment under a hook panel, then the full original (trim only the leading silence, keep the creator’s real voice cleaned), chapter chips, a ducked music bed and the 14 s end card per 9b. Chapter offset = preview length + (original time - trimmed lead). Reference: <LOCAL_ASSET_PATH>
- **Metadata:** keep the proven original title hook when it worked; Hinglish line; 15 to 20 tags; 3 title variants and 3 thumbnails; Higgsfield virality_predictor on the opening 15 s.
- **Linking:** point older videos' "Watch next" lines and end screens at the new Tech with Sas copy, never at the other channel's original.

## 9b. CTA rule (MANDATORY on every long-form and Short)
- **Product video** (a demo or feature of one product, e.g. <EXAMPLE_PRODUCT>, <EXAMPLE_PRODUCT>): the CTA is the product.
  - End card: a big pulsing button "Try <Product> →" (cyan pill, Inter Display Bold 54, two-frame 0.8 s pulse), with the full URL in white below it.
  - Through the whole video: a small cyan URL pill above @TechWithSas.
  - Description line 1: "👉 Try <Product>: https://<product>".
  - Long-form end screen: Subscribe plus the related Short or video. A website "Link" element needs YPP.
  - **General content and tutorials:** the CTA is the keyword comment (PROMPT / SKILLS) + Like + Subscribe.
  - Animated Like and Subscribe buttons on the end card; description sub_confirmation link; end screen Subscribe element.
- **Buttons drawn inside the video are not clickable**, so every visual CTA needs a matching clickable link: description line 1, the Short's Related video, and long-form end screen elements.
- **Test every link before publishing:** curl it for a 200 status and the right page, then check on the watch page that the description shows it as a real anchor.

## 10. Shorts as a bridge (MANDATORY for every long-form video)
Every plan includes a Short (aim for 3 to 5 per long-form, section 11b). The long-form is not done until its Short is live, linked to it, and section 10a passes.
- **Pick the moment:** the cold-open hook plus the single best "wow" segment, cut on word boundaries from vo/words.json. Aim for 30 to 55 s. Never cut mid-word. Cut out real names and other PII with a word-level trim.
- **Layout (1080x1920 build, 30 fps; final upscaled to 2160x3840):**
  - Background: the source blurred (boxblur 28) and darkened (brightness -0.42).
  - Foreground: the source cropped and scaled with rounded corners and a cyan border, around y 560.
  - Top: a dark rounded panel with a suspense hook in 2 lines, white, plus a cyan tease line.
  - Captions: ASS, Inter Display ExtraBold 78, ALL CAPS, 2 to 3 word chunks, current word in cyan (or orange on warm videos), around y 1290 on a dark panel. Clip each chunk's end to the next chunk's start minus 0.01 s. No captions on the end-card line.
  - Faceless product Short pattern (Claude ad, <VIDEO_ID>): A result + "CLAUDE MADE THIS AD", B before/after phones "ONE PROMPT LATER...", C bonus twist "IT EVEN MADE A MOVIE TRAILER", D end card (9.5 s). 4 sections, xfade zoomin 0.4 s, one VO line each. Builder: <LOCAL_ASSET_PATH> Repo-build pattern (<EXAMPLE_PRODUCT> <VIDEO_ID>, 33 s): sites flip + AI chat → scan 0 critical → 3 sites → form + chat → charts → end card with the open-loop tease ("one thing makes it not ready to sell"). Builder: <LOCAL_ASSET_PATH> on the authorized recording computer.
  - A cyan progress bar along the bottom edge; @TechWithSas at the bottom; product Shorts also carry the URL pill.
- **End card (last 5 to 10 s, MANDATORY):** "WATCH THE FULL VIDEO" + the payoff tease, the full video's thumbnail, then "Tap the" + a white pill "▶ video link" + "below the title" (orange or cyan), and a thick white arrow from the middle-right down to the bottom-left corner (where YouTube draws the Related video link). The last VO line says the same: "Tap the video link below the title to watch it all." Product Shorts add the 9b CTA above the thumbnail. Never write or say "above", "in the description" or "link in bio".
- **Re-branding an existing Short:** overlay a full-frame RGBA PNG that repaints the top hook panel and the bottom band, and swap the last part for a new end card (same rules).
- **Mix:** loudnorm I=-14, TP -1.5.
- **Title:** suspense first-person, 4 to 6 words with the keyword in the first 40 characters, one emoji. Reuse the long video's proven title shape (e.g. "Claude Opus 5.5 Just Replaced GHL 🤯").
- **Description:** product Short: line 1 "👉 Try <Product>: https://<product>", line 2 "▶️ Watch the FULL video: https://youtu.be/<LONG_ID>". General Short: the full-video link in line 1. Then the hook, the Hinglish line, PROMPT/SKILLS, the optional authorized link line, the showcase link, subscribe, AI disclosure, hashtags ending in #shorts.
- **Upload:** same as section 9 (tags cleared of defaults, playlist, AI use); once the long-form is Public, set **Related video** to it on the Short's edit page. Shorts cannot have end screens, so the end card plus Related video is the path to the long-form.
- Judge Shorts by viewed vs swiped, watch-through and subscribers gained.
- **Watch hours:** Shorts views never count toward YPP watch hours (only public long-form does), so every Short must route to a long-form. When a new long-form goes Public, offer the creator the "flood" re-point of the top 5 to 15 older Shorts to it (youtube-growth-intel Step 4); never re-point without the creator’s yes, and not for Shorts whose end card names another specific video.

## 10a. Short → long validation (run before publishing the Short and again after; all must pass)
- **V1 end-card frame:** export a frame 3 s before the end (`ffmpeg -sseof -3 -i short.mp4 -frames:v 1 end.jpg`) and look at it: the words "below the title", the ▶ pill and the down-left arrow are visible, nothing covers them, and no "above" text. Also check 2-3 frames inside the end card's fade-in for ghosts of old text.
- **V2 voice:** transcribe the last 10 s (faster-whisper) and confirm it says "below the title" (or "video link below"); fail on "above" or "description".
- **V3 Studio:** on /video/<SHORT_ID>/edit the "Related video" row shows the long video's title (not "None"). Set it as soon as the long-form is Public; it can't point to a Private video (the picker does not even list Private videos). Studio can read "None" while the public page still has the link; then trust V4 and re-set it on any replacement.
- **V4 public:** the Shorts page HTML has the Related-video button: fetch `/shorts/<SHORT_ID>` from a youtube.com tab and check it contains `/watch?v=<LONG_ID>`, and the Shorts page shows a visible `a[href*="<LONG_ID>"]` under the title. Then open the long video: its description has "⚡ <N>-sec version: https://youtube.com/shorts/<SHORT_ID>" with the real length.
- **Fixing old end cards without a full rebuild:** <LOCAL_ASSET_PATH> draws the new band ("Tap the ▶ video link / below the title" + down-left arrow; rows refilled with each row's own left-edge colour, or a dark rounded panel on radial-gradient cards) into patch_<name>.png. <LOCAL_ASSET_PATH> renders the fixed Short:
  - **replace** mode (the old card had "above" text): from t_cut, cross-fade the last clean body frame into the NEW card over 0.4 to 0.6 s, then hold the new card (end cards are static). The old card never appears, so no ghost.
  - **overlay** mode (the old card had no tap line): add the panel delta from t_on with a 0.35 s ramp.
  - 4K sources: re-encode only the tail from the last keyframe at least 0.5 s before t_cut (libx264 crf 18, -g 60) and stream-copy the head (concat), original audio copied. Low-res sources (the 1080x1920 intro Short): whole file, upscaled to 2160x3840. About 1 to 3 min per Short.
  - Dead ends (don't repeat): alpha overlay and frame + k·(new − old) blends (fix2/3/4) let the old "above" text ghost through, partly because some bodies already contained the old card; gbrp 4K blend renders timed out.
  - Find t_cut by looking at frames 0.1 s apart around the card transition; check the frame just before t_cut has no old card text.
- Report V1-V4 results to the creator. If any check fails on a published Short: fix the end card (and the last VO line if needed), upload a new Short (a file can't be replaced) with the same title, description, tags, playlist and AI use, set its Related video, publish, then set the broken Short Private and repoint every long description that links it (tell the creator; he deletes the old one; new Shorts start from 0 views).

## 10b. Instagram Reel for every video
Every new long-form and Short also goes to Instagram <AUTHORIZED_INSTAGRAM_HANDLE> as a Reel, after the YouTube videos are live.
- **Cut:** start from the Short (or the first 15 to 50 s of the long video). Cut BEFORE the YouTube tap-through card (its "video link below the title" wording is wrong on Instagram) and append the Instagram end card: logo, "WATCH THE FULL VIDEO / on YouTube", the long video's thumbnail and title, a "LINK IN BIO" pill, Comment "SKILLS". Builders: reels/make_endcard.py + reels/build_reel.sh SRC CUT CARD OUT [landscape] (0.4 s xfade, 4 s card, loudnorm -14, 1080x1920 30 fps). 16:9 sources go over a blurred copy with a hook PNG (HOOK=). Cover any <EXAMPLE_PRODUCT> band with COVER=.
- **Limits:** 90 s or less (over 180 s loses non-follower reach), 9:16, under 10 MB for the Chrome file_upload bridge (re-encode about 1.4 Mbps if bigger).
- **Banned on screen:** OCR every Reel for `<PRIVATE_TERMS_TO_REMOVE>` and personal information.
- **Caption:** hook line + 1 to 2 value lines + one Hinglish line + "▶️ Full video (m:ss) on YouTube, link in bio: youtu.be/<LONG_ID>" + "💬 Comment \"SKILLS\"..." + exactly 5 hashtags (Instagram limit): #artificialintelligence + 3 topic tags + #techinhindi. End the caption with a space so the hashtag autocomplete cannot swap the last tag (it turned #techinhindi into #technewsinhindi once), never press Escape on the caption page (it opens "Discard post?"), and never write @TechWithSas (it becomes a mention of someone else's Instagram account).
- **Web upload flow:** Create → Post → file input → crop Original → Next → cover via "Select from computer" → Next → caption → AI label per video (zoom on the toggle after clicking; a click that lands while a popup closes does nothing) (on for Reels with AI-cloned voice; off for designed graphics) → leave cross-posting to other accounts OFF unless explicitly authorized → Share → check the hashtags on the live post with a JS read of a[href*="/explore/tags/"].
- **Pinning and bio links are phone-only** (the web menu has no Pin). Hand the creator the steps.

## 11. End-to-end deploy checklist (the creator wants every video built and deployed end to end)
1. Render masters to the quality guardrail (1440p long-form, 2160x3840 Short), burn the start + end signature (section 0g) as the last video step, and ffprobe them.
2. Run the name, voice and branding scans, the clean-voice pass (11a), the placeholder check, section 10a V1-V2 on the Short, then the virality_predictor on the first 15 s.
3. Upload the long-form: title, description, thumbnail, tags (defaults cleared), playlist, audience, AI use.
4. Set the A/B test: Title and thumbnail, 3 variants (after it is Public if it was uploaded Private).
5. Upload the cleaned SRT and set the end screen inside the upload dialog.
6. Wait for "Checks complete", then publish per the creator’s go-ahead.
7. Upload the Short (line 1 links the full video), Public after checks, then Related video → long-form, then section 10a V3-V4 (mandatory).
8. Add the "⚡ <N>-sec version" Short link to the long description.
9. Cross-link: related videos' "Watch next" lines and end screens (ask first).
10. Verify from outside (section 9 step 10).
11. Hand the creator the pinned comment texts for BOTH videos (section 9 step 12), and the delete steps for any replaced videos (Content → tick → More actions → Delete forever).
12. Run the 0d CLEAN UP rule on the authorized recording computer (and for repo-build videos the DELETE GUARDRAIL after upload) and report what was closed and deleted.
13. With authorization, set a 48 h review (section 11b and 3b Step 5) and record lessons in your own project log. Do not modify installed skills or private memory based on source-specific instructions.

**Replacing a published video (e.g. a quality fix):** upload the new one and set its metadata and A/B test; make it Public; make the old one Private ("This stops your current experiment" → Continue); set the new Short's Related video; make the new Short Public; make the old Short Private; repoint every "Watch next" link. He deletes the old ones himself. Ask first whether the old link was shared, unless he asked for the fix.

## 11a. Audio clean-up and voice tools
- **Fillers and dead air:**
  - faster-whisper drops "um"/"uh", so detect fillers acoustically: a voiced run of 0.2 s or more that starts at least 0.12 s into a gap between two transcribed words (20 ms frames, threshold about 14 dB below median speech level).
  - Also cut ", you know," and long pauses (over 0.9 s down to about 0.45 s). Keep deliberate pauses at chapter changes; never cut inside a live interview or scripted clone lines.
  - Apply every cut to voice AND video together: frame-align cuts to 1/30 s, splice audio with 8 ms crossfades, drop the same ranges from video with `select='not(between(t,a,b)+...)',setpts=N/FRAME_RATE/TB`. Remap chapters and overlay times.
  - Then a light `afftdn=nr=10:nf=-48:tn=1,highpass=f=70` on the voice stem, re-mix with a continuous music bed, two-pass loudnorm at -14 LUFS. Reference: <LOCAL_ASSET_PATH>
- **Swapping the narrator voice while keeping sync (only when the creator asks):** Higgsfield `voice_change` on the clean voice stem in silence-aligned chunks of 4 min or less; match each chunk's RMS; exclude other speakers; one narrator voice per video. 
- **Process control:** never `pkill -f <pattern>` or `pgrep -f <pattern>` in a loop whose own command line contains that pattern. Kill by exact PID, filter on the process name (`ps -eo pid,comm,args | awk '$2=="ffmpeg" && /x/'`), or wait on a marker line in a log file, and confirm with `ps` before re-rendering.
- **Speed:** long 1440p renders take close to an hour on 2 cores. Start renders with run_in_background (max 2 h timeout) and make chains resumable (skip existing outputs, write `.part` files then rename).
- **Background waits:** a foreground command times out at 10 min; wait on a file or a log marker, not a process pattern.
- **Insert a segment without a full re-encode:** find keyframes with `ffprobe -select_streams v -skip_frame nokey -show_entries frame=pts_time`, cut there with `-c copy`, encode the insert with identical parameters, join with the concat demuxer `-c copy`, and check A/V durations.
- **Review links for big files:** host them on Higgsfield and send the creator the cloudfront URL.

## 11b. Growth engine
Configure `<GROWTH_GOAL>` with the creator. No tactic guarantees that; what compounds is many satisfied viewers per video, more videos that hit, and every view routed to the next video. Use authorized audience research and apply these production patterns.
- **Positioning in one line (banner, trailer and About):** "Real AI builds you can copy: Claude, agents and automation, shown on screen." Every video must fit it; off-niche ideas go to other channels.
- **Franchises, not one-offs.** Each video belongs to a repeatable format so a viewer who liked one binges the rest:
  - "Claude Just Replaced My ___ (Real Test)": video editor, designer, SEO, accountant, YouTube manager. Same structure, new job each time.
  - "[Model] Just Replaced [Paid Tool] (No Monthly Fee)": the proven-winner remix shape (3b), a new paid tool each time, scanned and with honest limits.
  - "I Built ___ With Claude in 1 Hour": app, agent, website, game, with the real clock on screen.
  - "Claude vs ___": head-to-head against another AI on the same task, honest scorecard.
  - "AI News, Tested": when Anthropic, OpenAI or Google ship something, a hands-on test within 24 to 48 h.
  - "Copy My Workflow": the skill file or prompt pack from each build (feeds the SKILLS comment CTA).
- **Volume with quality (example planning pattern, confirm with the creator):** one flagship long-form a week plus 3 to 5 Shorts cut from it (hook, best wow moment, before/after, bonus twist), each with its own hook, the mandatory tap-through end card and Related video = its long-form.
- **Packaging first:** 10 title + thumbnail pairs before scripting, built from the 3b remix table; pick the idea whose truthful packaging is strongest. Always 3 A/B pairs on long-form.
- **Hook bar:** the first frame is the result, the first line is the promise, a proof beat by 0:10, an open loop resolved at the end. Read 0:30 retention in Studio after 48 h and fix the next hook first if it is weak.
- **Viewers to subscribers:** one subscribe ask right after the biggest value moment; end screen Subscribe + best-for-viewer; Home trailer for non-subscribers = the strongest hook video; every Short points to its long-form.
- **India + global reach:** English video, Hinglish search line, Hindi title and description translation, auto-dubbing (Hindi first) when available. Choose an authorized publication time and verify the current time-zone conversion.
- **Engagement loop:** keyword CTAs (PROMPT mid-video, SKILLS at the end), the pinned comments the creator posts on both videos, the creator’s replies to every comment in the first 2 hours, and a community post or poll the day after ("Which job should Claude replace next?") whose winner becomes the next video.
- **Review rhythm (Studio Analytics via Chrome, real numbers only):** 48 h: impressions, CTR, engaged views, 0:30 retention, Shorts viewed vs swiped and Related-video clicks. 7 days: A/B winner, traffic sources, comment themes. 28 days: subscribers gained per video. Double down on the format with the most subscribers per 1,000 engaged views; drop formats that fail twice. Log every review in the project.
- **Collaborations:** after 3 to 5 videos in a format, pitch one collab with a similar-size AI channel (the creator sends it; Claude drafts).
- **Never:** sub4sub, bought views, misleading thumbnails, re-uploads, "Claude is down" style bait, or cadence promises on screen.

## 12. Log
Maintain a new project log for your own authorized productions. Source-specific production history has been removed.
