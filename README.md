# Text to SPARQL

## Notebooks

| Type     | Use-Models                                                         | FineTuning                                                                 | T5 Task Prefix                  |
| -------- | ------------------------------------------------------------------ | -------------------------------------------------------------------------- | ------------------------------- |
| Wikidata | [use-t5-small-lcquad.ipynb](src/lc-quad/use-t5-small-lcquad.ipynb) | [finetune-t5-base-lcquad.ipynb](src/lc-quad/finetune-t5-base-lcquad.ipynb) | `translate english to sparql:`  |
| DBPedia  | [use-t5-small-qald9.ipynb](src/qald/use-t5-small-qald9.ipynb)      | [finetune-qald-t5-base.ipynb](src/qald/finetune-qald-t5-base.ipynb)        | `translate english to sparql2:` |

All our notebooks during development with more details: <https://github.com/yazdipour/text-to-sparql-development>

## Model

| Based on | Dataset         | Date       | Model Link                                                                                                |
| -------- | --------------- | ---------- | --------------------------------------------------------------------------------------------------------- |
| t5-base  | lc-quad & qald9 | 2021-10-19 | [yazdipour/text-to-sparql-t5-base-qald9](https://huggingface.co/yazdipour/text-to-sparql-t5-base-qald9)   |
| t5-small | lc-quad & qald9 | 2021-10-19 | [yazdipour/text-to-sparql-t5-small-qald9](https://huggingface.co/yazdipour/text-to-sparql-t5-small-qald9) |
| t5-base  | lc-quad         | 2021-10-19 | [yazdipour/text-to-sparql-t5-base](https://huggingface.co/yazdipour/text-to-sparql-t5-base)               |
| t5-small | lc-quad         | 2021-10-19 | [yazdipour/text-to-sparql-t5-small](https://huggingface.co/yazdipour/text-to-sparql-t5-small)             |

## Datasets

| Name                | Source                                                                                                         |
| ------------------- | -------------------------------------------------------------------------------------------------------------- |
| Processed LcQuad-v2 | https://github.com/yazdipour/text-to-sparql-development/tree/main/data/dataset                                 |
| Processed QALD 9    | https://github.com/yazdipour/text-to-sparql-development/tree/main/data/dataset/qald-text-to-sparql             |
| QALD 9 Prefixes     | https://github.com/yazdipour/text-to-sparql-development/blob/main/data/qald-9-preprocess/2021-04-19/prefix.csv |
| Original LcQuad v2  | http://lc-quad.sda.tech/                                                                                       |
| Original QALD 9     | https://github.com/ag-sc/QALD/                                                                                 |

## T5 Prefixes

| Task Prefix                     | Model                  | Type            |
| ------------------------------- | ---------------------- | --------------- |
| `translate english to sparql:`  | text-to-sparql-t5      | WikiData Sparql |
| `translate english to sparql2:` | text-to-sparql-t5-QALD | DBPedia Sparql  |
