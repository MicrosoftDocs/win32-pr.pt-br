---
title: Função RtmAddRoute (RTM. h)
description: A função RtmAddRoute adiciona uma entrada de rota ou atualiza uma entrada de rota existente.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- Função RtmAddRoute RAS
topic_type:
- apiref
api_name:
- RtmAddRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c3ee68c9b026fc37457819777e69d2be7984e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770127"
---
# <a name="rtmaddroute-function"></a><span data-ttu-id="e7e19-104">Função RtmAddRoute</span><span class="sxs-lookup"><span data-stu-id="e7e19-104">RtmAddRoute function</span></span>

<span data-ttu-id="e7e19-105">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e7e19-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="e7e19-106">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="e7e19-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="e7e19-107">A função **RtmAddRoute** adiciona uma entrada de rota ou atualiza uma entrada de rota existente.</span><span class="sxs-lookup"><span data-stu-id="e7e19-107">The **RtmAddRoute** function adds a route entry or updates an existing route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7e19-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e7e19-108">Syntax</span></span>


```C++
DWORD RtmAddRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _In_  DWORD  TimeToLive,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="e7e19-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e7e19-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7e19-110">*ClientHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7e19-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e19-111">Identificador que identifica o cliente e, portanto, o protocolo de roteamento, que adicionou ou atualizou a rota.</span><span class="sxs-lookup"><span data-stu-id="e7e19-111">Handle that identifies the client, and therefore the routing protocol, that added or updated the route.</span></span> <span data-ttu-id="e7e19-112">Obtenha esse identificador chamando [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="e7e19-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="e7e19-113">*Rota* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7e19-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e19-114">Ponteiro para uma estrutura específica de família de protocolos que especifica a rota nova ou atualizada.</span><span class="sxs-lookup"><span data-stu-id="e7e19-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="e7e19-115">Os campos a seguir são usados pelo Gerenciador de tabela de roteamento para atualizar a tabela de roteamento:</span><span class="sxs-lookup"><span data-stu-id="e7e19-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="e7e19-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e7e19-116">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="e7e19-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e7e19-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="e7e19-118"><dt>**\_Rede RR**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-118"><dt>**RR\_Network**</dt></span></span> </dl>                                                     | <span data-ttu-id="e7e19-119">Especifica o número de rede de destino.</span><span class="sxs-lookup"><span data-stu-id="e7e19-119">Specifies the destination network number.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="e7e19-120"><dt>**Tipo de registro de recurso \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>                                     | <span data-ttu-id="e7e19-121">Especifica o índice da interface por meio da qual a rota foi recebida.</span><span class="sxs-lookup"><span data-stu-id="e7e19-121">Specifies the index of the interface through which the route was received.</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="e7e19-122"><dt>**\_NEXTHOPADDRESS RR**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl>                         | <span data-ttu-id="e7e19-123">Especifica o endereço do roteador do próximo salto.</span><span class="sxs-lookup"><span data-stu-id="e7e19-123">Specifies the address of the next-hop router.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <span data-ttu-id="e7e19-124"><dt>**\_FAMILYSPECIFICDATA RR**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-124"><dt>**RR\_FamilySpecificData**</dt></span></span> </dl>         | <span data-ttu-id="e7e19-125">Especifica os dados que são específicos para a família de protocolos.</span><span class="sxs-lookup"><span data-stu-id="e7e19-125">Specifies data that is specific to the protocol family.</span></span> <span data-ttu-id="e7e19-126">Embora os dados sejam transparentes para o Gerenciador de tabela de roteamento, eles são considerados durante a comparação de rotas para determinar se as informações de rota foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="e7e19-126">Although the data is transparent to the routing table manager, it is considered when comparing routes to determine if route information has changed.</span></span> <span data-ttu-id="e7e19-127">Os dados também são usados para definir valores de métrica que são independentes do protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="e7e19-127">The data is also used to set metric values that are independent of the routing protocol.</span></span> <span data-ttu-id="e7e19-128">Consequentemente, esses dados são usados para determinar a melhor rota para a rede de destino.</span><span class="sxs-lookup"><span data-stu-id="e7e19-128">Consequently, this data is used to determine the best route for the destination network.</span></span><br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <span data-ttu-id="e7e19-129"><dt>**\_PROTOCOLSPECIFICDATA RR**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-129"><dt>**RR\_ProtocolSpecificData**</dt></span></span> </dl> | <span data-ttu-id="e7e19-130">Especifica os dados que são específicos para o protocolo de roteamento que forneceu a rota.</span><span class="sxs-lookup"><span data-stu-id="e7e19-130">Specifies data which is specific to the routing protocol that supplied the route.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <span data-ttu-id="e7e19-131"><dt>**\_Carimbo de data/hora RR**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-131"><dt>**RR\_TimeStamp**</dt></span></span> </dl>                                             | <span data-ttu-id="e7e19-132">Especifica a hora atual do sistema.</span><span class="sxs-lookup"><span data-stu-id="e7e19-132">Specifies the current system time.</span></span> <span data-ttu-id="e7e19-133">Esse campo é definido pelo Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="e7e19-133">This field is set by the routing table manager.</span></span><br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="e7e19-134">*TimeToLive* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e7e19-134">*TimeToLive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e19-135">Especifica o número de segundos que a rota especificada deve ser mantida na tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="e7e19-135">Specifies the number of seconds the specified route should be kept in the routing table.</span></span> <span data-ttu-id="e7e19-136">Se esse parâmetro for definido como infinito, a rota será mantida até ser explicitamente excluída.</span><span class="sxs-lookup"><span data-stu-id="e7e19-136">If this parameter is set to INFINITE, the route is kept until it is explicitly deleted.</span></span> <span data-ttu-id="e7e19-137">O limite atual para *TimeToLive* é 2147483 s (mais de 24 dias).</span><span class="sxs-lookup"><span data-stu-id="e7e19-137">The current limit for *TimeToLive* is 2147483 sec (24+ days).</span></span>

</dd> <dt>

<span data-ttu-id="e7e19-138">*Sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="e7e19-138">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e19-139">Ponteiro para uma variável **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="e7e19-139">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="e7e19-140">O valor dessa variável é definido pelo Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="e7e19-140">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="e7e19-141">O valor indica o tipo da alteração e quais informações foram retornadas nos buffers fornecidos.</span><span class="sxs-lookup"><span data-stu-id="e7e19-141">The value indicates the type of the change, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="e7e19-142">Esse parâmetro é um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="e7e19-142">This parameter is one of the following.</span></span>



| <span data-ttu-id="e7e19-143">Flags</span><span class="sxs-lookup"><span data-stu-id="e7e19-143">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="e7e19-144">Significado</span><span class="sxs-lookup"><span data-stu-id="e7e19-144">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="e7e19-145"><dt>**\_sem alteração no RTM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-145"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="e7e19-146">A adição ou atualização não alterou nenhum dos parâmetros de rota significativos ou a entrada de rota afetada não é a melhor rota entre as entradas da rede de destino.</span><span class="sxs-lookup"><span data-stu-id="e7e19-146">The addition or update either did not change any of the significant route parameters, or the route entry affected is not the best route among the entries for the destination network.</span></span><br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="e7e19-147"><dt>**\_rota RTM \_ adicionada**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-147"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="e7e19-148">A rota foi adicionada para a rede de destino.</span><span class="sxs-lookup"><span data-stu-id="e7e19-148">The route was added for the destination network.</span></span> <span data-ttu-id="e7e19-149">O parâmetro *CurBestRoute* aponta para as informações da rota adicionada.</span><span class="sxs-lookup"><span data-stu-id="e7e19-149">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="e7e19-150"><dt>**\_rota RTM \_ alterada**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-150"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="e7e19-151">Pelo menos um dos parâmetros significativos foi alterado para a melhor rota para a rede de destino.</span><span class="sxs-lookup"><span data-stu-id="e7e19-151">At least one of the significant parameters was changed for the best route to the destination network.</span></span> <span data-ttu-id="e7e19-152">Os parâmetros significativos são:</span><span class="sxs-lookup"><span data-stu-id="e7e19-152">The significant parameters are:</span></span> <br/> <span data-ttu-id="e7e19-153">Identificador de protocolo</span><span class="sxs-lookup"><span data-stu-id="e7e19-153">Protocol identifier</span></span><br/> <span data-ttu-id="e7e19-154">Índice de interface</span><span class="sxs-lookup"><span data-stu-id="e7e19-154">Interface index</span></span><br/> <span data-ttu-id="e7e19-155">Endereço do próximo salto</span><span class="sxs-lookup"><span data-stu-id="e7e19-155">Next-hop address</span></span><br/> <span data-ttu-id="e7e19-156">Protocolo-dados específicos da família (incluindo métricas de rota)</span><span class="sxs-lookup"><span data-stu-id="e7e19-156">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="e7e19-157">O parâmetro *PrevBestRoute* aponta para as informações de rota como estavam antes da alteração.</span><span class="sxs-lookup"><span data-stu-id="e7e19-157">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="e7e19-158">O parâmetro *CurBestRoute* aponta para as informações de rota atuais (ou seja, após a alteração).</span><span class="sxs-lookup"><span data-stu-id="e7e19-158">The *CurBestRoute* parameter points to the current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="e7e19-159">*CurBestRoute* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e7e19-159">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e19-160">Ponteiro para uma estrutura que recebe as informações atuais de melhor rota, se houver.</span><span class="sxs-lookup"><span data-stu-id="e7e19-160">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="e7e19-161">O tipo da estrutura é específico para a família de protocolos, por exemplo, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="e7e19-161">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="e7e19-162">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e7e19-162">This parameter is optional.</span></span> <span data-ttu-id="e7e19-163">Se o chamador especificar **NULL** para esse parâmetro, as informações de melhor rota atuais não serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="e7e19-163">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="e7e19-164">*PrevBestRoute* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e7e19-164">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7e19-165">Ponteiro para uma estrutura que recebe as informações de melhor rota anteriores, se houver.</span><span class="sxs-lookup"><span data-stu-id="e7e19-165">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="e7e19-166">O tipo da estrutura é específico para a família de protocolos, por exemplo, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="e7e19-166">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="e7e19-167">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="e7e19-167">This parameter is optional.</span></span> <span data-ttu-id="e7e19-168">Se o chamador especificar **NULL** para esse parâmetro, as informações de melhor rota anteriores não serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="e7e19-168">If the caller specifies **NULL** for this parameter the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7e19-169">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e7e19-169">Return value</span></span>

<span data-ttu-id="e7e19-170">O valor de retorno é um dos códigos a seguir.</span><span class="sxs-lookup"><span data-stu-id="e7e19-170">The return value is one of the following codes.</span></span>



| <span data-ttu-id="e7e19-171">Valor</span><span class="sxs-lookup"><span data-stu-id="e7e19-171">Value</span></span>                                                                                                       | <span data-ttu-id="e7e19-172">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7e19-172">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e7e19-173"><dt>**SEM \_ erros**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-173"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="e7e19-174">A rota foi adicionada ou atualizada com êxito.</span><span class="sxs-lookup"><span data-stu-id="e7e19-174">The route was added or updated successfully.</span></span><br/>                 |
| <dl> <span data-ttu-id="e7e19-175"><dt>**\_identificador inválido do erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-175"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="e7e19-176">O parâmetro identificador do cliente não é um identificador válido.</span><span class="sxs-lookup"><span data-stu-id="e7e19-176">The client handle parameter is not a valid handle.</span></span><br/>           |
| <dl> <span data-ttu-id="e7e19-177"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-177"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="e7e19-178">A estrutura de rota contém um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="e7e19-178">The route structure contains an invalid parameter.</span></span><br/>           |
| <dl> <span data-ttu-id="e7e19-179"><dt>**ERRO \_ sem \_ recursos do sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-179"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="e7e19-180">Não há recursos suficientes para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="e7e19-180">There are insufficient resources to carry out the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e7e19-181"><dt>**ERRO \_ de \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-181"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="e7e19-182">Memória insuficiente para alocar a entrada de rota.</span><span class="sxs-lookup"><span data-stu-id="e7e19-182">There is insufficient memory to allocate the route entry.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="e7e19-183">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7e19-183">Remarks</span></span>

<span data-ttu-id="e7e19-184">A função gera uma mensagem de alteração de rota se a melhor rota para uma rede de destino foi alterada como resultado dessa operação.</span><span class="sxs-lookup"><span data-stu-id="e7e19-184">The function generates a route-change message if the best route to a destination network has changed as the result of this operation.</span></span> <span data-ttu-id="e7e19-185">No entanto, a mensagem de alteração de rota não é enviada ao cliente que faz essa chamada.</span><span class="sxs-lookup"><span data-stu-id="e7e19-185">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="e7e19-186">Em vez disso, as informações relevantes são retornadas por essa função diretamente para esse cliente por meio dos parâmetros *flags*, *CurBestRoute* e *PrevBestRoute* .</span><span class="sxs-lookup"><span data-stu-id="e7e19-186">Instead, relevant information is returned by this function directly to that client through the *Flags*, *CurBestRoute*, and *PrevBestRoute* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7e19-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7e19-187">Requirements</span></span>



| <span data-ttu-id="e7e19-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7e19-188">Requirement</span></span> | <span data-ttu-id="e7e19-189">Valor</span><span class="sxs-lookup"><span data-stu-id="e7e19-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7e19-190">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7e19-190">Minimum supported client</span></span><br/> | <span data-ttu-id="e7e19-191">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e7e19-191">None supported</span></span><br/>                                                          |
| <span data-ttu-id="e7e19-192">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e7e19-192">Minimum supported server</span></span><br/> | <span data-ttu-id="e7e19-193">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e7e19-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e7e19-194">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e7e19-194">End of server support</span></span><br/>    | <span data-ttu-id="e7e19-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7e19-195">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="e7e19-196">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e7e19-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7e19-197"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-197"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7e19-198">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e7e19-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7e19-199"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-199"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="e7e19-200">DLL</span><span class="sxs-lookup"><span data-stu-id="e7e19-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7e19-201"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7e19-201"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7e19-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7e19-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7e19-203">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="e7e19-203">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="e7e19-204">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="e7e19-204">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="e7e19-205">**RtmDeleteRoute**</span><span class="sxs-lookup"><span data-stu-id="e7e19-205">**RtmDeleteRoute**</span></span>](rtmdeleteroute.md)
</dt> <dt>

[<span data-ttu-id="e7e19-206">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="e7e19-206">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





