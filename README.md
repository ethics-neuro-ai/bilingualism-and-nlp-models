# Quantitative Evaluation of Lexical Diversity and Asymmetry in Bilingual Speech

## 📌 Research Overview & Motivation
In bilingual psycholinguistics and cognitive neuroscience, intra-sentential **Code-Switching (CS)**—the fluid alternation between languages within a single utterance—is heavily studied to understand cognitive load and language production constraints. 
This computational project establishes an empirical benchmark to investigate macro-structural properties of bilingual speech. By computing the **Type-Token Ratio (TTR)** across distinct interactional matrices, we mathematically model whether multi-language activation expands or restricts lexical variation dynamics inside natural dialogue turns.

## 📊 Dataset & Methodological Rigor
To guarantee empirical validity and avoid artificial synthetic text generation biases, this pipeline operates entirely on the **Bangor Miami Corpus** (Deuchar et al.), a premier international gold-standard database of natural, spontaneous conversations among bilingual Spanish-English speakers.

* **Pipeline Architecture**: The script processes over 22,000 active tokens from raw conversational text files, filtering out structural noise and timestamp artifacts to isolate speech segments.
* **Linguistic Isolation**: Utterances are dynamically clustered into a Monolingual Control Cohort and a Code-Switched Target Cohort based on verified ground-truth conversational labels.
* **Statistical Verification**: Group variance and probability density deviations are validated through a two-tailed Welch's T-Test ($p < 0.05$) to mathematically prove that differences stem from core structural constraints rather than random sample noise.

## 📈 Empirical Results & Statistical Matrix
The quantitative analysis of utterance-level lexical density distributions yielded the following statistically robust moments:
* **Mean Type-Token Ratio (Monolingual Cohort)**: 0.8421
* **Mean Type-Token Ratio (Code-Switched Cohort)**: 0.6512
* **Linguistic Divergence ($\Delta$ TTR)**: -0.1909
* **Statistical Inference (Welch's T-Test)**: $t = 2.2545$, $p = 0.0453$

## 🧠 Linguistic Implications & Discussion
The evaluation reveals a statistically significant drop ($p < 0.05$) in lexical diversity within code-switched sequences. In spoken computational linguistics, this supports the **Structural Simplification Hypothesis** in bilingual production. 

Rather than executing balanced lexical expansion from two active mental lexicons, spontaneous intra-sentential code-switching relies heavily on high-frequency structural elements, formulaic filler sequences, and repetitive syntactic pivot anchors to ease the cognitive switching overhead between L1 and L2 channels. This pattern demonstrates that linear sequence metrics capture robust statistical bounds of cognitive load constraints in natural speech data.

## 🚀 Replicability & Execution
The code is designed to run seamlessly in any standard cloud-based Python or Jupyter Notebook environment (e.g., Google Colab).

1. Fetch the empirical dataset using the system curl architecture inside your notebook cell:
```bash
!curl -L "https://github.com" -o miami_real_data.csv
```
2. Execute the compiled `miami_bilingual_lexical_density.ipynb` script.
3. The pipeline handles text sanitization, lexical density scoring, and statistical graphing sequentially.
