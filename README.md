# Análise Preditiva de Avanço Físico em Projetos

## Sobre o Projeto
Este repositório contém um modelo de regressão não linear desenvolvido em Python para realizar a análise preditiva do avanço físico de projetos complexos. O script foi estruturado como parte de estudos aplicados em Business Intelligence & Analytics, focando na transição de uma análise puramente descritiva para projeções futuras automatizadas.

O algoritmo ingere o histórico de medições reais, aplica tratamento de dados e utiliza otimização matemática (Mínimos Quadrados Não Lineares) para ajustar as curvas de crescimento Logística e de Gompertz. O objetivo central é prever cenários de conclusão de escopo com base na velocidade de avanço documentada.

## Tecnologias e Bibliotecas
* **Linguagem:** Python
* **Tratamento de Dados:** Pandas, NumPy
* **Otimização Numérica:** SciPy (`curve_fit`, `brentq`)
* **Métricas de Validação Estatística:** Scikit-Learn (R², RMSE, MAE)

## Funcionalidades do Pipeline
1. Carga e agregação semanal da série de avanço
2. Indicadores de valor agregado (SV, SPI) por linha de base
3. Ajuste dos modelos de crescimento (Logístico e Gompertz)
4. Estimativa do prazo de conclusão
5. Validação fora da amostra (walk-forward)
6. Sensibilidade da janela de treino
7. Identificabilidade do parâmetro de assíntota (L)
8. Cenários de teto físico (L = 0,80 vs. L = 1,00)
9. Consolidação e exportação dos resultados
10. Figuras finais

Nota: O arquivo de dados original (AVANCO SEMANAL.xlsx) não foi incluído neste repositório público por questões de confidencialidade e proteção de dados do projeto.

Nota 2: O uso do parâmetro bounds faz com que o SciPy adote automaticamente o método Trust Region Reflective (TRF) em vez do Levenberg-Marquardt.
