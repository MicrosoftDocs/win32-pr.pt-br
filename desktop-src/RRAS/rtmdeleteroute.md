---
title: Função RtmDeleteRoute (RTM. h)
description: A função RtmDeleteRoute exclui uma entrada de rota.
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- Função RtmDeleteRoute RAS
topic_type:
- apiref
api_name:
- RtmDeleteRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 310364bdb6e6ba7daf285316fcaaf16884e53929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918675"
---
# <a name="rtmdeleteroute-function"></a><span data-ttu-id="c0983-104">Função RtmDeleteRoute</span><span class="sxs-lookup"><span data-stu-id="c0983-104">RtmDeleteRoute function</span></span>

<span data-ttu-id="c0983-105">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c0983-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="c0983-106">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="c0983-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="c0983-107">A função **RtmDeleteRoute** exclui uma entrada de rota.</span><span class="sxs-lookup"><span data-stu-id="c0983-107">The **RtmDeleteRoute** function deletes a route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0983-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0983-108">Syntax</span></span>


```C++
DWORD RtmDeleteRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="c0983-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0983-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0983-110">*ClientHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0983-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0983-111">Identificador que identifica o cliente e, portanto, o protocolo de roteamento da rota adicionada ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="c0983-111">Handle that identifies the client and therefore the routing protocol of the added or updated route.</span></span> <span data-ttu-id="c0983-112">Obtenha esse identificador chamando [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="c0983-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0983-113">*Rota* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0983-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0983-114">Ponteiro para uma estrutura específica de família de protocolos que especifica a rota nova ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="c0983-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="c0983-115">Os campos a seguir são usados pelo Gerenciador de tabela de roteamento para atualizar a tabela de roteamento:</span><span class="sxs-lookup"><span data-stu-id="c0983-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="c0983-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c0983-116">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="c0983-117">Significado</span><span class="sxs-lookup"><span data-stu-id="c0983-117">Meaning</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="c0983-118"><dt>**\_Rede RR**</dt></span><span class="sxs-lookup"><span data-stu-id="c0983-118"><dt>**RR\_Network**</dt></span></span> </dl>                             | <span data-ttu-id="c0983-119">Especifica o número de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="c0983-119">Specifies the destination network number.</span></span> <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="c0983-120"><dt>**Tipo de registro de recurso \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0983-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>             | <span data-ttu-id="c0983-121">Especifica o índice da interface por meio da qual a rota foi recebida.</span><span class="sxs-lookup"><span data-stu-id="c0983-121">Specifies the index of the interface through which the route was received.</span></span><br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="c0983-122"><dt>**\_NEXTHOPADDRESS RR**</dt></span><span class="sxs-lookup"><span data-stu-id="c0983-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl> | <span data-ttu-id="c0983-123">Especifica o endereço de rede do roteador do próximo salto.</span><span class="sxs-lookup"><span data-stu-id="c0983-123">Specifies the network address of the next-hop router.</span></span><br/>                      |



 

</dd> <dt>

<span data-ttu-id="c0983-124">*Sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="c0983-124">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0983-125">Ponteiro para um conjunto de sinalizadores que indicam o tipo da mensagem de alteração e quais informações foram colocadas nos buffers fornecidos.</span><span class="sxs-lookup"><span data-stu-id="c0983-125">Pointer to a set of flags that indicate the type of the change message, and what information was placed in the provided buffers.</span></span> <span data-ttu-id="c0983-126">Esse parâmetro é um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0983-126">This parameter is one of the following values.</span></span>



| <span data-ttu-id="c0983-127">Flags</span><span class="sxs-lookup"><span data-stu-id="c0983-127">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="c0983-128">Significado</span><span class="sxs-lookup"><span data-stu-id="c0983-128">Meaning</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="c0983-129"><dt>**\_sem alteração no RTM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0983-129"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="c0983-130">A exclusão da rota não afetou a melhor rota para qualquer rede de destino.</span><span class="sxs-lookup"><span data-stu-id="c0983-130">Deleting the route did not affect the best route to any destination network.</span></span> <span data-ttu-id="c0983-131">Em outras palavras, outra entrada representa uma rota para a mesma rede de destino e tem uma métrica mais baixa.</span><span class="sxs-lookup"><span data-stu-id="c0983-131">In other words, another entry represents a route to the same destination network and has a lower metric.</span></span><br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="c0983-132"><dt>**\_rota RTM \_ excluída**</dt></span><span class="sxs-lookup"><span data-stu-id="c0983-132"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="c0983-133">A rota excluída foi a única rota disponível para uma rede de destino específica.</span><span class="sxs-lookup"><span data-stu-id="c0983-133">The route deleted was the only route available for a particular destination network.</span></span><br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="c0983-134"><dt>**\_rota RTM \_ alterada**</dt></span><span class="sxs-lookup"><span data-stu-id="c0983-134"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="c0983-135">Depois que essa rota foi excluída, outra rota se tornou a melhor rota para uma rede de destino específica.</span><span class="sxs-lookup"><span data-stu-id="c0983-135">After this route was deleted, another route became the best route to a particular destination network.</span></span> <span data-ttu-id="c0983-136">*CurBestRoute* aponta para as informações para a nova rota recomendada.</span><span class="sxs-lookup"><span data-stu-id="c0983-136">*CurBestRoute* points to the information for the new best route.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="c0983-137">*CurBestRoute* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c0983-137">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0983-138">Ponteiro para uma estrutura que recebe as informações atuais de melhor rota, se houver.</span><span class="sxs-lookup"><span data-stu-id="c0983-138">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="c0983-139">O tipo da estrutura é específico para a família de protocolos, por exemplo, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="c0983-139">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="c0983-140">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="c0983-140">This parameter is optional.</span></span> <span data-ttu-id="c0983-141">Se o chamador especificar **NULL** para esse parâmetro, as informações de melhor rota atuais não serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="c0983-141">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0983-142">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0983-142">Return value</span></span>

<span data-ttu-id="c0983-143">Se a função for realizada com sucesso, o valor de retorno **não será um \_ erro**.</span><span class="sxs-lookup"><span data-stu-id="c0983-143">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="c0983-144">Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0983-144">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="c0983-145">Valor</span><span class="sxs-lookup"><span data-stu-id="c0983-145">Value</span></span>                                                                                                       | <span data-ttu-id="c0983-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0983-146">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0983-147"><dt>**\_identificador inválido do erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0983-147"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="c0983-148">O parâmetro identificador do cliente não é um identificador válido.</span><span class="sxs-lookup"><span data-stu-id="c0983-148">The client handle parameter is not a valid handle.</span></span><br/>                                          |
| <dl> <span data-ttu-id="c0983-149"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0983-149"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="c0983-150">A estrutura de rota apontada pelo parâmetro de *rota* contém um valor de membro.</span><span class="sxs-lookup"><span data-stu-id="c0983-150">The route structure pointed to by the *Route* parameter contains a member value.</span></span><br/>            |
| <dl> <span data-ttu-id="c0983-151"><dt>**ERRO \_ sem \_ \_ rota**</dt></span><span class="sxs-lookup"><span data-stu-id="c0983-151"><dt>**ERROR\_NO\_SUCH\_ROUTE**</dt></span></span> </dl>       | <span data-ttu-id="c0983-152">Não há entradas na tabela de roteamento que correspondam aos parâmetros da rota especificada.</span><span class="sxs-lookup"><span data-stu-id="c0983-152">There are no entries in the routing table that match the parameters of the specified route.</span></span><br/> |
| <dl> <span data-ttu-id="c0983-153"><dt>**ERRO \_ sem \_ recursos do sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c0983-153"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="c0983-154">Não há recursos suficientes para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="c0983-154">There are insufficient resources to perform the operation.</span></span> <br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="c0983-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0983-155">Remarks</span></span>

<span data-ttu-id="c0983-156">A função gera uma mensagem de alteração de rota se a melhor rota para uma rede de destino foi alterada como resultado da exclusão.</span><span class="sxs-lookup"><span data-stu-id="c0983-156">The function generates a route-change message if the best route to a destination network has changed as the result of the deletion.</span></span> <span data-ttu-id="c0983-157">No entanto, a mensagem de alteração de rota não é enviada ao cliente que faz essa chamada.</span><span class="sxs-lookup"><span data-stu-id="c0983-157">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="c0983-158">Em vez disso, as informações relevantes são retornadas por essa função diretamente para esse cliente.</span><span class="sxs-lookup"><span data-stu-id="c0983-158">Instead, relevant information is returned by this function directly to that client.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0983-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0983-159">Requirements</span></span>



| <span data-ttu-id="c0983-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0983-160">Requirement</span></span> | <span data-ttu-id="c0983-161">Valor</span><span class="sxs-lookup"><span data-stu-id="c0983-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c0983-162">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0983-162">Minimum supported client</span></span><br/> | <span data-ttu-id="c0983-163">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c0983-163">None supported</span></span><br/>                                                          |
| <span data-ttu-id="c0983-164">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0983-164">Minimum supported server</span></span><br/> | <span data-ttu-id="c0983-165">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c0983-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c0983-166">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="c0983-166">End of server support</span></span><br/>    | <span data-ttu-id="c0983-167">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c0983-167">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="c0983-168">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0983-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0983-169"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0983-169"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0983-170">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0983-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="c0983-171"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0983-171"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="c0983-172">DLL</span><span class="sxs-lookup"><span data-stu-id="c0983-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0983-173"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0983-173"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0983-174">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0983-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0983-175">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="c0983-175">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="c0983-176">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="c0983-176">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="c0983-177">**RtmAddRoute**</span><span class="sxs-lookup"><span data-stu-id="c0983-177">**RtmAddRoute**</span></span>](rtmaddroute.md)
</dt> <dt>

[<span data-ttu-id="c0983-178">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="c0983-178">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





