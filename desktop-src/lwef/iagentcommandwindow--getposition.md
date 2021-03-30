---
title: GetPosition IAgentCommandWindow
description: GetPosition IAgentCommandWindow
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8c036d02c210ecb26da5dfde207bfe56afe8a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916358"
---
# <a name="iagentcommandwindowgetposition"></a>IAgentCommandWindow:: GetPosition

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

Recupera a posição da janela de comandos de voz.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Endereço de uma variável que recebe a coordenada de tela da borda esquerda da janela de comandos de voz em pixels, em relação à origem da tela (superior esquerda).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Endereço de uma variável que recebe a coordenada de tela da borda superior da janela de comandos de voz em pixels, em relação à origem da tela (superior esquerda).

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommandWindow::GetSize**](iagentcommandwindow--getsize.md)


 

 




