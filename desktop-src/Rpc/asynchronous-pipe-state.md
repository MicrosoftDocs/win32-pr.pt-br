---
title: Estado de pipe assíncrono
description: Esta página descreve o estado de pipe assíncrono para chamadas RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8396b08c7ef7b8152457d9426883645fab39bdef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007121"
---
# <a name="asynchronous-pipe-state"></a><span data-ttu-id="ca85c-103">Estado de pipe assíncrono</span><span class="sxs-lookup"><span data-stu-id="ca85c-103">Asynchronous Pipe State</span></span>

<span data-ttu-id="ca85c-104">Esta página descreve o estado de pipe assíncrono para chamadas RPC.</span><span class="sxs-lookup"><span data-stu-id="ca85c-104">This page describes the Asynchronous Pipe State for RPC calls.</span></span>

## <a name="in-pipe"></a><span data-ttu-id="ca85c-105">NO pipe</span><span class="sxs-lookup"><span data-stu-id="ca85c-105">IN Pipe</span></span>

<span data-ttu-id="ca85c-106">Comportamento do cliente</span><span class="sxs-lookup"><span data-stu-id="ca85c-106">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca85c-107">Estado</span><span class="sxs-lookup"><span data-stu-id="ca85c-107">State</span></span></th>
<th><span data-ttu-id="ca85c-108">Nome do Estado</span><span class="sxs-lookup"><span data-stu-id="ca85c-108">State Name</span></span></th>
<th><span data-ttu-id="ca85c-109">Ação</span><span class="sxs-lookup"><span data-stu-id="ca85c-109">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca85c-110">C</span><span class="sxs-lookup"><span data-stu-id="ca85c-110">C</span></span></td>
<td><span data-ttu-id="ca85c-111">Faça a chamada</span><span class="sxs-lookup"><span data-stu-id="ca85c-111">Make the call</span></span></td>
<td><span data-ttu-id="ca85c-112">Tornar o RPC</span><span class="sxs-lookup"><span data-stu-id="ca85c-112">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="ca85c-113">Em ir para o estado de êxito WS</span><span class="sxs-lookup"><span data-stu-id="ca85c-113">On success go to state WS</span></span></li>
<li><span data-ttu-id="ca85c-114">Na exceção, vá para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-114">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="ca85c-115">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-115">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-116">P</span><span class="sxs-lookup"><span data-stu-id="ca85c-116">P</span></span></td>
<td><span data-ttu-id="ca85c-117">Push</span><span class="sxs-lookup"><span data-stu-id="ca85c-117">Push</span></span></td>
<td><span data-ttu-id="ca85c-118">Fazer um envio por push</span><span class="sxs-lookup"><span data-stu-id="ca85c-118">Make a push</span></span>
<ul>
<li><span data-ttu-id="ca85c-119">Em caso de falha, vá para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-119">On failure go to End</span></span></li>
<li><span data-ttu-id="ca85c-120">Em caso de sucesso, vá para WS</span><span class="sxs-lookup"><span data-stu-id="ca85c-120">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="ca85c-121">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-121">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-122">WS</span><span class="sxs-lookup"><span data-stu-id="ca85c-122">WS</span></span></td>
<td><span data-ttu-id="ca85c-123">Aguardar envio</span><span class="sxs-lookup"><span data-stu-id="ca85c-123">Wait for Send</span></span></td>
<td><span data-ttu-id="ca85c-124">Aguardar notificação</span><span class="sxs-lookup"><span data-stu-id="ca85c-124">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="ca85c-125">Em caso de falha ao obter uma notificação, acesse pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-125">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="ca85c-126">Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados precisarem ser enviados, vá para P</span><span class="sxs-lookup"><span data-stu-id="ca85c-126">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="ca85c-127">Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados não precisarem ser enviados, vá para NP</span><span class="sxs-lookup"><span data-stu-id="ca85c-127">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="ca85c-128">Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> de falha for recebida, acesse comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-128">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="ca85c-129">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-129">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-130">NP</span><span class="sxs-lookup"><span data-stu-id="ca85c-130">NP</span></span></td>
<td><span data-ttu-id="ca85c-131">Envio por push nulo</span><span class="sxs-lookup"><span data-stu-id="ca85c-131">Null Push</span></span></td>
<td><span data-ttu-id="ca85c-132">Enviar 0 bytes por push (Push nulo)</span><span class="sxs-lookup"><span data-stu-id="ca85c-132">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="ca85c-133">Em caso de falha, vá para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-133">On failure go to End</span></span></li>
<li><span data-ttu-id="ca85c-134">Em caso de sucesso, vá para WComp</span><span class="sxs-lookup"><span data-stu-id="ca85c-134">On success go to WComp</span></span></li>
</ul>
<span data-ttu-id="ca85c-135">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-135">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-136">Podem</span><span class="sxs-lookup"><span data-stu-id="ca85c-136">Can</span></span></td>
<td><span data-ttu-id="ca85c-137">Cancelar a chamada</span><span class="sxs-lookup"><span data-stu-id="ca85c-137">Cancel the Call</span></span></td>
<td><span data-ttu-id="ca85c-138">Chame <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>go to WComp</span><span class="sxs-lookup"><span data-stu-id="ca85c-138">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-139">WComp</span><span class="sxs-lookup"><span data-stu-id="ca85c-139">WComp</span></span></td>
<td><span data-ttu-id="ca85c-140">Aguardar a conclusão</span><span class="sxs-lookup"><span data-stu-id="ca85c-140">Wait for Completion</span></span></td>
<td><span data-ttu-id="ca85c-141">Aguarde até que a notificação de notificationCall seja recebida.</span><span class="sxs-lookup"><span data-stu-id="ca85c-141">Wait for notificationCall-complete notification should be received.</span></span><br/> <span data-ttu-id="ca85c-142">Ir para comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-142">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-143">Às</span><span class="sxs-lookup"><span data-stu-id="ca85c-143">Comp</span></span></td>
<td><span data-ttu-id="ca85c-144">Completion</span><span class="sxs-lookup"><span data-stu-id="ca85c-144">Completion</span></span></td>
<td><span data-ttu-id="ca85c-145">Emitir <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-145">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-146">End</span><span class="sxs-lookup"><span data-stu-id="ca85c-146">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="ca85c-147">Comportamento do servidor</span><span class="sxs-lookup"><span data-stu-id="ca85c-147">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca85c-148">Estado</span><span class="sxs-lookup"><span data-stu-id="ca85c-148">State</span></span></th>
<th><span data-ttu-id="ca85c-149">Nome do Estado</span><span class="sxs-lookup"><span data-stu-id="ca85c-149">State Name</span></span></th>
<th><span data-ttu-id="ca85c-150">Ação</span><span class="sxs-lookup"><span data-stu-id="ca85c-150">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca85c-151">D</span><span class="sxs-lookup"><span data-stu-id="ca85c-151">D</span></span></td>
<td><span data-ttu-id="ca85c-152">Dispatch</span><span class="sxs-lookup"><span data-stu-id="ca85c-152">Dispatch</span></span></td>
<td><span data-ttu-id="ca85c-153">A chamada é expedida pelo tempo de execução RPC, vá para P</span><span class="sxs-lookup"><span data-stu-id="ca85c-153">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="ca85c-154">Para falhar fatalmente (ao executar no thread RPC): gerar exceção; ir para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-154">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="ca85c-155">Para falhar normalmente: Vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-155">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-156">P</span><span class="sxs-lookup"><span data-stu-id="ca85c-156">P</span></span></td>
<td><span data-ttu-id="ca85c-157">Recepção</span><span class="sxs-lookup"><span data-stu-id="ca85c-157">Pull</span></span></td>
<td><span data-ttu-id="ca85c-158">Fazer um pull</span><span class="sxs-lookup"><span data-stu-id="ca85c-158">Make a pull</span></span>
<ul>
<li><span data-ttu-id="ca85c-159">Em caso de falha, vá para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-159">On failure go to End</span></span></li>
<li><span data-ttu-id="ca85c-160">Em caso de êxito e conclusão síncrona com bytes diferentes de zero lidos, vá para P</span><span class="sxs-lookup"><span data-stu-id="ca85c-160">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="ca85c-161">Em caso de êxito e conclusão síncrona com zero bytes lidos (pull nulo), vá para comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-161">On success and synchronous completion with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="ca85c-162">Em caso de êxito e conclusão assíncrona (ERROR_IO_PENDING é retornado), vá para WP</span><span class="sxs-lookup"><span data-stu-id="ca85c-162">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="ca85c-163">Para falhar: Vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-163">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-164">WP</span><span class="sxs-lookup"><span data-stu-id="ca85c-164">WP</span></span></td>
<td><span data-ttu-id="ca85c-165">Aguardar pull</span><span class="sxs-lookup"><span data-stu-id="ca85c-165">Wait for Pull</span></span></td>
<td><span data-ttu-id="ca85c-166">Aguardar notificação</span><span class="sxs-lookup"><span data-stu-id="ca85c-166">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="ca85c-167">Em caso de falha ao obter uma conclusão, vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-167">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="ca85c-168">Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de falha for recebido, vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-168">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="ca85c-169">Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com bytes diferentes de zero, leia ir para P</span><span class="sxs-lookup"><span data-stu-id="ca85c-169">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="ca85c-170">Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com zero bytes lidos (pull nulo), vá para comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-170">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="ca85c-171">Se uma falha for recebida, vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-171">If a failure is received go to A</span></span></li>
</ul>
<span data-ttu-id="ca85c-172">Para falhar: Vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-172">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-173">Um</span><span class="sxs-lookup"><span data-stu-id="ca85c-173">A</span></span></td>
<td><span data-ttu-id="ca85c-174">Anular a chamada</span><span class="sxs-lookup"><span data-stu-id="ca85c-174">Abort the Call</span></span></td>
<td><span data-ttu-id="ca85c-175">Chamar <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>ir para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-175">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-176">Às</span><span class="sxs-lookup"><span data-stu-id="ca85c-176">Comp</span></span></td>
<td><span data-ttu-id="ca85c-177">Completion</span><span class="sxs-lookup"><span data-stu-id="ca85c-177">Completion</span></span></td>
<td><span data-ttu-id="ca85c-178">Chamar <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-178">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-179">End</span><span class="sxs-lookup"><span data-stu-id="ca85c-179">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a><span data-ttu-id="ca85c-180">SAÍDA de pipe</span><span class="sxs-lookup"><span data-stu-id="ca85c-180">OUT Pipe</span></span>

<span data-ttu-id="ca85c-181">Comportamento do cliente</span><span class="sxs-lookup"><span data-stu-id="ca85c-181">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca85c-182">Estado</span><span class="sxs-lookup"><span data-stu-id="ca85c-182">State</span></span></th>
<th><span data-ttu-id="ca85c-183">Nome do Estado</span><span class="sxs-lookup"><span data-stu-id="ca85c-183">State Name</span></span></th>
<th><span data-ttu-id="ca85c-184">Ação</span><span class="sxs-lookup"><span data-stu-id="ca85c-184">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca85c-185">C</span><span class="sxs-lookup"><span data-stu-id="ca85c-185">C</span></span></td>
<td><span data-ttu-id="ca85c-186">Faça a chamada</span><span class="sxs-lookup"><span data-stu-id="ca85c-186">Make the call</span></span></td>
<td><span data-ttu-id="ca85c-187">Tornar o RPC</span><span class="sxs-lookup"><span data-stu-id="ca85c-187">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="ca85c-188">Em caso de sucesso, vá para P</span><span class="sxs-lookup"><span data-stu-id="ca85c-188">On success go to P</span></span></li>
<li><span data-ttu-id="ca85c-189">Em caso de falha, vá para comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-189">On failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="ca85c-190">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-190">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-191">P</span><span class="sxs-lookup"><span data-stu-id="ca85c-191">P</span></span></td>
<td><span data-ttu-id="ca85c-192">Recepção</span><span class="sxs-lookup"><span data-stu-id="ca85c-192">Pull</span></span></td>
<td><span data-ttu-id="ca85c-193">Fazer um pull</span><span class="sxs-lookup"><span data-stu-id="ca85c-193">Make a pull</span></span>
<ul>
<li><span data-ttu-id="ca85c-194">Em caso de falha, vá para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-194">On failure go to End</span></span></li>
<li><span data-ttu-id="ca85c-195">Em caso de êxito e conclusão síncrona com bytes diferentes de zero lidos, vá para P</span><span class="sxs-lookup"><span data-stu-id="ca85c-195">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="ca85c-196">Em caso de êxito e conclusão síncrona com zero bytes lidos (pull nulo), vá para WComp</span><span class="sxs-lookup"><span data-stu-id="ca85c-196">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="ca85c-197">Em caso de êxito e conclusão assíncrona (ERROR_IO_PENDING é retornado), vá para WP</span><span class="sxs-lookup"><span data-stu-id="ca85c-197">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="ca85c-198">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-198">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-199">WP</span><span class="sxs-lookup"><span data-stu-id="ca85c-199">WP</span></span></td>
<td><span data-ttu-id="ca85c-200">Aguardar pull</span><span class="sxs-lookup"><span data-stu-id="ca85c-200">Wait for Pull</span></span></td>
<td><span data-ttu-id="ca85c-201">Aguardar notificação</span><span class="sxs-lookup"><span data-stu-id="ca85c-201">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="ca85c-202">Em caso de falha ao obter uma conclusão, vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-202">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="ca85c-203">Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de falha for recebida, vá para Can</span><span class="sxs-lookup"><span data-stu-id="ca85c-203">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="ca85c-204">Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com bytes diferentes de zero, leia ir para P</span><span class="sxs-lookup"><span data-stu-id="ca85c-204">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="ca85c-205">Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com zero bytes lidos (pull nulo), vá para comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-205">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="ca85c-206">Se uma falha for recebida, vá pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-206">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="ca85c-207">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-207">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-208">Podem</span><span class="sxs-lookup"><span data-stu-id="ca85c-208">Can</span></span></td>
<td><span data-ttu-id="ca85c-209">Cancelar a chamada</span><span class="sxs-lookup"><span data-stu-id="ca85c-209">Cancel the Call</span></span></td>
<td><span data-ttu-id="ca85c-210">Chame <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>go to WComp</span><span class="sxs-lookup"><span data-stu-id="ca85c-210">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-211">WComp</span><span class="sxs-lookup"><span data-stu-id="ca85c-211">WComp</span></span></td>
<td><span data-ttu-id="ca85c-212">Aguardar a conclusão</span><span class="sxs-lookup"><span data-stu-id="ca85c-212">Wait for Completion</span></span></td>
<td><span data-ttu-id="ca85c-213">Aguarde a notificação.</span><span class="sxs-lookup"><span data-stu-id="ca85c-213">Wait for notification.</span></span> <span data-ttu-id="ca85c-214">A notificação de conclusão de chamada deve ser recebida.</span><span class="sxs-lookup"><span data-stu-id="ca85c-214">Call-complete notification should be received.</span></span><br/> <span data-ttu-id="ca85c-215">Ir para comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-215">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-216">Às</span><span class="sxs-lookup"><span data-stu-id="ca85c-216">Comp</span></span></td>
<td><span data-ttu-id="ca85c-217">Completion</span><span class="sxs-lookup"><span data-stu-id="ca85c-217">Completion</span></span></td>
<td><span data-ttu-id="ca85c-218">Emitir <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-218">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-219">End</span><span class="sxs-lookup"><span data-stu-id="ca85c-219">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="ca85c-220">Comportamento do servidor</span><span class="sxs-lookup"><span data-stu-id="ca85c-220">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca85c-221">Estado</span><span class="sxs-lookup"><span data-stu-id="ca85c-221">State</span></span></th>
<th><span data-ttu-id="ca85c-222">Nome do Estado</span><span class="sxs-lookup"><span data-stu-id="ca85c-222">State Name</span></span></th>
<th><span data-ttu-id="ca85c-223">Ação</span><span class="sxs-lookup"><span data-stu-id="ca85c-223">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca85c-224">D</span><span class="sxs-lookup"><span data-stu-id="ca85c-224">D</span></span></td>
<td><span data-ttu-id="ca85c-225">Dispatch</span><span class="sxs-lookup"><span data-stu-id="ca85c-225">Dispatch</span></span></td>
<td><span data-ttu-id="ca85c-226">A chamada é expedida pelo tempo de execução RPC, vá para P</span><span class="sxs-lookup"><span data-stu-id="ca85c-226">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="ca85c-227">Para falhar fatalmente (ao executar no thread RPC): gerar exceção; ir para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-227">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="ca85c-228">Para falhar normalmente: Vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-228">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-229">P</span><span class="sxs-lookup"><span data-stu-id="ca85c-229">P</span></span></td>
<td><span data-ttu-id="ca85c-230">Push</span><span class="sxs-lookup"><span data-stu-id="ca85c-230">Push</span></span></td>
<td><span data-ttu-id="ca85c-231">Fazer um envio por push</span><span class="sxs-lookup"><span data-stu-id="ca85c-231">Make a push</span></span>
<ul>
<li><span data-ttu-id="ca85c-232">Em caso de sucesso, vá para WP</span><span class="sxs-lookup"><span data-stu-id="ca85c-232">On success go to WP</span></span></li>
<li><span data-ttu-id="ca85c-233">Em caso de falha, vá para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-233">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="ca85c-234">Para falhar: Vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-234">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-235">WP</span><span class="sxs-lookup"><span data-stu-id="ca85c-235">WP</span></span></td>
<td><span data-ttu-id="ca85c-236">Aguardar envio por push</span><span class="sxs-lookup"><span data-stu-id="ca85c-236">Wait for Push</span></span></td>
<td><span data-ttu-id="ca85c-237">Aguardar notificação</span><span class="sxs-lookup"><span data-stu-id="ca85c-237">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="ca85c-238">Em caso de falha ao obter uma conclusão, vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-238">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="ca85c-239">Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados precisarem ser enviados, vá para P</span><span class="sxs-lookup"><span data-stu-id="ca85c-239">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="ca85c-240">Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados não precisarem ser enviados, vá para NP</span><span class="sxs-lookup"><span data-stu-id="ca85c-240">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="ca85c-241">Se uma falha for recebida, go comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-241">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="ca85c-242">Para falhar: Vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-242">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-243">NP</span><span class="sxs-lookup"><span data-stu-id="ca85c-243">NP</span></span></td>
<td><span data-ttu-id="ca85c-244">Envio por push nulo</span><span class="sxs-lookup"><span data-stu-id="ca85c-244">Null Push</span></span></td>
<td><span data-ttu-id="ca85c-245">Enviar 0 bytes por push</span><span class="sxs-lookup"><span data-stu-id="ca85c-245">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="ca85c-246">em caso de sucesso, vá para o WNP</span><span class="sxs-lookup"><span data-stu-id="ca85c-246">on success go to WNP</span></span></li>
<li><span data-ttu-id="ca85c-247">em caso de falha, vá para comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-247">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="ca85c-248">Para falhar: Vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-248">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-249">WNP</span><span class="sxs-lookup"><span data-stu-id="ca85c-249">WNP</span></span></td>
<td><span data-ttu-id="ca85c-250">Aguardar envio por push nulo</span><span class="sxs-lookup"><span data-stu-id="ca85c-250">Wait for Null Push</span></span></td>
<td><span data-ttu-id="ca85c-251">Aguardar notificação</span><span class="sxs-lookup"><span data-stu-id="ca85c-251">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="ca85c-252">Em caso de falha ao obter uma conclusão, vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-252">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="ca85c-253">Se uma falha for recebida, go comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-253">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="ca85c-254">Se um sucesso for recebido, acesse comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-254">If a success is received go Comp</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-255">Um</span><span class="sxs-lookup"><span data-stu-id="ca85c-255">A</span></span></td>
<td><span data-ttu-id="ca85c-256">Anular a chamada</span><span class="sxs-lookup"><span data-stu-id="ca85c-256">Abort the Call</span></span></td>
<td><span data-ttu-id="ca85c-257">Chamar <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; ir para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-257">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-258">Às</span><span class="sxs-lookup"><span data-stu-id="ca85c-258">Comp</span></span></td>
<td><span data-ttu-id="ca85c-259">Completion</span><span class="sxs-lookup"><span data-stu-id="ca85c-259">Completion</span></span></td>
<td><span data-ttu-id="ca85c-260">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; ir para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-260">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-261">End</span><span class="sxs-lookup"><span data-stu-id="ca85c-261">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a><span data-ttu-id="ca85c-262">Pipe de saída</span><span class="sxs-lookup"><span data-stu-id="ca85c-262">IN-OUT Pipe</span></span>

<span data-ttu-id="ca85c-263">Comportamento do cliente</span><span class="sxs-lookup"><span data-stu-id="ca85c-263">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca85c-264">Estado</span><span class="sxs-lookup"><span data-stu-id="ca85c-264">State</span></span></th>
<th><span data-ttu-id="ca85c-265">Nome do Estado</span><span class="sxs-lookup"><span data-stu-id="ca85c-265">State Name</span></span></th>
<th><span data-ttu-id="ca85c-266">Ação</span><span class="sxs-lookup"><span data-stu-id="ca85c-266">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca85c-267">C</span><span class="sxs-lookup"><span data-stu-id="ca85c-267">C</span></span></td>
<td><span data-ttu-id="ca85c-268">Faça a chamada</span><span class="sxs-lookup"><span data-stu-id="ca85c-268">Make the call</span></span></td>
<td><span data-ttu-id="ca85c-269">Tornar o RPC</span><span class="sxs-lookup"><span data-stu-id="ca85c-269">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="ca85c-270">Em caso de sucesso, vá para WS</span><span class="sxs-lookup"><span data-stu-id="ca85c-270">On success go to WS</span></span></li>
<li><span data-ttu-id="ca85c-271">Na exceção, vá para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-271">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="ca85c-272">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-272">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-273">PS</span><span class="sxs-lookup"><span data-stu-id="ca85c-273">PS</span></span></td>
<td><span data-ttu-id="ca85c-274">Push</span><span class="sxs-lookup"><span data-stu-id="ca85c-274">Push</span></span></td>
<td><span data-ttu-id="ca85c-275">Fazer um envio por push</span><span class="sxs-lookup"><span data-stu-id="ca85c-275">Make a push</span></span>
<ul>
<li><span data-ttu-id="ca85c-276">Em caso de falha, vá para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-276">On failure go to End</span></span></li>
<li><span data-ttu-id="ca85c-277">Em caso de sucesso, vá para WS</span><span class="sxs-lookup"><span data-stu-id="ca85c-277">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="ca85c-278">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-278">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-279">WS</span><span class="sxs-lookup"><span data-stu-id="ca85c-279">WS</span></span></td>
<td><span data-ttu-id="ca85c-280">Aguardar envio</span><span class="sxs-lookup"><span data-stu-id="ca85c-280">Wait for Send</span></span></td>
<td><span data-ttu-id="ca85c-281">Aguardar notificação</span><span class="sxs-lookup"><span data-stu-id="ca85c-281">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="ca85c-282">Em caso de falha ao obter uma notificação, acesse pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-282">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="ca85c-283">Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados precisarem ser enviados, vá para PS</span><span class="sxs-lookup"><span data-stu-id="ca85c-283">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="ca85c-284">Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados não precisarem ser enviados, vá para NP</span><span class="sxs-lookup"><span data-stu-id="ca85c-284">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="ca85c-285">Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> de falha for recebida, acesse comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-285">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="ca85c-286">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-286">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-287">NP</span><span class="sxs-lookup"><span data-stu-id="ca85c-287">NP</span></span></td>
<td><span data-ttu-id="ca85c-288">Envio por push nulo</span><span class="sxs-lookup"><span data-stu-id="ca85c-288">Null Push</span></span></td>
<td><span data-ttu-id="ca85c-289">Enviar 0 bytes por push (Push nulo)</span><span class="sxs-lookup"><span data-stu-id="ca85c-289">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="ca85c-290">Em caso de falha, vá para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-290">On failure go to End</span></span></li>
<li><span data-ttu-id="ca85c-291">Em caso de sucesso, vá para PL</span><span class="sxs-lookup"><span data-stu-id="ca85c-291">On success go to PL</span></span></li>
</ul>
<span data-ttu-id="ca85c-292">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-292">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-293">PL</span><span class="sxs-lookup"><span data-stu-id="ca85c-293">PL</span></span></td>
<td><span data-ttu-id="ca85c-294">Recepção</span><span class="sxs-lookup"><span data-stu-id="ca85c-294">Pull</span></span></td>
<td><span data-ttu-id="ca85c-295">Fazer um pull</span><span class="sxs-lookup"><span data-stu-id="ca85c-295">Make a pull</span></span>
<ul>
<li><span data-ttu-id="ca85c-296">Em caso de falha, vá para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-296">On failure go to End</span></span></li>
<li><span data-ttu-id="ca85c-297">Em caso de êxito e conclusão síncrona com bytes diferentes de zero lidos, acesse PL</span><span class="sxs-lookup"><span data-stu-id="ca85c-297">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="ca85c-298">Em caso de êxito e conclusão síncrona com zero bytes lidos (pull nulo), vá para WComp</span><span class="sxs-lookup"><span data-stu-id="ca85c-298">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="ca85c-299">Em caso de êxito e conclusão assíncrona (ERROR_IO_PENDING é retornado), vá para WPL</span><span class="sxs-lookup"><span data-stu-id="ca85c-299">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="ca85c-300">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-300">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-301">WPL</span><span class="sxs-lookup"><span data-stu-id="ca85c-301">WPL</span></span></td>
<td><span data-ttu-id="ca85c-302">Aguardar pull</span><span class="sxs-lookup"><span data-stu-id="ca85c-302">Wait for Pull</span></span></td>
<td><span data-ttu-id="ca85c-303">Aguardar notificação</span><span class="sxs-lookup"><span data-stu-id="ca85c-303">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="ca85c-304">Em caso de falha ao obter uma conclusão, vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-304">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="ca85c-305">Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de falha for recebida, vá para Can</span><span class="sxs-lookup"><span data-stu-id="ca85c-305">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="ca85c-306">Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com bytes diferentes de zero, leia ir para pl</span><span class="sxs-lookup"><span data-stu-id="ca85c-306">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="ca85c-307">Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com zero bytes lido, vá para comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-307">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to Comp</span></span></li>
<li><span data-ttu-id="ca85c-308">Se uma falha for recebida, vá pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-308">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="ca85c-309">Para falhar: Vá para pode</span><span class="sxs-lookup"><span data-stu-id="ca85c-309">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-310">Podem</span><span class="sxs-lookup"><span data-stu-id="ca85c-310">Can</span></span></td>
<td><span data-ttu-id="ca85c-311">Cancelar a chamada</span><span class="sxs-lookup"><span data-stu-id="ca85c-311">Cancel the Call</span></span></td>
<td><span data-ttu-id="ca85c-312">Chame <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>go to WComp</span><span class="sxs-lookup"><span data-stu-id="ca85c-312">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-313">WComp</span><span class="sxs-lookup"><span data-stu-id="ca85c-313">WComp</span></span></td>
<td><span data-ttu-id="ca85c-314">Aguardar a conclusão</span><span class="sxs-lookup"><span data-stu-id="ca85c-314">Wait for Completion</span></span></td>
<td><span data-ttu-id="ca85c-315">Aguarde a notificação.</span><span class="sxs-lookup"><span data-stu-id="ca85c-315">Wait for notification.</span></span> <span data-ttu-id="ca85c-316">A notificação de CallComplete deve ser recebida.</span><span class="sxs-lookup"><span data-stu-id="ca85c-316">CallComplete notification should be received.</span></span><br/> <span data-ttu-id="ca85c-317">Ir para comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-317">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-318">Às</span><span class="sxs-lookup"><span data-stu-id="ca85c-318">Comp</span></span></td>
<td><span data-ttu-id="ca85c-319">Completion</span><span class="sxs-lookup"><span data-stu-id="ca85c-319">Completion</span></span></td>
<td><span data-ttu-id="ca85c-320">Emitir <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-320">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-321">End</span><span class="sxs-lookup"><span data-stu-id="ca85c-321">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="ca85c-322">Comportamento do servidor</span><span class="sxs-lookup"><span data-stu-id="ca85c-322">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ca85c-323">Estado</span><span class="sxs-lookup"><span data-stu-id="ca85c-323">State</span></span></th>
<th><span data-ttu-id="ca85c-324">Nome do Estado</span><span class="sxs-lookup"><span data-stu-id="ca85c-324">State Name</span></span></th>
<th><span data-ttu-id="ca85c-325">Ação</span><span class="sxs-lookup"><span data-stu-id="ca85c-325">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ca85c-326">D</span><span class="sxs-lookup"><span data-stu-id="ca85c-326">D</span></span></td>
<td><span data-ttu-id="ca85c-327">Dispatch</span><span class="sxs-lookup"><span data-stu-id="ca85c-327">Dispatch</span></span></td>
<td><span data-ttu-id="ca85c-328">A chamada é expedida pelo RPC runtimeGo para PL</span><span class="sxs-lookup"><span data-stu-id="ca85c-328">The call is dispatched by the RPC runtimeGo to PL</span></span><br/> <span data-ttu-id="ca85c-329">Para falhar fatalmente (ao executar no thread RPC): gerar exceção; ir para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-329">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="ca85c-330">Para falhar normalmente: Vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-330">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-331">PL</span><span class="sxs-lookup"><span data-stu-id="ca85c-331">PL</span></span></td>
<td><span data-ttu-id="ca85c-332">Recepção</span><span class="sxs-lookup"><span data-stu-id="ca85c-332">Pull</span></span></td>
<td><span data-ttu-id="ca85c-333">Fazer um pull</span><span class="sxs-lookup"><span data-stu-id="ca85c-333">Make a pull</span></span>
<ul>
<li><span data-ttu-id="ca85c-334">Em caso de falha, vá para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-334">On failure go to End</span></span></li>
<li><span data-ttu-id="ca85c-335">Em caso de êxito e conclusão síncrona com bytes diferentes de zero lidos, acesse PL</span><span class="sxs-lookup"><span data-stu-id="ca85c-335">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="ca85c-336">Em caso de êxito e conclusão síncrona com zero bytes lidos (pull nulo), vá para PS</span><span class="sxs-lookup"><span data-stu-id="ca85c-336">On success and synchronous completion with zero bytes read (null pull) go to PS</span></span></li>
<li><span data-ttu-id="ca85c-337">Em caso de êxito e conclusão assíncrona (ERROR_IO_PENDING é retornado), vá para WPL</span><span class="sxs-lookup"><span data-stu-id="ca85c-337">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="ca85c-338">Para falhar: Vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-338">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-339">WPL</span><span class="sxs-lookup"><span data-stu-id="ca85c-339">WPL</span></span></td>
<td><span data-ttu-id="ca85c-340">Aguardar pull</span><span class="sxs-lookup"><span data-stu-id="ca85c-340">Wait for Pull</span></span></td>
<td><span data-ttu-id="ca85c-341">Aguardar notificação</span><span class="sxs-lookup"><span data-stu-id="ca85c-341">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="ca85c-342">Em caso de falha ao obter uma conclusão, vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-342">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="ca85c-343">Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de falha for recebido, vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-343">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="ca85c-344">Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com bytes diferentes de zero, leia ir para pl</span><span class="sxs-lookup"><span data-stu-id="ca85c-344">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="ca85c-345">Se uma <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de sucesso for recebida com zero bytes lido, vá para PS</span><span class="sxs-lookup"><span data-stu-id="ca85c-345">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to PS</span></span></li>
<li><span data-ttu-id="ca85c-346">Se uma falha for recebida, vá para</span><span class="sxs-lookup"><span data-stu-id="ca85c-346">If a failure is received go A</span></span></li>
</ul>
<span data-ttu-id="ca85c-347">Para falhar: Vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-347">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-348">PS</span><span class="sxs-lookup"><span data-stu-id="ca85c-348">PS</span></span></td>
<td><span data-ttu-id="ca85c-349">Push</span><span class="sxs-lookup"><span data-stu-id="ca85c-349">Push</span></span></td>
<td><span data-ttu-id="ca85c-350">Fazer um envio por push</span><span class="sxs-lookup"><span data-stu-id="ca85c-350">Make a push</span></span>
<ul>
<li><span data-ttu-id="ca85c-351">Em caso de sucesso, vá para WPS</span><span class="sxs-lookup"><span data-stu-id="ca85c-351">On success go to WPS</span></span></li>
<li><span data-ttu-id="ca85c-352">Em caso de falha, vá para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-352">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="ca85c-353">Para falhar: Vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-353">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-354">WPS</span><span class="sxs-lookup"><span data-stu-id="ca85c-354">WPS</span></span></td>
<td><span data-ttu-id="ca85c-355">Aguardar envio por push</span><span class="sxs-lookup"><span data-stu-id="ca85c-355">Wait for Push</span></span></td>
<td><span data-ttu-id="ca85c-356">Aguardar notificação</span><span class="sxs-lookup"><span data-stu-id="ca85c-356">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="ca85c-357">Em caso de falha ao obter uma conclusão, vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-357">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="ca85c-358">Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados precisarem ser enviados, vá para PS</span><span class="sxs-lookup"><span data-stu-id="ca85c-358">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="ca85c-359">Se um <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de sucesso for recebido e mais dados não precisarem ser enviados, vá para NP</span><span class="sxs-lookup"><span data-stu-id="ca85c-359">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="ca85c-360">Se uma falha for recebida, go comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-360">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="ca85c-361">Para falhar: Vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-361">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-362">NP</span><span class="sxs-lookup"><span data-stu-id="ca85c-362">NP</span></span></td>
<td><span data-ttu-id="ca85c-363">Envio por push nulo</span><span class="sxs-lookup"><span data-stu-id="ca85c-363">Null Push</span></span></td>
<td><span data-ttu-id="ca85c-364">Enviar 0 bytes por push</span><span class="sxs-lookup"><span data-stu-id="ca85c-364">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="ca85c-365">em caso de sucesso, vá para o WNP</span><span class="sxs-lookup"><span data-stu-id="ca85c-365">on success go to WNP</span></span></li>
<li><span data-ttu-id="ca85c-366">em caso de falha, vá para comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-366">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="ca85c-367">Para falhar: Vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-367">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-368">WNP</span><span class="sxs-lookup"><span data-stu-id="ca85c-368">WNP</span></span></td>
<td><span data-ttu-id="ca85c-369">Aguardar envio por push nulo</span><span class="sxs-lookup"><span data-stu-id="ca85c-369">Wait for Null Push</span></span></td>
<td><span data-ttu-id="ca85c-370">Aguardar notificação</span><span class="sxs-lookup"><span data-stu-id="ca85c-370">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="ca85c-371">Em caso de falha ao obter uma conclusão, vá para um</span><span class="sxs-lookup"><span data-stu-id="ca85c-371">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="ca85c-372">Se uma falha for recebida, go comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-372">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="ca85c-373">Se um sucesso for recebido, acesse comp</span><span class="sxs-lookup"><span data-stu-id="ca85c-373">If a success is received go Comp</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-374">Um</span><span class="sxs-lookup"><span data-stu-id="ca85c-374">A</span></span></td>
<td><span data-ttu-id="ca85c-375">Anular a chamada</span><span class="sxs-lookup"><span data-stu-id="ca85c-375">Abort the Call</span></span></td>
<td><span data-ttu-id="ca85c-376">Chamar <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; ir para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-376">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ca85c-377">Às</span><span class="sxs-lookup"><span data-stu-id="ca85c-377">Comp</span></span></td>
<td><span data-ttu-id="ca85c-378">Completion</span><span class="sxs-lookup"><span data-stu-id="ca85c-378">Completion</span></span></td>
<td><span data-ttu-id="ca85c-379">Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; ir para o fim</span><span class="sxs-lookup"><span data-stu-id="ca85c-379">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ca85c-380">End</span><span class="sxs-lookup"><span data-stu-id="ca85c-380">End</span></span></td>


</tr>
</tbody>
</table>



 

 

 





