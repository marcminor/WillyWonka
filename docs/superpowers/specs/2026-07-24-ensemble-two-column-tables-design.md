# Ensemble Two-Column Tables Design

**Date:** 2026-07-24  
**Scope:** Cast section of `index.html` — Oompa-Loompa Ensemble and Squirrel Ensemble only.

## Goal

Make the Oompa-Loompa and Squirrel Ensemble sections match the table style and layout of Candy Man Kids Ensemble, using two columns of student names (no Character column).

## Out of scope

- Candy Man Kids Ensemble stays as Student / Character table.
- No changes to footnotes, main cast table, musical numbers, or other page sections.
- No new visual theme or card redesign.

## Approach

Reuse existing `table.cast` / `.cast-wrap` / `.nm` styles. Both column headers are `Student`. Name cells use `.nm` (bold name style). No dedicated ensemble table class; no CSS columns layout.

## Structure

For each of Oompa-Loompa Ensemble and Squirrel Ensemble:

1. Keep the existing `subhead`.
2. Replace the `ensemble-block` paragraph with a `cast-wrap` + `table.cast`.
3. Header row: `Student` | `Student`.
4. Body rows: pairs of names, left-to-right then down.
5. If the list has an odd count, the final row has one name and an empty second cell.

## Content rules

- Preserve current list order for each ensemble.
- Featured Oompa-Loompas keep roles inline in the name cell: `Name (Oompa Loompa N)`.
- All other names are plain (no role suffix).
- Both columns use `.nm` only (no `.rl` character column).

### Oompa-Loompa Ensemble (10 names → 5 rows)

| Student | Student |
|---|---|
| Henry Corpening (Oompa Loompa 1) | Luke Barton (Oompa Loompa 2) |
| Grant Schneider (Oompa Loompa 3) | Abigail Wilkins |
| Callie Whitenack | Raegan Schultz |
| Julia Embry | Piper Pettigrew |
| Nora Helm | Mirabelle Chea |

### Squirrel Ensemble (13 names → 7 rows)

| Student | Student |
|---|---|
| Emma Overman | Colgan Pikaart |
| Lydia Jones | Adelaide Cunningham |
| Calysta Quirino | Ellie Rose Schultz |
| Karis Overman | Eloise Thompson |
| Maggie Pikaart | John Brooks Perry |
| Brynna Helm | Makoto Chea |
| David Honeycutt | *(empty)* |

## Styling

- No CSS changes required if existing `table.cast` rules cover two equal `.nm` columns.
- Optional follow-up only if visual imbalance appears (e.g. force 50/50 column widths); not part of the initial change unless needed after a visual check.

## Success criteria

- Oompa-Loompa and Squirrel read as the same table treatment as Candy Man Kids.
- Difference is intentional: two Student columns, no Character column.
- Featured Oompa roles remain visible inline.
- Footnotes block below the ensembles is unchanged.
