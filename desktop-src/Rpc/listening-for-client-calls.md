---
title: Escutando chamadas de cliente
description: Depois que o aplicativo de servidor registrou suas interfaces, criou as informações de associação necessárias e registrou seus pontos de extremidade, ele está pronto para começar a escutar chamadas de procedimento remoto de programas cliente.
ms.assetid: ca9d24ed-0acc-45de-bbb2-761c56745a58
keywords:
- Chamada de procedimento remoto RPC, tarefas, escutando chamadas de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f375a4620e301f59d168bf5f7a4dbeedc0fb89f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822931"
---
# <a name="listening-for-client-calls"></a><span data-ttu-id="587c4-104">Escutando chamadas de cliente</span><span class="sxs-lookup"><span data-stu-id="587c4-104">Listening for Client Calls</span></span>

<span data-ttu-id="587c4-105">Depois que o aplicativo de servidor registrou suas interfaces, criou as informações de associação necessárias e registrou seus pontos de extremidade, ele está pronto para começar a escutar chamadas de procedimento remoto de programas cliente.</span><span class="sxs-lookup"><span data-stu-id="587c4-105">After your server application has registered its interfaces, created the necessary binding information, and registered its endpoints, it is ready to begin listening for remote procedure calls from client programs.</span></span>

<span data-ttu-id="587c4-106">Para escutar chamadas de procedimento remoto, o programa do servidor deve chamar [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), conforme mostrado no fragmento de código a seguir:</span><span class="sxs-lookup"><span data-stu-id="587c4-106">To listen for remote procedure calls, your server program must call [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), as shown in the following code fragment:</span></span>


```C++
RPC_STATUS status;
status = RpcServerListen(
    1,
    RPC_C_LISTEN_MAX_CALLS_DEFAULT,
    0);
```



<span data-ttu-id="587c4-107">Um servidor RPC tem um ou mais threads que pegam chamadas de cliente e as entregam às rotinas nas interfaces registradas.</span><span class="sxs-lookup"><span data-stu-id="587c4-107">An RPC Server has one or more threads that pick up client calls and deliver them to the routines in the registered interfaces.</span></span> <span data-ttu-id="587c4-108">O primeiro parâmetro para a função [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) é o número mínimo de threads a serem criados.</span><span class="sxs-lookup"><span data-stu-id="587c4-108">The first parameter to the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function is the minimum number of threads to create.</span></span> <span data-ttu-id="587c4-109">O parâmetro é apenas uma dica; o tempo de execução RPC pode optar por ignorá-lo.</span><span class="sxs-lookup"><span data-stu-id="587c4-109">The parameter is only a hint; the RPC run time may chose to ignore it.</span></span>

<span data-ttu-id="587c4-110">O segundo parâmetro para [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) é o número máximo de chamadas de procedimento remoto simultâneas a serem manipuladas.</span><span class="sxs-lookup"><span data-stu-id="587c4-110">The second parameter to [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) is the maximum number of concurrent remote procedure calls to handle.</span></span> <span data-ttu-id="587c4-111">Se você quiser que seu aplicativo use o valor máximo padrão, passe RPC \_ C \_ escutar \_ Max \_ calls \_ padrão como o valor para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="587c4-111">If you want your application to use the default maximum value, pass RPC\_C\_LISTEN\_MAX\_CALLS\_DEFAULT as the value for this parameter.</span></span>

<span data-ttu-id="587c4-112">A especificação do DCE chama o [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para continuar em execução até receber um sinal para parar.</span><span class="sxs-lookup"><span data-stu-id="587c4-112">The DCE specification calls for [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) to keep running until it receives a signal to stop.</span></span> <span data-ttu-id="587c4-113">Uma extensão da Microsoft para essa função é permitir que ela comece a escutar e retornar imediatamente.</span><span class="sxs-lookup"><span data-stu-id="587c4-113">One Microsoft extension to this function is to enable it to begin listening and return immediately.</span></span> <span data-ttu-id="587c4-114">Se você quiser que seu aplicativo use o comportamento padrão do DCE, defina o terceiro parâmetro como zero.</span><span class="sxs-lookup"><span data-stu-id="587c4-114">If you want your application to use the default DCE behavior, set the third parameter to zero.</span></span> <span data-ttu-id="587c4-115">Consulte [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)e [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="587c4-115">See [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), and [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) for details.</span></span>

 

 




