---
title: IAgentCommandWindow GetPosition
description: IAgentCommandWindow GetPosition
ms.assetid: d85a7a2c-f0ea-4612-aa73-2e44c49e4e18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52571311a87ee0846dcaf515912762069fe3025a25c5a2589770ee9738bb2de7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716096"
---
# <a name="iagentcommandwindowgetposition"></a>IAgentCommandWindow::GetPosition

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of Voice Commands Window
   long * plTop    // address of variable for top edge of Voice Commands Window
);
```

Recupera a posição da janela Comandos de Voz.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Endereço de uma variável que recebe a coordenada de tela da borda esquerda da Janela comandos de voz em pixels, em relação à origem da tela (superior esquerdo).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Endereço de uma variável que recebe a coordenada de tela da borda superior da Janela comandos de voz em pixels, em relação à origem da tela (superior esquerdo).

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommandWindow::GetSize**](iagentcommandwindow--getsize.md)


 

 




