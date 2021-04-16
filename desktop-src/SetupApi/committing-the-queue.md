---
description: Se a função de retorno de chamada padrão for chamada durante o compromisso de fila, o contexto para ela deverá ser inicializado usando as funções SetupInitDefaultQueueCallback ou SetupInitDefaultQueueCallbackEx.
ms.assetid: e87f8a66-33e5-4065-98ce-2e904c115b38
title: Confirmando a fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ed721c60457a77a168218aa0294bf448889129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753711"
---
# <a name="committing-the-queue"></a><span data-ttu-id="b03aa-103">Confirmando a fila</span><span class="sxs-lookup"><span data-stu-id="b03aa-103">Committing the Queue</span></span>

<span data-ttu-id="b03aa-104">Se a função de retorno de chamada padrão for chamada durante o compromisso de fila, o contexto para ela deverá ser inicializado usando as funções [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) .</span><span class="sxs-lookup"><span data-stu-id="b03aa-104">If the default callback function is going to be called during the queue commitment, the context for it must be initialized using the [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex) functions.</span></span> <span data-ttu-id="b03aa-105">Se você estiver usando uma função de retorno de chamada personalizada que nunca chama a função de retorno de chamada padrão, essa etapa não será necessária.</span><span class="sxs-lookup"><span data-stu-id="b03aa-105">If you are using a custom callback function that never calls the default callback function, this step is not necessary.</span></span>

<span data-ttu-id="b03aa-106">Depois que a fila é criada e a função de retorno de chamada que processará as notificações de fila foi inicializada, você pode chamar [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para confirmar as operações que foram enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="b03aa-106">After the queue is built and the callback function that will process queue notifications has been initialized, you can call [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to commit the operations that have been enqueued.</span></span>

<span data-ttu-id="b03aa-107">O exemplo a seguir usa [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) para confirmar a fila usando a rotina de retorno de chamada padrão.</span><span class="sxs-lookup"><span data-stu-id="b03aa-107">The following example uses [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) to commit the queue using the default callback routine.</span></span>

``` syntax
test = SetupCommitFileQueue (
     OwnerWindow,          //window that will own dialog boxes
                           //created by the callback routine
     MyQueue,              //the queue to commit
  
                           //use the default callback routine
     SetupDefaultQueueCallback,  
  
     Context               //context information that will be 
                           //  used by the callback routine
);
```

<span data-ttu-id="b03aa-108">No exemplo anterior, MyQueue é a fila a ser confirmada, OwnerWindow é a janela que terá qualquer caixa de diálogo criada pela rotina de retorno de chamada padrão, SetupDefaultQueueCallback especifica que a função de retorno de chamada padrão será usada e o *contexto* é um ponteiro para a estrutura retornada pela chamada anterior para [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).</span><span class="sxs-lookup"><span data-stu-id="b03aa-108">In the preceding example, MyQueue is the queue to commit, OwnerWindow is the window that will own any dialog boxes created by the default callback routine, SetupDefaultQueueCallback specifies that the default callback function will be used, and *Context* is a pointer to the structure returned by the previous call to [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback).</span></span>

 

 



