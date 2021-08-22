---
title: Sobreposição, subposição e planos principais
description: Você pode usar planos de camada de hardware (planos de sobreposição e de sobreposição) em seus aplicativos.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL em Windows, planos de camada de hardware
- planos de camada de hardware OpenGL
- planos de sobreposição OpenGL
- planos de sobreposição OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b968a0ab028fd0a699e31ad3a3601d7140435e2b36d0188bef46c5dca7cbad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936485"
---
# <a name="overlay-underlay-and-main-planes"></a>Sobreposição, subposição e planos principais

Você pode usar planos de camada de hardware (planos de sobreposição e de sobreposição) em seus aplicativos. Com Windows, os formatos de pixel descrevem as configurações de pixel de um dispositivo gráfico. Cada formato de pixel descreve a profundidade e outras características dos buffers de cores principais e descreve buffers adicionais (como profundidade, acúmulo, estêncil e auxiliar) que o plano principal usa. Os formatos de pixel agora são estendidos para incluir buffers de sobreposição e de sobreposição.

Os planos de camada sempre têm um buffer de cores à frente esquerda e também podem incluir buffers de cores de frente para a direita e para trás. Cada plano de camada tem um contexto de renderização específico para renderizar nos buffers de camada. Não é possível usar funções de desenho GDI em planos de camada.

Uma janela gerencia os buffers de cores dos planos de camada de forma semelhante à maneira como gerencia buffers de cores do plano principal. Você pode exibir várias janelas com planos de sobreposição e/ou de sobreposição ao mesmo tempo. Você não pode ter janelas de sobreposição flutuante livre que podem se mover sobre qualquer janela no plano de desenho principal. Além disso, como ele ocultaria planos subjacentes em uma janela o tempo todo, você não pode usar planos pop-up de hardware que não têm cor transparente.

Cada plano de camada em uma janela tem uma paleta associada. Você pode definir a paleta de um plano de camada de índice de cores, mas a paleta de um plano de cores RGBA é fixa. Você deve perceber a paleta apropriada quando uma janela estiver em primeiro plano. Os planos de camada têm uma cor de pixel transparente ou índice que permite que os planos de camada subjacentes mostrem.

Você pode copiar o estado de um contexto de renderização para outro contexto de renderização em um plano de camada separado. Você também pode compartilhar listas de exibição entre contextos de renderização em diferentes planos de camada.

As seguintes funções são usadas com planos de camada:

-   [**wglCopyContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [**wglCreateLayerContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [**wglDescribeLayerPlane**](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [**wglGetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [**wglRealizeLayerPalette**](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [**wglSetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [**wglSwapLayerBuffers**](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




