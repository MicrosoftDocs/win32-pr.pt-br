---
title: IAgentNotifySink indicador
description: IAgentNotifySink indicador
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02562b7cbf42c3445a25edc5071476da1b2d8dc53d80923ad875fddf09e5d31b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477092"
---
# <a name="iagentnotifysinkbookmark"></a>IAgentNotifySink:: indicador

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

Notifica um aplicativo cliente quando seu indicador é concluído.

-   Sem valor de retorno.

<dl> <dt>

<span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*
</dt> <dd>

Identificador do indicador que resultou no disparo do evento.

</dd> </dl>

Quando você inclui marcas de indicador em um método de [**fala**](speak-method.md) , pode controlar quando elas ocorrem com esse evento.

## <a name="see-also"></a>Consulte Também

[**IAgentCharacter:: falar**](iagentcharacter--speak.md), [marcas de saída de fala do Microsoft Agent](microsoft-agent-speech-output-tags.md)


 

 




