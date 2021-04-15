---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb1fe6cdf6f667011eb048625349f6905913a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364071"
---
# <a name="iagentpropertysheetgetpage"></a>IAgentPropertySheet:: GetPage

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

Recupera a página atual da folha de propriedades do Microsoft Agent.

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*
</dt> <dd>

Endereço de uma variável que recebe a página atual da folha de Propriedades (última página exibida se a janela não estiver aberta). O parâmetro pode ser um dos seguintes:



|                 |                        |
|-----------------|------------------------|
| **Palestra**    | A página de entrada de fala. |
| **Der**    | A página saída.       |
| **Internacionais** | A página de direitos autorais.    |



 

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentPropertySheet:: SetPage**](iagentpropertysheet--setpage.md)


 

 




