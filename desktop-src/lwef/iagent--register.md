---
title: Registro de IAgent
description: Registro de IAgent
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dd611219fa994f4fe61f7f3e08facf02c9fb73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822680"
---
# <a name="iagentregister"></a><span data-ttu-id="a0f93-103">IAgent:: Register</span><span class="sxs-lookup"><span data-stu-id="a0f93-103">IAgent::Register</span></span>

<span data-ttu-id="a0f93-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a0f93-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

<span data-ttu-id="a0f93-105">Registra um coletor de notificação para o aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="a0f93-105">Registers a notification sink for the client application.</span></span>

-   <span data-ttu-id="a0f93-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a0f93-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a0f93-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="a0f93-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="a0f93-108">Endereço de [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) para sua interface de coletor de notificação.</span><span class="sxs-lookup"><span data-stu-id="a0f93-108">Address of [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) for your notification sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="a0f93-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*</span><span class="sxs-lookup"><span data-stu-id="a0f93-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="a0f93-110">Endereço da ID do coletor de notificação (usado para cancelar o registro do coletor de notificação).</span><span class="sxs-lookup"><span data-stu-id="a0f93-110">Address of notification sink ID (used to unregister the notification sink).</span></span>

</dd> </dl>

<span data-ttu-id="a0f93-111">Você precisa registrar seu coletor de notificações (também conhecido como coletor de notificação ou coletor de eventos) para receber eventos do servidor do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a0f93-111">You need to register your notification sink (also known as a notify sink or event sink) to receive events from the Microsoft Agent server.</span></span>

## <a name="see-also"></a><span data-ttu-id="a0f93-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a0f93-112">See Also</span></span>

[<span data-ttu-id="a0f93-113">**IAgent:: cancelar registro**</span><span class="sxs-lookup"><span data-stu-id="a0f93-113">**IAgent::Unregister**</span></span>](iagent--unregister.md)


 

 




