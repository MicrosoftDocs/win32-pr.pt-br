---
title: Função RtmGetNextRoute (RTM. h)
description: A função RtmGetNextRoute retorna a próxima rota do subconjunto especificado de rotas na tabela.
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- Função RtmGetNextRoute RAS
topic_type:
- apiref
api_name:
- RtmGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8592855e0c30cef2ed43b7818badd336bc2ab6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499478"
---
# <a name="rtmgetnextroute-function"></a><span data-ttu-id="1f9ce-104">Função RtmGetNextRoute</span><span class="sxs-lookup"><span data-stu-id="1f9ce-104">RtmGetNextRoute function</span></span>

<span data-ttu-id="1f9ce-105">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1f9ce-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="1f9ce-106">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="1f9ce-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="1f9ce-107">A função **RtmGetNextRoute** retorna a próxima rota do subconjunto especificado de rotas na tabela.</span><span class="sxs-lookup"><span data-stu-id="1f9ce-107">The **RtmGetNextRoute** function returns the next route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f9ce-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f9ce-108">Syntax</span></span>


```C++
DWORD RtmGetNextRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="1f9ce-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f9ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f9ce-110">*ProtocolFamily* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f9ce-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f9ce-111">Especifica a família de protocolos de rotas a recuperar, por exemplo, IP ou IPX.</span><span class="sxs-lookup"><span data-stu-id="1f9ce-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="1f9ce-112">*EnumerationFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1f9ce-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f9ce-113">Especifica quais rotas devem ser enumeradas.</span><span class="sxs-lookup"><span data-stu-id="1f9ce-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="1f9ce-114">Esse parâmetro limita o conjunto de rotas excluídas a um subconjunto definido pelos seguintes sinalizadores e os valores nos membros correspondentes da estrutura apontada pelo parâmetro *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="1f9ce-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="1f9ce-115">Os sinalizadores são os mesmos usados em [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="1f9ce-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="1f9ce-116">*Rota* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="1f9ce-116">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f9ce-117">Na entrada, a *rota* aponta para uma estrutura específica da família de protocolos [**( \_ \_ rota IP RTM**](rtm-ip-route.md) ou [**\_ \_ rota IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="1f9ce-117">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="1f9ce-118">A função de chamada fornece valores de membro para esta estrutura.</span><span class="sxs-lookup"><span data-stu-id="1f9ce-118">The calling function provides member values for this structure.</span></span> <span data-ttu-id="1f9ce-119">Esses valores, em conjunto com o parâmetro *EnumerationFlags* , especificam o conjunto a partir do qual as rotas são retornadas.</span><span class="sxs-lookup"><span data-stu-id="1f9ce-119">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="1f9ce-120">Na saída, a *rota* aponta para uma estrutura que recebe a primeira rota correspondente aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="1f9ce-120">On output, *Route* points to a structure that receives the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f9ce-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1f9ce-121">Return value</span></span>

<span data-ttu-id="1f9ce-122">Se a função for realizada com sucesso, o valor de retorno **não será um \_ erro**.</span><span class="sxs-lookup"><span data-stu-id="1f9ce-122">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="1f9ce-123">Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f9ce-123">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="1f9ce-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1f9ce-124">Value</span></span>                                                                                                       | <span data-ttu-id="1f9ce-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f9ce-125">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1f9ce-126"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f9ce-126"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="1f9ce-127">Um dos parâmetros é inválido.</span><span class="sxs-lookup"><span data-stu-id="1f9ce-127">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="1f9ce-128"><dt>**ERRO \_ sem \_ rotas**</dt></span><span class="sxs-lookup"><span data-stu-id="1f9ce-128"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="1f9ce-129">Não há rotas que correspondam aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="1f9ce-129">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="1f9ce-130"><dt>**ERRO \_ sem \_ recursos do sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1f9ce-130"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="1f9ce-131">Não há recursos suficientes para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="1f9ce-131">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1f9ce-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f9ce-132">Remarks</span></span>

<span data-ttu-id="1f9ce-133">As rotas são retornadas na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="1f9ce-133">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="1f9ce-134">Número de rede</span><span class="sxs-lookup"><span data-stu-id="1f9ce-134">Network number</span></span>
2.  <span data-ttu-id="1f9ce-135">Protocolo de roteamento</span><span class="sxs-lookup"><span data-stu-id="1f9ce-135">Routing protocol</span></span>
3.  <span data-ttu-id="1f9ce-136">Identificador de interface</span><span class="sxs-lookup"><span data-stu-id="1f9ce-136">Interface identifier</span></span>
4.  <span data-ttu-id="1f9ce-137">Endereço do próximo salto</span><span class="sxs-lookup"><span data-stu-id="1f9ce-137">Next-hop address</span></span>

<span data-ttu-id="1f9ce-138">Essa função é menos eficiente do que as funções de identificador de enumeração correspondentes.</span><span class="sxs-lookup"><span data-stu-id="1f9ce-138">This function is less efficient than the corresponding enumeration handle functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f9ce-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f9ce-139">Requirements</span></span>



| <span data-ttu-id="1f9ce-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f9ce-140">Requirement</span></span> | <span data-ttu-id="1f9ce-141">Valor</span><span class="sxs-lookup"><span data-stu-id="1f9ce-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1f9ce-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f9ce-142">Minimum supported client</span></span><br/> | <span data-ttu-id="1f9ce-143">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1f9ce-143">None supported</span></span><br/>                                                          |
| <span data-ttu-id="1f9ce-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1f9ce-144">Minimum supported server</span></span><br/> | <span data-ttu-id="1f9ce-145">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1f9ce-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1f9ce-146">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1f9ce-146">End of server support</span></span><br/>    | <span data-ttu-id="1f9ce-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1f9ce-147">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="1f9ce-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f9ce-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f9ce-149"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f9ce-149"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f9ce-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1f9ce-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f9ce-151"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f9ce-151"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="1f9ce-152">DLL</span><span class="sxs-lookup"><span data-stu-id="1f9ce-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f9ce-153"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f9ce-153"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f9ce-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f9ce-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f9ce-155">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="1f9ce-155">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="1f9ce-156">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="1f9ce-156">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="1f9ce-157">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="1f9ce-157">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="1f9ce-158">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="1f9ce-158">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="1f9ce-159">**RtmEnumerateGetNextRoute**</span><span class="sxs-lookup"><span data-stu-id="1f9ce-159">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="1f9ce-160">**RtmGetFirstRoute**</span><span class="sxs-lookup"><span data-stu-id="1f9ce-160">**RtmGetFirstRoute**</span></span>](rtmgetfirstroute.md)
</dt> </dl>

 

 





