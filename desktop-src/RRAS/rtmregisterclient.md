---
title: Função RtmRegisterClient (RTM. h)
description: A função RtmRegisterClient registra um cliente como um manipulador do protocolo especificado. Ele estabelece um mecanismo de notificação de alteração de rota para o cliente e define as opções de protocolo.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- Função RtmRegisterClient RAS
topic_type:
- apiref
api_name:
- RtmRegisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 564f47e68fd6cdce3d5437fe184bac1ed74d8322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645052"
---
# <a name="rtmregisterclient-function"></a><span data-ttu-id="bffe3-105">Função RtmRegisterClient</span><span class="sxs-lookup"><span data-stu-id="bffe3-105">RtmRegisterClient function</span></span>

<span data-ttu-id="bffe3-106">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bffe3-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="bffe3-107">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="bffe3-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="bffe3-108">A função **RtmRegisterClient** registra um cliente como um manipulador do protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="bffe3-108">The **RtmRegisterClient** function registers a client as a handler of the specified protocol.</span></span> <span data-ttu-id="bffe3-109">Ele estabelece um mecanismo de notificação de alteração de rota para o cliente e define as opções de protocolo.</span><span class="sxs-lookup"><span data-stu-id="bffe3-109">It establishes a route change notification mechanism for the client, and sets protocol options.</span></span>

## <a name="syntax"></a><span data-ttu-id="bffe3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bffe3-110">Syntax</span></span>


```C++
HANDLE RtmRegisterClient(
  _In_ DWORD  ProtocolFamily,
  _In_ DWORD  RoutingProtocol,
  _In_ HANDLE ChangeEvent,
  _In_ DWORD  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="bffe3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bffe3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bffe3-112">*ProtocolFamily* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bffe3-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bffe3-113">Especifica a família de protocolos do protocolo de roteamento a ser registrado.</span><span class="sxs-lookup"><span data-stu-id="bffe3-113">Specifies the protocol family of the routing protocol to register.</span></span>

</dd> <dt>

<span data-ttu-id="bffe3-114">*RoutingProtocol* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bffe3-114">*RoutingProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bffe3-115">Especifica o identificador do protocolo de roteamento, o mesmo usado durante o registro com o Gerenciador do roteador.</span><span class="sxs-lookup"><span data-stu-id="bffe3-115">Specifies the routing protocol identifier, the same as that used when registering with the router manager.</span></span> <span data-ttu-id="bffe3-116">Consulte [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).</span><span class="sxs-lookup"><span data-stu-id="bffe3-116">See [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).</span></span>

</dd> <dt>

<span data-ttu-id="bffe3-117">*ChangeEvent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bffe3-117">*ChangeEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bffe3-118">Especifica que uma melhor rota para uma rede na tabela foi alterada.</span><span class="sxs-lookup"><span data-stu-id="bffe3-118">Specifies that a best route to a network in the table has changed.</span></span> <span data-ttu-id="bffe3-119">O Gerenciador de tabela de roteamento sinaliza esse evento após uma alteração na melhor rota para qualquer rede na tabela.</span><span class="sxs-lookup"><span data-stu-id="bffe3-119">The routing table manager signals this event after a change to the best route to any network in the table.</span></span> <span data-ttu-id="bffe3-120">Consulte [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) para obter mais informações sobre a notificação de alteração de rota.</span><span class="sxs-lookup"><span data-stu-id="bffe3-120">See [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) for more information about route-change notification.</span></span>

<span data-ttu-id="bffe3-121">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="bffe3-121">This parameter is optional.</span></span> <span data-ttu-id="bffe3-122">Se o chamador especificar **NULL** para esse parâmetro, o Gerenciador de tabela de roteamento não notificará o cliente sobre as alterações no melhor status de rota.</span><span class="sxs-lookup"><span data-stu-id="bffe3-122">If the caller specifies **NULL** for this parameter, the routing table manager does not notify the client of changes in best route status.</span></span>

</dd> <dt>

<span data-ttu-id="bffe3-123">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="bffe3-123">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bffe3-124">Especifica opções diversas para tratamento especial do protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="bffe3-124">Specifies miscellaneous options for special handling of the routing protocol.</span></span> <span data-ttu-id="bffe3-125">No momento, há suporte para o seguinte valor.</span><span class="sxs-lookup"><span data-stu-id="bffe3-125">The following value is currently supported.</span></span>



| <span data-ttu-id="bffe3-126">Flags</span><span class="sxs-lookup"><span data-stu-id="bffe3-126">Flags</span></span>                                                                                                                                                                                               | <span data-ttu-id="bffe3-127">Significado</span><span class="sxs-lookup"><span data-stu-id="bffe3-127">Meaning</span></span>                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <span data-ttu-id="bffe3-128"><dt>**\_ \_ rota única do protocolo RTM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bffe3-128"><dt>**RTM\_PROTOCOL\_SINGLE\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="bffe3-129">O Gerenciador de tabela de roteamento mantém apenas uma rota por rede de destino para o protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="bffe3-129">The routing table manager keeps only one route per destination network for the routing protocol.</span></span> <span data-ttu-id="bffe3-130">Em outras palavras, o Gerenciador de tabela de roteamento substitui as entradas de rota que têm os mesmos números de rede de destino em vez de adicionar novas.</span><span class="sxs-lookup"><span data-stu-id="bffe3-130">In other words, the routing table manager replaces route entries that have the same destination network numbers instead of adding new ones.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bffe3-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bffe3-131">Return value</span></span>

<span data-ttu-id="bffe3-132">No retorno bem-sucedido, um valor de **identificador** que identifica o cliente em chamadas subsequentes para o Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="bffe3-132">On successful return, a **HANDLE** value that identifies the client in subsequent calls to the routing table manager.</span></span>

<span data-ttu-id="bffe3-133">Um identificador **nulo** indica que o Gerenciador de tabelas de roteamento não pôde registrar o cliente.</span><span class="sxs-lookup"><span data-stu-id="bffe3-133">A **NULL** handle indicates that the routing table manager was unable to register the client.</span></span> <span data-ttu-id="bffe3-134">Chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="bffe3-134">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain the reason for the failure.</span></span>



| <span data-ttu-id="bffe3-135">Valor</span><span class="sxs-lookup"><span data-stu-id="bffe3-135">Value</span></span>                                                                                                         | <span data-ttu-id="bffe3-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="bffe3-136">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bffe3-137"><dt>**o \_ cliente de erro \_ já \_ existe**</dt></span><span class="sxs-lookup"><span data-stu-id="bffe3-137"><dt>**ERROR\_CLIENT\_ALREADY\_EXISTS**</dt></span></span> </dl> | <span data-ttu-id="bffe3-138">Outro cliente já se registrou para manipular o protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="bffe3-138">Another client has already registered to handle the specified protocol.</span></span><br/>              |
| <dl> <span data-ttu-id="bffe3-139"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bffe3-139"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>      | <span data-ttu-id="bffe3-140">A família de protocolos especificada não tem suporte ou o parâmetro *flags* é inválido.</span><span class="sxs-lookup"><span data-stu-id="bffe3-140">The specified protocol family is not supported, or the *Flags* parameter is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="bffe3-141"><dt>**ERRO \_ sem \_ recursos do sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bffe3-141"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl>   | <span data-ttu-id="bffe3-142">Recursos insuficientes para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="bffe3-142">Insufficient resources to carry out the operation.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bffe3-143"><dt>**ERRO \_ de \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bffe3-143"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>     | <span data-ttu-id="bffe3-144">Memória insuficiente para alocar estruturas de dados para o cliente.</span><span class="sxs-lookup"><span data-stu-id="bffe3-144">Insufficient memory to allocate data structures for the client.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="bffe3-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bffe3-145">Requirements</span></span>



| <span data-ttu-id="bffe3-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="bffe3-146">Requirement</span></span> | <span data-ttu-id="bffe3-147">Valor</span><span class="sxs-lookup"><span data-stu-id="bffe3-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bffe3-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bffe3-148">Minimum supported client</span></span><br/> | <span data-ttu-id="bffe3-149">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bffe3-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="bffe3-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bffe3-150">Minimum supported server</span></span><br/> | <span data-ttu-id="bffe3-151">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bffe3-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bffe3-152">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="bffe3-152">End of server support</span></span><br/>    | <span data-ttu-id="bffe3-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bffe3-153">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="bffe3-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bffe3-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="bffe3-155"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="bffe3-155"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="bffe3-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bffe3-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="bffe3-157"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bffe3-157"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="bffe3-158">DLL</span><span class="sxs-lookup"><span data-stu-id="bffe3-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bffe3-159"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bffe3-159"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bffe3-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="bffe3-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bffe3-161">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="bffe3-161">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="bffe3-162">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="bffe3-162">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="bffe3-163">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="bffe3-163">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="bffe3-164">**RegisterProtocol**</span><span class="sxs-lookup"><span data-stu-id="bffe3-164">**RegisterProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[<span data-ttu-id="bffe3-165">Identificadores da família de protocolos RTMv1</span><span class="sxs-lookup"><span data-stu-id="bffe3-165">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[<span data-ttu-id="bffe3-166">**RtmDequeueRouteChangeMessage**</span><span class="sxs-lookup"><span data-stu-id="bffe3-166">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> <dt>

[<span data-ttu-id="bffe3-167">**RtmDeregisterClient**</span><span class="sxs-lookup"><span data-stu-id="bffe3-167">**RtmDeregisterClient**</span></span>](rtmderegisterclient.md)
</dt> </dl>

 

