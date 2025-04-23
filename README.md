# ClimateIE: A Dataset for Climate Science Information Extraction

**ClimateIE** is a hybrid human-AI framework for structured information extraction (IE) from climate science literature. It combines large language models (LLMs) with expert-guided validation to extract climate-specific named entities, relationships, and ontology-linked concepts. The resulting corpus, tools, and taxonomy provide a foundation for building climate knowledge graphs and advancing climate informatics.

## 🧩 Key Features

- **ClimateIE Corpus**:  
  - Located in `./corpus/`: 625 climate publications annotated via a hybrid human-AI pipeline with mappings to the GCMD+ taxonomy.
- **GCMD+ Taxonomy**:  
  - Used to guide entity linking and normalization. File: `GCMD_plus.json` (Version: 12142024).
- **Expert Annotations**:  
  - Located in `./human_corpus/`: 25 climate publications annotated by domain experts and mapped to GCMD+.
- **Extended Taxonomy (GCMD+)**: An expansion of NASA’s Global Change Master Directory with 16,000+ climate-relevant entities and links to Wikidata.
- **Three Core IE Tasks**:
  - **Named Entity Recognition (NER)** – Recognizes domain-specific entities (e.g., models, variables, platforms).
  - **Relationship Extraction (RE)** – Extracts scientific relationships (e.g., *MeasuredAt*, *ComparedTo*).
  - **Entity Linking (EL)** – Maps extracted entities to GCMD+.
- **Model Evaluation**: Benchmarks 7 models including Llama-3.3, GPT-4o, GLiNER, and ClimateBERT.
- **Tools & Guidelines**: Includes annotation protocols, taxonomy files, and evaluation scripts.

## 📊 Benchmark Results (Strict F1)

| Model         | NER   | RE    | EL    |
|---------------|-------|-------|-------|
| Llama-3.3-70B | 0.378 | 0.053 | 0.367 |
| GPT-4o        | 0.291 | 0.079 | 0.304 |
| ClimateGPT    | 0.062 | 0.022 | 0.058 |

> Llama-3.3-70B shows best performance across all tasks compared to domain-specific and commercial LLMs.

## 📂 Repository Structure
ClimateIE/
├── corpus/            # 625 AI-assisted annotated publications
├── human_corpus/      # 25 expert-annotated publications
├── GCMD_plus.json     #The GCMD+ Taxonomy discussed in the paper (Version: 12142024)
├── Annotation Guideline .pdf      # Annotation guidelines (PDF)
├── README.md

## 📚 Citation

If you use this dataset or framework, please cite our paper:

> **Huitong Pan**, **Qi Zhang**, **Adamu Mustapha**, **Eduard C. Dragut**, and **Longin Jan Latecki**.  
> *ClimateIE: A Dataset for Climate Science Information Extraction*.  
> In *Proceedings of the ACL 2025 Workshop on ClimateNLP*.

```bibtex
@inproceedings{pan2025climateie,
  title     = {ClimateIE: A Dataset for Climate Science Information Extraction},
  author    = {Pan, Huitong and Zhang, Qi and Mustapha, Adamu and Dragut, Eduard C. and Latecki, Longin Jan},
  booktitle = {Proceedings of the ACL 2025 Workshop on ClimateNLP},
  year      = {2025}
}