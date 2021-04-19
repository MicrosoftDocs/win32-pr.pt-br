---
title: IAgentNotifySink ocioso
description: IAgentNotifySink ocioso
ms.assetid: 7770a698-31d9-4f3a-9c7e-858c480b640e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43e060f361499b02bc0a83db697938975c76291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811631"
---
# <a name="iagentnotifysinkidle"></a><span data-ttu-id="d6399-103">IAgentNotifySink:: Idle</span><span class="sxs-lookup"><span data-stu-id="d6399-103">IAgentNotifySink::Idle</span></span>

<span data-ttu-id="d6399-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d6399-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Idle(
   long dwCharID,  // character ID
   long bStart     // start flag
);                          
```

<span data-ttu-id="d6399-105">Notifica um aplicativo cliente quando o estado de **deixar** de um caractere é alterado.</span><span class="sxs-lookup"><span data-stu-id="d6399-105">Notifies a client application when a character's **Idling** state has changed.</span></span>

-   <span data-ttu-id="d6399-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d6399-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="d6399-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="d6399-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="d6399-108">Identificador da solicitação iniciada.</span><span class="sxs-lookup"><span data-stu-id="d6399-108">Identifier of the request that started.</span></span>

</dd> <dt>

<span data-ttu-id="d6399-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bIniciar*</span><span class="sxs-lookup"><span data-stu-id="d6399-109"><span id="bStart"></span><span id="bstart"></span><span id="BSTART"></span>*bStart*</span></span>
</dt> <dd>

<span data-ttu-id="d6399-110">Sinalizador de início.</span><span class="sxs-lookup"><span data-stu-id="d6399-110">Start flag.</span></span> <span data-ttu-id="d6399-111">Esse valor booliano é **true** quando o caractere começa deixar e **false** quando ele para deixar.</span><span class="sxs-lookup"><span data-stu-id="d6399-111">This Boolean value is **True** when the character begins idling and **False** when it stops idling.</span></span>

</dd> </dl>

<span data-ttu-id="d6399-112">Esse evento permite que você acompanhe quando o servidor do Microsoft Agent inicia ou para o processamento ocioso de um caractere.</span><span class="sxs-lookup"><span data-stu-id="d6399-112">This event enables you to track when the Microsoft Agent server starts or stops idle processing for a character.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6399-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d6399-113">See Also</span></span>

<span data-ttu-id="d6399-114">[**IAgentCharacter:: getidlement**](iagentcharacter--getidleon.md), [ **IAgentCharacter:: setidleion**](iagentcharacter--setidleon.md)</span><span class="sxs-lookup"><span data-stu-id="d6399-114">[**IAgentCharacter::GetIdleOn**](iagentcharacter--getidleon.md), [**IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)</span></span>


 

 




