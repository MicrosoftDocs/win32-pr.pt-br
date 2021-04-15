---
description: Incluído com as funções de instalação, há uma rotina de retorno de chamada padrão, SetupDefaultQueueCallback, que você pode usar para processar as notificações retornadas pelo SetupCommitFileQueue.
ms.assetid: c6ba6398-4119-4bdd-b264-1bc645800b03
title: Rotina de retorno de chamada de fila padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fad7b192ca19a652a948f5884a9ae97295de9c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753920"
---
# <a name="default-queue-callback-routine"></a><span data-ttu-id="84e65-103">Rotina de retorno de chamada de fila padrão</span><span class="sxs-lookup"><span data-stu-id="84e65-103">Default Queue Callback Routine</span></span>

<span data-ttu-id="84e65-104">Incluído com as funções de instalação, há uma rotina de retorno de chamada padrão, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), que você pode usar para processar as notificações retornadas pelo [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea).</span><span class="sxs-lookup"><span data-stu-id="84e65-104">Included with the setup functions is a default callback routine, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), that you can use to process notifications returned by [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea).</span></span>

<span data-ttu-id="84e65-105">As seções a seguir discutem o formato da rotina de retorno de chamada de fila padrão, usando a rotina de retorno de chamada de fila padrão com [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)e como criar uma rotina de retorno de chamada de filtro que se baseia na funcionalidade fornecida pela rotina de retorno de chamada de fila padrão.</span><span class="sxs-lookup"><span data-stu-id="84e65-105">The following sections discuss the format of the default queue callback routine, using the default queue callback routine with [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), and how to create a filter callback routine that builds on the functionality provided by the default queue callback routine.</span></span>

-   [<span data-ttu-id="84e65-106">Sobre a rotina de retorno de chamada de fila padrão</span><span class="sxs-lookup"><span data-stu-id="84e65-106">About the Default Queue Callback Routine</span></span>](about-the-default-queue-callback-routine.md)
-   [<span data-ttu-id="84e65-107">Usando a rotina de retorno de chamada de fila padrão</span><span class="sxs-lookup"><span data-stu-id="84e65-107">Using the Default Queue Callback Routine</span></span>](using-the-default-queue-callback-routine.md)
-   [<span data-ttu-id="84e65-108">Referência de rotina de retorno de chamada de fila padrão</span><span class="sxs-lookup"><span data-stu-id="84e65-108">Default Queue Callback Routine Reference</span></span>](default-queue-callback-routine-reference.md)

 

 



