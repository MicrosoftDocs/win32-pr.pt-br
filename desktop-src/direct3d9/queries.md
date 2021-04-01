---
description: Há vários tipos de consultas que são projetadas para consultar o status dos recursos.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Consultas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825488"
---
# <a name="queries-direct3d-9"></a><span data-ttu-id="88842-103">Consultas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="88842-103">Queries (Direct3D 9)</span></span>

<span data-ttu-id="88842-104">Há vários tipos de consultas que são projetadas para consultar o status dos recursos.</span><span class="sxs-lookup"><span data-stu-id="88842-104">There are several types of queries which are designed to query the status of resources.</span></span> <span data-ttu-id="88842-105">O status de um determinado recurso inclui o status da GPU (unidade de processamento gráfico), o status do driver ou o status do tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="88842-105">The status of a given resource includes graphics processing unit (GPU) status, driver status, or runtime status.</span></span> <span data-ttu-id="88842-106">Para entender a diferença entre os diferentes tipos de consulta, você precisa entender os Estados de consulta.</span><span class="sxs-lookup"><span data-stu-id="88842-106">To understand the difference between the different query types, you need to understand the query states.</span></span> <span data-ttu-id="88842-107">O diagrama de transição de estado a seguir explica cada um dos Estados de consulta.</span><span class="sxs-lookup"><span data-stu-id="88842-107">The following state transition diagram explains each of the query states.</span></span>

![diagrama mostrando transições entre Estados de consulta](images/queries.png)

<span data-ttu-id="88842-109">O diagrama mostra três Estados, cada um definido pelos círculos.</span><span class="sxs-lookup"><span data-stu-id="88842-109">The diagram shows three states, each defined by circles.</span></span> <span data-ttu-id="88842-110">Cada uma das linhas sólidas são eventos controlados por aplicativo que causam uma transição de estado.</span><span class="sxs-lookup"><span data-stu-id="88842-110">Each of the solid lines are application-driven events that cause a state transition.</span></span> <span data-ttu-id="88842-111">A linha tracejada é um evento controlado por recursos que alterna uma consulta do estado emitido para o estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="88842-111">The dashed line is a resource-driven event that switches a query from the issued state to the signaled state.</span></span> <span data-ttu-id="88842-112">Cada um desses Estados tem uma finalidade diferente:</span><span class="sxs-lookup"><span data-stu-id="88842-112">Each of these states has a different purpose:</span></span>

-   <span data-ttu-id="88842-113">O estado sinalizado é como um estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="88842-113">The signaled state is like an idle state.</span></span> <span data-ttu-id="88842-114">O objeto de consulta foi gerado e está aguardando que o aplicativo emita a consulta.</span><span class="sxs-lookup"><span data-stu-id="88842-114">The query object has been generated and is waiting for the application to issue the query.</span></span> <span data-ttu-id="88842-115">Depois que uma consulta for concluída e feita a transição de volta para o estado sinalizado, a resposta para a consulta poderá ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="88842-115">Once a query has completed and transitioned back to the signaled state, the answer to the query can be retrieved.</span></span>
-   <span data-ttu-id="88842-116">O estado de compilação é como uma área de preparo para uma consulta.</span><span class="sxs-lookup"><span data-stu-id="88842-116">The building state is like a staging area for a query.</span></span> <span data-ttu-id="88842-117">A partir do estado de compilação, uma consulta foi emitida (chamando [**D3DISSUE \_ begin**](d3dissue-begin.md)), mas ainda não foi transferida para o estado emitido.</span><span class="sxs-lookup"><span data-stu-id="88842-117">From the building state, a query has been issued (by calling [**D3DISSUE\_BEGIN**](d3dissue-begin.md)) but has not yet transitioned to the issued state.</span></span> <span data-ttu-id="88842-118">Quando um aplicativo emite uma extremidade de consulta (chamando [**D3DISSUE \_ end**](d3dissue-end.md)), a consulta faz a transição para o estado emitido.</span><span class="sxs-lookup"><span data-stu-id="88842-118">When an application issues a query end (by calling [**D3DISSUE\_END**](d3dissue-end.md)), the query transitions to the issued state.</span></span>
-   <span data-ttu-id="88842-119">O estado emitido significa que o recurso que está sendo consultado tem controle da consulta.</span><span class="sxs-lookup"><span data-stu-id="88842-119">The issued state means that the resource being queried has control of the query.</span></span> <span data-ttu-id="88842-120">Depois que o recurso concluir seu trabalho, o recurso faz a transição da máquina de estado para o estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="88842-120">Once the resource finishes its work, the resource transitions the state machine to the signaled state.</span></span> <span data-ttu-id="88842-121">Durante o estado emitido, o aplicativo deve sondar para detectar a transição para o estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="88842-121">During the issued state, the application must poll to detect the transition to the signaled state.</span></span> <span data-ttu-id="88842-122">Quando ocorre a transição para o estado sinalizado, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) retorna o resultado da consulta (por meio de um argumento) para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="88842-122">Once the transition to the signaled state occurs, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns the query result (through an argument) to the application.</span></span>

<span data-ttu-id="88842-123">A tabela a seguir lista os tipos de consulta disponíveis.</span><span class="sxs-lookup"><span data-stu-id="88842-123">The following table lists the available query types.</span></span>



| <span data-ttu-id="88842-124">Tipo de consulta</span><span class="sxs-lookup"><span data-stu-id="88842-124">Query Type</span></span>        | <span data-ttu-id="88842-125">Evento de problema</span><span class="sxs-lookup"><span data-stu-id="88842-125">Issue Event</span></span>                                                                      | <span data-ttu-id="88842-126">Buffer GetData</span><span class="sxs-lookup"><span data-stu-id="88842-126">GetData buffer</span></span>                                                              | <span data-ttu-id="88842-127">Runtime</span><span class="sxs-lookup"><span data-stu-id="88842-127">Runtime</span></span>      | <span data-ttu-id="88842-128">Início implícito da consulta</span><span class="sxs-lookup"><span data-stu-id="88842-128">Implicit beginning of query</span></span>                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| <span data-ttu-id="88842-129">BANDWIDTHTIMINGS</span><span class="sxs-lookup"><span data-stu-id="88842-129">BANDWIDTHTIMINGS</span></span>  | <span data-ttu-id="88842-130">[**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="88842-130">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="88842-131">**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="88842-131">**D3DDEVINFO\_D3D9BANDWIDTHTIMINGS**</span></span>](d3ddevinfo-d3d9bandwidthtimings.md) | <span data-ttu-id="88842-132">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="88842-132">Retail/Debug</span></span> | <span data-ttu-id="88842-133">N/D</span><span class="sxs-lookup"><span data-stu-id="88842-133">N/A</span></span>                                              |
| <span data-ttu-id="88842-134">CACHEUTILIZATION</span><span class="sxs-lookup"><span data-stu-id="88842-134">CACHEUTILIZATION</span></span>  | <span data-ttu-id="88842-135">[**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="88842-135">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="88842-136">**D3DDEVINFO \_ D3D9CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="88842-136">**D3DDEVINFO\_D3D9CACHEUTILIZATION**</span></span>](d3ddevinfo-d3d9cacheutilization.md) | <span data-ttu-id="88842-137">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="88842-137">Retail/Debug</span></span> | <span data-ttu-id="88842-138">N/D</span><span class="sxs-lookup"><span data-stu-id="88842-138">N/A</span></span>                                              |
| <span data-ttu-id="88842-139">CIRCUNSTÂNCIA</span><span class="sxs-lookup"><span data-stu-id="88842-139">EVENT</span></span>             | [<span data-ttu-id="88842-140">**D3DISSUE \_ fim**</span><span class="sxs-lookup"><span data-stu-id="88842-140">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="88842-141">BOOL</span><span class="sxs-lookup"><span data-stu-id="88842-141">BOOL</span></span>                                                                        | <span data-ttu-id="88842-142">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="88842-142">Retail/Debug</span></span> | [<span data-ttu-id="88842-143">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="88842-143">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="88842-144">INTERFACETIMINGS</span><span class="sxs-lookup"><span data-stu-id="88842-144">INTERFACETIMINGS</span></span>  | <span data-ttu-id="88842-145">[**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="88842-145">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="88842-146">**D3DDEVINFO \_ D3D9INTERFACETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="88842-146">**D3DDEVINFO\_D3D9INTERFACETIMINGS**</span></span>](d3ddevinfo-d3d9interfacetimings.md) | <span data-ttu-id="88842-147">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="88842-147">Retail/Debug</span></span> | <span data-ttu-id="88842-148">N/D</span><span class="sxs-lookup"><span data-stu-id="88842-148">N/A</span></span>                                              |
| <span data-ttu-id="88842-149">OCLUSÃO</span><span class="sxs-lookup"><span data-stu-id="88842-149">OCCLUSION</span></span>         | <span data-ttu-id="88842-150">[**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="88842-150">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="88842-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="88842-151">DWORD</span></span>                                                                       | <span data-ttu-id="88842-152">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="88842-152">Retail/Debug</span></span> | <span data-ttu-id="88842-153">N/D</span><span class="sxs-lookup"><span data-stu-id="88842-153">N/A</span></span>                                              |
| <span data-ttu-id="88842-154">PIPELINETIMINGS</span><span class="sxs-lookup"><span data-stu-id="88842-154">PIPELINETIMINGS</span></span>   | <span data-ttu-id="88842-155">[**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="88842-155">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="88842-156">**D3DDEVINFO \_ D3D9PIPELINETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="88842-156">**D3DDEVINFO\_D3D9PIPELINETIMINGS**</span></span>](d3ddevinfo-d3d9pipelinetimings.md)   | <span data-ttu-id="88842-157">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="88842-157">Retail/Debug</span></span> | <span data-ttu-id="88842-158">N/D</span><span class="sxs-lookup"><span data-stu-id="88842-158">N/A</span></span>                                              |
| <span data-ttu-id="88842-159">RESOURCEMANAGER</span><span class="sxs-lookup"><span data-stu-id="88842-159">RESOURCEMANAGER</span></span>   | [<span data-ttu-id="88842-160">**D3DISSUE \_ fim**</span><span class="sxs-lookup"><span data-stu-id="88842-160">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="88842-161">**\_RESOURCEMANAGER D3DDEVINFO**</span><span class="sxs-lookup"><span data-stu-id="88842-161">**D3DDEVINFO\_ResourceManager**</span></span>](d3ddevinfo-resourcemanager.md)           | <span data-ttu-id="88842-162">Somente depuração</span><span class="sxs-lookup"><span data-stu-id="88842-162">Debug only</span></span>   | [<span data-ttu-id="88842-163">**Existi**</span><span class="sxs-lookup"><span data-stu-id="88842-163">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="88842-164">timestamp</span><span class="sxs-lookup"><span data-stu-id="88842-164">TIMESTAMP</span></span>         | [<span data-ttu-id="88842-165">**D3DISSUE \_ fim**</span><span class="sxs-lookup"><span data-stu-id="88842-165">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="88842-166">UINT64</span><span class="sxs-lookup"><span data-stu-id="88842-166">UINT64</span></span>                                                                      | <span data-ttu-id="88842-167">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="88842-167">Retail/Debug</span></span> | <span data-ttu-id="88842-168">N/D</span><span class="sxs-lookup"><span data-stu-id="88842-168">N/A</span></span>                                              |
| <span data-ttu-id="88842-169">TIMESTAMPDISJOINT</span><span class="sxs-lookup"><span data-stu-id="88842-169">TIMESTAMPDISJOINT</span></span> | <span data-ttu-id="88842-170">[**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="88842-170">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="88842-171">BOOL</span><span class="sxs-lookup"><span data-stu-id="88842-171">BOOL</span></span>                                                                        | <span data-ttu-id="88842-172">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="88842-172">Retail/Debug</span></span> | <span data-ttu-id="88842-173">N/D</span><span class="sxs-lookup"><span data-stu-id="88842-173">N/A</span></span>                                              |
| <span data-ttu-id="88842-174">TIMESTAMPFREQ</span><span class="sxs-lookup"><span data-stu-id="88842-174">TIMESTAMPFREQ</span></span>     | [<span data-ttu-id="88842-175">**D3DISSUE \_ fim**</span><span class="sxs-lookup"><span data-stu-id="88842-175">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="88842-176">UINT64</span><span class="sxs-lookup"><span data-stu-id="88842-176">UINT64</span></span>                                                                      | <span data-ttu-id="88842-177">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="88842-177">Retail/Debug</span></span> | <span data-ttu-id="88842-178">N/D</span><span class="sxs-lookup"><span data-stu-id="88842-178">N/A</span></span>                                              |
| <span data-ttu-id="88842-179">VCACHE</span><span class="sxs-lookup"><span data-stu-id="88842-179">VCACHE</span></span>            | [<span data-ttu-id="88842-180">**D3DISSUE \_ fim**</span><span class="sxs-lookup"><span data-stu-id="88842-180">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="88842-181">**D3DDEVINFO \_ VCACHE**</span><span class="sxs-lookup"><span data-stu-id="88842-181">**D3DDEVINFO\_VCACHE**</span></span>](d3ddevinfo-vcache.md)                             | <span data-ttu-id="88842-182">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="88842-182">Retail/Debug</span></span> | [<span data-ttu-id="88842-183">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="88842-183">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="88842-184">VERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="88842-184">VERTEXSTATS</span></span>       | [<span data-ttu-id="88842-185">**D3DISSUE \_ fim**</span><span class="sxs-lookup"><span data-stu-id="88842-185">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="88842-186">**D3DDEVINFO \_ D3DVERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="88842-186">**D3DDEVINFO\_D3DVERTEXSTATS**</span></span>](d3ddevinfo-d3dvertexstats.md)             | <span data-ttu-id="88842-187">Somente depuração</span><span class="sxs-lookup"><span data-stu-id="88842-187">Debug only</span></span>   | [<span data-ttu-id="88842-188">**Existi**</span><span class="sxs-lookup"><span data-stu-id="88842-188">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="88842-189">VERTEXTIMINGS</span><span class="sxs-lookup"><span data-stu-id="88842-189">VERTEXTIMINGS</span></span>     | <span data-ttu-id="88842-190">[**D3DISSUE \_ Início**](d3dissue-begin.md), [ **\_ fim do D3DISSUE**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="88842-190">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="88842-191">**D3DDEVINFO \_ D3D9STAGETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="88842-191">**D3DDEVINFO\_D3D9STAGETIMINGS**</span></span>](d3ddevinfo-d3d9stagetimings.md)         | <span data-ttu-id="88842-192">Varejo/depuração</span><span class="sxs-lookup"><span data-stu-id="88842-192">Retail/Debug</span></span> | <span data-ttu-id="88842-193">N/D</span><span class="sxs-lookup"><span data-stu-id="88842-193">N/A</span></span>                                              |



 

<span data-ttu-id="88842-194">Algumas das consultas exigem um evento de início e término, enquanto outras exigem apenas um evento de término.</span><span class="sxs-lookup"><span data-stu-id="88842-194">Some of the queries require a begin and end event, while others only require an end event.</span></span> <span data-ttu-id="88842-195">As consultas que exigem apenas um evento de término começam quando outro evento implícito ocorre (que é listado na tabela).</span><span class="sxs-lookup"><span data-stu-id="88842-195">The queries that only require an end event begin when another implicit event occurs (which is listed in the table).</span></span> <span data-ttu-id="88842-196">Todas as consultas retornam uma resposta, exceto a consulta de evento cuja resposta é sempre **verdadeira**.</span><span class="sxs-lookup"><span data-stu-id="88842-196">All queries return an answer, except the event query whose answer is always **TRUE**.</span></span> <span data-ttu-id="88842-197">Um aplicativo usa o estado da consulta ou o código de retorno de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="88842-197">An application uses either the state of the query or the return code of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>

## <a name="create-a-query"></a><span data-ttu-id="88842-198">Criar uma consulta</span><span class="sxs-lookup"><span data-stu-id="88842-198">Create a Query</span></span>

<span data-ttu-id="88842-199">Antes de criar uma consulta, você pode verificar se o tempo de execução dá suporte a consultas chamando [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) com um ponteiro **nulo** como este:</span><span class="sxs-lookup"><span data-stu-id="88842-199">Before you create a query, you can check to see if the runtime supports queries by calling [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) with a **NULL** pointer like this:</span></span>


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



<span data-ttu-id="88842-200">Esse método retornará um código de êxito se uma consulta puder ser criada; caso contrário, ele retorna um código de erro.</span><span class="sxs-lookup"><span data-stu-id="88842-200">This method returns a success code if a query can be created; otherwise it returns an error code.</span></span> <span data-ttu-id="88842-201">Depois que o [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) for executado com sucesso, você poderá criar um objeto de consulta como este:</span><span class="sxs-lookup"><span data-stu-id="88842-201">Once [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) succeeds, you can create a query object like this:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



<span data-ttu-id="88842-202">Se essa chamada for realizada com sucesso, um objeto de consulta será criado.</span><span class="sxs-lookup"><span data-stu-id="88842-202">If this call succeeds, a query object is created.</span></span> <span data-ttu-id="88842-203">A consulta está essencialmente ociosa no estado sinalizado (com uma resposta não inicializada) aguardando para ser emitida.</span><span class="sxs-lookup"><span data-stu-id="88842-203">The query is essentially idle in the signaled state (with an uninitialized answer) waiting to be issued.</span></span> <span data-ttu-id="88842-204">Quando terminar com a consulta, libere-a como qualquer outra interface.</span><span class="sxs-lookup"><span data-stu-id="88842-204">When you are finished with the query, release it like any other interface.</span></span>

## <a name="issue-a-query"></a><span data-ttu-id="88842-205">Emitir uma consulta</span><span class="sxs-lookup"><span data-stu-id="88842-205">Issue a Query</span></span>

<span data-ttu-id="88842-206">Um aplicativo altera um estado de consulta emitindo uma consulta.</span><span class="sxs-lookup"><span data-stu-id="88842-206">An application changes a query state by issuing a query.</span></span> <span data-ttu-id="88842-207">Aqui está um exemplo de como emitir uma consulta:</span><span class="sxs-lookup"><span data-stu-id="88842-207">Here is an example of issuing a query:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



<span data-ttu-id="88842-208">Uma consulta no estado sinalizado fará a transição como esta quando for emitida:</span><span class="sxs-lookup"><span data-stu-id="88842-208">A query in the signaled state will transition like this when issued:</span></span>



| <span data-ttu-id="88842-209">Tipo de problema</span><span class="sxs-lookup"><span data-stu-id="88842-209">Issue Type</span></span>                                | <span data-ttu-id="88842-210">A consulta faz a transição para o.</span><span class="sxs-lookup"><span data-stu-id="88842-210">Query Transitions to the .</span></span> <span data-ttu-id="88842-211">.</span><span class="sxs-lookup"><span data-stu-id="88842-211">.</span></span> <span data-ttu-id="88842-212">.</span><span class="sxs-lookup"><span data-stu-id="88842-212">.</span></span> |
|-------------------------------------------|--------------------------------|
| [<span data-ttu-id="88842-213">**Início do D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="88842-213">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="88842-214">Estado de compilação.</span><span class="sxs-lookup"><span data-stu-id="88842-214">Building state.</span></span>                |
| [<span data-ttu-id="88842-215">**D3DISSUE \_ fim**</span><span class="sxs-lookup"><span data-stu-id="88842-215">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="88842-216">Estado emitido.</span><span class="sxs-lookup"><span data-stu-id="88842-216">Issued state.</span></span>                  |



 

<span data-ttu-id="88842-217">Uma consulta no estado de compilação será transferida como esta quando for emitida:</span><span class="sxs-lookup"><span data-stu-id="88842-217">A query in the building state will transition like this when issued:</span></span>



| <span data-ttu-id="88842-218">Tipo de problema</span><span class="sxs-lookup"><span data-stu-id="88842-218">Issue Type</span></span>                                | <span data-ttu-id="88842-219">A consulta faz a transição para o.</span><span class="sxs-lookup"><span data-stu-id="88842-219">Query Transitions to the .</span></span> <span data-ttu-id="88842-220">.</span><span class="sxs-lookup"><span data-stu-id="88842-220">.</span></span> <span data-ttu-id="88842-221">.</span><span class="sxs-lookup"><span data-stu-id="88842-221">.</span></span>                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="88842-222">**Início do D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="88842-222">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="88842-223">(Sem transição, permanece no estado de compilação.</span><span class="sxs-lookup"><span data-stu-id="88842-223">(No transition, stays in the building state.</span></span> <span data-ttu-id="88842-224">Reinicia o colchete de consulta.)</span><span class="sxs-lookup"><span data-stu-id="88842-224">Restarts the query bracket.)</span></span> |
| [<span data-ttu-id="88842-225">**D3DISSUE \_ fim**</span><span class="sxs-lookup"><span data-stu-id="88842-225">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="88842-226">Estado emitido.</span><span class="sxs-lookup"><span data-stu-id="88842-226">Issued state.</span></span>                                                             |



 

<span data-ttu-id="88842-227">Uma consulta no estado emitido fará a transição como esta quando for emitida:</span><span class="sxs-lookup"><span data-stu-id="88842-227">A query in the issued state will transition like this when issued:</span></span>



| <span data-ttu-id="88842-228">Tipo de problema</span><span class="sxs-lookup"><span data-stu-id="88842-228">Issue Type</span></span>                                | <span data-ttu-id="88842-229">A consulta faz a transição para o.</span><span class="sxs-lookup"><span data-stu-id="88842-229">Query Transitions to the .</span></span> <span data-ttu-id="88842-230">.</span><span class="sxs-lookup"><span data-stu-id="88842-230">.</span></span> <span data-ttu-id="88842-231">.</span><span class="sxs-lookup"><span data-stu-id="88842-231">.</span></span>                    |
|-------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="88842-232">**Início do D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="88842-232">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="88842-233">Criando o estado e reinicia o colchete de consulta.</span><span class="sxs-lookup"><span data-stu-id="88842-233">Building state and restarts the query bracket.</span></span>    |
| [<span data-ttu-id="88842-234">**D3DISSUE \_ fim**</span><span class="sxs-lookup"><span data-stu-id="88842-234">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="88842-235">Estado emitido após abandonar a consulta existente.</span><span class="sxs-lookup"><span data-stu-id="88842-235">Issued state after abandoning the existing query.</span></span> |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a><span data-ttu-id="88842-236">Verificar o estado da consulta e obter a resposta para a consulta</span><span class="sxs-lookup"><span data-stu-id="88842-236">Check the Query State and Get the Answer to the Query</span></span>

<span data-ttu-id="88842-237">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) faz duas coisas:</span><span class="sxs-lookup"><span data-stu-id="88842-237">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) does two things:</span></span>

1.  <span data-ttu-id="88842-238">Retorna o estado da consulta no código de retorno.</span><span class="sxs-lookup"><span data-stu-id="88842-238">Returns the query state in the return code.</span></span>
2.  <span data-ttu-id="88842-239">Retorna a resposta à consulta em *pData*.</span><span class="sxs-lookup"><span data-stu-id="88842-239">Returns the answer to the query in *pData*.</span></span>

<span data-ttu-id="88842-240">De cada um dos três Estados de consulta, aqui estão os códigos de retorno de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) :</span><span class="sxs-lookup"><span data-stu-id="88842-240">From each of the three query states, here are the [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) return codes:</span></span>



| <span data-ttu-id="88842-241">Estado de consulta</span><span class="sxs-lookup"><span data-stu-id="88842-241">Query State</span></span> | <span data-ttu-id="88842-242">Código de retorno GetData</span><span class="sxs-lookup"><span data-stu-id="88842-242">GetData return code</span></span> |
|-------------|---------------------|
| <span data-ttu-id="88842-243">Sinalizado</span><span class="sxs-lookup"><span data-stu-id="88842-243">Signaled</span></span>    | <span data-ttu-id="88842-244">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="88842-244">S\_OK</span></span>               |
| <span data-ttu-id="88842-245">Construção</span><span class="sxs-lookup"><span data-stu-id="88842-245">Building</span></span>    | <span data-ttu-id="88842-246">Código do erro</span><span class="sxs-lookup"><span data-stu-id="88842-246">Error code</span></span>          |
| <span data-ttu-id="88842-247">Emitido</span><span class="sxs-lookup"><span data-stu-id="88842-247">Issued</span></span>      | <span data-ttu-id="88842-248">\_falso</span><span class="sxs-lookup"><span data-stu-id="88842-248">S\_FALSE</span></span>            |



 

<span data-ttu-id="88842-249">Por exemplo, quando uma consulta está no estado emitido e a resposta à consulta não está disponível, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) retorna S \_ false.</span><span class="sxs-lookup"><span data-stu-id="88842-249">For example, when a query is in the issued state and the answer to the query is not available, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns S\_FALSE.</span></span> <span data-ttu-id="88842-250">Quando o recurso conclui seu trabalho e o aplicativo emitiu uma extremidade de consulta, o recurso faz a transição da consulta para o estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="88842-250">When the resource finishes its work and the application has issued a query end, the resource transitions the query to the signaled state.</span></span> <span data-ttu-id="88842-251">Do estado sinalizado, **GetData** retorna S \_ OK, o que significa que a resposta para a consulta também é retornada em *pData*.</span><span class="sxs-lookup"><span data-stu-id="88842-251">From the signaled state, **GetData** returns S\_OK which means that the answer to the query is also returned in *pData*.</span></span> <span data-ttu-id="88842-252">Por exemplo, aqui está a sequência de eventos para retornar o número de pixels desenhados em uma sequência de renderização:</span><span class="sxs-lookup"><span data-stu-id="88842-252">For instance, here is the sequence of events to return the number of pixels drawn in a render sequence:</span></span>

-   <span data-ttu-id="88842-253">Criar a consulta.</span><span class="sxs-lookup"><span data-stu-id="88842-253">Create the query.</span></span>
-   <span data-ttu-id="88842-254">Emitir um evento de início.</span><span class="sxs-lookup"><span data-stu-id="88842-254">Issue a begin event.</span></span>
-   <span data-ttu-id="88842-255">Desenhe algo.</span><span class="sxs-lookup"><span data-stu-id="88842-255">Draw something.</span></span>
-   <span data-ttu-id="88842-256">Emita um evento de término.</span><span class="sxs-lookup"><span data-stu-id="88842-256">Issue an end event.</span></span>

<span data-ttu-id="88842-257">A seguir está a sequência de código correspondente:</span><span class="sxs-lookup"><span data-stu-id="88842-257">The following is the corresponding sequence of code:</span></span>


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="88842-258">Essas linhas de código fazem várias coisas:</span><span class="sxs-lookup"><span data-stu-id="88842-258">These lines of code do several things:</span></span>

-   <span data-ttu-id="88842-259">Chame [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) para retornar o número de pixels desenhados.</span><span class="sxs-lookup"><span data-stu-id="88842-259">Call [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to return the number of pixels drawn.</span></span>
-   <span data-ttu-id="88842-260">Especifique [**a \_ liberação de D3DGETDATA**](d3dgetdata-flush.md) para habilitar o recurso para fazer a transição da consulta para o estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="88842-260">Specify [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md) to enable the resource to transition the query to the signaled state.</span></span>
-   <span data-ttu-id="88842-261">Sondar o recurso de consulta chamando [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) a partir de um loop.</span><span class="sxs-lookup"><span data-stu-id="88842-261">Poll the query resource by calling [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) from a loop.</span></span> <span data-ttu-id="88842-262">Desde que **GetData** retorne S \_ false, isso significa que o recurso ainda não retornou a resposta.</span><span class="sxs-lookup"><span data-stu-id="88842-262">As long as **GetData** returns S\_FALSE, this means the resource has not returned the answer yet.</span></span>

<span data-ttu-id="88842-263">O valor de retorno de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) essencialmente informa em que estado a consulta é.</span><span class="sxs-lookup"><span data-stu-id="88842-263">The return value of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) essentially tells you in what state the query is.</span></span> <span data-ttu-id="88842-264">Os valores possíveis são S \_ OK, s \_ false e um erro.</span><span class="sxs-lookup"><span data-stu-id="88842-264">Possible values are S\_OK, S\_FALSE, and an error.</span></span> <span data-ttu-id="88842-265">Não chame **GetData** em uma consulta que esteja no estado de compilação.</span><span class="sxs-lookup"><span data-stu-id="88842-265">Do not call **GetData** on a query that is in the building state.</span></span>

-   <span data-ttu-id="88842-266">S \_ OK significa que o recurso (GPU ou driver ou tempo de execução) foi concluído.</span><span class="sxs-lookup"><span data-stu-id="88842-266">S\_OK means the resource (GPU or driver, or runtime) is finished.</span></span> <span data-ttu-id="88842-267">A consulta está retornando ao estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="88842-267">The query is returning to the signaled state.</span></span> <span data-ttu-id="88842-268">A resposta (se houver) está sendo retornada por [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="88842-268">The answer (if any) is being returned by [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>
-   <span data-ttu-id="88842-269">S \_ false significa que o recurso (GPU ou driver ou tempo de execução) não pode retornar uma resposta ainda.</span><span class="sxs-lookup"><span data-stu-id="88842-269">S\_FALSE means the resource (GPU or driver, or runtime) cannot return an answer yet.</span></span> <span data-ttu-id="88842-270">Isso pode ocorrer porque a GPU não foi concluída ou ainda não viu o trabalho.</span><span class="sxs-lookup"><span data-stu-id="88842-270">This could be because the GPU is not finished or has not seen the work yet.</span></span>
-   <span data-ttu-id="88842-271">Um erro significa que a consulta gerou um erro do qual não pode se recuperar.</span><span class="sxs-lookup"><span data-stu-id="88842-271">An error means that the query has generated an error from which it cannot recover.</span></span> <span data-ttu-id="88842-272">Esse pode ser o caso se o dispositivo for perdido durante uma consulta.</span><span class="sxs-lookup"><span data-stu-id="88842-272">This could be the case if the device is lost during a query.</span></span> <span data-ttu-id="88842-273">Depois que uma consulta gerar um erro (diferente de S \_ false), a consulta deverá ser recriada, o que reiniciará a sequência de consulta do estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="88842-273">Once a query has generated an error (other than S\_FALSE), the query must be recreated which will restart the query sequence from the signaled state.</span></span>

<span data-ttu-id="88842-274">Em vez de especificar [**D3DGETDATA \_ flush**](d3dgetdata-flush.md), que fornece informações mais atualizadas, você pode fornecer zero, que é uma verificação de peso mais leve se a consulta estiver no estado emitido.</span><span class="sxs-lookup"><span data-stu-id="88842-274">Instead of specifying [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md), which provides more up-to-date information, you could supply zero which is a more light-weight check if the query is in the issued state.</span></span> <span data-ttu-id="88842-275">Fornecer zero fará com que [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) não libere o buffer de comando.</span><span class="sxs-lookup"><span data-stu-id="88842-275">Supplying zero will cause [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to not flush the command buffer.</span></span> <span data-ttu-id="88842-276">Por esse motivo, deve-se ter cuidado para evitar loops infinate (consulte **GetData** para obter detalhes).</span><span class="sxs-lookup"><span data-stu-id="88842-276">For this reason, care must be taken to avoid infinate loops (see **GetData** for details).</span></span> <span data-ttu-id="88842-277">Como o tempo de execução faz a fila funcionar no buffer de comando, o **D3DGETDATA \_ flush** é um mecanismo para liberar o buffer de comando para o driver (e, portanto, a GPU; consulte com [precisão a criação de perfil de chamadas de API do Direct3D (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="88842-277">Since the runtime queues up work in the command buffer, **D3DGETDATA\_FLUSH** is a mechanism for flushing the command buffer to the driver (and hence the GPU; see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="88842-278">Durante a liberação do buffer de comando, uma consulta pode fazer a transição para o estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="88842-278">During the command buffer flush, a query may transition to the signaled state.</span></span>

## <a name="example-an-event-query"></a><span data-ttu-id="88842-279">Exemplo: uma consulta de evento</span><span class="sxs-lookup"><span data-stu-id="88842-279">Example: An Event Query</span></span>

<span data-ttu-id="88842-280">Uma consulta de evento não dá suporte a um evento de início.</span><span class="sxs-lookup"><span data-stu-id="88842-280">An event query does not support a begin event.</span></span>

-   <span data-ttu-id="88842-281">Criar a consulta.</span><span class="sxs-lookup"><span data-stu-id="88842-281">Create the query.</span></span>
-   <span data-ttu-id="88842-282">Emita um evento de término.</span><span class="sxs-lookup"><span data-stu-id="88842-282">Issue an end event.</span></span>
-   <span data-ttu-id="88842-283">Sondagem até que a GPU esteja ociosa.</span><span class="sxs-lookup"><span data-stu-id="88842-283">Poll until the GPU is idle.</span></span>
-   <span data-ttu-id="88842-284">Emita um evento de término.</span><span class="sxs-lookup"><span data-stu-id="88842-284">Issue an end event.</span></span>


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="88842-285">Essa é a sequência de comandos usada por uma consulta de evento para criar o perfil de chamadas de API (interface de programação de aplicativo) (consulte com [precisão a criação de perfis do Direct3D API (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="88842-285">This is the sequence of commands an event query uses to profile application programming interface (API) calls (see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="88842-286">Essa sequência usa marcadores para ajudar a controlar a quantidade de trabalho no buffer de comando.</span><span class="sxs-lookup"><span data-stu-id="88842-286">This sequence uses markers to help control the amount of work in the command buffer.</span></span>

<span data-ttu-id="88842-287">Observe que os aplicativos devem prestar atenção especial ao grande custo associado à liberação do buffer de comando, pois isso faz com que o sistema operacional mude para o modo kernel, o que incorrerá em uma penalidade de desempenho considerável.</span><span class="sxs-lookup"><span data-stu-id="88842-287">Note that applications should pay special attention to the large cost associated with flushing the command buffer because this causes the operating system to switch into kernel mode, thus incurring a sizeable performance penalty.</span></span> <span data-ttu-id="88842-288">Os aplicativos também devem estar cientes do desperdício de ciclos de CPU aguardando a conclusão das consultas.</span><span class="sxs-lookup"><span data-stu-id="88842-288">Applications should also be aware of wasting CPU cycles by waiting for queries to complete.</span></span>

<span data-ttu-id="88842-289">As consultas são uma otimização a ser usada durante a renderização para aumentar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="88842-289">Queries are an optimization to be used during rendering to increase performance.</span></span> <span data-ttu-id="88842-290">Portanto, não é benéfico gastar tempo aguardando a conclusão de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="88842-290">Therefore, it is not beneficial to spend time waiting for a query to finish.</span></span> <span data-ttu-id="88842-291">Se uma consulta for emitida e se os resultados ainda não estiverem prontos no momento em que o aplicativo verificá-los, a tentativa de otimização não teve sucesso e a renderização deve continuar normalmente.</span><span class="sxs-lookup"><span data-stu-id="88842-291">If a query is issued and if the results are not yet ready by the time the application checks for them, the attempt at optimizing did not succeed and rendering should continue as normal.</span></span>

<span data-ttu-id="88842-292">O exemplo clássico disso é durante a remoção de oclusão.</span><span class="sxs-lookup"><span data-stu-id="88842-292">The classic example of this is during Occlusion Culling.</span></span> <span data-ttu-id="88842-293">Em vez do loop **while** acima, um aplicativo que usa consultas pode implementar a remoção de oclusão para verificar se uma consulta foi concluída no momento em que precisa do resultado.</span><span class="sxs-lookup"><span data-stu-id="88842-293">Instead of the **while** loop above, an application using queries can implement occlusion culling to check to see if a query had finished by the time it needs the result.</span></span> <span data-ttu-id="88842-294">Se a consulta não tiver sido concluída, continue (como um cenário de pior caso) como se o objeto que está sendo testado não for obstruído (ou seja, visível) e renderizá-lo.</span><span class="sxs-lookup"><span data-stu-id="88842-294">If the query has not finished, continue (as a worst-case scenario) as if the object being tested against is not occluded (i.e. it is visible) and render it.</span></span> <span data-ttu-id="88842-295">O código deve ser semelhante ao seguinte.</span><span class="sxs-lookup"><span data-stu-id="88842-295">The code would look similar to the following.</span></span>


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a><span data-ttu-id="88842-296">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="88842-296">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88842-297">Tópicos avançados</span><span class="sxs-lookup"><span data-stu-id="88842-297">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
