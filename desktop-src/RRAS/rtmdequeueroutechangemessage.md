---
title: Função RtmDequeueRouteChangeMessage (RTM. h)
description: A função RtmDequeueRouteChangeMessage retorna a próxima mensagem de alteração de rota na fila associada ao cliente especificado.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- Função RtmDequeueRouteChangeMessage RAS
topic_type:
- apiref
api_name:
- RtmDequeueRouteChangeMessage
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448df230742b03f82294de102bf14b50fefa035c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085792"
---
# <a name="rtmdequeueroutechangemessage-function"></a><span data-ttu-id="89d1b-104">Função RtmDequeueRouteChangeMessage</span><span class="sxs-lookup"><span data-stu-id="89d1b-104">RtmDequeueRouteChangeMessage function</span></span>

<span data-ttu-id="89d1b-105">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="89d1b-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="89d1b-106">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="89d1b-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="89d1b-107">A função **RtmDequeueRouteChangeMessage** retorna a próxima mensagem de alteração de rota na fila associada ao cliente especificado.</span><span class="sxs-lookup"><span data-stu-id="89d1b-107">The **RtmDequeueRouteChangeMessage** function returns the next route-change message in the queue associated with the specified client.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d1b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89d1b-108">Syntax</span></span>


```C++
DWORD RtmDequeueRouteChangeMessage(
  _In_  HANDLE ClientHandle,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="89d1b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89d1b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89d1b-110">*ClientHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="89d1b-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89d1b-111">Identificador que identifica o cliente para o qual a operação é executada.</span><span class="sxs-lookup"><span data-stu-id="89d1b-111">Handle that identifies the client for which the operation is performed.</span></span> <span data-ttu-id="89d1b-112">Obtenha esse identificador chamando [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="89d1b-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="89d1b-113">*Sinalizadores* \[ de fora\]</span><span class="sxs-lookup"><span data-stu-id="89d1b-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89d1b-114">Ponteiro para uma variável **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="89d1b-114">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="89d1b-115">O valor dessa variável é definido pelo Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="89d1b-115">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="89d1b-116">O valor especifica o tipo da mensagem de alteração e quais informações foram retornadas nos buffers fornecidos.</span><span class="sxs-lookup"><span data-stu-id="89d1b-116">The value specifies the type of the change message, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="89d1b-117">Esse parâmetro é um dos seguintes.</span><span class="sxs-lookup"><span data-stu-id="89d1b-117">This parameter is one of the following.</span></span>



| <span data-ttu-id="89d1b-118">Flags</span><span class="sxs-lookup"><span data-stu-id="89d1b-118">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="89d1b-119">Significado</span><span class="sxs-lookup"><span data-stu-id="89d1b-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="89d1b-120"><dt>**\_rota RTM \_ adicionada**</dt></span><span class="sxs-lookup"><span data-stu-id="89d1b-120"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="89d1b-121">A primeira rota foi adicionada para uma rede de destino específica.</span><span class="sxs-lookup"><span data-stu-id="89d1b-121">The first route was added for a particular destination network.</span></span> <span data-ttu-id="89d1b-122">O parâmetro *CurBestRoute* aponta para as informações da rota adicionada.</span><span class="sxs-lookup"><span data-stu-id="89d1b-122">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="89d1b-123"><dt>**\_rota RTM \_ excluída**</dt></span><span class="sxs-lookup"><span data-stu-id="89d1b-123"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="89d1b-124">A única rota disponível para uma rede de destino específica foi excluída.</span><span class="sxs-lookup"><span data-stu-id="89d1b-124">The only route available for a particular destination network was deleted.</span></span> <span data-ttu-id="89d1b-125">O parâmetro *PrevBestRoute* aponta para as informações da rota excluída.</span><span class="sxs-lookup"><span data-stu-id="89d1b-125">The *PrevBestRoute* parameter points to the information for the deleted route.</span></span><br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="89d1b-126"><dt>**\_rota RTM \_ alterada**</dt></span><span class="sxs-lookup"><span data-stu-id="89d1b-126"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="89d1b-127">Pelo menos um dos parâmetros significativos foi alterado para uma rota melhor para uma rede de destino específica.</span><span class="sxs-lookup"><span data-stu-id="89d1b-127">At least one of the significant parameters was changed for a best route to a particular destination network.</span></span> <span data-ttu-id="89d1b-128">Os parâmetros significativos são:</span><span class="sxs-lookup"><span data-stu-id="89d1b-128">The significant parameters are:</span></span> <br/> <span data-ttu-id="89d1b-129">Identificador de protocolo</span><span class="sxs-lookup"><span data-stu-id="89d1b-129">Protocol identifier</span></span><br/> <span data-ttu-id="89d1b-130">Índice de interface</span><span class="sxs-lookup"><span data-stu-id="89d1b-130">Interface index</span></span><br/> <span data-ttu-id="89d1b-131">Endereço do próximo salto</span><span class="sxs-lookup"><span data-stu-id="89d1b-131">Next-hop address</span></span><br/> <span data-ttu-id="89d1b-132">Protocolo-dados específicos da família (incluindo métricas de rota)</span><span class="sxs-lookup"><span data-stu-id="89d1b-132">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="89d1b-133">O parâmetro *PrevBestRoute* aponta para as informações de rota como estavam antes da alteração.</span><span class="sxs-lookup"><span data-stu-id="89d1b-133">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="89d1b-134">O parâmetro *CurBestRoute* aponta para as informações de rota atuais (ou seja, após a alteração).</span><span class="sxs-lookup"><span data-stu-id="89d1b-134">The *CurBestRoute* parameter points to current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="89d1b-135">*CurBestRoute* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="89d1b-135">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89d1b-136">Ponteiro para uma estrutura que recebe as informações atuais de melhor rota (se houver).</span><span class="sxs-lookup"><span data-stu-id="89d1b-136">Pointer to a structure that receives the current best-route information (if any).</span></span> <span data-ttu-id="89d1b-137">O tipo da estrutura é específico para a família de protocolos, por exemplo, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="89d1b-137">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="89d1b-138">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="89d1b-138">This parameter is optional.</span></span> <span data-ttu-id="89d1b-139">Se o chamador especificar **NULL** para esse parâmetro, as informações de melhor rota atuais não serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="89d1b-139">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="89d1b-140">*PrevBestRoute* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="89d1b-140">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89d1b-141">Ponteiro para uma estrutura que recebe as informações de melhor rota anteriores, se houver.</span><span class="sxs-lookup"><span data-stu-id="89d1b-141">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="89d1b-142">O tipo da estrutura é específico para a família de protocolos, por exemplo, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="89d1b-142">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="89d1b-143">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="89d1b-143">This parameter is optional.</span></span> <span data-ttu-id="89d1b-144">Se o chamador especificar **NULL** para esse parâmetro, as informações de melhor rota anteriores não serão retornadas.</span><span class="sxs-lookup"><span data-stu-id="89d1b-144">If the caller specifies **NULL** for this parameter, the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89d1b-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="89d1b-145">Return value</span></span>

<span data-ttu-id="89d1b-146">O valor de retorno é um dos códigos a seguir.</span><span class="sxs-lookup"><span data-stu-id="89d1b-146">The return value is one of the following codes.</span></span>



| <span data-ttu-id="89d1b-147">Valor</span><span class="sxs-lookup"><span data-stu-id="89d1b-147">Value</span></span>                                                                                                       | <span data-ttu-id="89d1b-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="89d1b-148">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89d1b-149"><dt>**SEM \_ erros**</dt></span><span class="sxs-lookup"><span data-stu-id="89d1b-149"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="89d1b-150">Esta mensagem foi a última mensagem na fila do cliente.</span><span class="sxs-lookup"><span data-stu-id="89d1b-150">This message was the last message in the client's queue.</span></span> <span data-ttu-id="89d1b-151">O objeto de evento é redefinido.</span><span class="sxs-lookup"><span data-stu-id="89d1b-151">The event object is reset.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="89d1b-152"><dt>**\_identificador inválido do erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="89d1b-152"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="89d1b-153">O parâmetro *ClientHandle* não é um identificador válido ou, no registro, o cliente não forneceu um objeto de evento para notificação de mensagem de alteração (consulte [**RtmRegisterClient**](rtmregisterclient.md)).</span><span class="sxs-lookup"><span data-stu-id="89d1b-153">The *ClientHandle* parameter is not a valid handle, or at registration the client did not provide an event object for change message notification (see [**RtmRegisterClient**](rtmregisterclient.md)).</span></span><br/>                           |
| <dl> <span data-ttu-id="89d1b-154"><dt>**ERRO de \_ mais \_ mensagens**</dt></span><span class="sxs-lookup"><span data-stu-id="89d1b-154"><dt>**ERROR\_MORE\_MESSAGES**</dt></span></span> </dl>        | <span data-ttu-id="89d1b-155">A fila do cliente contém mensagens adicionais.</span><span class="sxs-lookup"><span data-stu-id="89d1b-155">The client's queue contains additional messages.</span></span> <span data-ttu-id="89d1b-156">O cliente deve chamar **RtmDequeueRouteChangeMessage** novamente assim que possível para permitir que o Gerenciador de tabela de roteamento libere os recursos associados às mensagens pendentes.</span><span class="sxs-lookup"><span data-stu-id="89d1b-156">The client should call **RtmDequeueRouteChangeMessage** again as soon as possible to allow the routing table manager to free the resources associated with the pending messages.</span></span><br/> |
| <dl> <span data-ttu-id="89d1b-157"><dt>**ERRO \_ sem \_ mensagens**</dt></span><span class="sxs-lookup"><span data-stu-id="89d1b-157"><dt>**ERROR\_NO\_MESSAGES**</dt></span></span> </dl>          | <span data-ttu-id="89d1b-158">A fila do cliente não contém mensagens; a chamada não foi solicitada.</span><span class="sxs-lookup"><span data-stu-id="89d1b-158">The client's queue contains no messages; the call was unsolicited.</span></span> <span data-ttu-id="89d1b-159">O evento é redefinido.</span><span class="sxs-lookup"><span data-stu-id="89d1b-159">The event is reset.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="89d1b-160"><dt>**ERRO \_ sem \_ recursos do sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="89d1b-160"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="89d1b-161">Não há recursos suficientes para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="89d1b-161">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="89d1b-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89d1b-162">Requirements</span></span>



| <span data-ttu-id="89d1b-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="89d1b-163">Requirement</span></span> | <span data-ttu-id="89d1b-164">Valor</span><span class="sxs-lookup"><span data-stu-id="89d1b-164">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="89d1b-165">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89d1b-165">Minimum supported client</span></span><br/> | <span data-ttu-id="89d1b-166">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="89d1b-166">None supported</span></span><br/>                                                          |
| <span data-ttu-id="89d1b-167">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="89d1b-167">Minimum supported server</span></span><br/> | <span data-ttu-id="89d1b-168">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="89d1b-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="89d1b-169">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="89d1b-169">End of server support</span></span><br/>    | <span data-ttu-id="89d1b-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="89d1b-170">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="89d1b-171">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89d1b-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="89d1b-172"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="89d1b-172"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="89d1b-173">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89d1b-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="89d1b-174"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89d1b-174"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="89d1b-175">DLL</span><span class="sxs-lookup"><span data-stu-id="89d1b-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89d1b-176"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89d1b-176"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89d1b-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="89d1b-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89d1b-178">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="89d1b-178">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="89d1b-179">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="89d1b-179">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="89d1b-180">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="89d1b-180">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





