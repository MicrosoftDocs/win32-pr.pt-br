---
description: Depois que uma fila é confirmada chamando SetupCommitFileQueue, ela começará a processar as operações em fila. Em cada etapa, a fila envia uma notificação para a rotina de retorno de chamada especificada na chamada para SetupCommitFileQueue.
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: Notificações de fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842a3ebc82640789fdb6e730e881d6790a0d642b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756547"
---
# <a name="queue-notifications"></a><span data-ttu-id="bc1bf-104">Notificações de fila</span><span class="sxs-lookup"><span data-stu-id="bc1bf-104">Queue Notifications</span></span>

<span data-ttu-id="bc1bf-105">Depois que uma fila é confirmada chamando [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), ela começará a processar as operações em fila.</span><span class="sxs-lookup"><span data-stu-id="bc1bf-105">After a queue is committed by calling [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), it will begin to process the queued operations.</span></span> <span data-ttu-id="bc1bf-106">Em cada etapa, a fila envia uma notificação para a rotina de retorno de chamada especificada na chamada para **SetupCommitFileQueue**.</span><span class="sxs-lookup"><span data-stu-id="bc1bf-106">At each step, the queue sends a notification to the callback routine specified in the call to **SetupCommitFileQueue**.</span></span>

<span data-ttu-id="bc1bf-107">Veja a seguir a sintaxe que o [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) usa para enviar uma notificação para a rotina de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="bc1bf-107">Following is the syntax that [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) uses to send a notification to the callback routine.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

<span data-ttu-id="bc1bf-108">Os valores de *param1* e *param2* contêm informações adicionais relevantes para a notificação que está sendo enviada para a rotina de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="bc1bf-108">The values of *Param1* and *Param2* contain additional information relevant to the notification being sent to the callback routine.</span></span> <span data-ttu-id="bc1bf-109">Cada notificação, seus valores *param1* e *param2* e como a rotina de retorno de chamada de fila padrão manipula essa notificação, é descrita em detalhes em notificações de [fila de arquivos](file-queue-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="bc1bf-109">Each notification, its *Param1* and *Param2* values, and how the default queue callback routine handles that notification, is described in detail in [File Queue Notifications](file-queue-notifications.md).</span></span>

 

 



