---
description: Depois que todas as operações de arquivo desejadas tiverem sido enfileiradas, a fila deverá ser confirmada. Isso faz com que as operações de arquivo enfileiradas sejam processadas.
ms.assetid: 536f47f5-785e-4a83-a500-c769442e3e68
title: Confirmando uma fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d995f6811dbd19bba9e13f29bc119cdf2f471f74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663252"
---
# <a name="committing-a-queue"></a><span data-ttu-id="eb858-104">Confirmando uma fila</span><span class="sxs-lookup"><span data-stu-id="eb858-104">Committing a Queue</span></span>

<span data-ttu-id="eb858-105">Depois que todas as operações de arquivo desejadas tiverem sido enfileiradas, a fila deverá ser confirmada.</span><span class="sxs-lookup"><span data-stu-id="eb858-105">After all the desired file operations have been queued, the queue must be committed.</span></span> <span data-ttu-id="eb858-106">Isso faz com que as operações de arquivo enfileiradas sejam processadas.</span><span class="sxs-lookup"><span data-stu-id="eb858-106">This causes the enqueued file operations to be processed.</span></span>

<span data-ttu-id="eb858-107">Uma fila de arquivos não pode ser reutilizada após ser confirmada.</span><span class="sxs-lookup"><span data-stu-id="eb858-107">A file queue cannot be reused after it has been committed.</span></span> <span data-ttu-id="eb858-108">A prática recomendada é coletar todas as operações de arquivo necessárias para a fila de arquivos e confirmar a fila apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="eb858-108">The best practice is to collect all the required file operations for the file queue and commit the queue only once.</span></span> <span data-ttu-id="eb858-109">Se o processamento adicional da fila for necessário depois que ela tiver sido confirmada, o identificador da fila deverá ser fechado e uma nova fila de arquivos será criada.</span><span class="sxs-lookup"><span data-stu-id="eb858-109">If additional processing of the queue is required after it has been committed, the handle to the queue should be closed and a new file queue created.</span></span> <span data-ttu-id="eb858-110">Para confirmar a fila de arquivos, chame a função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , especificando uma rotina de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="eb858-110">To commit the file queue, call the [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function, specifying a callback routine.</span></span> <span data-ttu-id="eb858-111">A rotina de retorno de chamada receberá notificações de **SetupCommitFileQueue** conforme as operações de arquivo são processadas.</span><span class="sxs-lookup"><span data-stu-id="eb858-111">The callback routine will receive notifications from **SetupCommitFileQueue** as the file operations are processed.</span></span> <span data-ttu-id="eb858-112">Se você quiser usar a rotina de retorno de chamada de fila padrão, primeiro deverá inicializar o contexto necessário chamando [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span><span class="sxs-lookup"><span data-stu-id="eb858-112">If you want to use the default queue callback routine, you must first initialize the necessary context by calling either [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) or [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).</span></span> <span data-ttu-id="eb858-113">Para obter mais informações sobre a rotina de retorno de chamada de fila padrão, consulte [rotina de retorno de chamada de fila padrão](default-queue-callback-routine.md).</span><span class="sxs-lookup"><span data-stu-id="eb858-113">For more information about the default queue callback routine, see [Default Queue Callback Routine](default-queue-callback-routine.md).</span></span>

> [!Note]  
> <span data-ttu-id="eb858-114">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) deve ser chamado antes que a fila seja fechada.</span><span class="sxs-lookup"><span data-stu-id="eb858-114">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) should be called before the queue is closed.</span></span> <span data-ttu-id="eb858-115">Todas as operações que não forem confirmadas quando [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) for chamado não serão executadas.</span><span class="sxs-lookup"><span data-stu-id="eb858-115">Any operations that are uncommitted when [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) is called will not be performed.</span></span>

 

 

 



