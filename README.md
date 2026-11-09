# Boundary-Preserving Alignment

**From Bounded Artifacts to Bounded Authority: Implementing Safety in Long-Horizon Human-AI Systems Through the Governance of Authority Promotion**

Kentaro Sato · Independent Researcher · [info@metaclan.jp](mailto:info@metaclan.jp)

**Edition:** v1.1 · **Document date:** 5 November 2026 · **Type:** Position paper / preprint

[Read the paper](boundary_preserving_alignment.pdf) · [Zenodo record](https://zenodo.org/records/23969376) · [DOI: 10.5281/zenodo.23969376](https://doi.org/10.5281/zenodo.23969376)

> Exploration may be broad. Authority must be narrow, use-specific, time-bounded, and revalidatable.

## Overview

A useful summary is not necessarily a faithful quotation. An approved plan does not automatically remain authorized after conditions change. A successful tool call is not proof that the intended outcome occurred.

This paper proposes **boundary-preserving alignment** as a complementary layer of AI safety for long-horizon human-AI systems. Its central object is the promotion of artifacts into more consequential uses: display, external execution, verification, persistence, publication, and reinjection into later reasoning.

Each transition must retain and revalidate the distinctions that justified the artifact's use, including provenance, scope, time, uncertainty, permitted use, and authority. The human supervisor is treated as a finite-bandwidth participant in this control structure, not as an infallible safety mechanism.

The contribution is an integrated audit vocabulary, not a claim to have invented authority control. It connects:

- Epistemic status and operational authority within a single promotion graph.
- Bounded authorization and use-time revalidation.
- False promotion and false suppression as two-sided evaluation outcomes.
- Human oversight as a set of conformance conditions rather than the mere presence of an approval button.
- Design recommendations, testable hypotheses, concrete examples, and fault-injection cases.

This is a position paper, not a proof of safety or a report of experimentally demonstrated effectiveness. It complements research on model alignment, corrigibility, AI control, least privilege, ABAC, and zero trust.

## Repository Contents

| Path | Contents |
|---|---|
| [boundary_preserving_alignment.pdf](boundary_preserving_alignment.pdf) | English v1.1 PDF with the Zenodo DOI on its cover; 31 pages. |
| [English manuscript](manuscript/Boundary_Preserving_Alignment_English_v1.1.md) | Editable English Markdown manuscript. |
| [Japanese manuscript](manuscript/Boundary_Preserving_Alignment_Japanese_v1.1.md) | Corresponding Japanese Markdown manuscript. |
| [tex/main.tex](tex/main.tex) | Entry point for the English typeset edition. |
| [tex/gachi-report.sty](tex/gachi-report.sty) | Bundled report style; no external local project is required. |
| [tex/figures/](tex/figures/) | Four vector PDF figures used by the TeX source. |
| [CITATION.cff](CITATION.cff) | Machine-readable citation metadata. |

The Markdown files preserve the manuscript text and schematic Mermaid figure descriptions. The TeX files are the publication-layout snapshot with the final vector figures and table formatting. Editing Markdown does **not** automatically update TeX; this repository does not include an automatic Markdown-to-TeX conversion pipeline.

The Japanese manuscript is provided as a companion source. The included PDF and TeX build are English. The cover DOI is defined in `tex/main.tex`; the Markdown files remain unchanged from the reference-audited v1.1 manuscripts.

## Build the English PDF

Use **LuaLaTeX** and **latexmk** with a sufficiently complete TeX Live, MacTeX, or TinyTeX installation. Pandoc, Python, and BibTeX are not needed to compile the checked-in TeX.

From the repository root:

```sh
cd tex
latexmk -lualatex -interaction=nonstopmode -halt-on-error main.tex
```

This creates `tex/main.pdf`. It does not overwrite the archived PDF in the repository root.

The source uses standard LaTeX packages including `fontspec`, `unicode-math`, `luatexja-fontspec`, `geometry`, `microtype`, `booktabs`, `longtable`, `enumitem`, `titlesec`, `caption`, `listings`, `tcolorbox`, `fancyhdr`, `xurl`, `hyperref`, and `bookmark`, together with their dependencies. Minimal TinyTeX installations may require additional packages.

**Fonts:** TeX Gyre Pagella, Heros, Cursor, and Pagella Math are required. For Japanese glyphs, the style uses Hiragino fonts where installed and otherwise falls back to Harano Aji fonts supplied by TeX Live. Fonts are not redistributed here.

The repository root PDF is the preserved publication artifact. Recompilation may change PDF metadata, font embedding, or pagination across environments; byte-for-byte reproducibility is not claimed.

## Citation

Please cite the archived edition by DOI:

> Sato, K. (2026). *Boundary-Preserving Alignment: From Bounded Artifacts to Bounded Authority: Implementing Safety in Long-Horizon Human-AI Systems Through the Governance of Authority Promotion* (Version 1.1). Zenodo. https://doi.org/10.5281/zenodo.23969376

```bibtex
@misc{sato2026boundary,
  author    = {Sato, Kentaro},
  title     = {Boundary-Preserving Alignment: From Bounded Artifacts to Bounded Authority:
               Implementing Safety in Long-Horizon Human-AI Systems Through
               the Governance of Authority Promotion},
  year      = {2026},
  version   = {1.1},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.23969376},
  url       = {https://doi.org/10.5281/zenodo.23969376}
}
```

For the deposited paper's license and archive metadata, consult the [Zenodo record](https://zenodo.org/records/23969376). This repository does not assign a separate software license to its build-support files.

## 日本語

「境界保存型アライメント」の原稿・組版ソース置き場です。AIの出力が、発言の引用、実行権限、検証済みの結果、永続記憶などへ扱いを変える際に、根拠・用途・時点・不確実性・権限の境界を保持することを提案します。

公開済み英語PDF、日本語・英語MD、図を含む自己完結した英語TeX一式を収録しています。引用は上記のZenodo DOIを使用してください。
