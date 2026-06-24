# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

This is not a software project — it is the worldbuilding and manuscript repository for **"Herederos de las Ruinas"**, a fantasy fanfic/novel written in Spanish. All content is Markdown. There is no build, lint, or test process; "correctness" means narrative/lore consistency, not code correctness.

Note: the manuscript volume (`Volumen_I_El_Heredero_sin_Nombre/`) and `Hoja_de_Ruta_Protagonista.md` were deleted from the working tree but still exist in git history (`git show HEAD~1:Volumen_I_El_Heredero_sin_Nombre/Capitulo_001.md`, etc.) — check before assuming they don't exist when asked about chapters or the protagonist's roadmap.

## Document map and how they relate

The lore was substantially rebuilt: the old 6-origins/21-level magic system and all faction/college/house worldbuilding tied to it (formerly in `Lore_Mundo_Completo.md`, `Mundo_Humano.md`, `Hoja_de_Ruta_Historia.md`, `Sellados.md`, `Mapa_Ruta_Sistema_Magia.md`, `Sistema_de_Niveles_Digestion_Eco.md`, `Sistemas_de_Magia_Clasificacion.md`) were deleted — that lore is being rewritten from scratch around the new magic system. Only two lore docs currently exist:

- **Sistema_del_Rastro.md** — the current magic system: Trazadores extract "huellas" (temporal fragments) from themselves, others, or objects under a strict equivalent-exchange law. Defines the 4+1 Categories, the 10-stage soul progression ("Calado"), Voluntad training, and the Sendas (combat/utility/social specializations). This is the central reference going forward — any new lore should be built consistent with it, not the deleted system.
- **Geografia_del_Mundo.md** — the 25 known continents (3 habited, 22 uninhabited) and the Tortugas-León. Each habited continent has exactly 10 cities, a limit tied directly to Sistema_del_Rastro.md's Calado stage 10 ("Trascendencia") and its Marcas de Alma mechanic — keep that link consistent when extending either doc. Cosmology, eras, and human society are still unwritten.
- **Fauna_y_Flora.md** — non-human life (beasts, world-scale creatures, flora). Still uses its own independent 1–22 beast level scale (unrelated to human Trazador progression now) — only beasts of Level 7+ form núcleos usable by Trazadores (Sistema_del_Rastro.md section 5.2).
- **Prompts_Mapas_Mundo.md** — 7 image-generation prompts (1 world map + 6 regional) sharing a common style guide, kept even though it predates the rewrite — useful for visual consistency once geography is redefined.
- **Sendas_y_Poderes.md** — combat/power-progression rules for each of the 15 Sendas in Sistema_del_Rastro.md section 9: base abilities, per-Senda Calado milestones (no uniform table across Sendas — each unlocks on the stage that fits its own logic), and a marginal combat use for every non-offensive Senda. Complements, never contradicts, Sistema_del_Rastro.md.
- **Biblia_de_la_Historia.md** — the story roadmap: premise, theme, protagonist (Kael Doran, full character sheet + timeline), Volume I act structure, and his saga-wide power progression (final ceiling: Vorágine; dual Senda Rastreador/Profeta del Rastro unlocked at Sima). The manuscript itself doesn't exist yet — this is the blueprint before prose.

Everything else (cosmology, eras, factions, language, human society, story roadmap) is being rebuilt and does not exist yet — don't assume any of the old names/structures (Ascendidos, Sellados, the 6 facciones-dioses, etc.) still apply unless redefined under the new system.

## Working conventions

- Documents are written in **Spanish**; match that language and tone when editing or extending lore/prose.
- Each doc's intro paragraph lists which other docs it "complementa" (complements) — when changing a fact, check and update cross-referenced docs rather than letting them diverge.
- Numbered sections inside lore docs are referenced by number from other docs — preserve section numbering or update all cross-references if reordering.
- `Sistema_del_Rastro.md` has a "Pendiente por desarrollar" section tracking open design questions and decisions already resolved (marked with strikethrough) — check it before re-deciding something already settled, and update it as new lore questions get resolved in conversation.
