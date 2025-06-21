## 📊 Syntactic & Lexical Complexity Analysis using NeoSCA

This notebook performs large-scale syntactic and lexical complexity analysis of `.txt` files using [NeoSCA](https://github.com/tanloong/neosca), a modern Python-based tool for analyzing linguistic features in text.

It supports batch processing with automatic output consolidation into Excel files and extraction of 14 core metrics.

---

### 📁 Folder Structure

```
syntactic_and_lexial_complexity_analysis/
├── data/                         # All your .txt files go here (e.g., 1.txt, 2.txt, ...)
├── neosca/                       # Cloned NeoSCA repo & output CSVs
├── syntactic_complexity.xlsx     # Full syntactic metrics
├── lexical_complexity.xlsx       # Full lexical metrics
├── syntactic_complexity_full.xlsx        # Duplicate of above (with ID column)
├── syntactic_complexity_14_metrics.xlsx  # Filtered to 14 core syntactic metrics
├── lexical_complexity_full.xlsx          # Duplicate of above (with ID column)
├── lexical_complexity_14_metrics.xlsx    # Filtered to 14 core lexical metrics
```

---

### ✅ Features

* ✅ One-click installation of NeoSCA and its dependencies (incl. Stanza)
* ✅ Runs SCA (syntactic) and LCA (lexical) analysis on all `.txt` files in `data/`
* ✅ Outputs two CSVs: `neosca_sca_results.csv` and `neosca_lca_results.csv`
* ✅ Extracts participant ID automatically from filenames
* ✅ Converts results into clean Excel files
* ✅ Extracts **14 core metrics** from each analysis (based on SLA research standards)

---

### 🔧 Setup

Run the following in **Google Colab**:

1. Clone and install NeoSCA
2. Install dependencies:

   ```bash
   pip install stanza openpyxl
   ```
3. Download and move Stanza resources into NeoSCA folder.
4. Run NeoSCA on all `.txt` files:

   ```bash
   python -m neosca sca data/*.txt
   python -m neosca lca data/*.txt
   ```

---

### 📦 Output

| File                                   | Description                            |
| -------------------------------------- | -------------------------------------- |
| `syntactic_complexity.xlsx`            | Full syntactic metrics for all samples |
| `lexical_complexity.xlsx`              | Full lexical metrics for all samples   |
| `syntactic_complexity_14_metrics.xlsx` | 14 key syntactic metrics only          |
| `lexical_complexity_14_metrics.xlsx`   | 14 key lexical metrics only            |

---

### 📐 14 Core Metrics

#### Syntactic Metrics (`syntactic_complexity_14_metrics.xlsx`)

* MLC (Mean Length of Clause)
* MLS (Mean Length of Sentence)
* MLT (Mean Length of T-unit)
* C/T (Clauses per T-unit)
* CT/T (Complex T-units per T-unit)
* DC/C (Dependent Clauses per Clause)
* DC/T (Dependent Clauses per T-unit)
* CP/C (Coordinate Phrases per Clause)
* CP/T (Coordinate Phrases per T-unit)
* T/S (T-units per Sentence)
* CN/C (Complex Nominals per Clause)
* CN/T (Complex Nominals per T-unit)
* VP/T (Verb Phrases per T-unit)
* C/S (Clauses per Sentence)

#### Lexical Metrics (`lexical_complexity_14_metrics.xlsx`)

* LS1, LS2 (Lexical Sophistication measures)
* VS1, VS2 (Verb Sophistication)
* CVS1 (Content Verb Sophistication)
* NDW-50, NDW-ER50, NDW-ES50 (Diversity measures)
* VV1, VV2 (Verb Variety)
* SVV1 (Standardized Verb Variety)
* CVV1 (Content Verb Variety)
* NV (Noun Variety)
* ModV (Modifier Variety)

---

### 🧠 Notes

* Make sure your `.txt` files are named numerically (e.g., `1.txt`, `2.txt`, ...) for proper ID extraction.
* NeoSCA expects Stanza resources to be copied into `neosca/ns_data/stanza_resources`.

---

### 📍 License & Attribution

This project uses:

* **[NeoSCA](https://github.com/tanloong/neosca)** – MIT License
* **[Stanza](https://stanfordnlp.github.io/stanza/)** by Stanford NLP Group

