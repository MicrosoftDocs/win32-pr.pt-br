---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636186"
---
# <a name="iagentpropertysheetsetpage"></a>IAgentPropertySheet:: SetPage

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

Define a página atual da folha de propriedades do Microsoft Agent.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*
</dt> <dd>

Um BSTR que define a página atual da propriedade. O parâmetro pode ser um dos seguintes.



|                 |                        |
|-----------------|------------------------|
| **Palestra**    | A página de entrada de fala. |
| **Der**    | A página saída.       |
| **Internacionais** | A página de direitos autorais.    |



 

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentPropertySheet:: GetPage**](iagentpropertysheet--getpage.md)


 

 




