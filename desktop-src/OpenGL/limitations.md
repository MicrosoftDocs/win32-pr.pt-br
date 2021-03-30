---
title: Limitações
description: Limitações
ms.assetid: 5f41620d-dde0-4e82-92f0-ada9d4acf127
keywords:
- OpenGL no Windows, limitações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478a139326f74c236ca0109fddbbc3d4ffb46e1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635643"
---
# <a name="limitations"></a>Limitações

A implementação genérica tem as seguintes limitações:

-   Imprimindo.

    Você pode imprimir uma imagem OpenGL diretamente em uma impressora usando apenas os metaarquivos. Para obter mais informações, consulte [imprimindo uma imagem OpenGL](printing-an-opengl-image.md).

-   Os elementos gráficos OpenGL e GDI não podem ser misturados em uma janela com buffer duplo.

    Um aplicativo pode desenhar diretamente elementos gráficos OpenGL e GDI em uma janela de buffer único, mas não em uma janela com buffer duplo.

-   Não há paletas de cores de hardware por janela.

    O Windows tem uma paleta de cores de hardware de sistema único, que se aplica à tela inteira. Uma janela OpenGL não pode ter sua própria paleta de hardware, mas pode ter sua própria paleta lógica. Para fazer isso, ele deve se tornar um aplicativo com reconhecimento de paleta. Para obter mais informações, consulte [OpenGL Color Modes e Windows Palette Management](opengl-color-modes-and-windows-palette-management.md).

-   Não há suporte direto para a área de transferência, DDE (Dynamic Data Exchange) ou OLE.

    Uma janela com gráficos OpenGL não dá suporte diretamente a esses recursos do Windows. No entanto, há soluções alternativas para o uso da área de transferência. Para obter mais informações, consulte [copiando uma imagem OpenGL para a área de transferência](copying-an-opengl-image-to-the-clipboard.md).

-   A biblioteca de classes C++ do inventário 2,0 não está incluída.

    A biblioteca de classes de inventário, criada com base no OpenGL, fornece construções de nível superior para programação de gráficos 3-D. Ele não está incluído na versão atual da implementação do OpenGL para Windows da Microsoft.

-   Não há suporte para os seguintes recursos de formato de pixel: imagens estereoscópico, Alpha bitplanes e buffers auxiliares.

    Há, no entanto, suporte para vários buffers auxiliares, incluindo: buffer de estêncil, buffer de acumulação, buffer de fundo (buffer duplo), sobreposição e buffer de plano underlay e buffer de profundidade (eixo z).

 

 




