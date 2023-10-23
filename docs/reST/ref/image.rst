import pygame
from pygame.locals import *

# Inicialização do Pygame
pygame.init()

# Definindo as dimensões da tela
largura, altura = 800, 600
tela = pygame.display.set_mode((largura, altura))

# Loop principal
executando = True
while executando:
    for evento in pygame.event.get():
        if evento.type == QUIT:
            executando = False

    # Lógica de desenho de pixel art
    tela.fill((255, 255, 255))  # Preenche a tela com fundo branco
    # Desenha pixels (cores diferentes)
    pygame.draw.rect(tela, (255, 0, 0), (100, 100, 10, 10))  # Pixel vermelho
    pygame.draw.rect(tela, (0, 255, 0), (120, 100, 10, 10))  # Pixel verde
    pygame.draw.rect(tela, (0, 0, 255), (140, 100, 10, 10))  # Pixel azul

    pygame.display.flip()  # Atualiza a tela

# Encerramento do Pygame
pygame.quit()
