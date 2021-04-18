---
title: GetPosition IAgentPropertySheet
description: GetPosition IAgentPropertySheet
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff4dcac994901824d7dc37868d7fcfc3f39cefd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789293"
---
# <a name="iagentpropertysheetgetposition"></a>IAgentPropertySheet:: GetPosition

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetPosition(
   long * plLeft,  // address of variable for left edge of property sheet
   long * plTop    // address of variable for top edge of property sheet
);
```

Recupera a posição da janela da folha de propriedades do Microsoft Agent.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plLeft"></span><span id="plleft"></span><span id="PLLEFT"></span>*plLeft*
</dt> <dd>

Endereço de uma variável que recebe a coordenada de tela da borda esquerda da folha de propriedades em pixels, em relação à origem da tela (superior esquerda).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Endereço de uma variável que recebe a coordenada de tela da borda superior da folha de propriedades em pixels, em relação à origem da tela (superior esquerda).

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentPropertySheet::GetSize**](iagentpropertysheet--getsize.md)


 

 




