The Portuguese course previously covered only units 0–1. This PR revises those 10 sections, translates the remaining 40 across units 2–8 and events, and completes the Portuguese table of contents against English reference `56b6e8334aef7e0efa0137574f068c968f3f6e1c`. Code examples, recorded outputs, model identifiers, URLs and quiz answer logic are preserved. Presentation fixes make literal tokens, quiz emphasis and tip content render correctly.

Related to huggingface/audio-transformers-course#173. Translation and separate comparative and linguistic review passes were performed with Codex; this is not an independent human review. All 50 sections are translated and textually reviewed. The glossary, per-section progress, invariant checker and validation report are included under `docs/traducao-pt-br/`.

Validation repeated on 2026-10-12:
- `make quality` passed across the repository.
- `verificar.py --complete` passed for all 50 sections: code/output blocks, URLs, heading counts, index order and quiz structure.
- The translation validator reports no missing sections; `pip check` passed.
- All 21 Portuguese notebooks were regenerated in a fresh directory and passed `nbformat` schema validation. ML cells were not executed.
- English and other language sources remain unchanged; the upstream English reference still matches the translation baseline.

Earlier validation recorded in `relatorio.md` and `evidencias.json`: full pt-BR doc-builder compilation; all 50 browser routes returning HTTP 200 with no page JavaScript errors; visual inspection of every page; all 41 alternatives across 14 quiz questions exercised; notebook code and recorded outputs checked against the chapters. These browser/build checks were not repeated during the submission pass.

Limitations: remote images, audio and embeds could not be inspected in the earlier restricted environment; two broken relative links inherited from English are documented and preserved. Generic renderer controls and notebook-generator boilerplate remain in English. Original technical inconsistencies are recorded separately. A local KaTeX CSS workaround affected only the earlier preview kit, not the course files or deployed renderer. These limits remain disclosed for maintainer review. This submission covers documentation and does not guarantee the operation of external services.

The translation is ready for maintainer review. No merge or deployment is included.
