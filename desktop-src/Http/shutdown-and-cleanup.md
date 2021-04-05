---
title: Desligamento e limpeza
description: Para que um aplicativo seja encerrado normalmente, ele deve executar as seguintes operações de limpeza.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf1c59534b73fee21489439c7818c286874185d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005623"
---
# <a name="shutdown-and-cleanup"></a><span data-ttu-id="0bd27-103">Desligamento e limpeza</span><span class="sxs-lookup"><span data-stu-id="0bd27-103">Shutdown and Cleanup</span></span>

<span data-ttu-id="0bd27-104">Para que um aplicativo seja encerrado normalmente, ele deve executar as seguintes operações de limpeza:</span><span class="sxs-lookup"><span data-stu-id="0bd27-104">For an application to terminate gracefully, it must perform the following cleanup operations:</span></span>

-   <span data-ttu-id="0bd27-105">Remova todas as URLs registradas do grupo de URLs chamando a função [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) para cancelar o registro de URLs registradas anteriormente na chamada para [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).</span><span class="sxs-lookup"><span data-stu-id="0bd27-105">Remove all registered URLs from the URL group by calling the [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) function to deregister URLs previously registered in the call to [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).</span></span>
-   <span data-ttu-id="0bd27-106">Feche o grupo de URLs chamando a função [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) .</span><span class="sxs-lookup"><span data-stu-id="0bd27-106">Close the URL Group by calling the [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) function.</span></span> <span data-ttu-id="0bd27-107">Todos os grupos de URLs criados em uma sessão de servidor devem ser fechados antes de fechar a sessão do servidor.</span><span class="sxs-lookup"><span data-stu-id="0bd27-107">All the URL groups created under a server session must be closed before closing the server session.</span></span>
-   <span data-ttu-id="0bd27-108">Feche a sessão de servidor chamando [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).</span><span class="sxs-lookup"><span data-stu-id="0bd27-108">Close the server session by calling [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).</span></span>
-   <span data-ttu-id="0bd27-109">Feche o identificador para a fila de solicitações chamando [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).</span><span class="sxs-lookup"><span data-stu-id="0bd27-109">Close the handle to the request queue by calling [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).</span></span>
-   <span data-ttu-id="0bd27-110">Encerre os recursos criados pela API do servidor HTTP chamando a função [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) com as configurações de sinalizador correspondentes para cada chamada que o aplicativo fez originalmente para o [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span><span class="sxs-lookup"><span data-stu-id="0bd27-110">Terminate the resources created by the HTTP Server API by calling the [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) function with matching flag settings for each call the application originally made to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span> <span data-ttu-id="0bd27-111">Cada uma dessas chamadas encerra todos os recursos criados na chamada para [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span><span class="sxs-lookup"><span data-stu-id="0bd27-111">Each of these calls terminates all resources created in the call to [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).</span></span>

 

 




