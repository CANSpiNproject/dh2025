# dh2025
![version](https://img.shields.io/badge/version-1.0.0-blue)
[![License: GPL v3](https://img.shields.io/badge/License-GPL_v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0.html)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15423439.svg)](https://doi.org/10.5281/zenodo.15423439)

This repository contains the data and code for our short paper "They crossed the valley of Catamarca: A study of narrative space in novel openings" presented at DH2025 in Lisbon.

## Content
### Folders and files
- cs1 annotation data as `.tsv` files:
  - `/canspin-deu-19`
  - `/canspin-deu-20` (for legal reasons, this data from the 20th century is only available as shuffled tsv)
  - `/canspin-spa-19`
  - `/canspin-lat-19`
- cs1 annotation data as Catma project:
  - `/CATMA_4AA4ADC0-4C28-54F9-B6A1-5DCEFF34B90B_DH2025_CANSpiN`
- data and documentation of the novel beginning analysis:
  - `/novel_beginning_analysis`
    - `categories.md`: documents our definitions of the novel beginning analysis categories and their application to the texts
    - `categorization.tsv`: contains the novel beginning analysis data
- data and visualizations derived from the analysis:
  - `/results`
    - `annotation_distribution__<chapter_id>.html.json`: contains data on the distribution of cs1 annotations over a chapter in text units of 200 (spa-19 and lat-19) and 300 tokens (deu-19 and deu-20)
    - `annotation_statistics__first_1000_token.json`: documents the relative and absolute cs1 annotations amounts and most frequent token per annotation class for the first 1000 token of the first chapters of all texts
    - `annotation_statistics__whole_chapters.json`: documents the relative and absolute cs1 annotations amounts and most frequent token per annotation class for the whole first chapters of all texts
    - `/visualizations`
      - `annotation_distribution__<chapter_id>.html/.png`: visualizes the distribution data of cs1 annotations for each chapter
      - `cs1_annotation_amounts__1000_tokens.html/.png`: shows the proportion of annotation amount to the token amount in the first 1000 tokens of each text
      - `cs1_annotation_amounts__all_tokens.html/.png`: shows the proportion of annotation amount to the token amount in the whole first chapter of each text
      - `first_character_event_overview.png`: shows the token position the first character event occurs in each text
      - `first-character-event-cs1-relation__<chapter_id>.png`: combines the data on cs1 annotation distribution of each chapter with the first character event data of each chapter
- bibliography of the short paper:
  - `bibliography.bib`
- notebook to recreate analysis results that are already saved in the `/results` folder:
  - `perform_analysis.ipynb`

### Corpus overview
It consists of the first chapters of eight german, spanish, and latin-american novels from the 19th and 20th century. The data originates from the corpora of the [European Literary Text Collection (ELTeC)](https://github.com/COST-ELTeC), the [Corpus de novelas hispanoamericanas del siglo XIX (conha19)](https://doi.org/10.5281/zenodo.4766987), the [Complete Works of Uwe Johnson project (CWUJ)](https://www.germanistik.uni-rostock.de/en/forschung/uwe-johnson/werkausgabe/), and E-Books.

| Corpus | ID | Title | Author | Year | Token | Source |
|--------|----|-------|--------|------|-------|--------|
| DEU19 | DEU19_001 | Weisse Sclaven oder die Leiden des Volkes | Willkomm, Ernst Adolf | 1845 | 5491 | ELTeC-deu |
| DEU19 | DEU19_030 | Die verlorene Handschrift | Freytag, Gustav | 1864 | 7179 | ELTeC-deu |
| DEU20 | DEU20_002 | Ansichten eines Clowns | Böll, Heinrich | 1963 | 2689 | E-Book: Kiepenheuer & Witsch 2009 | restricted |
| DEU20 | DEU20_021 | Zwei Ansichten | Johnson, Uwe | 1965 | 744 | CWUJ | restricted |
| SPA19 | SPA19_001 | El Señor de Bembibre | Gil y Carrasco, Enrique | 1855 | 1843 | ELTeC-spa |
| SPA19 | SPA19_008 | Los templarios | Mora, Juan de Dios | 1856 | 4300 | ELTeC-spa |
| LAT19 | LAT19_004 | El falso Inca. Cronicón de la conquista | Payró, Roberto | 1905 | 1210 | conha19 |
| LAT19 | LAT19_041 | El pozo del Yocci | Gorriti, Juana Manuela | 1876 | 1074 | conha19 |

### Annotation overview
#### Classes
The annotation system **CANSpiN.CS1** (v1.1.0) is defined in the respective [guideline](https://doi.org/10.5281/zenodo.10437030).

#### Amount
![annotation_overview](results/visualizations/cs1_annotation_amounts__all_tokens.png)

## Usage
To use the notebook `perform_analysis.ipynb`, install the [gitma-canspin package (v1.6.5)](https://github.com/CANSpiNproject/gitma-canspin/tree/v1.6.5) following the instructions of its README. The notebook enables the user to reproduce the analysis steps we have performed. It is not necessary to execute it, if you wish to see the analysis results only. In this case, see our paper and the content of the `/results` folder.

## Licenses
The original texts are in the public domain, with the exception of the German-language novels from the 20th century, which are protected by copyright. Accordingly, the latter data is published here in a derived format as shuffled `.tsv` only.

We publish the annotations under [Creative Commons Attribution International 4.0 licence](https://creativecommons.org/licenses/by/4.0/), the Jupyter Notebook under [GNU General Public License 3](https://www.gnu.org/licenses/gpl-3.0.html).

The [Aspekta](https://github.com/ivodolenc/aspekta) font used for the creation of visualizations with the `Pillow` package in the notebook is licensed under the [Open Font License 1.1](https://openfontlicense.org/open-font-license-official-text/).
