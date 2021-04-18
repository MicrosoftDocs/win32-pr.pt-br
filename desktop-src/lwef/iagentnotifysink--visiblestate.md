---
title: IAgentNotifySink Visiblestate
description: IAgentNotifySink Visiblestate
ms.assetid: b0346296-74e9-448f-aa6d-a9fb1e645f05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3525c079ecd1b566ac2230f06e3effa1ceb7a694
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764470"
---
# <a name="iagentnotifysinkvisiblestate"></a><span data-ttu-id="03059-103">IAgentNotifySink:: Visiblestate</span><span class="sxs-lookup"><span data-stu-id="03059-103">IAgentNotifySink::VisibleState</span></span>

<span data-ttu-id="03059-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="03059-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT VisibleState(
   long dwCharID,  // character ID
   long bVisible,  // visibility flag
   long dwCause,   // cause of visible state
);                          
```

<span data-ttu-id="03059-105">Notifica um aplicativo cliente quando o estado de visibilidade do caractere é alterado.</span><span class="sxs-lookup"><span data-stu-id="03059-105">Notifies a client application when the visibility state of the character changes.</span></span>

-   <span data-ttu-id="03059-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="03059-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="03059-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="03059-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="03059-108">Identificador do caractere cujo estado de visibilidade é alterado.</span><span class="sxs-lookup"><span data-stu-id="03059-108">Identifier of the character whose visibility state is changed.</span></span>

</dd> <dt>

<span data-ttu-id="03059-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="03059-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="03059-110">Sinalizador de visibilidade.</span><span class="sxs-lookup"><span data-stu-id="03059-110">Visibility flag.</span></span> <span data-ttu-id="03059-111">Esse valor booliano é **true** quando o caractere se torna visível e **false** quando o caractere se torna oculto.</span><span class="sxs-lookup"><span data-stu-id="03059-111">This Boolean value is **True** when character becomes visible and **False** when the character becomes hidden.</span></span>

</dd> <dt>

<span data-ttu-id="03059-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="03059-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="03059-113">Causa da última alteração no estado de visibilidade do caractere.</span><span class="sxs-lookup"><span data-stu-id="03059-113">Cause of last change to the character's visibility state.</span></span> <span data-ttu-id="03059-114">O parâmetro pode ser um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="03059-114">The parameter may be one of the following:</span></span>



| <span data-ttu-id="03059-115">Valor</span><span class="sxs-lookup"><span data-stu-id="03059-115">Value</span></span>                                                                   | <span data-ttu-id="03059-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="03059-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="03059-117">**const NeverShown curto não assinado** **= 0;**</span><span class="sxs-lookup"><span data-stu-id="03059-117">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="03059-118">O caractere não foi mostrado.</span><span class="sxs-lookup"><span data-stu-id="03059-118">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="03059-119">**const UserHid curto não assinado** **= 1;**</span><span class="sxs-lookup"><span data-stu-id="03059-119">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="03059-120">O usuário ocultou o caractere com o menu pop-up de ícone da barra de tarefas do caractere ou com entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="03059-120">User hid the character with the character's taskbar icon pop-up menu or with speech input..</span></span> |
| <span data-ttu-id="03059-121">**const não assinada curto não assinado** **= 2;**</span><span class="sxs-lookup"><span data-stu-id="03059-121">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="03059-122">O usuário mostrou o caractere.</span><span class="sxs-lookup"><span data-stu-id="03059-122">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="03059-123">**const ProgramHid curto não assinado** **= 3;**</span><span class="sxs-lookup"><span data-stu-id="03059-123">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="03059-124">O aplicativo ocultou o caractere.</span><span class="sxs-lookup"><span data-stu-id="03059-124">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="03059-125">**const ProgramShowed curto não assinado** **= 4;**</span><span class="sxs-lookup"><span data-stu-id="03059-125">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="03059-126">Seu aplicativo mostrou o caractere.</span><span class="sxs-lookup"><span data-stu-id="03059-126">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="03059-127">**const OtherProgramHid curto não assinado** **= 5;**</span><span class="sxs-lookup"><span data-stu-id="03059-127">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="03059-128">Outro aplicativo ocultou o caractere.</span><span class="sxs-lookup"><span data-stu-id="03059-128">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="03059-129">**const OtherProgramShowed curto não assinado** **= 6;**</span><span class="sxs-lookup"><span data-stu-id="03059-129">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="03059-130">Outro aplicativo mostrou o caractere.</span><span class="sxs-lookup"><span data-stu-id="03059-130">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="03059-131">**const UserHidViaCharacterMenu curto sem sinal** **= 7**</span><span class="sxs-lookup"><span data-stu-id="03059-131">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="03059-132">O usuário ocultou o caractere com o menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="03059-132">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="03059-133">**const UserHidViaTaskbarIcon Short sem sinal** **= UserHid**</span><span class="sxs-lookup"><span data-stu-id="03059-133">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="03059-134">O usuário ocultou o caractere com o menu pop-up de ícone da barra de tarefas do caractere ou usando a entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="03059-134">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="03059-135">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="03059-135">See Also</span></span>

<span data-ttu-id="03059-136">[**IAgentCharacter:: getVisible**](iagentcharacter--getvisible.md), [ **IAgentCharacter:: GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)</span><span class="sxs-lookup"><span data-stu-id="03059-136">[**IAgentCharacter::GetVisible**](iagentcharacter--getvisible.md), [**IAgentCharacter::GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)</span></span>


 

 





