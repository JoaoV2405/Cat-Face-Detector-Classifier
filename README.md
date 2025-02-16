# 🐱 Cat Face Detector & Classifier

Este projeto detecta e classifica rostos de gatos usando um modelo treinado. Ele funciona no Google Colab e utiliza OpenCV para a detecção e o modelo MobileNetV2 para a classificação.

## 🔹 Como Funciona
1. **Captura de Imagem**
   - Utiliza Imagem carregada.

2. **Detecção de Rosto do Gato**
   - OpenCV detecta a face do gato usando Haar Cascades.
   
![image](https://github.com/user-attachments/assets/a929b971-2a34-41bd-805a-15385f33a221)


3. **Classificação**
   - O modelo de deep learning recebe a face detectada e classifica entre diferentes categorias: Nina, Lucius, Alan ou Morgana

4. **Exibição do Resultado**
   - Desenha um retângulo ao redor da face e exibe o nome da classe junto com a confiança da previsão.

![image](https://github.com/user-attachments/assets/a64fa0e0-8ce7-4986-943c-dd5804007d85)


## 📝 Explicação do Código
Utilizei a rede MobileNetV2 pré-treinada com os pesos da imagenet como modelo de classificação.
O dataset de treino contém fotos de 4 gatos diferentes e utilizei transfer learning para que ela aprendesse a classificar essas 4 classes corretamente.
Temos uma função chamada detect_and_classify, nós recortamos a face detectada pelo cascade, convertemos essa imagem para o formato aceito pelo modelo e passamos a imagem por ele. A classe prevista é então escrita na imagem próximo ao retângulo gerado, assim como a confiança do modelo.



## 📂 Arquivos Principais
- `Cat_colab_webcam.ipynb`: Notebook com todo o código para rodar no Google Colab.

## 🚀 Tecnologias Utilizadas
- **Python**
- **OpenCV** para detecção
- **TensorFlow/Keras** para classificação
- **Google Colab** para execução online

