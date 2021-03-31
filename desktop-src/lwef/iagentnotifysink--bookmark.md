---
title: IAgentNotifySink indicador
description: IAgentNotifySink indicador
ms.assetid: 172042af-a524-4ea4-955d-4e3dee079344
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1febedfc962904544a49b8621812d0518026b459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635505"
---
# <a name="iagentnotifysinkbookmark"></a>IAgentNotifySink:: indicador

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

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


 

 




