# 🧠 CP-IOT — Classificação de Vinhos com TensorFlow

## 📋 Descrição
Este projeto tem como objetivo realizar a **classificação de tipos de vinho** (tinto ou branco) utilizando aprendizado de máquina com **TensorFlow e Keras**.  
O modelo foi treinado com um conjunto de dados contendo propriedades químicas dos vinhos, e o objetivo é prever o tipo a partir dessas características.

---

## 🚀 Como rodar o experimento

### 1️⃣ Clonar o repositório
git clone https://github.com/Davi-lima081022/CP-IOT.git
cd CP-IOT

### 2️⃣ Instalar as dependências
Certifique-se de ter o **Python 3.9+** instalado.  
Em seguida, instale as bibliotecas necessárias executando o comando abaixo:

pip install tensorflow numpy pandas scikit-learn matplotlib

Ou, se preferir, crie um arquivo chamado **requirements.txt** com o conteúdo abaixo e rode:
pip install -r requirements.txt

Conteúdo do arquivo `requirements.txt`:
tensorflow
numpy
pandas
scikit-learn
matplotlib

---

## ▶️ Executar o experimento

Abra o arquivo principal do projeto (`vinho_classificacao.ipynb') em:
- **Jupyter Notebook**, ou  
- **Google Colab**, ou  
- **VS Code** (com a extensão Jupyter instalada)

Depois, execute todas as células (ou o script) para treinar o modelo e visualizar os resultados.

---

## 📊 Resultados Obtidos
Após o treinamento, o modelo apresentou os seguintes resultados:

- **Acurácia (Keras):** 0.9722 (~97%)  
- O modelo foi capaz de classificar corretamente os vinhos com alta precisão.  
- As métricas de avaliação mostraram valores equilibrados entre as classes analisadas.  

Relatório de classificação (exemplo):

Classe | Precisão | Recall | F1-score | Suporte
-------|-----------|--------|----------|---------
0 | 1.00 | 1.00 | 1.00 | 12
1 | 0.93 | 1.00 | 0.96 | 14
2 | 1.00 | 0.90 | 0.95 | 10
Acurácia geral | — | — | 0.97 | 36

---

## ⚠️ Aviso sobre o warning do TensorFlow
Durante a execução, pode aparecer o aviso:
WARNING:tensorflow:5 out of the last 133 calls to <function ...> triggered tf.function retracing.
Isso **não é um erro**, apenas um alerta de desempenho.  
Ele ocorre quando o TensorFlow recompila funções repetidamente, mas **não afeta a acurácia nem o resultado final do modelo**.

---

## ⚙️ Tecnologias utilizadas
- **Python**
- **TensorFlow / Keras**
- **Pandas**
- **NumPy**
- **Scikit-learn**
- **Matplotlib**

---

## 📂 Estrutura do Projeto
CP-IOT/
│
├── vinho_classificacao.ipynb     # Notebook principal do projeto
├── README.md                      # Documentação do projeto (este arquivo)

---

Link do vídeo: https://youtu.be/p3s-vH-l6XM?si=jeyxqMhKn0D4K8Oq

## Integrantes: 
Nome:**Davi Alves de Lima**  
RM: **556008**
Nome:**Rodrigo Alcides Bohac Ríos**
RM: **554826**
Nome:**Celina Alcântara do Carmo**
RM:**558090**


