---
title: Estado de chamada assíncrona
description: Esta página descreve o estado de chamada assíncrona para chamadas RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96331a18b267b2e44072840727c8fd06afd11d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823045"
---
# <a name="asynchronous-call-state"></a><span data-ttu-id="6cde0-103">Estado de chamada assíncrona</span><span class="sxs-lookup"><span data-stu-id="6cde0-103">Asynchronous Call State</span></span>

<span data-ttu-id="6cde0-104">Esta página descreve o estado de chamada assíncrona para chamadas RPC.</span><span class="sxs-lookup"><span data-stu-id="6cde0-104">This page describes the Asynchronous Call State for RPC calls.</span></span>

## <a name="client-behavior"></a><span data-ttu-id="6cde0-105">Comportamento do cliente</span><span class="sxs-lookup"><span data-stu-id="6cde0-105">Client Behavior</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6cde0-106">Estado</span><span class="sxs-lookup"><span data-stu-id="6cde0-106">State</span></span></th>
<th><span data-ttu-id="6cde0-107">Nome do estado</span><span class="sxs-lookup"><span data-stu-id="6cde0-107">State name</span></span></th>
<th><span data-ttu-id="6cde0-108">Ação</span><span class="sxs-lookup"><span data-stu-id="6cde0-108">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6cde0-109">C</span><span class="sxs-lookup"><span data-stu-id="6cde0-109">C</span></span></td>
<td><span data-ttu-id="6cde0-110">Faça a chamada</span><span class="sxs-lookup"><span data-stu-id="6cde0-110">Make the call</span></span></td>
<td><span data-ttu-id="6cde0-111">Tornar o RPC</span><span class="sxs-lookup"><span data-stu-id="6cde0-111">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="6cde0-112">Em caso de sucesso, vá para o estado WComp</span><span class="sxs-lookup"><span data-stu-id="6cde0-112">On success go to state WComp</span></span></li>
<li><span data-ttu-id="6cde0-113">Na exceção, vá para o fim</span><span class="sxs-lookup"><span data-stu-id="6cde0-113">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="6cde0-114">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="6cde0-114">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cde0-115">Podem</span><span class="sxs-lookup"><span data-stu-id="6cde0-115">Can</span></span></td>
<td><span data-ttu-id="6cde0-116">Cancelar a chamada</span><span class="sxs-lookup"><span data-stu-id="6cde0-116">Cancel the call</span></span></td>
<td><span data-ttu-id="6cde0-117">Chame <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>go to WComp</span><span class="sxs-lookup"><span data-stu-id="6cde0-117">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6cde0-118">WComp</span><span class="sxs-lookup"><span data-stu-id="6cde0-118">WComp</span></span></td>
<td><span data-ttu-id="6cde0-119">Aguardar a conclusão</span><span class="sxs-lookup"><span data-stu-id="6cde0-119">Wait for completion</span></span></td>
<td><span data-ttu-id="6cde0-120">Aguarde até que a notificação de notificationCall seja recebida</span><span class="sxs-lookup"><span data-stu-id="6cde0-120">Wait for notificationCall-complete notification should be received</span></span><br/> <span data-ttu-id="6cde0-121">Ir para comp</span><span class="sxs-lookup"><span data-stu-id="6cde0-121">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6cde0-122">Às</span><span class="sxs-lookup"><span data-stu-id="6cde0-122">Comp</span></span></td>
<td><span data-ttu-id="6cde0-123">Completion</span><span class="sxs-lookup"><span data-stu-id="6cde0-123">Completion</span></span></td>
<td><span data-ttu-id="6cde0-124">Emitir <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir para o fim</span><span class="sxs-lookup"><span data-stu-id="6cde0-124">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6cde0-125">End</span><span class="sxs-lookup"><span data-stu-id="6cde0-125">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="server-behavior"></a><span data-ttu-id="6cde0-126">Comportamento do servidor</span><span class="sxs-lookup"><span data-stu-id="6cde0-126">Server Behavior</span></span>



| <span data-ttu-id="6cde0-127">Estado</span><span class="sxs-lookup"><span data-stu-id="6cde0-127">State</span></span> | <span data-ttu-id="6cde0-128">Nome do estado</span><span class="sxs-lookup"><span data-stu-id="6cde0-128">State name</span></span>     | <span data-ttu-id="6cde0-129">Ação</span><span class="sxs-lookup"><span data-stu-id="6cde0-129">Action</span></span>                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cde0-130">D</span><span class="sxs-lookup"><span data-stu-id="6cde0-130">D</span></span>     | <span data-ttu-id="6cde0-131">Dispatch</span><span class="sxs-lookup"><span data-stu-id="6cde0-131">Dispatch</span></span>       | <span data-ttu-id="6cde0-132">A chamada é expedida pelo runtimeProcess RPC</span><span class="sxs-lookup"><span data-stu-id="6cde0-132">The call is dispatched by the RPC runtimeProcess</span></span><br/> <span data-ttu-id="6cde0-133">Ir para comp</span><span class="sxs-lookup"><span data-stu-id="6cde0-133">Go to Comp</span></span><br/> <span data-ttu-id="6cde0-134">Para falhar fatalmente (ao executar no thread RPC): gerar exceção; ir para o fim</span><span class="sxs-lookup"><span data-stu-id="6cde0-134">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="6cde0-135">Para falhar normalmente: Vá para um</span><span class="sxs-lookup"><span data-stu-id="6cde0-135">To fail gracefully: go to A</span></span><br/> |
| <span data-ttu-id="6cde0-136">Um</span><span class="sxs-lookup"><span data-stu-id="6cde0-136">A</span></span>     | <span data-ttu-id="6cde0-137">Anular a chamada</span><span class="sxs-lookup"><span data-stu-id="6cde0-137">Abort the call</span></span> | <span data-ttu-id="6cde0-138">Chamar [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)ir para o fim</span><span class="sxs-lookup"><span data-stu-id="6cde0-138">Call [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Go to End</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="6cde0-139">Às</span><span class="sxs-lookup"><span data-stu-id="6cde0-139">Comp</span></span>  | <span data-ttu-id="6cde0-140">Completion</span><span class="sxs-lookup"><span data-stu-id="6cde0-140">Completion</span></span>     | <span data-ttu-id="6cde0-141">Emitir [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)ir para o fim</span><span class="sxs-lookup"><span data-stu-id="6cde0-141">Issue [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)Go to End</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="6cde0-142">End</span><span class="sxs-lookup"><span data-stu-id="6cde0-142">End</span></span>   |                |                                                                                                                                                                                                                     |



 

 

 





