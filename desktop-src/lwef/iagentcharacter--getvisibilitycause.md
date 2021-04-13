---
title: IAgentCharacter GetVisibilityCause
description: IAgentCharacter GetVisibilityCause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6013385144b82b79a0f17ae6443b094a9d9c8a4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364500"
---
# <a name="iagentcharactergetvisibilitycause"></a><span data-ttu-id="09572-103">IAgentCharacter::GetVisibilityCause</span><span class="sxs-lookup"><span data-stu-id="09572-103">IAgentCharacter::GetVisibilityCause</span></span>

<span data-ttu-id="09572-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="09572-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

<span data-ttu-id="09572-105">Recupera a causa do estado visível do caractere.</span><span class="sxs-lookup"><span data-stu-id="09572-105">Retrieves the cause of the character's visible state.</span></span>

-   <span data-ttu-id="09572-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="09572-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="09572-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span><span class="sxs-lookup"><span data-stu-id="09572-107"><span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*</span></span>
</dt> <dd>

<span data-ttu-id="09572-108">Endereço de uma variável que recebe a causa da alteração do estado da última visibilidade do caractere e será um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="09572-108">Address of a variable that receives the cause of the character's last visibility state change and will be one of the following:</span></span>



| <span data-ttu-id="09572-109">Valor</span><span class="sxs-lookup"><span data-stu-id="09572-109">Value</span></span>                                                                   | <span data-ttu-id="09572-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="09572-110">Description</span></span>                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="09572-111">**const NeverShown curto não assinado** **= 0;**</span><span class="sxs-lookup"><span data-stu-id="09572-111">**const unsigned short** **NeverShown = 0;**</span></span><br/>                 | <span data-ttu-id="09572-112">O caractere não foi mostrado.</span><span class="sxs-lookup"><span data-stu-id="09572-112">Character has not been shown.</span></span>                                                               |
| <span data-ttu-id="09572-113">**const UserHid curto não assinado** **= 1;**</span><span class="sxs-lookup"><span data-stu-id="09572-113">**const unsigned short** **UserHid = 1;**</span></span><br/>                    | <span data-ttu-id="09572-114">O usuário ocultou o caractere com o menu pop-up de ícone da barra de tarefas do caractere ou usando a entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="09572-114">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |
| <span data-ttu-id="09572-115">**const não assinada curto não assinado** **= 2;**</span><span class="sxs-lookup"><span data-stu-id="09572-115">**const unsigned short** **UserShowed = 2;**</span></span><br/>                 | <span data-ttu-id="09572-116">O usuário mostrou o caractere.</span><span class="sxs-lookup"><span data-stu-id="09572-116">User showed the character.</span></span>                                                                  |
| <span data-ttu-id="09572-117">**const ProgramHid curto não assinado** **= 3;**</span><span class="sxs-lookup"><span data-stu-id="09572-117">**const unsigned short** **ProgramHid = 3;**</span></span><br/>                 | <span data-ttu-id="09572-118">O aplicativo ocultou o caractere.</span><span class="sxs-lookup"><span data-stu-id="09572-118">Your application hid the character.</span></span>                                                         |
| <span data-ttu-id="09572-119">**const ProgramShowed curto não assinado** **= 4;**</span><span class="sxs-lookup"><span data-stu-id="09572-119">**const unsigned short** **ProgramShowed = 4;**</span></span><br/>              | <span data-ttu-id="09572-120">Seu aplicativo mostrou o caractere.</span><span class="sxs-lookup"><span data-stu-id="09572-120">Your application showed the character.</span></span>                                                      |
| <span data-ttu-id="09572-121">**const OtherProgramHid curto não assinado** **= 5;**</span><span class="sxs-lookup"><span data-stu-id="09572-121">**const unsigned short** **OtherProgramHid = 5;**</span></span><br/>            | <span data-ttu-id="09572-122">Outro aplicativo ocultou o caractere.</span><span class="sxs-lookup"><span data-stu-id="09572-122">Another application hid the character.</span></span>                                                      |
| <span data-ttu-id="09572-123">**const OtherProgramShowed curto não assinado** **= 6;**</span><span class="sxs-lookup"><span data-stu-id="09572-123">**const unsigned short** **OtherProgramShowed = 6;**</span></span><br/>         | <span data-ttu-id="09572-124">Outro aplicativo mostrou o caractere.</span><span class="sxs-lookup"><span data-stu-id="09572-124">Another application showed the character.</span></span>                                                   |
| <span data-ttu-id="09572-125">**const UserHidViaCharacterMenu curto sem sinal** **= 7**</span><span class="sxs-lookup"><span data-stu-id="09572-125">**const unsigned short** **UserHidViaCharacterMenu = 7**</span></span><br/>     | <span data-ttu-id="09572-126">O usuário ocultou o caractere com o menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="09572-126">User hid the character with the character's pop-up menu.</span></span>                                    |
| <span data-ttu-id="09572-127">**const UserHidViaTaskbarIcon Short sem sinal** **= UserHid**</span><span class="sxs-lookup"><span data-stu-id="09572-127">**const unsigned short** **UserHidViaTaskbarIcon = UserHid**</span></span><br/> | <span data-ttu-id="09572-128">O usuário ocultou o caractere com o menu pop-up de ícone da barra de tarefas do caractere ou usando a entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="09572-128">User hid the character with the character's taskbar icon pop-up menu or using speech input.</span></span> |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="09572-129">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="09572-129">See Also</span></span>

[<span data-ttu-id="09572-130">**IAgentNotifySink:: Visiblestate**</span><span class="sxs-lookup"><span data-stu-id="09572-130">**IAgentNotifySink::VisibleState**</span></span>](iagentnotifysink--visiblestate.md)


 

 





