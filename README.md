# BRSET Metadata Fusion — DINOv3

🇬🇧 English | 🇧🇷 [Português](#português)

## English

Supporting code for the paper **"Comparing Clinical Metadata Fusion Strategies for Diabetic and Hypertensive Retinopathy Classification"** (Rispoli et al.). It compares strategies for fusing clinical metadata (age, sex, diabetes, and hypertension) with fundus photographs for binary classification of diabetic retinopathy (DR) and hypertensive retinopathy (HR), using DINOv3 ViT-B/16 and ViT-L/16 models adapted with LoRA on the Brazilian Retinography Data Set (BRSET).

### Notebooks

- **`brset_dr_metadata.ipynb`** — training and evaluation of the metadata fusion strategies (image-only, visual patch, learned tokens, late fusion) for diabetic retinopathy.
- **`brset_hr_metadata.ipynb`** — the same pipeline applied to hypertensive retinopathy.
- **`revision_experiments.ipynb`** — additional revision experiments (per-variable metadata sensitivity analyses, metadata-only baselines, etc.).

The notebooks were developed to run on Google Colab, with the BRSET dataset mounted via Google Drive.

---

## Português

Código de apoio ao artigo **"Comparing Clinical Metadata Fusion Strategies for Diabetic and Hypertensive Retinopathy Classification"** (Rispoli et al.), que compara estratégias de fusão de metadados clínicos (idade, sexo, diabetes e hipertensão) com fotografias de fundo de olho para classificação binária de retinopatia diabética (RD) e retinopatia hipertensiva (RH), usando os modelos DINOv3 ViT-B/16 e ViT-L/16 adaptados com LoRA sobre o Brazilian Retinography Data Set (BRSET).

### Notebooks

- **`brset_dr_metadata.ipynb`** — treinamento e avaliação das estratégias de fusão de metadados (image-only, patch visual, tokens aprendidos, late fusion) para retinopatia diabética.
- **`brset_hr_metadata.ipynb`** — mesmo pipeline aplicado à retinopatia hipertensiva.
- **`revision_experiments.ipynb`** — experimentos adicionais da revisão (análises de sensibilidade por variável de metadado, baselines apenas com metadados, etc.).

Os notebooks foram desenvolvidos para rodar no Google Colab com acesso ao dataset BRSET montado via Google Drive.
