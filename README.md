#  Simulação de Resfriamento de Café com Redes Neurais e PINNs

Este projeto implementa a modelagem do resfriamento de uma xícara de café utilizando três abordagens:

1. **Solução Analítica** da equação diferencial de resfriamento.
2. **Rede Neural Simples** treinada apenas com dados sintéticos (temperatura vs tempo).
3. **PINN (Physics-Informed Neural Network)** que aprende a constante de resfriamento `r` incorporando a equação diferencial como restrição física durante o treinamento.

##  Funcionalidades

- Geração de dados sintéticos com ruído a partir da solução analítica.
- Treinamento de uma rede neural para prever a temperatura ao longo do tempo (inclusive fora da faixa de dados).
- Treinamento de uma PINN para estimar a constante `r` e prever o comportamento físico de longo prazo com maior precisão.
- Visualização gráfica das curvas de temperatura para comparação entre as abordagens.


##  Objetivo

Comparar o desempenho da regressão via redes neurais com e sem conhecimento físico embutido, destacando o poder das PINNs em problemas de extrapolação com poucos dados.

##  Resultados:

Neste caso, observei que, ao utilizarmos uma regressão simples, a rede neural se comporta bem apenas nos dados iniciais fornecidos. No entanto, à medida que extrapola, ela se desvia do comportamento esperado. Por outro lado, quando aplicamos a PINN (Physics-Informed Neural Network), incorporando as leis físicas ao problema, a rede é capaz de representar com precisão o resfriamento da xícara de café, seguindo de perto a solução analítica.

![NN simples](img1e4.png)

![PINN](img2e4.png)
