---
title: IAgentNotifySink RequestComplete
description: IAgentNotifySink RequestComplete
ms.assetid: 995bc961-f175-4429-94a4-91962161298b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0265a7111369dec687fd74b9c66c27275a40e164
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292689"
---
# <a name="iagentnotifysinkrequestcomplete"></a><span data-ttu-id="40204-103">IAgentNotifySink::RequestComplete</span><span class="sxs-lookup"><span data-stu-id="40204-103">IAgentNotifySink::RequestComplete</span></span>

<span data-ttu-id="40204-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="40204-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT RequestComplete(
   long dwRequestID,  // request ID
   long hrStatus      // status code
);                          
```

<span data-ttu-id="40204-105">Notifica um aplicativo cliente quando uma solicitação é concluída.</span><span class="sxs-lookup"><span data-stu-id="40204-105">Notifies a client application when a request completes.</span></span>

-   <span data-ttu-id="40204-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="40204-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="40204-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span><span class="sxs-lookup"><span data-stu-id="40204-107"><span id="dwRequestID"></span><span id="dwrequestid"></span><span id="DWREQUESTID"></span>*dwRequestID*</span></span>
</dt> <dd>

<span data-ttu-id="40204-108">Identificador da solicitação iniciada.</span><span class="sxs-lookup"><span data-stu-id="40204-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="40204-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*</span><span class="sxs-lookup"><span data-stu-id="40204-109"><span id="hrStatus"></span><span id="hrstatus"></span><span id="HRSTATUS"></span>*hrStatus*</span></span>
</dt> <dd>

<span data-ttu-id="40204-110">Código de status.</span><span class="sxs-lookup"><span data-stu-id="40204-110">Status code.</span></span> <span data-ttu-id="40204-111">Esse parâmetro retorna o código de status para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="40204-111">This parameter returns the status code for the request.</span></span>

</dd> </dl>

<span data-ttu-id="40204-112">Esse evento permite que você acompanhe quando um método enfileirado é concluído usando sua ID de solicitação.</span><span class="sxs-lookup"><span data-stu-id="40204-112">This event enables you to track when a queued method completes using its request ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="40204-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="40204-113">See Also</span></span>

<span data-ttu-id="40204-114">[**IAgentNotifySink:: RequestStart**](iagentnotifysink--requeststart.md), [**IAgent:: Load**](iagent--load.md), [**IAgentCharacter:: GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter:: Hide**](iagentcharacter--hide.md), [**IAgentCharacter:: interrupção**](iagentcharacter--interrupt.md), [**IAgentCharacter:: MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::P reparênteses**](iagentcharacter--prepare.md), [**IAgentCharacter::P Laye**](iagentcharacter--play.md), [**IAgentCharacter:: show**](iagentcharacter--show.md), [**IAgentCharacter:: Fale**](iagentcharacter--speak.md), [**IAgentCharacter:: Wait**](iagentcharacter--wait.md)</span><span class="sxs-lookup"><span data-stu-id="40204-114">[**IAgentNotifySink::RequestStart**](iagentnotifysink--requeststart.md), [**IAgent::Load**](iagent--load.md), [**IAgentCharacter::GestureAt**](iagentcharacter--gestureat.md), [**IAgentCharacter::Hide**](iagentcharacter--hide.md), [**IAgentCharacter::Interrupt**](iagentcharacter--interrupt.md), [**IAgentCharacter::MoveTo**](iagentcharacter--moveto.md), [**IAgentCharacter::Prepare**](iagentcharacter--prepare.md), [**IAgentCharacter::Play**](iagentcharacter--play.md), [**IAgentCharacter::Show**](iagentcharacter--show.md), [**IAgentCharacter::Speak**](iagentcharacter--speak.md), [**IAgentCharacter::Wait**](iagentcharacter--wait.md)</span></span>


 

 




