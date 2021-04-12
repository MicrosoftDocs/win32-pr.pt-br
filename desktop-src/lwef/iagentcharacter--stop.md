---
title: IAgentCharacter parar
description: IAgentCharacter parar
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356c81996a9410eccb2007dc5261913e30a1b414
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364254"
---
# <a name="iagentcharacterstop"></a><span data-ttu-id="07534-103">IAgentCharacter:: Stop</span><span class="sxs-lookup"><span data-stu-id="07534-103">IAgentCharacter::Stop</span></span>

<span data-ttu-id="07534-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="07534-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

<span data-ttu-id="07534-105">Interrompe a animação especificada (solicitação) e a remove da fila de animação do caractere.</span><span class="sxs-lookup"><span data-stu-id="07534-105">Stops the specified animation (request) and removes it from the character's animation queue.</span></span>

-   <span data-ttu-id="07534-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="07534-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="07534-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="07534-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="07534-108">A ID da solicitação a ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="07534-108">The ID of the request to stop.</span></span>

</dd> </dl>

<span data-ttu-id="07534-109">**Stop** também pode ser usado para interromper qualquer chamada de [**preparação**](iagentcharacter--prepare.md) em fila.</span><span class="sxs-lookup"><span data-stu-id="07534-109">**Stop** can also be used to halt any queued [**Prepare**](iagentcharacter--prepare.md) calls.</span></span>

## <a name="see-also"></a><span data-ttu-id="07534-110">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="07534-110">See Also</span></span>

<span data-ttu-id="07534-111">[**IAgentCharacter::P reparêntese**](iagentcharacter--prepare.md), [ **IAgentCharacter:: stopAll**](iagentcharacter--stopall.md)</span><span class="sxs-lookup"><span data-stu-id="07534-111">[**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::StopAll**](iagentcharacter--stopall.md)</span></span>


 

 




