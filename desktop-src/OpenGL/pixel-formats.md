---
title: Formatos de pixel
description: Formatos de pixel
ms.assetid: 2e179340-c487-4b72-a22e-078b800af11d
keywords:
- OpenGL no Windows, pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16f9f78edc0cf935fb602de8d88792091588ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105755972"
---
# <a name="pixel-formats"></a>Formatos de pixel

Um *formato de pixel* especifica várias propriedades de uma superfície de desenho OpenGL. Algumas das propriedades especificadas por um formato de pixel são:

-   Se o buffer de pixel é de buffer único ou duplo.
-   Se os dados de pixel estão em um formato RGBA ou de índice de cor.
-   O número de bits usados para armazenar dados de cores.
-   O número de bits usados para o buffer de profundidade (eixo z).
-   O número de bits usados para o buffer de estêncil.
-   O número de planos de sobreposição e Underlay.
-   Várias máscaras de visibilidade.

A implementação da Microsoft do OpenGL para Windows usa a estrutura de dados [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) para transmitir dados de formato de pixel. Os membros da estrutura especificam as propriedades anteriores e várias outras.

Um determinado contexto de dispositivo pode dar suporte A vários formatos de pixel. O Windows identifica os formatos de pixel para os quais um contexto de dispositivo dá suporte com valores de índice baseados em um consecutivos (1, 2, 3, 4 e assim por diante). Um contexto de dispositivo pode ter apenas um formato de pixel atual, escolhido do conjunto de formatos de pixel com suporte.

Cada janela tem seu próprio formato de pixel atual no OpenGL no Windows. Isso significa, por exemplo, que um aplicativo pode exibir simultaneamente o RGBA e o índice de cores OpenGL do Windows, ou janelas OpenGL de buffer único e duplo. Esse recurso de formato de pixel por janela é limitado a janelas OpenGL.

Normalmente, você obtém um contexto de dispositivo, define o formato de pixel do contexto do dispositivo e, em seguida, cria um contexto de renderização OpenGL adequado para esse dispositivo.

> [!Note]  
> Você define o formato de pixel antes de criar um contexto de renderização porque o contexto de renderização herda o formato de pixel do contexto do dispositivo.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções de formato de pixel](pixel-format-functions.md)
</dt> </dl>

 

 




