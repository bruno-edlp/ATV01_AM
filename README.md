# AT1 — Aprendizagem de Máquina

Aluno: Bruno. Implementação em Python e NumPy de Perceptron, KNN e recomendação de servidores, reunida em `at1_am.ipynb`.

[Enunciado original](https://i-davies.github.io/conteudo-fatec-2026-2/AM/05_AT1_Perceptron_KNN/01_Atividade_Avaliativa/)

## Executar no VS Code

Requer Python 3.12 e as extensões Python e Jupyter da Microsoft.

No terminal PowerShell, dentro da pasta do projeto:

```powershell
py -3.12 -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

Se `.venv` já estiver preparado, não é necessário recriá-lo. Abra `at1_am.ipynb`, clique em **Select Kernel** e escolha **Python Environments → .venv**. Se necessário, selecione o executável `.venv\Scripts\python.exe` manualmente. Use **Restart Kernel and Run All Cells** para executar do início ao fim. Não é necessário ativar o ambiente pelo PowerShell.

## Organização e decisões

- **Perceptron:** inicialização em zero, taxa 0,1, até 100 épocas e parada após uma época sem erros. Degrau com saída 1 quando z ≥ 0. Pesos atualizados pela regra de Rosenblatt.
- **KNN:** três vizinhos, distâncias Euclidiana e Manhattan vetorizadas e votação majoritária. Índices começam em zero; empates de distância preservam a ordem da base.
- **Recomendador:** duas instâncias ordenadas por distância Euclidiana. Mantém as escalas originais do exercício, sem filtragem de capacidade mínima.
- **Validação:** última célula verifica distâncias conhecidas, ajuste à base, classes de teste e ranking.

Os dados do professor estão no próprio notebook. Os algoritmos usam apenas NumPy; as demais dependências permitem executar e validar notebooks. A pasta `.venv` é local e não deve ser enviada ao GitHub.

