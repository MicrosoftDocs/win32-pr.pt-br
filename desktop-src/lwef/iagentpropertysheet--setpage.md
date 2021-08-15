---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf67c3ecb10ec5a8372a00e11d356e4b050b50be4a0563d9c4ebeefcd8040f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476786"
---
# <a name="iagentpropertysheetsetpage"></a>IAgentPropertySheet::SetPage

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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
| **"Fala"**    | A página Entrada de Fala. |
| **"Saída"**    | A página Saída.       |
| **"Copyright"** | A página Direitos Autorais.    |



 

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentPropertySheet::GetPage**](iagentpropertysheet--getpage.md)


 

 




