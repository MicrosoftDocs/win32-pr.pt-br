---
title: Função RtmEnumerateGetNextRoute (RTM. h)
description: A função RtmEnumerateGetNextRoute retorna a entrada Next-rota na enumeração iniciada por uma chamada para RtmCreateEnumerationHandle.
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- Função RtmEnumerateGetNextRoute RAS
topic_type:
- apiref
api_name:
- RtmEnumerateGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e74cc5aa15c1014056075e876efca296556066d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105785395"
---
# <a name="rtmenumerategetnextroute-function"></a><span data-ttu-id="b5fb1-104">Função RtmEnumerateGetNextRoute</span><span class="sxs-lookup"><span data-stu-id="b5fb1-104">RtmEnumerateGetNextRoute function</span></span>

<span data-ttu-id="b5fb1-105">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="b5fb1-106">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="b5fb1-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="b5fb1-107">A função **RtmEnumerateGetNextRoute** retorna a entrada Next-rota na enumeração iniciada por uma chamada para [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="b5fb1-107">The **RtmEnumerateGetNextRoute** function returns the next-route entry in the enumeration started by a call to [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b5fb1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5fb1-108">Syntax</span></span>


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a><span data-ttu-id="b5fb1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5fb1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5fb1-110">*EnumerationHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b5fb1-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5fb1-111">Identificador que identifica a enumeração e especifica seu escopo.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-111">Handle that identifies the enumeration and specifies its scope.</span></span> <span data-ttu-id="b5fb1-112">Obtenha esse identificador chamando [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span><span class="sxs-lookup"><span data-stu-id="b5fb1-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="b5fb1-113">*Rota* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b5fb1-113">*Route* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5fb1-114">Ponteiro para uma estrutura de rota específica da família de protocolos [**( \_ \_ rota de IP RTM**](rtm-ip-route.md) ou [**\_ \_ rota IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="b5fb1-114">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="b5fb1-115">Essa estrutura receberá a próxima rota na enumeração.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-115">This structure will receive the next route in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5fb1-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5fb1-116">Return value</span></span>

<span data-ttu-id="b5fb1-117">Se a função for realizada com sucesso, o valor de retorno não será um \_ erro.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-117">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="b5fb1-118">Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-118">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="b5fb1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b5fb1-119">Value</span></span>                                                                                                       | <span data-ttu-id="b5fb1-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5fb1-120">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b5fb1-121"><dt>**\_identificador inválido do erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5fb1-121"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="b5fb1-122">O parâmetro *EnumerationHandle* não é válido.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-122">The *EnumerationHandle* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="b5fb1-123"><dt>**ERRO \_ não há \_ mais \_ rotas**</dt></span><span class="sxs-lookup"><span data-stu-id="b5fb1-123"><dt>**ERROR\_NO\_MORE\_ROUTES**</dt></span></span> </dl>      | <span data-ttu-id="b5fb1-124">Não há mais rotas na enumeração.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-124">There are no more routes in the enumeration.</span></span><br/>                 |
| <dl> <span data-ttu-id="b5fb1-125"><dt>**ERRO \_ sem \_ recursos do sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b5fb1-125"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="b5fb1-126">Não há recursos suficientes para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-126">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b5fb1-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5fb1-127">Remarks</span></span>

<span data-ttu-id="b5fb1-128">Embora as rotas não sejam retornadas em nenhuma ordem específica, cada rota na enumeração é retornada apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="b5fb1-128">Although routes are not returned in any particular order, each route in the enumeration is returned only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5fb1-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5fb1-129">Requirements</span></span>



| <span data-ttu-id="b5fb1-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5fb1-130">Requirement</span></span> | <span data-ttu-id="b5fb1-131">Valor</span><span class="sxs-lookup"><span data-stu-id="b5fb1-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b5fb1-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5fb1-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b5fb1-133">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b5fb1-133">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b5fb1-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b5fb1-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b5fb1-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b5fb1-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b5fb1-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b5fb1-136">End of server support</span></span><br/>    | <span data-ttu-id="b5fb1-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b5fb1-137">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="b5fb1-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5fb1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5fb1-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5fb1-139"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5fb1-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5fb1-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="b5fb1-141"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b5fb1-141"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="b5fb1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b5fb1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5fb1-143"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5fb1-143"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5fb1-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5fb1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5fb1-145">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="b5fb1-145">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="b5fb1-146">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="b5fb1-146">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="b5fb1-147">**\_rota de IP RTM \_**</span><span class="sxs-lookup"><span data-stu-id="b5fb1-147">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="b5fb1-148">**\_rota IPX do RTM \_**</span><span class="sxs-lookup"><span data-stu-id="b5fb1-148">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="b5fb1-149">**RtmCloseEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="b5fb1-149">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="b5fb1-150">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="b5fb1-150">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 





