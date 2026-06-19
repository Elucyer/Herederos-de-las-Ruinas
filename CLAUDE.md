# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project overview

This is not a software project — it is the worldbuilding and manuscript repository for **"Herederos de las Ruinas"**, a fantasy fanfic/novel written in Spanish. All content is Markdown. There is no build, lint, or test process; "correctness" means narrative/lore consistency, not code correctness.

Note: the manuscript volume (`Volumen_I_El_Heredero_sin_Nombre/`) and `Hoja_de_Ruta_Protagonista.md` were deleted from the working tree but still exist in git history (`git show HEAD~1:Volumen_I_El_Heredero_sin_Nombre/Capitulo_001.md`, etc.) — check before assuming they don't exist when asked about chapters or the protagonist's roadmap.

## Document map and how they relate

Lore is split into focused documents, each declaring in its header which others it complements — read those headers before editing, since claims must stay consistent across files:

- **Lore_Mundo_Completo.md** — consolidated core lore: cosmology, eras, factions, the power system ("El Eco"), geography, language. The central reference; other docs extend specific sections of it.
- **Mundo_Humano.md** — the non-practitioner human population: demographics, empires, daily life. Complements Lore_Mundo_Completo.md and Fauna_y_Flora.md.
- **Fauna_y_Flora.md** — non-human life tied to the Eco (beasts, world-scale creatures, flora). Complements the "Mapa de Poder" (Lore_Mundo_Completo.md section 7).
- **Sistemas_de_Magia_Clasificacion.md** — reference doc surveying magic-system tropes from literature/anime/RPGs, used as design input.
- **Mapa_Ruta_Sistema_Magia.md** — working roadmap that tracks decisions already made vs. pending for the magic system; cross-check before changing magic rules so decided points aren't silently reverted.
- **Sistema_de_Niveles_Digestion_Eco.md** — mechanics of leveling: the 21-level / 7-division / 4-tier system defined in Lore_Mundo_Completo.md section 6, and what advancing a level means mechanically per Senda (path).
- **Poderes_Nivel_1-5.md** — concrete powers/spells/rituals for each of the 6 power origins (Lore_Mundo_Completo.md section 5), for levels 1–5.
- **Sellados.md** — lore on "Los Sellados," practitioners from past eras (near Level 22, División VI–VII) who sealed themselves to survive their era's collapse.
- **Hoja_de_Ruta_Historia.md** — overall story skeleton across 10 planned volumes; complements Hoja_de_Ruta_Protagonista.md, Lore_Mundo_Completo.md, Mundo_Humano.md, Sellados.md (protagonist roadmap currently only in git history).
- **Prompts_Mapas_Mundo.md** — 7 image-generation prompts (1 world map + 6 regional) sharing a common style guide, for producing visually consistent maps.

## Working conventions

- Documents are written in **Spanish**; match that language and tone when editing or extending lore/prose.
- Each doc's intro paragraph lists which other docs it "complementa" (complements) — when changing a fact (level system, factions, geography, power origins), check and update cross-referenced docs rather than letting them diverge.
- Numbered sections inside lore docs (e.g., "Lore_Mundo_Completo.md sección 5/6/7") are referenced by number from other docs — preserve section numbering or update all cross-references if reordering.
- Roadmap-style docs (`Mapa_Ruta_Sistema_Magia.md`, `Hoja_de_Ruta_Historia.md`) distinguish "decisiones ya tomadas" (decided) from open/pending sections — don't overwrite decided material without being asked.
