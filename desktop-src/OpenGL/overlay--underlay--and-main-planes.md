---
title: Sobreposição, underlay e planos principais
description: Você pode usar planos de camada de hardware (planos de sobreposição e underlay) em seus aplicativos.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL no Windows, planos de camada de hardware
- planos de camada de hardware OpenGL
- planos de sobreposição OpenGL
- underlay planos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fe68c4bb57d431151c4d879965fcf7496c8615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105771831"
---
# <a name="overlay-underlay-and-main-planes"></a>Sobreposição, underlay e planos principais

Você pode usar planos de camada de hardware (planos de sobreposição e underlay) em seus aplicativos. Com o Windows, os formatos de pixel descrevem as configurações de pixel de um dispositivo de gráficos. Cada formato de pixel descreve a profundidade e outras características dos buffers de cores principais e descreve buffers adicionais (como profundidade, acúmulo, estêncil e auxiliar) que o plano principal usa. Os formatos de pixel agora são estendidos para incluir buffers de sobreposição e Underlay.

Os planos de camada sempre têm um buffer de cores front-Left e também podem incluir buffers de cor frontal e de fundo. Cada plano de camada tem um contexto de renderização específico para renderizar nos buffers de camada. Você não pode usar funções de desenho GDI em planos de camada.

Uma janela gerencia os buffers de cores dos planos de camada da mesma forma que gerencia os buffers de cores do plano principal. Você pode exibir várias janelas com os planos de sobreposição e/ou underlay ao mesmo tempo. Não é possível ter janelas de sobreposição flutuantes livres que podem ser movidas em qualquer janela no plano de desenho principal. Além disso, como ele obscureceria os planos subjacentes em uma janela o tempo todo, não é possível usar planos de pop-up de hardware sem cor transparente.

Cada plano de camada em uma janela tem uma paleta associada. Você pode definir a paleta de um plano de camada de índice de cor, mas a paleta de um plano de cores RGBA é fixa. Você deve perceber a paleta apropriada quando uma janela estiver em primeiro plano. Os planos de camada têm uma cor de pixel transparente ou um índice que permite que os planos de camada subjacentes sejam mostrados.

Você pode copiar o estado de um contexto de renderização para outro contexto de renderização em um plano de camada separado. Você também pode compartilhar listas de exibição entre contextos de renderização em diferentes planos de camada.

As funções a seguir são usadas com os planos de camada:

-   [**wglCopyContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [**wglCreateLayerContext**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [**wglDescribeLayerPlane**](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [**wglGetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [**wglRealizeLayerPalette**](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [**wglSetLayerPaletteEntries**](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [**wglSwapLayerBuffers**](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




