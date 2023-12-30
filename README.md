## Visão Computacional Aplicada ao Controle do Tráfego Urbano: Detecção, Classificação e Contagem de Veículos

### Projeto

Neste projeto, será utilizado o modelo pré-treinado yolov8n.pt, para detecção de objetos.

*Arquivo de entrada* 

Para teste, utilizaremos um arquivo baixado do portal da
Prefeitura Municipal de Juiz de Fora, com a captura do vídeo
da câmara 16 (http://camerasjf.gctnet.com.br:8880/cameras/?
cam=16), do cruzamento da Avenida Brasil com a Avenida
Rio Branco, do dia 16/10/2023, com início às 10:49:32, com
duração de 60s, no formato mp4, resolução 1920x1080,
Codec H.265, 29,97 fps, 448 kbps.

O arquivo de vídeo é fornecido em um container mkv, que
é um envelope que incorpora múltiplos formatos
multimídia.

Pré-processamento
Convertemos o arquivo de vídeo disponível para o formato
mp4, utilizando o seguinte script:

![image](https://github.com/guiajf/tfcv/assets/152413615/c4944fb6-710d-4955-b595-85d9da992d03)

Implementação

Instalamos o pacote Ultralytics, que contém a classe YOLO:

![image](https://github.com/guiajf/tfcv/assets/152413615/488c668a-c8de-4570-a7f1-ac95bdd69e7e)

Importamos as bibliotecas necessárias:

![image](https://github.com/guiajf/tfcv/assets/152413615/6b7a0544-e151-429e-837c-5f17e43641ab)




