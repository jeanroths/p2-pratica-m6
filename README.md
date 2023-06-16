# Parte prática da prova 2 do módulo 6 de Engenharia de Computação

## Enunciado

Desenvolva um código em Python capaz de utilizar o openCV para a leitura de um vídeo (frame a frame) e, para cada frame, o seu código deve identificar e marcar na imagem os retângulos correspondentes a cada uma das faces encontradas. Ao final do código, um novo vídeo deve ser salvo com a(s) face(s) identificada(s).

Para a detecção das faces, pode-se utilizar a abordagem que quiser (haar cascade, filtro de correlação, YOLO). Não há a necessidade de fazer o fine tuning da detecção. Se o código é capaz de identificar faces corretamente na maior parte do tempo, considera-se como uma aplicação aceitável para esta etapa da prova.

Boa prova =)

## Descrição da solução:

A solução proposta utiliza a biblioteca OpenCV para ler um vídeo frame a frame, identificar e marcar os retângulos correspondentes a cada uma das faces encontradas em cada frame. O código também salva um novo vídeo com as faces identificadas.

Primeiramente importamos as bibliotecas necessárias, depois, abrimos o arquivo de vídeo de entrada especificado em 'videoprova.mp4' usando `cv2.VideoCapture`. Verificamos se o arquivo de vídeo foi aberto corretamente. Se não for possível abrir o arquivo, exibimos uma mensagem de erro e encerramos o programa.
Criamos a estrutura do vídeo de saída usando cv2.VideoWriter. Especificamos o nome e localização do arquivo de saída, o codec a ser utilizado, a taxa de quadros por segundo e as dimensões do vídeo.

Utilizamos o modelo YOLO carregado para realizar a detecção de objetos no frame. Os resultados da detecção são armazenados em `results`. Criamos uma imagem annotated_frame que contém o frame original com as detecções de objeto plotadas. Editamos o frame original adicionando um retângulo usando a função cv2.rectangle. Neste exemplo, um retângulo é desenhado nas coordenadas (100, 100) e (300, 300) com cor vermelha (0, 0, 255) e espessura 5.

Por fim, salvamos o frame editado no vídeo de saída e exibimos o frame editado na tela.

## Comentários:
Oi Murilo, tudo bem? Então, tentei rodar o código no VSCode, mas deu algum problema na minha máquina, ai o Murilo sugeriu de passar pro Colab, então eu tive que codar la, e como funcionou, coloquei assim mesmo.