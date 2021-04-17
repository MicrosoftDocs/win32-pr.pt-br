---
description: Se a rotina de retorno de chamada de fila padrão for inicializada e especificada quando SetupCommitFileQueue for chamado, a fila chamará a rotina de retorno de chamada de fila padrão internamente e você não precisará fazer nada mais.
ms.assetid: a976c275-f128-490d-a544-efbfc6fd87f4
title: Chamando a rotina de retorno de chamada de fila padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24449fc1fcd92d8041de6f104092f45925a495b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811276"
---
# <a name="calling-the-default-queue-callback-routine"></a><span data-ttu-id="7764d-103">Chamando a rotina de retorno de chamada de fila padrão</span><span class="sxs-lookup"><span data-stu-id="7764d-103">Calling the Default Queue Callback Routine</span></span>

<span data-ttu-id="7764d-104">Se a rotina de retorno de chamada de fila padrão for inicializada e especificada quando [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) for chamado, a fila chamará a rotina de retorno de chamada de fila padrão internamente e você não precisará fazer nada mais.</span><span class="sxs-lookup"><span data-stu-id="7764d-104">If the default queue callback routine is initialized and specified when [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) is called, the queue calls the default queue callback routine internally and you need do nothing more.</span></span>

<span data-ttu-id="7764d-105">Se você criar uma rotina de retorno de chamada de filtro que dependa da rotina de retorno de chamada de fila padrão para manipular um subconjunto das notificações de fila, a rotina de retorno de chamada de filtro deverá chamar [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitamente.</span><span class="sxs-lookup"><span data-stu-id="7764d-105">If you create a filter callback routine that relies on the default queue callback routine to handle a subset of the queue notifications, your filter callback routine must call [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitly.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7764d-106">Ao chamar [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitamente, você deve passar o ponteiro void retornado por [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span><span class="sxs-lookup"><span data-stu-id="7764d-106">When you call [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitly, you must pass in the void pointer returned by either [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span>

 

> [!Note]  
> <span data-ttu-id="7764d-107">Uma maneira de fazer isso é criar uma estrutura de contexto para sua rotina de retorno de chamada personalizada que inclua como um de seus membros o ponteiro void retornado por [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span><span class="sxs-lookup"><span data-stu-id="7764d-107">One way to do this is to create a context structure for your custom callback routine that includes as one of its members the void pointer returned by [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span>

 

 

 



