---
description: Uma região de recorte é um dos objetos gráficos que um aplicativo pode selecionar em um DC (contexto de dispositivo).
ms.assetid: d9238ee5-3305-4e85-aef3-2c5c8b74aacd
title: Regiões de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0647d44d82e289b702e9111b62c5a138c8a0fa059428a6173af36f4eeca657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105911"
---
# <a name="clipping-regions"></a>Regiões de recorte

Uma região de recorte é um dos objetos gráficos que um aplicativo pode selecionar em um DC (contexto de dispositivo). Normalmente, é retangular. Alguns contextos de dispositivo fornecem uma região de recorte predefinida ou padrão, enquanto outras não. Por exemplo, se você obter um identificador de contexto de dispositivo da função [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) , o DC conterá uma região de recorte retangular predefinida que corresponde ao retângulo inválido que requer repintura. No entanto, quando você obtém um identificador de contexto de dispositivo chamando a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) com um parâmetro _hWnd_ **nulo** ou chamando a função [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) , o controlador de domínio não contém uma região de recorte padrão. Para obter mais informações sobre contextos de dispositivo retornados pela função **BeginPaint** , consulte [pintando e desenhando](painting-and-drawing.md) . Para obter mais informações sobre contextos de dispositivo retornados pelas funções **CreateDC** e **GetDC** , consulte [contextos de dispositivo](device-contexts.md).

Os aplicativos podem executar uma variedade de operações em regiões de recorte. Algumas dessas operações exigem um identificador que identifica a região e outras não. Por exemplo, um aplicativo pode executar as seguintes operações diretamente na região de recorte de um contexto de dispositivo.

-   Determine se a saída de gráficos aparece dentro das bordas da região passando coordenadas da linha, do arco, do bitmap, do texto ou da forma preenchida correspondentes para a função [**PtVisible**](/windows/desktop/api/Wingdi/nf-wingdi-ptvisible) .
-   Determine se parte da área do cliente intersecciona uma região chamando a função [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) .
-   Mova a região existente por um deslocamento especificado chamando a função [**OffsetClipRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetcliprgn) .
-   Exclua uma parte retangular da área do cliente da região de recorte atual chamando a função [**ExcludeClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-excludecliprect) .
-   Combine uma parte retangular da área do cliente com a região de recorte atual chamando a função [**IntersectClipRect**](/windows/desktop/api/Wingdi/nf-wingdi-intersectcliprect) .

Depois de obter um identificador que identifica a região de recorte, um aplicativo pode executar qualquer operação que seja comum com regiões, como:

-   Combinando uma cópia da região de recorte atual com uma segunda região chamando a função [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) .
-   Compare uma cópia da região de recorte atual com uma segunda região chamando a função [**EqualRgn**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn) .
-   Determine se um ponto está dentro do interior de uma cópia da região de recorte atual chamando a função [**PtInRegion**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion) .

 

 



