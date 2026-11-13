# BRSET Metadata Fusion — DINOv3

🇬🇧 English | 🇧🇷 [Português](#português)

## English

Code accompanying the paper:

> Rispoli, V. C.; Müller, A.; Medeiros, W. G.; Gomes, M. M. F.; Martins, T. A.; Deusdará, R. **Comparing Clinical Metadata Fusion Strategies for Diabetic and Hypertensive Retinopathy Classification.** *Machine Learning and Knowledge Extraction* 2026, 8(8), 299. https://doi.org/10.3390/make8100299

The paper compares an image-only baseline with three strategies for adding clinical metadata (age, sex, diabetes status and hypertension status) to a DINOv3-based fundus classifier, using ViT-B/16 and ViT-L/16 backbones adapted with Low-Rank Adaptation (LoRA) on the Brazilian Multilabel Ophthalmological Dataset (BRSET), with three patient-wise folds:

| Strategy | Description |
|---|---|
| Image-only | Baseline; fundus photograph only |
| Visual metadata patch | Variables encoded as a small manually designed region inside the photograph |
| Learned metadata tokens | Variables embedded as tokens inserted into the Transformer sequence (early fusion) |
| Late fusion | Variables encoded separately and concatenated with the final DINOv3 visual representation |

### Notebooks and paper correspondence

| Notebook | Content | Paper |
|---|---|---|
| [`brset_dr_metadata.ipynb`](brset_dr_metadata.ipynb) | Training and evaluation of the four configurations for **diabetic retinopathy** (9531 images, 1070 positive) | DR results (ViT-B/16 and ViT-L/16) |
| [`brset_hr_metadata.ipynb`](brset_hr_metadata.ipynb) | Same pipeline for **hypertensive retinopathy** (8745 images, 284 positive) | HR results (ViT-B/16 and ViT-L/16) |
| [`revision_experiments.ipynb`](revision_experiments.ipynb) | Additional experiments added during revision, run on top of the splits and outputs of the two notebooks above (e.g., target-status variable ablations, metadata-only models, paired bootstrap comparisons) | Ablation and statistical-comparison analyses |

### Usage

1. Obtain BRSET (`labels_brset.csv` and `fundus_photos/`) from PhysioNet under its data use agreement; the dataset is not redistributed here.
2. The notebooks were developed for Google Colab with a GPU and Google Drive mounted. Edit the path variables (`CSV_PATH`, `IMAGES_DIR`, `OUTPUT_DIR`) in the configuration cell.
3. DINOv3 weights are downloaded from Hugging Face and may require accepting the model license.
4. Run `brset_dr_metadata.ipynb` and/or `brset_hr_metadata.ipynb` first; `revision_experiments.ipynb` reads their patient-wise splits and outputs.

### Citation

If you use this code, please cite the paper above.

---

## Português

Código de apoio ao artigo:

> Rispoli, V. C.; Müller, A.; Medeiros, W. G.; Gomes, M. M. F.; Martins, T. A.; Deusdará, R. **Comparing Clinical Metadata Fusion Strategies for Diabetic and Hypertensive Retinopathy Classification.** *Machine Learning and Knowledge Extraction* 2026, 8(8), 299. https://doi.org/10.3390/make8100299

O artigo compara um baseline apenas com imagem a três estratégias de inclusão de metadados clínicos (idade, sexo, diabetes e hipertensão) em um classificador de fundo de olho baseado em DINOv3, usando os backbones ViT-B/16 e ViT-L/16 adaptados com Low-Rank Adaptation (LoRA) sobre o Brazilian Multilabel Ophthalmological Dataset (BRSET), com três folds separados por paciente:

| Estratégia | Descrição |
|---|---|
| Image-only | Baseline; apenas a fotografia de fundo de olho |
| Patch visual de metadados | Variáveis codificadas como uma pequena região projetada manualmente dentro da fotografia |
| Tokens de metadados aprendidos | Variáveis embutidas como tokens inseridos na sequência do Transformer (fusão precoce) |
| Late fusion | Variáveis codificadas separadamente e concatenadas à representação visual final do DINOv3 |

### Notebooks e correspondência com o artigo

| Notebook | Conteúdo | Artigo |
|---|---|---|
| [`brset_dr_metadata.ipynb`](brset_dr_metadata.ipynb) | Treinamento e avaliação das quatro configurações para **retinopatia diabética** (9531 imagens, 1070 positivas) | Resultados de RD (ViT-B/16 e ViT-L/16) |
| [`brset_hr_metadata.ipynb`](brset_hr_metadata.ipynb) | Mesmo pipeline para **retinopatia hipertensiva** (8745 imagens, 284 positivas) | Resultados de RH (ViT-B/16 e ViT-L/16) |
| [`revision_experiments.ipynb`](revision_experiments.ipynb) | Experimentos adicionais da revisão, executados sobre os splits e saídas dos dois notebooks anteriores (ex.: ablações da variável relacionada ao alvo, modelos apenas com metadados, comparações por bootstrap pareado) | Análises de ablação e comparação estatística |

### Uso

1. Obtenha o BRSET (`labels_brset.csv` e `fundus_photos/`) no PhysioNet, mediante o termo de uso dos dados; o dataset não é redistribuído aqui.
2. Os notebooks foram desenvolvidos para o Google Colab com GPU e Google Drive montado. Edite as variáveis de caminho (`CSV_PATH`, `IMAGES_DIR`, `OUTPUT_DIR`) na célula de configuração.
3. Os pesos do DINOv3 são baixados do Hugging Face e podem exigir o aceite da licença do modelo.
4. Execute primeiro `brset_dr_metadata.ipynb` e/ou `brset_hr_metadata.ipynb`; `revision_experiments.ipynb` lê os splits por paciente e as saídas deles.

### Citação

Se você usar este código, cite o artigo acima.
