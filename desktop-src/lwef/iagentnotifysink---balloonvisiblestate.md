---
title: IAgentNotifySink BalloonVisibleState
description: IAgentNotifySink BalloonVisibleState
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2dd63d8eef3a7f1a70af81e13506a7e92ad84f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105793264"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a><span data-ttu-id="5bc37-103">IAgentNotifySink::BalloonVisibleState</span><span class="sxs-lookup"><span data-stu-id="5bc37-103">IAgentNotifySink::BalloonVisibleState</span></span>

<span data-ttu-id="5bc37-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5bc37-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

<span data-ttu-id="5bc37-105">Notifica um aplicativo cliente quando o estado de visibilidade do balão de palavras do caractere é alterado.</span><span class="sxs-lookup"><span data-stu-id="5bc37-105">Notifies a client application when the visibility state of the character's word balloon changes.</span></span>

-   <span data-ttu-id="5bc37-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="5bc37-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="5bc37-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="5bc37-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="5bc37-108">Identificador do caractere cujo estado de visibilidade do balão de palavra foi alterado.</span><span class="sxs-lookup"><span data-stu-id="5bc37-108">Identifier of the character whose word balloon's visibility state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="5bc37-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="5bc37-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="5bc37-110">Sinalizador de visibilidade.</span><span class="sxs-lookup"><span data-stu-id="5bc37-110">Visibility flag.</span></span> <span data-ttu-id="5bc37-111">Esse valor booliano é **true** quando o balão de palavra do caractere se torna visível; e **false** quando ele se torna oculto.</span><span class="sxs-lookup"><span data-stu-id="5bc37-111">This Boolean value is **True** when character's word balloon becomes visible; and **False** when it becomes hidden.</span></span>

</dd> </dl>

<span data-ttu-id="5bc37-112">Esse evento é enviado a todos os clientes do caractere.</span><span class="sxs-lookup"><span data-stu-id="5bc37-112">This event is sent to all clients of the character.</span></span>

 

 




