---
title: Front, Back e outros buffers
description: O OpenGL armazena e manipula dados de pixel em um framebuffer.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL no Windows,buffers
- Framebuffers OpenGL
- buffers de cores OpenGL
- buffers de profundidade OpenGL
- buffers de acúmulo OpenGL
- Buffers de estêncil OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd64f980aad1df8576accd8c37d19521a5368e1fe295393d54c2836f2db8566
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082316"
---
# <a name="front-back-and-other-buffers"></a>Front, Back e outros buffers

O OpenGL armazena e manipula dados de pixel em um framebuffer. O framebuffer consiste em um conjunto de buffers lógicos: cor, profundidade, acúmulo e buffers de estêncil. O buffer de cores em si consiste em um conjunto de buffers lógicos; esse conjunto pode incluir um front-left, um front-right, um back-left, um back-right e um número de buffers auxiliares. Um formato de pixel específico ou implementação do OpenGL pode não fornecer todos esses buffers. Por exemplo, a versão atual da implementação do OpenGL da Microsoft no Windows não dá suporte a imagens estereotipagem, portanto, um formato de pixel não pode ter buffers de cores à esquerda e à direita. Além disso, a versão atual não dá suporte a buffers auxiliares. Para obter mais informações sobre buffers OpenGL e as funções OpenGL que operam neles, consulte o Manual de Referência do *OpenGL* e o Guia de *Programação OpenGL*.

A implementação da Microsoft do OpenGL no Windows dá suporte ao buffer duplo de imagens. Essa é uma técnica na qual um aplicativo desenha pixels para um buffer fora da tela e, em seguida, quando essa imagem está pronta para exibição, copia o conteúdo do buffer fora da tela para um buffer na tela. O buffer duplo permite alterações de imagem suaves, que são especialmente importantes para imagens animadas.

Dois buffers de cores estão disponíveis para aplicativos que usam buffer duplo: um buffer frontal e um buffer de fundo. Por padrão, os comandos de desenho são direcionados para o buffer de fundo (o buffer fora da tela), enquanto o buffer frontal é exibido na tela. Quando o buffer fora da tela estiver pronto para exibição, você chamar [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)e Windows copia o conteúdo do buffer fora da tela para o buffer na tela.

A implementação genérica usa um DIB (bitmap independente de dispositivo) como o buffer de fundo e a tela são exibidas como o buffer frontal. Dispositivos de hardware e seus drivers podem usar abordagens diferentes.

O buffer duplo é uma propriedade de formato de pixel. Para solicitar o buffer duplo para um formato de pixel, de definido o sinalizador PFD DOUBLEBUFFER na estrutura de dados \_ [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) em uma chamada para [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).

A função principal do OpenGL, [**glDrawBuffer,**](gldrawbuffer.md)seleciona buffers para escrita e limpeza.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de buffer](buffer-functions.md)
</dt> </dl>

 

 




