---
description: Os recursos de cores de dispositivos, como telas e impressoras, podem variar de monocromático a milhares de cores.
ms.assetid: 3d71c24c-77f4-4344-91c3-439052402fae
title: Noções básicas de cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29bcae40ee6771a9c46b892af6e6a8bceb4dcbc6498fb863353d39f92d4c2cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105745"
---
# <a name="color-basics"></a>Noções básicas de cor

Os recursos de cores de dispositivos, como telas e impressoras, podem variar de monocromático a milhares de cores. Como um aplicativo pode precisar gerar saída para dispositivos durante esse intervalo, ele deve estar preparado para lidar com recursos de cores variáveis.

Um aplicativo pode descobrir o número de cores disponíveis para um determinado dispositivo usando a função [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) para recuperar o valor de NUMCOLORS. Esse valor especifica a contagem de cores disponíveis para uso pelo aplicativo. Normalmente, essa contagem corresponde a uma propriedade física do dispositivo de saída, como o número de tintas na impressora ou o número de sinais de cor distintos que o adaptador de vídeo pode transmitir para o monitor.

Embora o valor de NUMCOLORS especifique a contagem de cores, ele não identifica quais são as cores disponíveis. Um aplicativo pode descobrir quais cores estão disponíveis enumerando todas as canetas com o \_ tipo sólido PS. Como o driver de dispositivo que dá suporte a um determinado dispositivo geralmente tem uma gama completa de canetas sólidas e como o sistema requer que as canetas sólidas tenham apenas cores que o dispositivo pode gerar, a enumeração dessas canetas geralmente é equivalente à enumeração das cores. Um aplicativo pode enumerar as canetas usando a função [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) . Para obter um exemplo de código, consulte [enumerando cores](enumerating-colors.md).

Para obter mais informações, consulte estes tópicos:

-   [Valores de cor](color-values.md)
-   [Aproximações de cores e pontilhamento](color-approximations-and-dithering.md)
-   [Cor em bitmaps](color-in-bitmaps.md)
-   [Mistura de cores](color-mixing.md)

 

 



