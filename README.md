# CP-IOT — Classificação de Vinhos com TensorFlow

## Descrição

Objetivo do Projeto
O objetivo principal deste projeto é aplicar e demonstrar o conhecimento em Redes Neurais e Visão Computacional, explorando e comparando diferentes ferramentas e técnicas de Deep Learning para análise de imagens e vídeos.

---

## Organização do Código

CP-IOT/
│
├── parte_01_redes_neurais          # Contém o código (.ipynb) dos exercícios de Redes Neurais.
├── parte_02_visao_computacional    # Contém o código (.ipynb) do exercício de Visão Computacional.
├── README.md 
│

---

## Link do vídeo: https://youtu.be/p3s-vH-l6XM?si=jeyxqMhKn0D4K8Oq


## Integrantes: 
Nome: **Davi Alves de Lima**  
RM: **556008**

Nome: **Rodrigo Alcides Bohac Ríos**
RM: **554826**

Nome: **Celina Alcântara do Carmo**
RM: **558090**

---

## Parte 01 – Redes Neurais (40%)
Esta parte contém a implementação e análise dos exercícios baseados no arquivo .ipynb da aula, focados em Redes Neurais.

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

## Parte 02 – Visão Computacional (60%)
A Parte 02 é onde exploramos a Visão Computacional aplicando a técnica de Detecção de Objetos para analisar Rótulos de Vinho. O objetivo é identificar e localizar áreas específicas (como nome do fabricante, logotipo e teor alcoólico) em imagens de garrafas.

---

### Ferramentas Utilizadas 
Para cumprir o requisito de utilizar duas ferramentas diferentes, escolhemos:

#### YOLOv8 via Google Colab (.ipynb)

Descrição: Foi utilizado para o treinamento (Fine-Tuning) e inferência do modelo de Detecção de Objetos. Escolhemos o YOLOv8 por ser um modelo de State-of-the-Art conhecido por sua alta velocidade (inferência de 9.1ms) e precisão, ideal para aplicações em tempo real.

#### Roboflow

Descrição: Foi crucial para o gerenciamento e preparação do dataset. Utilizamos o dataset público wine-label-detection (que continha mais de 4.000 rótulos pré-rotulados), o que economizou meses de trabalho, e exportamos os dados no formato otimizado para o YOLO.

---

### Dataset Utilizado

Dataset utilizado : https://universe.roboflow.com/wine-label/wine-label-detection

Classes de Detecção:	Maker-Name, Distinct Logos, AlcoholPercentage, etc.

---

### Configurações e Hiperparâmetros Principais

| Ferramenta/Modelo | Parâmetro | Valor/Descrição |
| :--- | :--- | :--- |
| **YOLOv8** | Épocas (Epochs) | 50 |
| **YOLOv8** | Tamanho da Imagem | 640x640 pixels |
| **YOLOv8** | Modelo Base | `yolov8n.pt` (Nano, para maior velocidade) |
| **Roboflow** | Data Augmentation | Utilizado para aumentar a diversidade do dataset. |

---

### Resultados e Observações sobre Desempenho

Desempenho (Métricas): O modelo YOLOv8 treinado atingiu um mAP50 de aproximadamente 0.614 (ou o valor real) na detecção das classes do rótulo de vinho.

Velocidade: O tempo de inferência obtido foi de 9.1ms por imagem, confirmando a adequação do YOLOv8 para aplicações em tempo real.

Observação Principal: A combinação do Roboflow com o YOLOv8 resultou em um detector de rótulos altamente funcional, capaz de identificar classes específicas mesmo em condições visuais variadas.

---

### Link do Vídeo de Demonstração (Requisito Atendido)
🎥 Demonstração da Detecção de Rótulos de Vinho: https://youtu.be/p3s-vH-l6XM?si=jeyxqMhKn0D4K8Oq