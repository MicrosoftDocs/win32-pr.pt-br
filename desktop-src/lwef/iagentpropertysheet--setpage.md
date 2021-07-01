---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b84f9b9d5f74170644488cc2049376ecf409997
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120741"
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



|                 | Descrição            |
|-----------------|------------------------|
| **Palestra**    | A página de entrada de fala. |
| **Der**    | A página saída.       |
| **Internacionais** | A página de direitos autorais.    |



 

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentPropertySheet:: GetPage**](iagentpropertysheet--getpage.md)


 

 




