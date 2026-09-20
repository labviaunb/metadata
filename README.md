# BRSET Metadata Fusion — DINOv3

Código de apoio ao artigo **"Comparing Clinical Metadata Fusion Strategies for Diabetic and Hypertensive Retinopathy Classification"** (Rispoli et al.), que compara estratégias de fusão de metadados clínicos (idade, sexo, diabetes e hipertensão) com fotografias de fundo de olho para classificação binária de retinopatia diabética (RD) e retinopatia hipertensiva (RH), usando os modelos DINOv3 ViT-B/16 e ViT-L/16 adaptados com LoRA sobre o Brazilian Retinography Data Set (BRSET).

## Notebooks

- **`brset_dr_metadata.ipynb`** — treinamento e avaliação das estratégias de fusão de metadados (image-only, patch visual, tokens aprendidos, late fusion) para retinopatia diabética.
- **`brset_hr_metadata.ipynb`** — mesmo pipeline aplicado à retinopatia hipertensiva.
- **`revision_experiments.ipynb`** — experimentos adicionais da revisão (análises de sensibilidade por variável de metadado, baselines apenas com metadados, etc.).

Os notebooks foram desenvolvidos para rodar no Google Colab com acesso ao dataset BRSET montado via Google Drive.
