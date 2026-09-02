# QA Checklist: E-Learning Localization (Articulate Storyline)

A working checklist built from a full English-to-German roundtrip on a Storyline module — translation export, reimport, layout repair, audio replacement and caption cleanup.

---

## 1. Before the export

- [ ] Generate the translation export and open it before sending it to translators
- [ ] Confirm the export contains: slide text, slide notes, alt text, feedback layers, button labels, layer text
- [ ] Flag slide names that must **not** be translated — they are internal identifiers, not learner-facing
- [ ] Clarify player labels separately — they are not part of the translation export
- [ ] Clarify closed captions separately — they use their own VTT import/export path
- [ ] Check menu entries for completeness; results slides are often missing by default
- [ ] Agree who supplies target-language player labels and captions, and by when

## 2. After the import

- [ ] Open every slide individually — spot checks are not enough
- [ ] Text boxes: check for overflow, scrollbars, or autofit silently shrinking type
- [ ] Buttons: confirm the translated label still fits the shape
- [ ] Master layout: confirm slide masters still apply after import
- [ ] Spot-check translations against the source for copy-paste errors between rows
- [ ] Verify special characters render correctly in the chosen font

## 3. Audio

- [ ] Document source and target clip lengths in a delta table before starting
- [ ] Use *Replace Audio* rather than delete-and-insert to preserve triggers and naming
- [ ] Adjust slide duration — this applies to **shorter** target clips as well as longer ones
- [ ] Reposition cue points to match the new voiceover rhythm
- [ ] Re-anchor timed objects to the moved cue points
- [ ] Play every slide end to end; do not rely on partial playback

## 4. Captions

- [ ] Confirm caption language matches the audio language on every slide
- [ ] Review AI-generated captions manually — automatic splits break mid-sentence
- [ ] Keep lines to roughly 42 characters, break at sense boundaries
- [ ] Check minimum display time (~1 s) and maximum (~6 s) per caption

## 5. Before delivery

- [ ] Full playthrough in Preview, covering every path: correct, incorrect, retry, review
- [ ] Verify player labels in the target language, including quiz result buttons
- [ ] Test the published output, not just Preview — publishing surfaces issues Preview hides
- [ ] Confirm file and folder naming conventions are intact for handover

---

## Notes from practice

**Text expansion is measurable.** In this project German ran on average 29% longer than English across six voiceover clips, with individual slides ranging from −17% to +44%. Plan layout headroom accordingly.

**Shorter is not safer.** A shortened target clip leaves trailing silence and desynchronises objects anchored to the end of the timeline. It needs the same attention as an overrun.

**Not everything translatable is in the export.** Player labels and closed captions sit outside the translation file. Establishing this before the project starts avoids unbudgeted rework.

**Structural changes belong in the source file.** Making them in the target-language file causes versions to diverge and the same fix to be repeated for every additional language.
