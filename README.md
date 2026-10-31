# Thesis analysis code

Analysis scripts supporting Haoyang Yuan’s doctoral thesis on X-ray-emitting
planetary nebulae and the LE01 telescope.

## Download the source

**[Download the updated source](thesis-analysis-20261030.zip)** (30 October 2026).

The complete source tree is distributed as a ZIP archive. Extract it to retain
the directories used by the scripts. The update contains 26 Python sources,
8 shell scripts, workflow documentation and selected reference results.
It adds fixed-mask and matching checks, the IC 1297 joint flux profile, and
the reviewed 73-pair catalogue. See `SHA256SUMS.txt` for checksums.
The [initial v0.1.0 archive](thesis-analysis-v0.1.0.zip) remains available.

```bash
unzip thesis-analysis-20261030.zip
cd thesis-analysis
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python tools/check_release.py
python pn/analyse_chanplans_controls.py
```

The ChanPlaNS statistics run from the included 59-object cohort. Other workflows
require the observing data and catalogue inputs described inside the archive.

## Contents

| Directory inside the archive | Contents |
|---|---|
| `le01/` | Adopted archived selection, Crab statistics and GRB aperture counts |
| `pn/` | HASH morphology matching, ChanPlaNS controls and optical-file inventory |
| `ic1297/` | EP/FXT processing, joint spectral fits and image diagnostics |
| `reference/` | Selected numerical outputs, cohort tables and fit transcripts |
| `docs/` | Input descriptions, commands, provenance and checks performed |
| `tools/` | Packaging and numerical-reference check |

Read `README.md` and `docs/data_and_software.md` inside the archive first.
Mission event files, calibration products and the full HASH export are supplied
separately from this code package. FXTDAS and HEASoft/XSPEC are required for the
IC 1297 reduction and spectral fitting.

## Supplementary 4XMM pair catalogue

[Download the reviewed 73-pair CSV](Chapter5_4XMM_reviewed_pairs_73_20261030.csv)
and read the [column descriptions and selection notes](4XMM_pairs_README.md).
The table contains 73 distinct 4XMM sources paired with 67 HASH PNe within
20 arcsec. It accompanies Appendix A, Section A.2 of the thesis and is supplied
both separately and inside the updated source ZIP. All 30 soft-selected pairs
are classified: 12 published associations, four preliminary candidates, five
rejected associations and nine unresolved cases. The
[original reconstructed CSV](Chapter5_4XMM_reconstructed_pairs_73.csv) is retained.

## Version and citation

The current source follows the thesis revision of 30 October 2026.
Use `CITATION.cff` and cite the scientific sources identified in the thesis and
workflow documentation. Cite a fixed repository commit or release in the thesis.

No open-source licence has been selected for this version.
