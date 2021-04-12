---
title: Criando um coletor de notificação
description: Criando um coletor de notificação
ms.assetid: 6a3cc771-1fef-4b79-baa1-c8d050e36d92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481cdd754e545ef87e3c0dc44324d46e48baf044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364413"
---
# <a name="creating-a-notification-sink"></a><span data-ttu-id="7d95a-103">Criando um coletor de notificação</span><span class="sxs-lookup"><span data-stu-id="7d95a-103">Creating a Notification Sink</span></span>

<span data-ttu-id="7d95a-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7d95a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="7d95a-105">Para ser notificado sobre eventos pelo Microsoft Agent, você deve implementar a interface [**IAgentNotifySink**](events.md)ou [**IAgentNotifySinkEx**](iagentnotifysinkex.md) e criar e registrar um objeto desse tipo seguindo as convenções com:</span><span class="sxs-lookup"><span data-stu-id="7d95a-105">To be notified of events by Microsoft Agent, you must implement either the [**IAgentNotifySink**](events.md)or the [**IAgentNotifySinkEx**](iagentnotifysinkex.md) interface, and create and register an object of that type following COM conventions:</span></span>


```
// Create a notification sink

pSinkEx = new AgentNotifySinkEx;

pSinkEx->AddRef();

// And register it with Microsoft Agent

hRes = pAgentEx->Register((IUnknown *)pSinkEx, &lNotifySinkID);
```



<span data-ttu-id="7d95a-106">Lembre-se de cancelar o registro do seu coletor de notificações quando seu aplicativo desligar e liberar as interfaces do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="7d95a-106">Remember to unregister your notification sink when your application shuts down and releases Microsoft Agent's interfaces.</span></span>

 

 




