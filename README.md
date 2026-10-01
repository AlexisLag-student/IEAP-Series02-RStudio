# IEAP-Series02-RStudio

Team solution to **IEAP-2025 Series 02: Data mining and statistical tests**
The report answers every question in the _Statistical tests_
section: definitions, the effect of a cardiac rehabilitation programme (pre/post data), and
tests of stereotypes about snorers.

## Team

| Role      | Name              | Main sections                              |
| :-------- | :---------------- | :----------------------------------------- |
| Student A | Alexis LAGARDE    | 2.1 Concepts, 3 Epilogue, repository setup |
| Student B | Vidusha THEBUWANA | 2.2 Effect of treatment over time          |
| Student C | Chloé GILLES      | 2.3 Testing some stereotypes               |

## Repository structure

```
IEAP-Series02-RStudio.qmd   master document (header, links, includes)
IEAP-Series02-RStudio.pdf   rendered report (the graded output)
references.bib              scientific references with DOIs
data/                       PrePost.csv, snore.txt
sections/                   one sub-document per section, each with one owner
```

The master document includes each file in `sections/` with
`{{< include sections/_xx.qmd >}}`. Because each person edits only their own file, we
never edit the same lines in parallel, so we avoid merge conflicts.
