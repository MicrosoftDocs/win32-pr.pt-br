---
title: IAgentPropertySheet getVisible
description: IAgentPropertySheet getVisible
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcda8be2a3ae3e4084087225e0d7ed79d33621a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292276"
---
# <a name="iagentpropertysheetgetvisible"></a>IAgentPropertySheet:: getVisible

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

Determina se a folha de propriedades do Microsoft Agent está visível ou oculta.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Endereço de uma variável que recebe **true** se a folha de propriedades estiver visível e **false** se estiver oculta.

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentPropertySheet:: setVisible**](iagentpropertysheet--setvisible.md)


 

 




