---
title: IAgentPropertySheet GetVisible
description: IAgentPropertySheet GetVisible
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac95d1da3d1c0b4e5bf65c2f5f43c67153cc1d6af934e1814735abb12ed8d00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692298"
---
# <a name="iagentpropertysheetgetvisible"></a>IAgentPropertySheet::GetVisible

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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

Endereço de uma variável que receberá **True se** a folha de propriedades estiver visível e **False** se estiver oculta.

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentPropertySheet::SetVisible**](iagentpropertysheet--setvisible.md)


 

 




