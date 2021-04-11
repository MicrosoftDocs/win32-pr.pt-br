---
title: Descarregando um servidor com identificadores de contexto pendentes
description: Tradicionalmente, o descarregamento de uma DLL que serviços chamadas RPC usando identificadores de contexto, sem antes parar o processo de hospedagem, tem sido problemático.
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1192b013a06def4bb1ee49e08e43b7165c9edfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160334"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a><span data-ttu-id="edc66-103">Descarregando um servidor com identificadores de contexto pendentes</span><span class="sxs-lookup"><span data-stu-id="edc66-103">Unloading a Server with Outstanding Context Handles</span></span>

<span data-ttu-id="edc66-104">Tradicionalmente, o descarregamento de uma DLL que serviços chamadas RPC usando identificadores de contexto, sem antes parar o processo de hospedagem, tem sido problemático.</span><span class="sxs-lookup"><span data-stu-id="edc66-104">Traditionally, unloading a DLL that services RPC calls using context handles, without first stopping the hosting process, has been problematic.</span></span> <span data-ttu-id="edc66-105">Isso ocorre porque a rotina de execução não é mais válida quando a DLL está sendo descarregada.</span><span class="sxs-lookup"><span data-stu-id="edc66-105">This is because the run-down routine is no longer valid when the DLL is being unloaded.</span></span> <span data-ttu-id="edc66-106">Quando um cliente com um identificador de contexto aberto anteriormente falha e o tempo de execução de RPC tenta fechar o identificador de contexto, sua tentativa de chamar o acesso de rotina de execução é violado e o servidor falha.</span><span class="sxs-lookup"><span data-stu-id="edc66-106">When a client with a previously open context handle fails, and the RPC run time tries to close the context handle, its attempt to call the run-down routine access violates, and the server crashes.</span></span>

<span data-ttu-id="edc66-107">A partir do Windows XP, uma nova API chamada [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) foi adicionada.</span><span class="sxs-lookup"><span data-stu-id="edc66-107">Beginning with Windows XP, a new API called [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex) has been added.</span></span> <span data-ttu-id="edc66-108">**RpcServerUnregisterIfEx** fecha identificadores de contexto abertos pela interface que está sendo cancelada no registro; a função [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) não.</span><span class="sxs-lookup"><span data-stu-id="edc66-108">**RpcServerUnregisterIfEx** closes context handles opened by the interface being unregistered; the [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) function does not.</span></span> <span data-ttu-id="edc66-109">O uso de **RpcServerUnregisterIfEx** não é necessário quando todo o processo é desligado, mas é necessário se uma ou mais DLLs que hospedam as rotinas de execução forem descarregadas enquanto houver identificadores de contexto pendentes.</span><span class="sxs-lookup"><span data-stu-id="edc66-109">Using **RpcServerUnregisterIfEx** is not necessary when the entire process shuts down, but it is necessary if one or more DLLs hosting the run-down routines is unloaded while outstanding context handles exist.</span></span>

 

 




