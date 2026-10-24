# Thesis analysis code

Analysis scripts supporting Haoyang Yuan’s doctoral thesis on X-ray-emitting
planetary nebulae and the LE01 telescope.

## Download the source

**[Download thesis-analysis v0.1.0](thesis-analysis-v0.1.0.zip)** (25 October 2026).

The complete source tree is distributed as a ZIP archive. Extract it to retain
the directories used by the scripts. The archive contains 70 files, including
23 Python sources, 8 shell scripts, workflow documentation and selected reference
results. See `SHA256SUMS.txt` for its checksum.

```bash
unzip thesis-analysis-v0.1.0.zip
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
| `le01/` | Hot-pixel screening, paired Crab comparisons and GRB aperture counts |
| `pn/` | HASH morphology matching, ChanPlaNS controls and optical-file inventory |
| `ic1297/` | EP/FXT processing, joint spectral fits and image diagnostics |
| `reference/` | Selected numerical outputs, cohort tables and fit transcripts |
| `docs/` | Input descriptions, commands, provenance and checks performed |
| `tools/` | Packaging and numerical-reference check |

Read `README.md` and `docs/data_and_software.md` inside the archive first.
Mission event files, calibration products and the full HASH export are supplied
separately from this code package. FXTDAS and HEASoft/XSPEC are required for the
IC 1297 reduction and spectral fitting.

## Version and citation

The code follows the thesis revision of 24 October 2026. Release version: 0.1.0.
Use `CITATION.cff` and cite the scientific sources identified in the thesis and
workflow documentation. Cite a fixed repository commit or release in the thesis.

No open-source licence has been selected for this version.
