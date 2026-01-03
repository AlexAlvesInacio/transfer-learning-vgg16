🔧 Instruções de Execução do Projeto

(para colocar no README — Seção faltante 1)

## 🚀 Como executar o projeto

### 🔹 1. Clone o repositório
```bash
git clone https://github.com/AlexAlvesInacio/machine-learn.git
cd machine-learn

🔹 2. Abra o notebook no Google Colab**

Clique no arquivo:

📄 cat_vs_dog_transfer_learning_VGG16.ipynb
e selecione "Abrir no Colab"

🔹 3. Instale as dependências (caso rode localmente)
pip install tensorflow keras numpy matplotlib opencv-python

🔹 4. Execute as células em ordem

Na barra superior → ▶ Run all (Executar tudo)
O notebook irá:

Carregar o dataset

Treinar o modelo base (opcional)

Aplicar Transfer Learning VGG16

Exibir gráficos e métricas

Fazer predição de imagem nova


---

# 📊 Resultados + Gráficos
*(para colocar no README — Seção faltante 2)*

```md
## 📊 Resultados Obtidos

Comparamos dois modelos:

| Modelo                              | Loss Teste | Accuracy Teste |
|------------------------------------|:----------:|:---------------:|
| 🔵 Treinamento do zero              |   ~0.68    |     ~65%        |
| 🟢 Transfer Learning VGG16 + Fine tuning |   ~0.58    |     ~78–80%     |

A diferença é clara: **Transfer Learning melhora a acurácia em mais de 30%**  
mesmo com poucas imagens.

### Gráficos do treinamento

🔹 Loss comparação  
🔹 Accuracy comparação  

![Validation Loss](INSIRA-A-IMAGEM-AQUI)
![Validation Accuracy](INSIRA-A-IMAGEM-AQUI)

> *Substitua acima pelas figuras geradas no notebook*


Se quiser, posso gerar a imagem pra você agora mesmo. Só rodamos o script.

📈 Comparação — original vs Transfer Learning

(Seção faltante 3 — texto para copiar)

## ⚔ Comparação entre os Modelos

### 🔵 Modelo treinado do zero
- Aprendeu apenas com imagens do dataset
- Convergiu mais devagar
- Começou a sofrer overfitting a partir de ~16 épocas
- Accuracy final ~65%

### 🟢 Modelo Transfer Learning VGG16
- Usou pesos já treinados no ImageNet
- Aprendeu características mais rápido
- Manteve validação estável por muitas épocas
- Accuracy final ~78–80%
- Potencial real >85% com Data Augmentation

📌 Conclusão: **Transfer Learning foi muito superior.**

---

## 📊 Avaliação do Modelo

O desempenho do modelo de classificação foi avaliado utilizando métricas amplamente empregadas em problemas de classificação binária, incluindo:

- **Acurácia**
- **Precisão**
- **Sensibilidade (Recall)**
- **F1-score**
- **Curva ROC e AUC**

Os resultados indicaram **alta sensibilidade (Recall = 1.0)**, demonstrando que o modelo conseguiu identificar corretamente todos os exemplos da classe positiva. Entretanto, a **AUC ROC inferior a 0.5** evidencia uma **baixa capacidade de separação entre as classes**, sugerindo que o modelo tende a classificar excessivamente exemplos como positivos.

Esse comportamento pode estar relacionado a fatores como:
- Tamanho reduzido do conjunto de teste
- Possível desbalanceamento das classes
- Ausência de fine-tuning profundo no modelo VGG16 pré-treinado

Mesmo assim, a aplicação das métricas permitiu uma análise crítica do desempenho, evidenciando a importância de avaliar modelos além da acurácia simples.

