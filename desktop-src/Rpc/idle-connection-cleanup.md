---
title: Limpeza de conexão ociosa
description: Por padrão, as conexões no pool de threads não são fechadas até que toda a associação seja desligada.
ms.assetid: e3d6c89b-0ec5-429d-96d9-1396cce10750
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75587781991c2aae86968d90c9da51331d7a29e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822371"
---
# <a name="idle-connection-cleanup"></a><span data-ttu-id="88459-103">Limpeza de conexão ociosa</span><span class="sxs-lookup"><span data-stu-id="88459-103">Idle Connection Cleanup</span></span>

<span data-ttu-id="88459-104">Por padrão, as conexões no pool de threads não são fechadas até que toda a associação seja desligada.</span><span class="sxs-lookup"><span data-stu-id="88459-104">By default, connections in the thread pool are not closed until the whole association is shut down.</span></span> <span data-ttu-id="88459-105">Essa política permite que clientes com um grande número de threads ou identidades de segurança façam chamadas RPC para o servidor de maneira eficiente.</span><span class="sxs-lookup"><span data-stu-id="88459-105">This policy enables clients with a large number of threads or security identities to make RPC calls to the server in an efficient manner.</span></span> <span data-ttu-id="88459-106">A desvantagem é que uma quantidade inordenada de recursos pode ser confirmada para manter essas conexões.</span><span class="sxs-lookup"><span data-stu-id="88459-106">The drawback is that an inordinate amount of resources may be committed to maintaining those connections.</span></span> <span data-ttu-id="88459-107">Para gerenciar o processo, o RPC fornece a função [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) .</span><span class="sxs-lookup"><span data-stu-id="88459-107">To manage the process, RPC provides the [**RpcMgmtEnableIdleCleanup**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtenableidlecleanup) function.</span></span> <span data-ttu-id="88459-108">Essa função habilita a limpeza de conexão ociosa; o cliente verifica periodicamente o pool de conexões e fecha as conexões que não foram usadas recentemente.</span><span class="sxs-lookup"><span data-stu-id="88459-108">This function enables idle connection cleanup; the client periodically scans the connection pool and closes connections that have not been recently used.</span></span> <span data-ttu-id="88459-109">Se a associação tiver mantido identificadores de contexto, a limpeza de conexão ociosa fechará todas as conexões ociosas, mas garantirá que pelo menos uma conexão seja deixada aberta, mesmo se a conexão estiver ociosa (caso contrário, o servidor obterá a execução do identificador de contexto).</span><span class="sxs-lookup"><span data-stu-id="88459-109">If the association has maintained context handles, the idle connection cleanup closes all idle connections, but makes sure at least one connection is left open, even if the connection is idle (otherwise the server gets context handle run downs).</span></span> <span data-ttu-id="88459-110">Se a associação não mantiver identificadores de contexto, a limpeza de conexão ociosa fechará todas as conexões ociosas, mesmo que isso não deixe nenhuma conexão no pool.</span><span class="sxs-lookup"><span data-stu-id="88459-110">If the association has not maintained context handles, idle connection cleanup closes all idle connections, even if doing so leaves no connections in the pool.</span></span>

<span data-ttu-id="88459-111">No Windows XP, o tempo de execução RPC controla o número de conexões abertas em uma associação e ativa automaticamente a limpeza de conexão ociosa se o número de conexões em qualquer associação exceder um determinado limite.</span><span class="sxs-lookup"><span data-stu-id="88459-111">On Windows XP, the RPC run time keeps track of the number of open connections in an association, and automatically turns on idle connection cleanup if the number of connections in any association exceeds a certain threshold.</span></span>

 

 




