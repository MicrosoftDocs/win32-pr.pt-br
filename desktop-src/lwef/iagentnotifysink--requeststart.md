---
title: IAgentNotifySink RequestStart
description: IAgentNotifySink RequestStart
ms.assetid: acac2bf8-7472-4952-a984-a29654fb8b0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ced12596114214cf712cef8dbbe81edb5af278
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636942"
---
# <a name="iagentnotifysinkrequeststart"></a><span data-ttu-id="b4158-103">IAgentNotifySink::RequestStart</span><span class="sxs-lookup"><span data-stu-id="b4158-103">IAgentNotifySink::RequestStart</span></span>

<span data-ttu-id="b4158-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b4158-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT RequestStart(
   long dwRequestID  // request ID
);                          
```

<span data-ttu-id="b4158-105">Notifica um aplicativo cliente quando uma solicitação é iniciada.</span><span class="sxs-lookup"><span data-stu-id="b4158-105">Notifies a client application when a request begins.</span></span>

-   <span data-ttu-id="b4158-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="b4158-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="b4158-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span><span class="sxs-lookup"><span data-stu-id="b4158-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span></span>
</dt> <dd>

<span data-ttu-id="b4158-108">Identificador da solicitação iniciada.</span><span class="sxs-lookup"><span data-stu-id="b4158-108">Identifier of the request that started.</span></span>

</dd> </dl>

<span data-ttu-id="b4158-109">Esse evento permite que você acompanhe quando uma solicitação em fila começa a usar sua ID de solicitação.</span><span class="sxs-lookup"><span data-stu-id="b4158-109">This event enables you to track when a queued request begins using its request ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4158-110">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b4158-110">See Also</span></span>

<span data-ttu-id="b4158-111">[**IAgentNotifySink:: RequestComplete**](iagentnotifysink--requestcomplete.md), [**IAgent:: Load**](iagent--load.md), [**IAgentCharacter:: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter:: Hide**](iagentcharacter--hide.md), [**IAgentCharacter:: interrupção**](iagentcharacter--interrupt.md), [**IAgentCharacter:: MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::P reparênteses**](iagentcharacter--prepare.md), [**IAgentCharacter::P Laye**](iagentcharacter--play.md), [**IAgentCharacter:: show**](iagentcharacter--show.md), [**IAgentCharacter:: Fale**](iagentcharacter--speak.md), [**IAgentCharacter:: Wait**](iagentcharacter--wait.md)</span><span class="sxs-lookup"><span data-stu-id="b4158-111">[**IAgentNotifySink::RequestComplete**](iagentnotifysink--requestcomplete.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)</span></span>


 

 




