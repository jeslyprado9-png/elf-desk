# Elf Desk

A browser-local character chatbot for a humanities local-model exercise. Pip is a fictional overworked North Pole elf. Published with GitHub Pages from main / root.

## Models
- onnx-community/SmolLM2-135M-Instruct-ONNX, q4: weights listed as 181 MB; allow about 200 MB including supporting files.
- onnx-community/SmolLM2-360M-Instruct-ONNX, q4: weights listed as 386 MB; allow about 400 MB including supporting files.

File sizes are not runtime RAM usage. Browser/runtime downloads and cached files affect actual transfers. WebGPU is preferred with WASM fallback.

## Character guidance
Edit `persona` and `examples` inside index.html to adjust the character. Version 2 adds short example dialogues and deterministic generation; this is in-context prompting, not fine-tuning. Examples can be repeated by the model. There is no scripted reply fallback. No API key, analytics, or cloud inference API is used.

## Comparison
1. Load Pocket Pip. Record the displayed load time (download plus initialization; cached loads differ).
2. Ask the same questions in the same order for each model: Why is the workshop behind? What happened with Santa and the glitter printer today? Tell me an elf joke. Then try an unseen question, e.g. Why are the reindeer on strike?
3. Record displayed reply durations and compare relevance, coherence and character voice.
4. Load Bigger Pip and repeat. Actual total browser/GPU memory is not measured by this page. Use your OS memory tools if required, distinguishing browser baseline from model usage.
5. Keep the loaded tab open and disable Wi-Fi to check local replies. Restore Wi-Fi afterward.
6. In Incognito, check public model downloading without a login.

The model retains one recent exchange plus fixed character examples. Chat history is kept in memory, not intentionally persisted. Browser cache may retain model files, but clearing cache or closing private browsing can require another download. An offline open tab is supported after assets load; offline page reload is not guaranteed.

Original screenshots document version 1. Do not label those screenshots as results from the revised prompt. Performance and character quality must be observed, not assumed.
