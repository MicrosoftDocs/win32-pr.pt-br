---
title: Buffers frontal, traseiro e outros
description: O OpenGL armazena e manipula dados de pixel em um framebuffer.
ms.assetid: 4af6a5e4-cc62-49e5-a4d5-e54b1348e8fe
keywords:
- OpenGL no Windows, buffers
- framebuffers OpenGL
- buffers de cores OpenGL
- buffers de profundidade OpenGL
- buffers de acumulação OpenGL
- buffers de estêncil OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea487b73af356853bee2054db292cdfe740bd16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364133"
---
# <a name="front-back-and-other-buffers"></a>Buffers frontal, traseiro e outros

O OpenGL armazena e manipula dados de pixel em um framebuffer. O framebuffer consiste em um conjunto de buffers lógicos: cor, profundidade, acumulação e buffers de estêncil. O buffer de cores em si consiste em um conjunto de buffers lógicos; Esse conjunto pode incluir um front-Left, um front-Right, um back-Left, um back-Right e um número de buffers auxiliares. Um formato de pixel específico ou implementação OpenGL pode não fornecer todos esses buffers. Por exemplo, a versão atual da implementação da Microsoft do OpenGL no Windows não oferece suporte a imagens estereoscópico; portanto, um formato de pixel não pode ter buffers de cores esquerdo e direito. Além disso, a versão atual não oferece suporte a buffers auxiliares. Para obter mais informações sobre buffers OpenGL e as funções OpenGL que operam neles, consulte o *manual de referência OpenGL* e o *Guia de programação OpenGL*.

A implementação da Microsoft do OpenGL no Windows dá suporte ao buffer duplo de imagens. Essa é uma técnica na qual um aplicativo desenha pixels para um buffer fora da tela e, em seguida, quando essa imagem está pronta para exibição, o copia o conteúdo do buffer fora da tela para um buffer na tela. O buffer duplo permite alterações de imagem suaves, que são especialmente importantes para imagens animadas.

Dois buffers de cores estão disponíveis para aplicativos que usam buffer duplo: um buffer frontal e um buffer de fundo. Por padrão, os comandos de desenho são direcionados para o buffer de fundo (o buffer fora da tela), enquanto o buffer frontal é exibido na tela. Quando o buffer fora da tela estiver pronto para exibição, você chamará [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)e o Windows copiará o conteúdo do buffer fora da tela para o buffer na tela.

A implementação genérica usa um DIB (bitmap independente de dispositivo) como o buffer de fundo e a tela são exibidos como o buffer frontal. Os dispositivos de hardware e seus drivers podem usar abordagens diferentes.

O buffer duplo é uma propriedade de formato de pixel. Para solicitar um buffer duplo para um formato de pixel, defina o \_ sinalizador PFD DOUBLEBUFFER na estrutura de dados [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) em uma chamada para [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat).

A função principal OpenGL, [**glDrawBuffer**](gldrawbuffer.md), seleciona buffers para gravação e limpeza.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de buffer](buffer-functions.md)
</dt> </dl>

 

 




