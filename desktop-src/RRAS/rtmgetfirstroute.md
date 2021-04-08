---
title: Função RtmGetFirstRoute (RTM. h)
description: A função RtmGetFirstRoute retorna a primeira rota do subconjunto especificado de rotas na tabela.
ms.assetid: f2071b50-4b06-432f-8dbf-45696f8a5cb1
keywords:
- Função RtmGetFirstRoute RAS
topic_type:
- apiref
api_name:
- RtmGetFirstRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e98a5deb0f925fbf3b27c21302060bbe4869b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085791"
---
# <a name="rtmgetfirstroute-function"></a><span data-ttu-id="9522f-104">Função RtmGetFirstRoute</span><span class="sxs-lookup"><span data-stu-id="9522f-104">RtmGetFirstRoute function</span></span>

<span data-ttu-id="9522f-105">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9522f-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="9522f-106">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="9522f-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="9522f-107">A função **RtmGetFirstRoute** retorna a primeira rota do subconjunto especificado de rotas na tabela.</span><span class="sxs-lookup"><span data-stu-id="9522f-107">The **RtmGetFirstRoute** function returns the first route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="9522f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9522f-108">Syntax</span></span>


```C++
DWORD RtmGetFirstRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="9522f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9522f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9522f-110">*ProtocolFamily* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9522f-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9522f-111">Especifica a família de protocolos de rotas a recuperar, por exemplo, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="9522f-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="9522f-112">*EnumerationFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9522f-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9522f-113">Especifica o limita o conjunto de rotas excluídas a um subconjunto definido por esses sinalizadores e os valores nos membros correspondentes da estrutura apontada pelo parâmetro *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="9522f-113">Specifies the limits the set of deleted routes to a subset defined by these flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="9522f-114">Os sinalizadores são os mesmos usados em [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="9522f-114">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="9522f-115">*Rota* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="9522f-115">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9522f-116">Na entrada, a *rota* aponta para uma estrutura específica da família de protocolos [**( \_ \_ rota IP RTM**](rtm-ip-route.md) ou [**\_ \_ rota IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="9522f-116">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="9522f-117">A função de chamada fornece valores de membro para esta estrutura.</span><span class="sxs-lookup"><span data-stu-id="9522f-117">The calling function provides member values for this structure.</span></span> <span data-ttu-id="9522f-118">Esses valores, em conjunto com o parâmetro *EnumerationFlags* , especificam o conjunto a partir do qual as rotas são retornadas.</span><span class="sxs-lookup"><span data-stu-id="9522f-118">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="9522f-119">Saída, a *rota* aponta para a primeira rota que correspondeu aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="9522f-119">Out output, *Route* points to the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9522f-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9522f-120">Return value</span></span>

<span data-ttu-id="9522f-121">Se a função for realizada com sucesso, o valor de retorno não será um \_ erro.</span><span class="sxs-lookup"><span data-stu-id="9522f-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="9522f-122">Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="9522f-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="9522f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9522f-123">Value</span></span>                                                                                                       | <span data-ttu-id="9522f-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="9522f-124">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9522f-125"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9522f-125"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="9522f-126">Um dos parâmetros é inválido.</span><span class="sxs-lookup"><span data-stu-id="9522f-126">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="9522f-127"><dt>**ERRO \_ sem \_ rotas**</dt></span><span class="sxs-lookup"><span data-stu-id="9522f-127"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="9522f-128">Não há rotas que correspondam aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="9522f-128">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="9522f-129"><dt>**ERRO \_ sem \_ recursos do sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9522f-129"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="9522f-130">Não há recursos suficientes para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="9522f-130">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9522f-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="9522f-131">Remarks</span></span>

<span data-ttu-id="9522f-132">As rotas são retornadas na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="9522f-132">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="9522f-133">Número de rede</span><span class="sxs-lookup"><span data-stu-id="9522f-133">Network number</span></span>
2.  <span data-ttu-id="9522f-134">Protocolo de roteamento</span><span class="sxs-lookup"><span data-stu-id="9522f-134">Routing protocol</span></span>
3.  <span data-ttu-id="9522f-135">Identificador de interface</span><span class="sxs-lookup"><span data-stu-id="9522f-135">Interface identifier</span></span>
4.  <span data-ttu-id="9522f-136">Endereço do próximo salto</span><span class="sxs-lookup"><span data-stu-id="9522f-136">Next-hop address</span></span>

<span data-ttu-id="9522f-137">Essa função é menos eficiente do que a função de identificador de enumeração correspondente, [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md).</span><span class="sxs-lookup"><span data-stu-id="9522f-137">This function is less efficient than the corresponding enumeration handle function, [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9522f-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9522f-138">Requirements</span></span>



| <span data-ttu-id="9522f-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="9522f-139">Requirement</span></span> | <span data-ttu-id="9522f-140">Valor</span><span class="sxs-lookup"><span data-stu-id="9522f-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9522f-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9522f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="9522f-142">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9522f-142">None supported</span></span><br/>                                                          |
| <span data-ttu-id="9522f-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9522f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="9522f-144">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9522f-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9522f-145">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="9522f-145">End of server support</span></span><br/>    | <span data-ttu-id="9522f-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9522f-146">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="9522f-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9522f-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="9522f-148"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="9522f-148"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="9522f-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9522f-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="9522f-150"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9522f-150"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="9522f-151">DLL</span><span class="sxs-lookup"><span data-stu-id="9522f-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9522f-152"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9522f-152"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9522f-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="9522f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9522f-154">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="9522f-154">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="9522f-155">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="9522f-155">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="9522f-156">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="9522f-156">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="9522f-157">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="9522f-157">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="9522f-158">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="9522f-158">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="9522f-159">**RtmGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="9522f-159">**RtmGetNextRoute**</span></span>](rtmgetnextroute.md)
</dt> </dl>

 

 





