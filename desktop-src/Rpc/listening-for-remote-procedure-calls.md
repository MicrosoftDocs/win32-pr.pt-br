---
title: Ouvindo chamadas de procedimento remoto
description: Depois que um programa de servidor registra suas informações de associação e anuncia sua presença em um banco de dados de serviço de nome, ele pode começar a escutar o ponto de extremidade para chamadas de procedimento remoto.
ms.assetid: 1c116e44-03a4-4b86-ae37-0b9187981e53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69d9463e0591279377502394541190be685cccd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004804"
---
# <a name="listening-for-remote-procedure-calls"></a><span data-ttu-id="4cfd9-103">Ouvindo chamadas de procedimento remoto</span><span class="sxs-lookup"><span data-stu-id="4cfd9-103">Listening for Remote Procedure Calls</span></span>

<span data-ttu-id="4cfd9-104">Depois que um programa de servidor registra suas informações de associação e anuncia sua presença em um banco de dados de serviço de nome, ele pode começar a escutar o ponto de extremidade para chamadas de procedimento remoto.</span><span class="sxs-lookup"><span data-stu-id="4cfd9-104">After a server program registers its binding information and advertises its presence in a name service database, it can begin listening to the endpoint for remote procedure calls.</span></span> <span data-ttu-id="4cfd9-105">Os programas de servidor chamam a função [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) para monitorar pontos de extremidade para invocações de cliente de procedimentos remotos.</span><span class="sxs-lookup"><span data-stu-id="4cfd9-105">Server programs call the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to monitor endpoints for client invocations of remote procedures.</span></span>

<span data-ttu-id="4cfd9-106">A especificação DCE de [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indica que ele não deve retornar até que uma função no programa de servidor chame [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening).</span><span class="sxs-lookup"><span data-stu-id="4cfd9-106">The DCE specification of [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) indicates that it should not return until a function in the server program calls [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening).</span></span> <span data-ttu-id="4cfd9-107">A implementação RPC da Microsoft do **RpcServerListen** usa dois parâmetros que não aparecem na especificação do DCE: *DontWait* e *MinimumCallThreads*.</span><span class="sxs-lookup"><span data-stu-id="4cfd9-107">The Microsoft RPC implementation of **RpcServerListen** uses two parameters that do not appear in the DCE specification: *DontWait* and *MinimumCallThreads*.</span></span> <span data-ttu-id="4cfd9-108">O programa do servidor pode passar um valor diferente de zero para o parâmetro *DontWait* .</span><span class="sxs-lookup"><span data-stu-id="4cfd9-108">Your server program can pass a nonzero value for the *DontWait* parameter.</span></span> <span data-ttu-id="4cfd9-109">Se tiver, a função **RpcServerListen** retornará imediatamente.</span><span class="sxs-lookup"><span data-stu-id="4cfd9-109">If it does, the **RpcServerListen** function will return immediately.</span></span> <span data-ttu-id="4cfd9-110">Use a rotina [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) para executar a operação de espera geralmente associada a **RpcServerListen**.</span><span class="sxs-lookup"><span data-stu-id="4cfd9-110">Use the [**RpcMgmtWaitServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtwaitserverlisten) routine to perform the wait operation usually associated with **RpcServerListen**.</span></span>

 

 




