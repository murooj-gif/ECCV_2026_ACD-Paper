# Grammar, Spelling & Acronym Fixes for main_neurips.tex and main.bib

Apply these changes manually in the Overleaf editor.
All 18 original fixes confirmed still present after reset to `bee05fe`.
14 new issues added (fixes 19-32) from fresh full-file audit.

---

## main_neurips.tex

### High-Priority (grammar / typos / critical LaTeX)

#### 1. Missing `~` before `\ref` (non-breaking space)
- **Line 123**
- Find: `Table\ref{tab:perclass_f1}`
- Replace: `Table~\ref{tab:perclass_f1}`

#### 2. Appendix reference fix (missing `~`, capitalize, split lines -> one)
- **Lines 123-125**
- Find (two lines):
  ```
  in the appendix
  \ref{table1}.)
  ```
- Replace: `in Appendix~\ref{table1}.)`

#### 3. Caption typo + inconsistent model names
- **Line 135**
- Find: `Comparision of VITERM, VITSPSD and OUR METhod on Per-class F1 (\%) of Train on Aptos and test on APTOS`
- Replace: `Comparison of ViT (ERM), SPSD-ViT, and Ours on Per-class F1 (\%) for models trained on APTOS and tested on APTOS`

#### 4. Redundant word "integration" in "integration if-then-else combination"
- **Line 239**
- Find: `\emph{class-conditional} integration if-then-else`
- Replace: `\emph{class-conditional} if-then-else`

#### 5. Missing comma after introductory clause (Contributions)
- **Line 248**
- Find: `Building on this theory we propose`
- Replace: `Building on this theory, we propose`

#### 6. Adjective form: "long-tail" -> "long-tailed"
- **Line 460**
- Find: `long-tail components of the per-class`
- Replace: `long-tailed components of the per-class`

#### 7. Theorem 2 - three fixes in one passage
- **Lines 467-470**
- Find:
  ```
  CCKR approach has a higher likelihood of achieving higher joint probability distribution
  $P_T(\phi_{\mathcal{Y}}(X),Y)$ than knowledge concatenation $P_T([h(X),K],Y)$ in the target domain

  (\emph{proof are in appendices ~\ref{proof}}).
  ```
- Replace:
  ```
  The CCKR approach has a higher likelihood of achieving a higher joint probability
  $P_T(\phi_{\mathcal{Y}}(X),Y)$ than knowledge concatenation $P_T([h(X),K],Y)$ in the target domain

  (\emph{the proof is in Appendix~\ref{proof}}).
  ```
  _(Fixes: missing "The"; "distribution" removed for concision; "proof are" -> "the proof is"; extra space before `\ref`)_

#### 8. Double spaces around "either...or" -> parentheses
- **Lines 509-510**
- Find:
  ```
  hypothesis functions  either
  knowledge-driven $h_{\text{kl}}(x)$ or deep learning-driven $h_{\text{dl}}(x)$  so that
  ```
- Replace:
  ```
  hypothesis functions (either
  knowledge-driven $h_{\text{kl}}(x)$ or deep learning-driven $h_{\text{dl}}(x)$) so that
  ```

#### 9. Missing comma after "To address this"
- **Line 910**
- Find: `To address this we propose Class-Conditional Knowledge`
- Replace: `To address this, we propose Class-Conditional Knowledge`

#### 10. Invalid LaTeX command `\texttit` -> `\textit`
- **Line 1091**
- Find: `\texttit{R3A}`
- Replace: `\textit{R3A}`

#### 11. Article missing: "under imbalance dataset" -> "under an imbalanced dataset"
- **Line 1106**
- Find: `under imbalance dataset`
- Replace: `under an imbalanced dataset`

#### 12. Missing "W" - sentence starts with lowercase "e"
- **Line 1513**
- Find: `e adopt DomainBed because it eliminates`
- Replace: `We adopt DomainBed because it eliminates`

#### 13. Missing period at end of sentence before new sentence
- **Line 1516**
- Find: `rather than dataset-specific tuning`
  (the sentence ends here with no period before "To explicitly assess" on the next line)
- Replace: `rather than dataset-specific tuning.`

#### 14. Missing space after period
- **Line 1565**
- Find: `structured tool calling.Importantly`
- Replace: `structured tool calling. Importantly`

#### 15. Figure caption: missing space after bold tag + garbled sentence
- **Lines 1816-1817**
- Fix A - missing space:
  - Find: `\textbf{Agent 2}CDA identifies`
  - Replace: `\textbf{Agent 2} (CDA) identifies`
- Fix B - garbled sentence:
  - Find: `than again agent CRA define rules from expert medical knowledge output by Agent 1 by adapting them to modality constraints and defining thresholds and confidence bounds.`
  - Replace: `CRA then refines rules from the expert medical knowledge extracted by Agent 1, adapting them to modality constraints and defining thresholds and confidence bounds.`

#### 16. Space inside bold command should be outside
- **Line 1387**
- Find: `\textbf{Limitations: }CCKR`
- Replace: `\textbf{Limitations:} CCKR`

#### 17. Capitalization in table caption
- **Line 1440**
- Find: `Eig criterion ablation. We keep cki/CCKR fixed`
- Replace: `EIG criterion ablation. We keep CKI/CCKR fixed`

#### 18. Missing comma after introductory phrase (line 118)
- **Line 118**
- Find: `In clinical data a few prevalent`
- Replace: `In clinical data, a few prevalent`

#### 19. Missing comma before verb (MESSIDOR sentence)
- **Line 123**
- Find: `such as MESSIDOR leads to a drop`
- Replace: `such as MESSIDOR, leads to a drop`

#### 20. CRITICAL LaTeX bug: `\label` used instead of `\ref`
- **Line 627**
- Find: `as illustrated in figure\label{medxai_framework2}`
- Replace: `as illustrated in Figure~\ref{medxai_framework2}`
  _(This produces no cross-reference in the PDF - it silently defines a label instead)_

#### 21. Missing article "an" before "agentic framework"
- **Line 914**
- Find: `we introduce agentic framework (R3A), a coordinated`
- Replace: `we introduce an agentic framework (R3A), a coordinated`

#### 22. Typo: "are" should be "area" in AUC expansion
- **Line 1261**
- Find: `and are under the curve (AUC)`
- Replace: `and area under the curve (AUC)`

#### 23. Double space after "(PPV),"
- **Line 1261**
- Find: `(PPV),  negative predictive`
- Replace: `(PPV), negative predictive`

---

### Medium-Priority (LaTeX ref/cite formatting)

#### 24. Missing `~` before `\ref` for Figure
- **Line 421**
- Find: `Figure \ref{medxai_framework2}`
- Replace: `Figure~\ref{medxai_framework2}`

#### 25. Lowercase "table" + missing `~` before `\ref`
- **Line 688**
- Find: `described in table \ref{app:dr_knowledge}`
- Replace: `described in Table~\ref{app:dr_knowledge}`

#### 26. Missing `~` before Figure `\ref`
- **Line 699**
- Find: `Figure \ref{fig:dr_framework}`
- Replace: `Figure~\ref{fig:dr_framework}`

#### 27. Missing `~` before Figure `\ref`
- **Line 859**
- Find: `Figure \ref{fig:deepxsoz_framework}`
- Replace: `Figure~\ref{fig:deepxsoz_framework}`

#### 28. Lowercase "table" + missing `~` before `\ref`
- **Line 894**
- Find: `as shown in the table \ref{tab:cad_results}`
- Replace: `as shown in Table~\ref{tab:cad_results}`

#### 29. Lowercase "figure" + missing `~` before `\ref`
- **Line 1088**
- Find: `as shown in figure \ref{fig3}`
- Replace: `as shown in Figure~\ref{fig3}`

#### 30. Extra space before `\ref` inside subsection heading
- **Line 1277**
- Find: `Table ~\ref{tab:perclass_f1}`
- Replace: `Table~\ref{tab:perclass_f1}`

#### 31. Lowercase "table" + missing `~` before `\ref`
- **Line 1462**
- Find: `as shown in table \ref{tab:eig_ablation}`
- Replace: `as shown in Table~\ref{tab:eig_ablation}`

---

### Acronym Issues

#### 32. "CKI" used but never defined
- **Lines 1424 and 1440**
- "CKI" appears as `CKI/CCKR pipeline` (line 1424) and `cki/CCKR` (line 1440, fixed to `CKI/CCKR` by fix #17).
- "CKI" is not introduced or defined anywhere in the paper. Options:
  - Define it on first use: `the Class-conditional Knowledge Integration (CKI)/CCKR pipeline`
  - Or replace both occurrences with just `CCKR` for simplicity.
- Recommended: replace `CKI/CCKR` with `CCKR` in both lines since CCKR is the established name.

---

## main.bib

#### 33. Wrong entry type for Su24a (has `booktitle` field but declared `@article`)
- **main.bib line 525**
- Find: `@article{Su24a,`
- Replace: `@inproceedings{Su24a,`

---

## Summary Table

| # | File | Line | Type | Find (short) | Replace (short) |
|---|------|------|------|-------------|-----------------|
| 1 | tex | 123 | spacing | `Table\ref` | `Table~\ref` |
| 2 | tex | 123-125 | spacing+caps | `appendix \n\ref{table1}` | `Appendix~\ref{table1}` |
| 3 | tex | 135 | typo+names | `Comparision of VITERM...` | `Comparison of ViT (ERM)...` |
| 4 | tex | 239 | redundant word | `integration if-then-else` | `if-then-else` |
| 5 | tex | 248 | comma | `theory we propose` | `theory, we propose` |
| 6 | tex | 460 | adjective | `long-tail components` | `long-tailed components` |
| 7 | tex | 467-470 | 3 fixes | `CCKR approach...proof are...appendices ~\ref` | `The CCKR...the proof is...Appendix~\ref` |
| 8 | tex | 509-510 | formatting | `functions  either...dl}}  so` | `functions (either...dl}}) so` |
| 9 | tex | 910 | comma | `this we propose` | `this, we propose` |
| 10 | tex | 1091 | LaTeX cmd | `\texttit{R3A}` | `\textit{R3A}` |
| 11 | tex | 1106 | article | `under imbalance dataset` | `under an imbalanced dataset` |
| 12 | tex | 1513 | typo | `e adopt DomainBed` | `We adopt DomainBed` |
| 13 | tex | 1516 | punctuation | `dataset-specific tuning` (no period) | `dataset-specific tuning.` |
| 14 | tex | 1565 | spacing | `calling.Importantly` | `calling. Importantly` |
| 15 | tex | 1816-1817 | typo+garbled | `Agent 2}CDA` + garbled sentence | `Agent 2} (CDA)` + rewritten |
| 16 | tex | 1387 | spacing | `\textbf{Limitations: }` | `\textbf{Limitations:} ` |
| 17 | tex | 1440 | caps | `Eig criterion...cki/CCKR` | `EIG criterion...CKI/CCKR` |
| 18 | tex | 118 | comma | `In clinical data a few` | `In clinical data, a few` |
| 19 | tex | 123 | comma | `MESSIDOR leads` | `MESSIDOR, leads` |
| 20 | tex | 627 | CRITICAL LaTeX | `figure\label{medxai_framework2}` | `Figure~\ref{medxai_framework2}` |
| 21 | tex | 914 | article | `introduce agentic framework` | `introduce an agentic framework` |
| 22 | tex | 1261 | typo | `and are under the curve` | `and area under the curve` |
| 23 | tex | 1261 | spacing | `(PPV),  negative` | `(PPV), negative` |
| 24 | tex | 421 | spacing | `Figure \ref{medxai_framework2}` | `Figure~\ref{medxai_framework2}` |
| 25 | tex | 688 | caps+spacing | `table \ref{app:dr_knowledge}` | `Table~\ref{app:dr_knowledge}` |
| 26 | tex | 699 | spacing | `Figure \ref{fig:dr_framework}` | `Figure~\ref{fig:dr_framework}` |
| 27 | tex | 859 | spacing | `Figure \ref{fig:deepxsoz_framework}` | `Figure~\ref{fig:deepxsoz_framework}` |
| 28 | tex | 894 | caps+spacing | `the table \ref{tab:cad_results}` | `Table~\ref{tab:cad_results}` |
| 29 | tex | 1088 | caps+spacing | `figure \ref{fig3}` | `Figure~\ref{fig3}` |
| 30 | tex | 1277 | spacing | `Table ~\ref` | `Table~\ref` |
| 31 | tex | 1462 | caps+spacing | `table \ref{tab:eig_ablation}` | `Table~\ref{tab:eig_ablation}` |
| 32 | tex | 1424+1440 | acronym | `CKI` (undefined) | define or replace with `CCKR` |
| 33 | bib | 525 | entry type | `@article{Su24a` | `@inproceedings{Su24a` |
