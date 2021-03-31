---
title: Limpeza no lado do servidor
description: Limpeza do lado do servidor e RPC (chamada de procedimento remoto).
ms.assetid: 8a48f698-82ae-464b-bdd9-f0245bbc7733
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a66272fc3cca209d6825ac34d5158094ddff39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005777"
---
# <a name="server-side-cleanup"></a><span data-ttu-id="923d4-103">Limpeza no lado do servidor</span><span class="sxs-lookup"><span data-stu-id="923d4-103">Server-side Cleanup</span></span>

<span data-ttu-id="923d4-104">Imagine o seguinte cenário:</span><span class="sxs-lookup"><span data-stu-id="923d4-104">Imagine the following scenario:</span></span>

<span data-ttu-id="923d4-105">Um cliente abre um identificador de contexto e, em seguida, interrompe ou perde a conectividade com o servidor.</span><span class="sxs-lookup"><span data-stu-id="923d4-105">A client opens a context handle, and then either stops or loses connectivity to the server.</span></span> <span data-ttu-id="923d4-106">Como o servidor detecta que o cliente falhou e o identificador de contexto deve ser executado?</span><span class="sxs-lookup"><span data-stu-id="923d4-106">How does the server detect that the client has failed and the context handle should be run down?</span></span> <span data-ttu-id="923d4-107">Há dois subcenários: um é que o cliente é desligado de maneira ordenada.</span><span class="sxs-lookup"><span data-stu-id="923d4-107">There are two subscenarios: one is that the client is shut down in an orderly manner.</span></span> <span data-ttu-id="923d4-108">Nesse caso, ele notifica o servidor de que ele está sendo desligado e o servidor pode ser limpo, incluindo a execução de um contexto.</span><span class="sxs-lookup"><span data-stu-id="923d4-108">In such case, it notifies the server that it is shutting down, and the server can clean up, including performing context run downs.</span></span> <span data-ttu-id="923d4-109">Se o cliente não desligar de maneira ordenada ou não puder notificar o servidor, o servidor usará o Keep Alive para determinar se o cliente ainda está disponível.</span><span class="sxs-lookup"><span data-stu-id="923d4-109">If the client does not shut down in an orderly manner or it cannot notify the server, the server uses keep alives to determine whether the client is still available.</span></span> <span data-ttu-id="923d4-110">No lado do servidor, a função [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="923d4-110">On the server side, the [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) function has no effect.</span></span> <span data-ttu-id="923d4-111">Em vez disso, o servidor usa a configuração global por máquina – Keep Alive, cujo padrão é aproximadamente duas horas.</span><span class="sxs-lookup"><span data-stu-id="923d4-111">Instead, the server uses the global per machine–keep alive setting, which defaults to approximately two hours.</span></span> <span data-ttu-id="923d4-112">Se o cliente não responder à Keep Alive do servidor, a conexão será fechada.</span><span class="sxs-lookup"><span data-stu-id="923d4-112">If the client does not respond to the server's keep alives, the connection is closed.</span></span> <span data-ttu-id="923d4-113">Quando todas as conexões com um determinado processo de cliente são fechadas, o servidor limpa e executa identificadores de contexto pendentes.</span><span class="sxs-lookup"><span data-stu-id="923d4-113">When all connections to a given client process are closed, the server cleans up and runs down outstanding context handles.</span></span>

 

 




