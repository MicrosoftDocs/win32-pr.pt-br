---
title: Tamanho do IAgentNotifySink
description: Tamanho do IAgentNotifySink
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498750"
---
# <a name="iagentnotifysinksize"></a><span data-ttu-id="cccf5-103">IAgentNotifySink:: tamanho</span><span class="sxs-lookup"><span data-stu-id="cccf5-103">IAgentNotifySink::Size</span></span>

<span data-ttu-id="cccf5-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cccf5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

<span data-ttu-id="cccf5-105">Notifica um aplicativo cliente quando o caractere é redimensionado.</span><span class="sxs-lookup"><span data-stu-id="cccf5-105">Notifies a client application when the character has been resized.</span></span>

-   <span data-ttu-id="cccf5-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="cccf5-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="cccf5-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="cccf5-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="cccf5-108">Identificador do caractere que foi redimensionado.</span><span class="sxs-lookup"><span data-stu-id="cccf5-108">Identifier of the character that has been resized.</span></span>

</dd> <dt>

<span data-ttu-id="cccf5-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span><span class="sxs-lookup"><span data-stu-id="cccf5-109"><span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*</span></span>
</dt> <dd>

<span data-ttu-id="cccf5-110">A largura do quadro de animação do caractere em pixels.</span><span class="sxs-lookup"><span data-stu-id="cccf5-110">The width of the character's animation frame in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="cccf5-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span><span class="sxs-lookup"><span data-stu-id="cccf5-111"><span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*</span></span>
</dt> <dd>

<span data-ttu-id="cccf5-112">A altura do quadro de animação do caractere em pixels.</span><span class="sxs-lookup"><span data-stu-id="cccf5-112">The height of the character's animation frame in pixels.</span></span>

</dd> </dl>

<span data-ttu-id="cccf5-113">Esse evento é enviado a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="cccf5-113">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="cccf5-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cccf5-114">See Also</span></span>

<span data-ttu-id="cccf5-115">[**IAgentCharacter:: GetSize**](iagentcharacter--getsize.md), [ **IAgentCharacter:: SetSize**](iagentcharacter--setsize.md)</span><span class="sxs-lookup"><span data-stu-id="cccf5-115">[**IAgentCharacter::GetSize**](iagentcharacter--getsize.md), [**IAgentCharacter::SetSize**](iagentcharacter--setsize.md)</span></span>


 

 




