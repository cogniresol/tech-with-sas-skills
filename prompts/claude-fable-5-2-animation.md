# Claude Fable 5.2 animation: the prompt and making-of

This is the prompt used for the Tech with Sas browser demonstration of **One Cable, Two Continents**, plus a practical guide to reproducing the workflow. The demonstration was recorded on November 11, 2026.

The result is an interactive eight-second 3D machinery scene. The YouTube Short and longer making-of are separate edits with screen recordings and narration. One prompt did not generate an entire finished YouTube video.

## What you need

- A Claude account with the model and Artifacts features available to you. The recorded session displayed **Fable 5.2**, with Medium and Auto shown beside it. Availability and usage limits can differ by account.
- A browser that can display WebGL scenes. The recorded demonstration used Chrome on a Mac.
- Screen-recording and video-editing tools.
- For narration, your own recording or a voice you have permission to use. ElevenLabs narration and any Higgsfield footage are separate production assets, not output from this animation prompt.

The text below can be copied. It is not a guarantee of identical code, images, timing, cost or model output. Check your own account's costs before running it.

## 1. The exact first prompt

This was transcribed from the expanded submitted prompt visible in the recording evidence. Line wrapping is normalized; the wording is preserved.

```text
I am testing Claude Fable 5.2 for a Tech with Sas video. Create an original interactive animation artifact titled One Cable, Two Continents: an 8-second cinematic view of illustrative nineteenth-century cable-paying-out machinery on a ship deck. The actual subject of my video is your AI coding process and resulting animation, not a standalone history documentary. Use React with Three.js if supported by Artifacts. Include detailed spoked guide wheels, linked rotating gears, a continuous cable visibly feeding through their grooves, a storage coil, timber deck, railings, a softly moving ocean and atmospheric light. Use a deliberate slow camera arc and physically coherent cable/wheel motion. Avoid a simple flat diagram or slideshow. Provide Play/Pause, Restart and a scrubbable time slider so I can compare frames and record the result. No external APIs, paid services, login, private data, copyrighted imagery or downloads. Keep it self-contained. This is an illustrative engineering scene, not a measured historical reconstruction. Build the working artifact now, then briefly state what you implemented and what you actually tested. Do not claim that you created our pre-existing Higgsfield footage or ElevenLabs narration. Do not claim success for untested output.
```

If you are adapting the prompt for your own channel, change the channel name and remove references to footage or narration you do not have. Preserve the distinction between generated animation, separately created media and the finished edit.

## 2. What the first run produced

Claude returned an interactive React/Three.js artifact with cable machinery on a timber deck, a moving ocean, a cinematic camera arc and playback controls. The generated controls included Play/Pause, Restart, a time slider and single-frame stepping.

The saved model response described a self-contained HTML page with bundled libraries and procedural textures. It also reported tangent-line/arc cable geometry and wheel-speed/gear-ratio checks. Those are **the model's reported implementation and tests**, not an independent engineering certification.

The scene is an illustrative mechanism. It should not be used as a historically exact reconstruction or as engineering design advice.

## 3. Test the result before recording it

These two checks are visible in the saved browser screenshots:

- Paused at **2.10 seconds, frame 63/240**.
- Pressed **+1 frame**, reaching **2.13 seconds, frame 64/240**.

For your own result, also check Restart, scrubbing, the beginning and end of the shot, cable continuity, clipping and whether the wheels move consistently with the cable. Record failures and fixes rather than assuming the model's test report is correct.

A real limitation appeared in the first view: the cinematic camera cropped the storage coil or cable outfeed at some moments, making the whole route hard to inspect at once.

## 4. The camera revision

The next request preserved the cinematic camera and asked for a separate fixed **Inspection** view containing the whole cable route and all five wheels.

The following is a **reusable reconstruction of that follow-up request**, based on the captured request and saved response. It is not presented as a verbatim transcript of the complete submitted follow-up.

```text
The cinematic camera crops the storage coil or cable outfeed at some moments, so viewers cannot inspect the full cable route at once.

Revise the same artifact once. Preserve the existing cinematic camera, mechanism and visual style. Add a clearly labelled Inspection camera mode with a fixed camera that keeps the whole coil-to-outfeed route and all five wheels in frame at 16:9, plus a small camera-mode selector.

Switching cameras must preserve the selected time, Play/Pause state and frame stepping. Keep the earlier version available for comparison.

Test the camera selector, Pause, Restart and single-frame controls in a browser. Report the exact observed values and what remains untested. Do not claim real-device smoothness or new physics validation unless you actually measure it.
```

The saved response reported a camera selector with **Cinematic arc** and **Inspection (fixed)** modes. It reported preserving time and paused state when switching, checking framing at 0, 4 and 8 seconds, and retaining the original version for comparison. The production recording includes a camera comparison and revision-control test.

## 5. Turn the demonstration into a video

The production used a genuine browser run, a recorded correction and separately generated narration. To reproduce that approach:

1. **Show the challenge and result early.** Make clear that you are testing an AI animation workflow.
2. **Record the actual model selection and prompt.** Hide private account details and unrelated conversations. Do not stage a fake response or terminal.
3. **Capture the first result.** Include a short readable view of the playback controls and a clean segment of the animation.
4. **Show the flaw.** Here it was the camera cropping parts of the mechanism.
5. **Record the revision and comparison.** Compare the two cameras at the same time value.
6. **Write narration from the observed result.** Explain what Claude generated, what you checked and what still needs work. Generate voiceover only with an authorized voice.
7. **Build separate edits.** The review pair for this demonstration was a 45-second vertical Short and a 4-minute-26-second landscape making-of. Use the Short for the challenge, prompt, result and one fix. Give the longer edit room for the controls, revision and tool attribution.
8. **Add readable captions and inspect the final exports.** Check the vertical crop separately, especially the machinery and control labels. Listen to the exported file and test it on the device where viewers will watch.

These are workflow instructions, not the exact editing project or a frame-by-frame recreation. The generated artifact source, private browser captures, narration files and editing project are not bundled in this document.

## Limits to keep visible

- This was a **Claude browser Artifacts** demonstration. It should not be described as a successful Claude Code/Blender run.
- Claude generated the 3D artifact. It did not create the pre-existing Higgsfield footage or ElevenLabs narration.
- The model reported testing in headless Chrome with software WebGL. It also reported that the software renderer was too slow to judge real-time smoothness.
- The first response warned that below 10 fps, playback can slow rather than skip frames. An eight-second animation timeline may therefore take longer than eight wall-clock seconds on a slow device.
- There is no verified cross-browser, mobile-performance, frame-rate or physical-simulation benchmark here.
- The original artifact link belongs to an account session and is not offered here as a public download.
- Prompts can produce different outputs on rerun. No cost, speed, quality or view-count guarantee is made.

## Questions

Use the comments on the relevant [Tech with Sas YouTube video](https://www.youtube.com/@TechWithSas). Comment **PROMPT** to ask for this prompt and workflow guide.
