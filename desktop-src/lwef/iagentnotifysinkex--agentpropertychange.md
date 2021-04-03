---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e27fe9e2318af0642c2df680af3a279ab57253d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916283"
---
# <a name="iagentnotifysinkexagentpropertychange"></a><span data-ttu-id="b59ac-103">IAgentNotifySinkEx::AgentPropertyChange</span><span class="sxs-lookup"><span data-stu-id="b59ac-103">IAgentNotifySinkEx::AgentPropertyChange</span></span>

<span data-ttu-id="b59ac-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b59ac-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT AgentPropertyChange(
);
```

<span data-ttu-id="b59ac-105">Notifica um aplicativo cliente quando o usuário altera uma configuração de Propriedade do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="b59ac-105">Notifies a client application when the user changes a Microsoft Agent property setting.</span></span>

-   <span data-ttu-id="b59ac-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="b59ac-106">No return value.</span></span>

<span data-ttu-id="b59ac-107">Quando o usuário altera uma configuração de Propriedade do Microsoft Agent na folha de propriedades do Microsoft Agent, o servidor envia esse evento a todos os clientes, a menos que o servidor esteja suspenso no momento.</span><span class="sxs-lookup"><span data-stu-id="b59ac-107">When the user changes a Microsoft Agent property setting in the Microsoft Agent property sheet, the server sends this event to all clients unless the server is currently suspended.</span></span>

## <a name="see-also"></a><span data-ttu-id="b59ac-108">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b59ac-108">See Also</span></span>

[<span data-ttu-id="b59ac-109">**IAgentNotifySinkEx::D efaultCharacterChange**</span><span class="sxs-lookup"><span data-stu-id="b59ac-109">**IAgentNotifySinkEx::DefaultCharacterChange**</span></span>](iagentnotifysinkex--defaultcharacterchange.md)


 

 




