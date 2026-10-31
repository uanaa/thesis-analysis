# Reconstructed 4XMM–HASH pair catalogue

`Chapter5_4XMM_reviewed_pairs_73_20261030.csv` accompanies Appendix A, Section A.2
of Haoyang Yuan's doctoral thesis. It contains 73 source–PN pairs: 73 distinct
4XMM-DR14 sources and 67 HASH planetary nebulae, with separations below
20 arcsec. The CSV preserves all 56 columns of the reconstructed local table
and adds two dated review columns. The original CSV is retained separately.
Blank common names are retained; use `HASH_id` to identify those objects.

## Columns

| Columns | Meaning |
|---|---|
| `SRCID`, `IAUNAME` | 4XMM source identifier and catalogue name |
| `SC_RA`, `SC_DEC` | Catalogue source coordinates in degrees |
| `SC_*`, `MJD_FIRST`, `MJD_LAST`, `N_DETECTIONS`, `CONFUSED`, `WEBPAGE_URL` | Retained 4XMM catalogue measurements, uncertainties, flags and metadata; their original catalogue definitions apply |
| `HASH_id`, `PNG`, `PN_Name` | HASH identifier, Galactic-coordinate identifier and common name |
| `separation_arcsec` | Angular separation between the catalogue positions, in arcsec |
| `F_soft` | Sum of `SC_EP_1_FLUX`, `SC_EP_2_FLUX` and `SC_EP_3_FLUX` (0.2–2.0 keV), in erg cm^-2 s^-1 |
| `F_hard` | Sum of `SC_EP_4_FLUX` and `SC_EP_5_FLUX` (2.0–12.0 keV), in erg cm^-2 s^-1 |
| `R` | `F_soft / F_hard` for positive hard-band flux; blank for the soft-only entry |
| `soft_selected` | Recalculated soft-band screen: `R > 1.5`, with the soft-only entry retained separately |
| `thesis_name` | Name used in the thesis object-level assessment, when included |
| `association_class` | Historical classification: `K`, `C`, `S`, or blank; superseded for the current assessment by the dated review column |
| `disposition` | Historical inclusion in the object-level table |
| `review_class_20261030` | Current classification: `K` published association, `C` preliminary candidate, `S` rejected association, `U` unresolved; blank for pairs failing the soft screen |
| `review_reason_20261030` | Reason for the current classification |

## Selection and relation to the thesis tables

Thirty pairs pass the recalculated soft screen: 29 have `R > 1.5` and Pe 1-7
is soft only (`F_hard = 0`). All 30 now appear in the thesis object-level
table: 12 published associations, four preliminary candidates, five rejected
associations and nine unresolved cases. The latter include seven entries with
blank common names and additional records near Abell 30 and BD+30 3639.
DPR1 and JaSt 73 are rejected because their catalogue offsets are inconsistent
with an association with the compact nebulae. The original
per-entry screening flags were not retained; `soft_selected` records the
recalculation from the catalogue fluxes.

The thesis discusses two additional rejected wide-offset comparisons,
LHA 115-N 18 and MPA J1752-2953. These lie outside the 20-arcsec
parent search and are consequently absent from this 73-row CSV. A positional
pair or a soft-band flag alone does not establish a physical PN association.

The source-catalogue references are given in the thesis (4XMM-DR14 and HASH).
The original CSV was added on 25 October 2026. The reviewed CSV was added on
30 October 2026 and is also included in the updated source ZIP. Checksums
for both are listed in `SHA256SUMS.txt`.
