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
# <a name="iagentnotifysinkbookmark"></a><span data-ttu-id="5e77a-103">IAgentNotifySink:: indicador</span><span class="sxs-lookup"><span data-stu-id="5e77a-103">IAgentNotifySink::Bookmark</span></span>

<span data-ttu-id="5e77a-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5e77a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Bookmark(
   long dwBookMarkID  // bookmark ID
);                          
```

<span data-ttu-id="5e77a-105">Notifica um aplicativo cliente quando seu indicador é concluído.</span><span class="sxs-lookup"><span data-stu-id="5e77a-105">Notifies a client application when its bookmark completes.</span></span>

-   <span data-ttu-id="5e77a-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="5e77a-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="5e77a-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*</span><span class="sxs-lookup"><span data-stu-id="5e77a-107"><span id="dwBookMarkID"></span><span id="dwbookmarkid"></span><span id="DWBOOKMARKID"></span>*dwBookMarkID*</span></span>
</dt> <dd>

<span data-ttu-id="5e77a-108">Identificador do indicador que resultou no disparo do evento.</span><span class="sxs-lookup"><span data-stu-id="5e77a-108">Identifier of the bookmark that resulted in triggering the event.</span></span>

</dd> </dl>

<span data-ttu-id="5e77a-109">Quando você inclui marcas de indicador em um método de [**fala**](speak-method.md) , pode controlar quando elas ocorrem com esse evento.</span><span class="sxs-lookup"><span data-stu-id="5e77a-109">When you include bookmark tags in a [**Speak**](speak-method.md) method, you can track when they occur with this event.</span></span>

## <a name="see-also"></a><span data-ttu-id="5e77a-110">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="5e77a-110">See Also</span></span>

<span data-ttu-id="5e77a-111">[**IAgentCharacter:: falar**](iagentcharacter--speak.md), [marcas de saída de fala do Microsoft Agent](microsoft-agent-speech-output-tags.md)</span><span class="sxs-lookup"><span data-stu-id="5e77a-111">[**IAgentCharacter::Speak**](iagentcharacter--speak.md), [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md)</span></span>


 

 




