# ai-ronaldo

Predição de $\lambda_{max}$ (comprimento de onda de máxima absorção) de moléculas orgânicas via aprendizado profundo, com aplicação a um conjunto proprietário de candidatos para triagem experimental.

Projeto da disciplina CCM-109 -- Tópicos Especiais em Inteligência Artificial (PPG em Ciência da Computação, UFABC).

## Estrutura

- `main.ipynb` -- notebook com todo o pipeline: pré-processamento, treino/comparação dos modelos (MLP, Gradient Boosting, Bi-LSTM e, opcionalmente, D-MPNN/Chemprop) e aplicação ao conjunto proprietário com quantificação de incerteza.
- `resources/` -- dados (Deep4Chem em cache, conjunto proprietário `banco_smiles_aromatizados.parquet`), figuras geradas e o ranking final exportado.
- `latex/` -- relatório em formato SBC (`relatorio_lambda_max_SBC.tex` + `sbc-template.sty`).

## Como rodar

Abra `main.ipynb` e execute as células em ordem. O flag `QUICK_TEST` no início do notebook alterna entre uma execução reduzida (validação rápida do pipeline) e a execução completa sobre o Deep4Chem inteiro (recomendado rodar em Google Colab com GPU).

O dataset público Deep4Chem é baixado automaticamente do Figshare na primeira execução.

