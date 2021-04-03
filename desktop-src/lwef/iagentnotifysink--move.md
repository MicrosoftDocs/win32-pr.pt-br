---
title: IAgentNotifySink mover
description: IAgentNotifySink mover
ms.assetid: d1809fdb-df4b-4884-b9e8-2877a814dc9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52563ff3838348b7bf8e6a2bcdfdf20a51c79723
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916576"
---
# <a name="iagentnotifysinkmove"></a><span data-ttu-id="e5ab0-103">IAgentNotifySink:: mover</span><span class="sxs-lookup"><span data-stu-id="e5ab0-103">IAgentNotifySink::Move</span></span>

<span data-ttu-id="e5ab0-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e5ab0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Move(
   long dwCharID,  // character ID
   long x,         // x-coordinate of new location
   long y,         // y-coordinate of new location
   long dwCause    // cause of move state
);                          
```

<span data-ttu-id="e5ab0-105">Notifica um aplicativo cliente quando o caractere é movido.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-105">Notifies a client application when the character has been moved.</span></span>

-   <span data-ttu-id="e5ab0-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="e5ab0-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="e5ab0-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="e5ab0-108">Identificador do caractere que foi movido.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-108">Identifier of the character that has been moved.</span></span>

</dd> <dt>

<span data-ttu-id="e5ab0-109"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="e5ab0-109"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="e5ab0-110">A coordenada x da nova posição em pixels, relativa à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="e5ab0-110">The x-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="e5ab0-111">O local de um caractere é baseado no canto superior esquerdo de seu quadro de animação.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-111">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="e5ab0-112"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="e5ab0-112"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="e5ab0-113">A coordenada y da nova posição em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="e5ab0-113">The y-coordinate of the new position in pixels, relative to the screen origin (upper left).</span></span> <span data-ttu-id="e5ab0-114">O local de um caractere é baseado no canto superior esquerdo de seu quadro de animação.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-114">The location of a character is based on the upper left corner of its animation frame.</span></span>

</dd> <dt>

<span data-ttu-id="e5ab0-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="e5ab0-115"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="e5ab0-116">A causa da movimentação de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-116">The cause of the character move.</span></span> <span data-ttu-id="e5ab0-117">O parâmetro pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="e5ab0-117">The parameter may be one of the following:</span></span>



| <span data-ttu-id="e5ab0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e5ab0-118">Value</span></span>                                                          | <span data-ttu-id="e5ab0-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5ab0-119">Description</span></span>                                                                          |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e5ab0-120">**const NeverMoved curto não assinado** **= 0;**</span><span class="sxs-lookup"><span data-stu-id="e5ab0-120">**const unsigned short** **NeverMoved = 0;**</span></span><br/>        | <span data-ttu-id="e5ab0-121">O caractere não foi movido.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-121">Character has not been moved.</span></span>                                                        |
| <span data-ttu-id="e5ab0-122">**const não assinada curto-** **movida = 1;**</span><span class="sxs-lookup"><span data-stu-id="e5ab0-122">**const unsigned short** **UserMoved = 1;**</span></span><br/>         | <span data-ttu-id="e5ab0-123">O usuário arrastou o caractere.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-123">User dragged the character.</span></span>                                                          |
| <span data-ttu-id="e5ab0-124">**const ProgramMoved curto não assinado** **= 2;**</span><span class="sxs-lookup"><span data-stu-id="e5ab0-124">**const unsigned short** **ProgramMoved = 2;**</span></span><br/>      | <span data-ttu-id="e5ab0-125">Seu aplicativo moveu o caractere.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-125">Your application moved the character.</span></span>                                                |
| <span data-ttu-id="e5ab0-126">**const OtherProgramMoved curto não assinado** **= 3;**</span><span class="sxs-lookup"><span data-stu-id="e5ab0-126">**const unsigned short** **OtherProgramMoved = 3;**</span></span><br/> | <span data-ttu-id="e5ab0-127">Outro aplicativo moveu o caractere.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-127">Another application moved the character.</span></span>                                             |
| <span data-ttu-id="e5ab0-128">**const SystemMoved curto sem sinal** **= 4**</span><span class="sxs-lookup"><span data-stu-id="e5ab0-128">**const unsigned short** **SystemMoved = 4**</span></span><br/>        | <span data-ttu-id="e5ab0-129">O servidor moveu o caractere para mantê-lo na tela após uma alteração de resolução de tela.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-129">The server moved the character to keep it onscreen after a screen resolution change.</span></span> |



 

</dd> </dl>

<span data-ttu-id="e5ab0-130">Esse evento é enviado a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="e5ab0-130">This event is sent to all clients of the character.</span></span>

## <a name="see-also"></a><span data-ttu-id="e5ab0-131">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e5ab0-131">See Also</span></span>

<span data-ttu-id="e5ab0-132">[**IAgentCharacter:: GetMoveCause**](iagentcharacter--getmovecause.md), [ **IAgentCharacter:: MoveTo**](iagentcharacter--moveto.md)</span><span class="sxs-lookup"><span data-stu-id="e5ab0-132">[**IAgentCharacter::GetMoveCause**](iagentcharacter--getmovecause.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md)</span></span>


 

 





