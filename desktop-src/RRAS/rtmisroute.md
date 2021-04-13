---
title: Função RtmIsRoute (RTM. h)
description: A função RtmIsRoute determina se existe uma ou mais rotas para uma rede de destino especificada. Nesse caso, a função retorna informações para a melhor rota para essa rede.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- Função RtmIsRoute RAS
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64621732f2f7a35223421e5f0fc86a309d332c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455648"
---
# <a name="rtmisroute-function"></a><span data-ttu-id="09f6f-105">Função RtmIsRoute</span><span class="sxs-lookup"><span data-stu-id="09f6f-105">RtmIsRoute function</span></span>

<span data-ttu-id="09f6f-106">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="09f6f-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="09f6f-107">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="09f6f-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="09f6f-108">A função **RtmIsRoute** determina se existe uma ou mais rotas para uma rede de destino especificada.</span><span class="sxs-lookup"><span data-stu-id="09f6f-108">The **RtmIsRoute** function determines if one or more routes to a specified destination network exist.</span></span> <span data-ttu-id="09f6f-109">Nesse caso, a função retorna informações para a melhor rota para essa rede.</span><span class="sxs-lookup"><span data-stu-id="09f6f-109">If so, the function returns information for the best route to that network.</span></span>

## <a name="syntax"></a><span data-ttu-id="09f6f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09f6f-110">Syntax</span></span>


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="09f6f-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09f6f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09f6f-112">*ProtocolFamily* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09f6f-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09f6f-113">Especifica o tipo de estrutura de dados apontado pelo parâmetro de *rede* , por exemplo [**, \_ rede IP**](ip-network.md), [**\_ rede IPX**](ipx-network.md).</span><span class="sxs-lookup"><span data-stu-id="09f6f-113">Specifies the type of data structure pointed to by the *Network* parameter, for example, [**IP\_NETWORK**](ip-network.md), [**IPX\_NETWORK**](ipx-network.md).</span></span>

</dd> <dt>

<span data-ttu-id="09f6f-114">*Rede* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="09f6f-114">*Network* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09f6f-115">Ponteiro para uma estrutura que especifica dados de número de rede específicos da família de protocolos.</span><span class="sxs-lookup"><span data-stu-id="09f6f-115">Pointer to a structure that specifies protocol-family-specific network number data.</span></span> <span data-ttu-id="09f6f-116">Esses dados identificam a rede para a qual o chamador busca informações de rota.</span><span class="sxs-lookup"><span data-stu-id="09f6f-116">This data identifies the network for which the caller seeks route information.</span></span>

</dd> <dt>

<span data-ttu-id="09f6f-117">*BestRoute* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="09f6f-117">*BestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09f6f-118">Ponteiro para uma estrutura específica de família de protocolos que recebe as melhores informações de rota atuais, se houver.</span><span class="sxs-lookup"><span data-stu-id="09f6f-118">Pointer to a protocol-family-specific structure that receives the current best route information, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09f6f-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="09f6f-119">Return value</span></span>

<span data-ttu-id="09f6f-120">O valor de retorno é um dos códigos a seguir.</span><span class="sxs-lookup"><span data-stu-id="09f6f-120">The return value is one of the following codes.</span></span>



| <span data-ttu-id="09f6f-121">Valor</span><span class="sxs-lookup"><span data-stu-id="09f6f-121">Value</span></span>                                                                                                       | <span data-ttu-id="09f6f-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="09f6f-122">Description</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09f6f-123"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="09f6f-123"><dt>**TRUE**</dt></span></span> </dl>                         | <span data-ttu-id="09f6f-124">Existe pelo menos uma rota para a rede especificada.</span><span class="sxs-lookup"><span data-stu-id="09f6f-124">At least one route to the specified network exists.</span></span> <span data-ttu-id="09f6f-125">A melhor rota é retornada na estrutura apontada pelo parâmetro *BestRoute* .</span><span class="sxs-lookup"><span data-stu-id="09f6f-125">The best route is returned in the structure pointed to by the *BestRoute* parameter.</span></span><br/>      |
| <dl> <span data-ttu-id="09f6f-126"><dt>**FOR**</dt></span><span class="sxs-lookup"><span data-stu-id="09f6f-126"><dt>**FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="09f6f-127">Não há rota para a rede especificada ou a operação falhou.</span><span class="sxs-lookup"><span data-stu-id="09f6f-127">There is no route to the specified network, or the operation failed.</span></span> <span data-ttu-id="09f6f-128">Chame [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) para obter mais informações:</span><span class="sxs-lookup"><span data-stu-id="09f6f-128">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information:</span></span><br/> |
| <dl> <span data-ttu-id="09f6f-129"><dt>**SEM \_ erros**</dt></span><span class="sxs-lookup"><span data-stu-id="09f6f-129"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="09f6f-130">A operação foi bem-sucedida, mas não há rota para a rede especificada.</span><span class="sxs-lookup"><span data-stu-id="09f6f-130">The operation succeeded, but there is no route to the specified network.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="09f6f-131"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09f6f-131"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="09f6f-132">O valor do parâmetro *ProtocolFamily* não corresponde a nenhuma família de protocolos instalada.</span><span class="sxs-lookup"><span data-stu-id="09f6f-132">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/>                                             |
| <dl> <span data-ttu-id="09f6f-133"><dt>**ERRO \_ sem \_ recursos do sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09f6f-133"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="09f6f-134">Não há recursos suficientes para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="09f6f-134">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="09f6f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09f6f-135">Requirements</span></span>



| <span data-ttu-id="09f6f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="09f6f-136">Requirement</span></span> | <span data-ttu-id="09f6f-137">Valor</span><span class="sxs-lookup"><span data-stu-id="09f6f-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="09f6f-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09f6f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="09f6f-139">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="09f6f-139">None supported</span></span><br/>                                                          |
| <span data-ttu-id="09f6f-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="09f6f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="09f6f-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="09f6f-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="09f6f-142">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="09f6f-142">End of server support</span></span><br/>    | <span data-ttu-id="09f6f-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="09f6f-143">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="09f6f-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09f6f-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="09f6f-145"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="09f6f-145"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="09f6f-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09f6f-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="09f6f-147"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09f6f-147"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="09f6f-148">DLL</span><span class="sxs-lookup"><span data-stu-id="09f6f-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09f6f-149"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09f6f-149"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09f6f-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="09f6f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f6f-151">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="09f6f-151">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="09f6f-152">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="09f6f-152">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="09f6f-153">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="09f6f-153">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="09f6f-154">**\_rede IP**</span><span class="sxs-lookup"><span data-stu-id="09f6f-154">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="09f6f-155">**\_rede IPX**</span><span class="sxs-lookup"><span data-stu-id="09f6f-155">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="09f6f-156">Identificadores da família de protocolos RTMv1</span><span class="sxs-lookup"><span data-stu-id="09f6f-156">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

