---
title: Função RtmCreateEnumerationHandle (RTM. h)
description: A função RtmCreateEnumerationHandle retorna um identificador a ser usado com RtmEnumerateGetNextRoute para examinar todas as rotas ou um subconjunto de rotas, conhecido pelo Gerenciador de tabelas de roteamento.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- Função RtmCreateEnumerationHandle RAS
topic_type:
- apiref
api_name:
- RtmCreateEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14086639db299038139e0e7d02eb12bb892042bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085281"
---
# <a name="rtmcreateenumerationhandle-function"></a><span data-ttu-id="e31f3-104">Função RtmCreateEnumerationHandle</span><span class="sxs-lookup"><span data-stu-id="e31f3-104">RtmCreateEnumerationHandle function</span></span>

<span data-ttu-id="e31f3-105">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e31f3-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="e31f3-106">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="e31f3-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="e31f3-107">A função **RtmCreateEnumerationHandle** retorna um identificador a ser usado com [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) para examinar todas as rotas ou um subconjunto de rotas, conhecido pelo Gerenciador de tabelas de roteamento.</span><span class="sxs-lookup"><span data-stu-id="e31f3-107">The **RtmCreateEnumerationHandle** function returns a handle to use with [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) to scan through all routes, or a subset of routes, known to the routing table manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="e31f3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e31f3-108">Syntax</span></span>


```C++
HANDLE RtmCreateEnumerationHandle(
  _In_ DWORD ProtocolFamily,
  _In_ DWORD EnumerationFlags,
  _In_ PVOID CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="e31f3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e31f3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e31f3-110">*ProtocolFamily* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e31f3-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31f3-111">Especifica a família de protocolos das rotas a serem enumeradas.</span><span class="sxs-lookup"><span data-stu-id="e31f3-111">Specifies the protocol family of the routes to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="e31f3-112">*EnumerationFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e31f3-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31f3-113">Especifica quais rotas devem ser enumeradas.</span><span class="sxs-lookup"><span data-stu-id="e31f3-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="e31f3-114">Esse parâmetro limita o conjunto de rotas retornado pela API de enumeração a um subconjunto definido pelos seguintes sinalizadores e os valores nos membros correspondentes da estrutura apontada pelo parâmetro *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="e31f3-114">This parameter limits the set of routes returned by the enumeration API to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="e31f3-115">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="e31f3-115">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="e31f3-116">EnumerationFlags</span><span class="sxs-lookup"><span data-stu-id="e31f3-116">EnumerationFlags</span></span>                                                                                                                                                                              | <span data-ttu-id="e31f3-117">Significado</span><span class="sxs-lookup"><span data-stu-id="e31f3-117">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <span data-ttu-id="e31f3-118"><dt>**\_somente RTM \_ desta \_ rede**</dt></span><span class="sxs-lookup"><span data-stu-id="e31f3-118"><dt>**RTM\_ONLY\_THIS\_NETWORK**</dt></span></span> </dl>       | <span data-ttu-id="e31f3-119">Enumere somente as rotas que têm o mesmo número de rede que o \_ membro de rede RR da estrutura apontada por CriteriaRoute.</span><span class="sxs-lookup"><span data-stu-id="e31f3-119">Enumerate only those routes that have the same network number as the RR\_Network member of the structure pointed to by CriteriaRoute.</span></span><br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <span data-ttu-id="e31f3-120"><dt>**RTM \_ somente \_ esta \_ interface**</dt></span><span class="sxs-lookup"><span data-stu-id="e31f3-120"><dt>**RTM\_ONLY\_THIS\_INTERFACE**</dt></span></span> </dl> | <span data-ttu-id="e31f3-121">Enumere somente as rotas que foram obtidas por meio da interface especificada pelo campo do RR \_ InterfaceName da estrutura apontada por CriteriaRoute.</span><span class="sxs-lookup"><span data-stu-id="e31f3-121">Enumerate only those routes that were obtained through the interface specified by the RR\_InterfaceID field of the structure pointed to by CriteriaRoute.</span></span><br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <span data-ttu-id="e31f3-122"><dt>**RTM \_ somente \_ esse \_ protocolo**</dt></span><span class="sxs-lookup"><span data-stu-id="e31f3-122"><dt>**RTM\_ONLY\_THIS\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="e31f3-123">Enumere somente as rotas que foram adicionadas pelo protocolo de roteamento especificado pelo \_ campo RR RoutingProtocol da estrutura apontada por CriteriaRoute.</span><span class="sxs-lookup"><span data-stu-id="e31f3-123">Enumerate only those routes that were added by the routing protocol specified by the RR\_RoutingProtocol field of the structure pointed to by CriteriaRoute.</span></span><br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <span data-ttu-id="e31f3-124"><dt>**\_somente \_ as melhores \_ rotas do RTM**</dt></span><span class="sxs-lookup"><span data-stu-id="e31f3-124"><dt>**RTM\_ONLY\_BEST\_ROUTES**</dt></span></span> </dl>          | <span data-ttu-id="e31f3-125">Enumere apenas as melhores rotas para cada uma das redes no conjunto.</span><span class="sxs-lookup"><span data-stu-id="e31f3-125">Enumerate only the best routes to each of the networks in the set.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="e31f3-126">*CriteriaRoute* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e31f3-126">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31f3-127">Ponteiro para uma estrutura de rota específica da família de protocolos [**( \_ \_ rota de IP RTM**](rtm-ip-route.md) ou [**\_ \_ rota IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="e31f3-127">Pointer to a protocol-family-specific route structure ([**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="e31f3-128">Os valores de membro nessa estrutura correspondem aos sinalizadores especificados pelo parâmetro *EnumerationFlags* .</span><span class="sxs-lookup"><span data-stu-id="e31f3-128">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e31f3-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e31f3-129">Return value</span></span>

<span data-ttu-id="e31f3-130">Se a função for realizada com sucesso, o valor de retorno será um **identificador** a ser usado com as chamadas de enumeração subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e31f3-130">If the function succeeds, the return value is a **HANDLE** to use with subsequent enumeration calls.</span></span>

<span data-ttu-id="e31f3-131">Se a função falhar ou não houver rotas com os critérios especificados, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e31f3-131">If the function fails, or no routes exist with the specified criteria, the return value is **NULL**.</span></span> <span data-ttu-id="e31f3-132">Chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="e31f3-132">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="e31f3-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e31f3-133">Value</span></span>                                                                                                       | <span data-ttu-id="e31f3-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="e31f3-134">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e31f3-135"><dt>**ERRO \_ sem \_ rotas**</dt></span><span class="sxs-lookup"><span data-stu-id="e31f3-135"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="e31f3-136">Não há rotas com os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="e31f3-136">There are no routes that have the specified criteria.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="e31f3-137"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e31f3-137"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="e31f3-138">Um ou mais dos parâmetros de entrada são inválidos (por exemplo, família de protocolos desconhecida, sinalizadores de enumeração inválidos).</span><span class="sxs-lookup"><span data-stu-id="e31f3-138">One or more of the input parameters is invalid (for example, unknown protocol family, invalid enumeration flags).</span></span><br/> |
| <dl> <span data-ttu-id="e31f3-139"><dt>**ERRO \_ sem \_ recursos do sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e31f3-139"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="e31f3-140">Não há recursos suficientes para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="e31f3-140">There are insufficient resources to carry out the operation.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="e31f3-141"><dt>**ERRO \_ de \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e31f3-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="e31f3-142">Memória insuficiente para alocar o identificador.</span><span class="sxs-lookup"><span data-stu-id="e31f3-142">There is insufficient memory to allocate the handle.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="e31f3-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e31f3-143">Requirements</span></span>



| <span data-ttu-id="e31f3-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="e31f3-144">Requirement</span></span> | <span data-ttu-id="e31f3-145">Valor</span><span class="sxs-lookup"><span data-stu-id="e31f3-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e31f3-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e31f3-146">Minimum supported client</span></span><br/> | <span data-ttu-id="e31f3-147">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e31f3-147">None supported</span></span><br/>                                                          |
| <span data-ttu-id="e31f3-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e31f3-148">Minimum supported server</span></span><br/> | <span data-ttu-id="e31f3-149">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e31f3-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e31f3-150">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e31f3-150">End of server support</span></span><br/>    | <span data-ttu-id="e31f3-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e31f3-151">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="e31f3-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e31f3-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="e31f3-153"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e31f3-153"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="e31f3-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e31f3-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="e31f3-155"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e31f3-155"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="e31f3-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e31f3-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e31f3-157"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e31f3-157"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e31f3-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="e31f3-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e31f3-159">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="e31f3-159">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="e31f3-160">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="e31f3-160">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="e31f3-161">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="e31f3-161">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="e31f3-162">**\_rota de IP RTM \_**</span><span class="sxs-lookup"><span data-stu-id="e31f3-162">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="e31f3-163">**\_rota IPX do RTM \_**</span><span class="sxs-lookup"><span data-stu-id="e31f3-163">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="e31f3-164">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="e31f3-164">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="e31f3-165">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="e31f3-165">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 

