---
title: Parando o aplicativo de servidor
description: Um aplicativo de servidor pode parar de escutar clientes chamando RpcMgmtStopServerListening e RpcServerUnregisterIf ou simplesmente saindo do processo de host.
ms.assetid: 9d310cfb-72ad-448f-a66a-db6ac2478824
keywords:
- Chamada de procedimento remoto RPC, tarefas, parando o aplicativo de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f95ba05588e0575949614e05370f86de78207d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636962"
---
# <a name="stopping-the-server-application"></a><span data-ttu-id="fc571-104">Parando o aplicativo de servidor</span><span class="sxs-lookup"><span data-stu-id="fc571-104">Stopping the Server Application</span></span>

<span data-ttu-id="fc571-105">Um aplicativo de servidor pode parar de escutar clientes chamando [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) e [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif)ou simplesmente saindo do processo de host.</span><span class="sxs-lookup"><span data-stu-id="fc571-105">A server application can stop listening for clients by calling [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif), or by simply exiting the host process.</span></span> <span data-ttu-id="fc571-106">Ambos os métodos são aceitáveis.</span><span class="sxs-lookup"><span data-stu-id="fc571-106">Both methods are acceptable.</span></span> <span data-ttu-id="fc571-107">Se o servidor seguir a primeira abordagem, ele deverá implementar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="fc571-107">If the server follows the first approach, it should implement the following steps:</span></span>

<span data-ttu-id="fc571-108">A função de servidor [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) não retorna ao programa de chamada até que ocorra uma exceção ou até que ocorra uma chamada para [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) .</span><span class="sxs-lookup"><span data-stu-id="fc571-108">The server function [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) does not return to the calling program until an exception occurs or until a call to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) occurs.</span></span> <span data-ttu-id="fc571-109">Por padrão, somente outro thread do servidor tem permissão para interromper o servidor RPC usando **RpcMgmtStopServerListening**.</span><span class="sxs-lookup"><span data-stu-id="fc571-109">By default, only another server thread is allowed to halt the RPC server by using **RpcMgmtStopServerListening**.</span></span> <span data-ttu-id="fc571-110">Os clientes que tentarem interromper o servidor receberão o erro \_ acesso a RPC S \_ \_ negado.</span><span class="sxs-lookup"><span data-stu-id="fc571-110">Clients who try to halt the server will receive the error RPC\_S\_ACCESS\_DENIED.</span></span> <span data-ttu-id="fc571-111">No entanto, é possível configurar o RPC para permitir que alguns ou todos os clientes interrompam o servidor.</span><span class="sxs-lookup"><span data-stu-id="fc571-111">However, it is possible to configure RPC to allow some or all clients to stop the server.</span></span> <span data-ttu-id="fc571-112">Consulte **RpcMgmtStopServerListening** para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="fc571-112">See **RpcMgmtStopServerListening** for details.</span></span>

<span data-ttu-id="fc571-113">Você também pode fazer com que o aplicativo cliente faça uma chamada de procedimento remoto para uma rotina de desligamento no servidor.</span><span class="sxs-lookup"><span data-stu-id="fc571-113">You can also have the client application make a remote procedure call to a shutdown routine on the server.</span></span> <span data-ttu-id="fc571-114">A rotina de desligamento chama [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) e [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif).</span><span class="sxs-lookup"><span data-stu-id="fc571-114">The shutdown routine calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) and [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif).</span></span> <span data-ttu-id="fc571-115">Este exemplo de aplicativo de programa de tutorial usa essa abordagem adicionando uma nova função remota, **desligada**, ao arquivo Hellop. c.</span><span class="sxs-lookup"><span data-stu-id="fc571-115">This tutorial example program application uses this approach by adding a new remote function, **Shutdown**, to the file Hellop.c.</span></span>

<span data-ttu-id="fc571-116">Na função de **desligamento** , o único parâmetro nulo para [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indica que o aplicativo local deve parar de escutar chamadas de procedimento remotas.</span><span class="sxs-lookup"><span data-stu-id="fc571-116">In the **Shutdown** function, the single null parameter to [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening) indicates that the local application should stop listening for remote procedure calls.</span></span> <span data-ttu-id="fc571-117">Os dois parâmetros nulos para [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) são curingas, indicando que todas as interfaces devem ter o registro cancelado.</span><span class="sxs-lookup"><span data-stu-id="fc571-117">The two null parameters to [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) are wildcards, indicating that all interfaces should be unregistered.</span></span> <span data-ttu-id="fc571-118">O parâmetro **false** indica que a interface deve ser removida do registro imediatamente, em vez de esperar que as chamadas pendentes sejam concluídas.</span><span class="sxs-lookup"><span data-stu-id="fc571-118">The **FALSE** parameter indicates that the interface should be removed from the registry immediately, rather than waiting for pending calls to complete.</span></span>


```C++
/* add this function to hellop.c */
void Shutdown(void)
{
    RPC_STATUS status;
 
    status = RpcMgmtStopServerListening(NULL);
 
    if (status) 
    {
       exit(status);
    }
 
    status = RpcServerUnregisterIf(NULL, NULL, FALSE);
 
    if (status) 
    {
       exit(status);
    }
} //end Shutdown
```



 

 




