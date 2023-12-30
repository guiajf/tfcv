![image](https://github.com/guiajf/tfcv/assets/152413615/37166913-a937-4ca5-98c3-03d4b5f72ee8)


### Projeto

Neste projeto, será utilizado o modelo pré-treinado yolov8n.pt, para detecção de objetos.

*Arquivo de entrada* 

Utilizaremos um arquivo baixado do portal da
Prefeitura Municipal de Juiz de Fora, com a captura do vídeo
da câmara 16 (http://camerasjf.gctnet.com.br:8880/cameras/?
cam=16), do cruzamento da Avenida Brasil com a Avenida
Rio Branco, do dia 16/10/2023, com início às 10:49:32, com
duração de 60s, no formato mp4, resolução 1920x1080,
Codec H.265, 29,97 fps, 448 kbps.

O arquivo de vídeo é fornecido em um container mkv, que
é um envelope que incorpora múltiplos formatos
multimídia.

*Pré-processamento*

Convertemos o arquivo de vídeo disponível para o formato
mp4, utilizando o seguinte script:

![image](https://github.com/guiajf/tfcv/assets/152413615/c4944fb6-710d-4955-b595-85d9da992d03)

*Implementação*

Instalamos o pacote Ultralytics, que contém a classe YOLO:

![image](https://github.com/guiajf/tfcv/assets/152413615/488c668a-c8de-4570-a7f1-ac95bdd69e7e)

Importamos as bibliotecas necessárias:

![image](https://github.com/guiajf/tfcv/assets/152413615/fef6d77b-0d30-4c59-9cf3-3efb667a252b)

Uma variável recebe o arquivo de entrada:

![image](https://github.com/guiajf/tfcv/assets/152413615/440d63ee-f7aa-4056-86b1-1d43e26e4e21)

Criamos um modelo de rede neural
(YOLOv8 é um grupo de modelos de rede neural, criados e treinados com a biblioteca Pytorch, exportados para arquivos com a extensão .pt.):

![image](https://github.com/guiajf/tfcv/assets/152413615/c7b74bdf-3e79-49a1-88f5-785a4b10b271)

Lemos o arquivo de entrada:

![image](https://github.com/guiajf/tfcv/assets/152413615/23d3f61f-e3e7-49e7-900f-1852fd734d63)

Utilizamos a classe VideoWriter do opencv para criar o objeto de saída, no formato mp4:

![image](https://github.com/guiajf/tfcv/assets/152413615/c051bd45-83f6-4e6b-be3a-05127dbe8c6e)

Listamos as classes do dataset COCO (https://cocodataset.org/#home):

![image](https://github.com/guiajf/tfcv/assets/152413615/f5f91a9b-76df-45f0-a284-c213bd573ca0)

Criamos dicionários auxiliares:

![image](https://github.com/guiajf/tfcv/assets/152413615/5e0a83c7-790d-4e73-8622-74047e895071)

Realizamos a leitura dos frames:

![image](https://github.com/guiajf/tfcv/assets/152413615/310603fa-ae84-461d-95c3-a34220e0f3b3)

Ao processar a entrada, o modelo retorna um array de resultados para cada frame:

![image](https://github.com/guiajf/tfcv/assets/152413615/f08e627d-d55e-4415-bd3c-8f14db9a700c)

Mapeamos algumas propriedades da caixa delimitadora:

![image](https://github.com/guiajf/tfcv/assets/152413615/f4a6fb9d-0abb-446a-8522-ca47e9cdf9d9)

Adicionamos rótulos às caixas delimitadoras:

![image](https://github.com/guiajf/tfcv/assets/152413615/362e0bf8-1eb9-449a-981f-40e25180bf0b)

Inserimos no frame a contagem de veículos por tipo:

![image](https://github.com/guiajf/tfcv/assets/152413615/0fe0ca09-ce58-4c27-9ed9-3e6976d4ba88)

Salvamos o arquivo de saída, liberamos os objetos de captura e gravação e fechamos todos os frames:

![image](https://github.com/guiajf/tfcv/assets/152413615/4207157d-15e9-43cb-a3ab-0a83c1372927)

Compactamos o arquivo de saída(ao compactá-lo, reduzimos o tamanho a um terço do original):

![image](https://github.com/guiajf/tfcv/assets/152413615/abf757da-d3db-4947-a1d5-7d29c141fab7)


Exibimos o arquivo de saída:

![image](https://github.com/guiajf/tfcv/assets/152413615/04b71d90-7b5e-49c1-9086-f1be6ef27ae8)






























