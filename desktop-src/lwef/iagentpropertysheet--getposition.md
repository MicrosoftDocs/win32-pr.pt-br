---
title: IAgentPropertySheet GetPosition
description: IAgentPropertySheet GetPosition
ms.assetid: 5d3de366-e48a-4643-81c5-ac4808671763
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74609f2e5f3201be07c425db17456f17e5202e6497b8b137815ae6124335650
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976136"
---
# <a name="iagentpropertysheetgetposition"></a>IAgentPropertySheet::GetPosition

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

Endereço de uma variável que recebe a coordenada de tela da borda esquerda da folha de propriedades em pixels, em relação à origem da tela (superior esquerdo).

</dd> <dt>

<span id="plTop"></span><span id="pltop"></span><span id="PLTOP"></span>*plTop*
</dt> <dd>

Endereço de uma variável que recebe a coordenada de tela da borda superior da folha de propriedades em pixels, em relação à origem da tela (superior esquerdo).

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentPropertySheet::GetSize**](iagentpropertysheet--getsize.md)


 

 




