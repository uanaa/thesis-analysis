# Reconstructed 4XMM–HASH pair catalogue

`Chapter5_4XMM_reconstructed_pairs_73.csv` accompanies Appendix A, Section A.2
of Haoyang Yuan's doctoral thesis. It contains 73 source–PN pairs: 73 distinct
4XMM-DR14 sources and 67 HASH planetary nebulae, with separations below
20 arcsec. The CSV preserves all 56 columns of the reconstructed local table.
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
| `association_class` | `K`: known PN-associated X-ray source; `C`: candidate; `S`: rejected positional association; blank for pairs not assessed individually |
| `disposition` | Whether the pair appears in the thesis object-level table |

## Selection and relation to the thesis tables

Thirty pairs pass the recalculated soft screen: 29 have `R > 1.5` and Pe 1-7
is soft only (`F_hard = 0`). Twenty of these pairs appear in the thesis
object-level table. The other ten are DPR1, seven entries with blank common
names, and additional records near Abell 30 and BD+30 3639. The original
per-entry screening flags were not retained; `soft_selected` records the
recalculation from the catalogue fluxes.

The thesis object-level table also contains two rejected wide-offset
comparisons, LHA 115-N 18 and MPA J1752-2953. These lie outside the 20-arcsec
parent search and are consequently absent from this 73-row CSV. A positional
pair or a soft-band flag alone does not establish a physical PN association.

The source-catalogue references are given in the thesis (4XMM-DR14 and HASH).
The CSV was added on 25 October 2026 and is separate from the v0.1.0 analysis
code ZIP. Its SHA-256 checksum is listed in `SHA256SUMS.txt`.
