# Desafio Técnico Animal Classification Challenge (Zindi Africa)

## Visão Geral
Este projeto é uma solução para um desafio técnico proposto pela [Zindi Africa](https://zindi.africa/competitions/sbtic-animal-classification), onde o objetivo é classificar imagens de zebras e elefantes utilizando técnicas de visão computacional. Para isso, utilizei o modelo **Vision Transformer (VIT)** com diferentes abordagens de fine-tuning, incluindo:

- Fine-tuning da última camada.
- Fine-tuning de múltiplas camadas.

O pipeline inclui leitura e preparação dos dados, treinamento e avaliação do modelo, e geração de predições em novos dados.

---

## Estrutura do Projeto

### 1. **Setup**
Configuração inicial do ambiente, incluindo:
- Importação das bibliotecas necessárias como TensorFlow, PyTorch e bibliotecas auxiliares.
- Configurações de hiperparâmetros, como tamanho do batch, taxa de aprendizado, e número de épocas.

### 2. **Leitura das Imagens**
- Leitura e exploração do conjunto de dados de imagens.
- Implementação de pré-processamento, incluindo:
  - Redimensionamento das imagens.
  - Normalização para padronizar os valores dos pixels.
  - Divisão em conjuntos de treino, validação e teste.

### 3. **Modelo 1 - VIT Fine-tuning (Ultima Camada)**
- Configuração do modelo Vision Transformer (VIT).
- Treinamento focado na última camada do modelo, mantendo as camadas anteriores congeladas para preservar os pesos pré-treinados.
- Monitoramento do desempenho com métricas como acurácia, precisão e F1-Score.

### 4. **Classe do Modelo**
- Implementação de uma classe para abstrair a arquitetura do modelo e permitir maior flexibilidade para experimentações.

### 5. **Treinamento**
- Fine-tuning de diferentes camadas para ajustar o modelo ao conjunto de dados.
- Uso de callbacks como EarlyStopping para evitar overfitting.
- Registro do histórico de treinamento para análise posterior.

### 6. **Avaliação e Deploy**
- Avaliação do modelo em dados de teste com métricas quantitativas e análise qualitativa de predições.
- Exportação do modelo treinado para uso em produção.

### 7. **Modelo 2 - VIT Fine-tuning (Múltiplas Camadas)**
- Abordagem onde várias camadas do modelo VIT foram descongeladas e treinadas.
- Comparativo com o Modelo 1 para identificar ganhos de desempenho.

### 8. **Predição em Dados Novos**
- Implementação de um pipeline para predição em novos dados.
- Análise dos resultados para verificação da generalização do modelo.

---

## Resultados
- O modelo final garantiu a classificação 65 entre os participantes do desafio. [Certificado](https://zindi.africa/users/aurelio/competitions/certificate)

---

## Requisitos do Ambiente
Para reproduzir este projeto, instale as dependências listadas no arquivo `requirements.txt`. As principais incluem:
- TensorFlow
- PyTorch
- Transformers
- NumPy
- Matplotlib

---

## Como Executar
1. Clone o repositório:
   ```bash
   git clone  https://github.com/AurelioGuilherme/VISAO-COMPUTACIONAL.git
   
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Execute o notebook `zebras_elefantes_copia.ipynb` em um ambiente Jupyter.

---

## Contribuições
Sugestões e contribuições são bem-vindas! Por favor, abra uma issue ou envie um pull request para melhorias.

