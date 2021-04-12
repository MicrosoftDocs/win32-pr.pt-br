---
title: Função RtmBlockDeleteRoutes (RTM. h)
description: A função RtmBlockDeleteRoutes exclui todas as rotas no subconjunto especificado de rotas na tabela.
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- Função RtmBlockDeleteRoutes RAS
topic_type:
- apiref
api_name:
- RtmBlockDeleteRoutes
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71090371fe8a84698b84b84391e5a782fdc636f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455411"
---
# <a name="rtmblockdeleteroutes-function"></a><span data-ttu-id="429c1-104">Função RtmBlockDeleteRoutes</span><span class="sxs-lookup"><span data-stu-id="429c1-104">RtmBlockDeleteRoutes function</span></span>

<span data-ttu-id="429c1-105">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="429c1-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="429c1-106">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="429c1-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="429c1-107">A função **RtmBlockDeleteRoutes** exclui todas as rotas no subconjunto especificado de rotas na tabela.</span><span class="sxs-lookup"><span data-stu-id="429c1-107">The **RtmBlockDeleteRoutes** function deletes all routes in the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="429c1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="429c1-108">Syntax</span></span>


```C++
HANDLE RtmBlockDeleteRoutes(
  _In_ HANDLE ClientHandle,
  _In_ DWORD  EnumerationFlags,
  _In_ PVOID  CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="429c1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="429c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="429c1-110">*ClientHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="429c1-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="429c1-111">Identificador que identifica o cliente e, portanto, o protocolo de roteamento, das rotas a serem excluídas.</span><span class="sxs-lookup"><span data-stu-id="429c1-111">Handle that identifies the client, and therefore the routing protocol, of the routes to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="429c1-112">*EnumerationFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="429c1-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="429c1-113">Especifica quais rotas devem ser enumeradas.</span><span class="sxs-lookup"><span data-stu-id="429c1-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="429c1-114">Esse parâmetro limita o conjunto de rotas excluídas a um subconjunto definido pelos seguintes sinalizadores e os valores nos membros correspondentes da estrutura apontada pelo parâmetro *CriteriaRoute* .</span><span class="sxs-lookup"><span data-stu-id="429c1-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="429c1-115">Os sinalizadores são os mesmos usados em [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) , exceto que o RTM \_ apenas \_ as melhores \_ rotas é redundante para **RtmBlockDeleteRoutes**.</span><span class="sxs-lookup"><span data-stu-id="429c1-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) except that RTM\_ONLY\_BEST\_ROUTES is redundant for **RtmBlockDeleteRoutes**.</span></span> <span data-ttu-id="429c1-116">A designação de melhor rota é ajustada conforme as rotas são excluídas, portanto, a função eventualmente exclui todas as rotas no subconjunto.</span><span class="sxs-lookup"><span data-stu-id="429c1-116">The best-route designation is adjusted as routes are deleted, so the function eventually deletes all the routes in the subset.</span></span>

</dd> <dt>

<span data-ttu-id="429c1-117">*CriteriaRoute* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="429c1-117">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="429c1-118">Ponteiro para uma estrutura de rota específica da família de protocolos [**( \_ \_ rota de IP RTM**](rtm-ip-route.md) ou [**\_ \_ rota IPX RTM**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="429c1-118">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="429c1-119">Os valores de membro nessa estrutura correspondem aos sinalizadores especificados pelo parâmetro *EnumerationFlags* .</span><span class="sxs-lookup"><span data-stu-id="429c1-119">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="429c1-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="429c1-120">Return value</span></span>

<span data-ttu-id="429c1-121">Se a função for realizada com sucesso, o valor de retorno não será um \_ erro.</span><span class="sxs-lookup"><span data-stu-id="429c1-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="429c1-122">Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="429c1-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="429c1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="429c1-123">Value</span></span>                                                                                                       | <span data-ttu-id="429c1-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="429c1-124">Description</span></span>                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="429c1-125"><dt>**ERRO \_ sem \_ rotas**</dt></span><span class="sxs-lookup"><span data-stu-id="429c1-125"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="429c1-126">Não há rotas com os critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="429c1-126">There are no routes that have the specified criteria.</span></span><br/>                                           |
| <dl> <span data-ttu-id="429c1-127"><dt>**\_identificador inválido do erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="429c1-127"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="429c1-128">O parâmetro *ClientHandle* não é válido.</span><span class="sxs-lookup"><span data-stu-id="429c1-128">The *ClientHandle* parameter is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="429c1-129"><dt>**\_parâmetro inválido de erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="429c1-129"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="429c1-130">Um ou mais dos parâmetros de entrada são inválidos, por exemplo, os sinalizadores de enumeração são inválidos.</span><span class="sxs-lookup"><span data-stu-id="429c1-130">One or more of the input parameters is invalid, for example, the enumeration flags are invalid.</span></span><br/> |
| <dl> <span data-ttu-id="429c1-131"><dt>**ERRO \_ sem \_ recursos do sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="429c1-131"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="429c1-132">Não há recursos suficientes para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="429c1-132">There are insufficient resources to carry out the operation.</span></span><br/>                                    |
| <dl> <span data-ttu-id="429c1-133"><dt>**ERRO \_ de \_ memória insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="429c1-133"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="429c1-134">Memória insuficiente para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="429c1-134">There is insufficient memory to carry out the operation.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="429c1-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="429c1-135">Remarks</span></span>

<span data-ttu-id="429c1-136">A função gera mensagens de notificação apropriadas para todos os clientes registrados, incluindo o chamador.</span><span class="sxs-lookup"><span data-stu-id="429c1-136">The function generates appropriate notification messages to all registered clients including the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="429c1-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="429c1-137">Requirements</span></span>



| <span data-ttu-id="429c1-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="429c1-138">Requirement</span></span> | <span data-ttu-id="429c1-139">Valor</span><span class="sxs-lookup"><span data-stu-id="429c1-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="429c1-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="429c1-140">Minimum supported client</span></span><br/> | <span data-ttu-id="429c1-141">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="429c1-141">None supported</span></span><br/>                                                          |
| <span data-ttu-id="429c1-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="429c1-142">Minimum supported server</span></span><br/> | <span data-ttu-id="429c1-143">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="429c1-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="429c1-144">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="429c1-144">End of server support</span></span><br/>    | <span data-ttu-id="429c1-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="429c1-145">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="429c1-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="429c1-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="429c1-147"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="429c1-147"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="429c1-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="429c1-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="429c1-149"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="429c1-149"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="429c1-150">DLL</span><span class="sxs-lookup"><span data-stu-id="429c1-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="429c1-151"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="429c1-151"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="429c1-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="429c1-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="429c1-153">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="429c1-153">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="429c1-154">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="429c1-154">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="429c1-155">**RtmCreateEnumerationHandle**</span><span class="sxs-lookup"><span data-stu-id="429c1-155">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="429c1-156">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="429c1-156">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





