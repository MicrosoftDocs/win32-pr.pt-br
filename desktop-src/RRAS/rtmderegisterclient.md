---
title: Função RtmDeregisterClient (RTM. h)
description: A função RtmDeregisterClient cancela o registro do cliente e libera os recursos associados ao cliente.
ms.assetid: 5d04f276-86a7-4e63-8266-e93f0d6e5241
keywords:
- Função RtmDeregisterClient RAS
topic_type:
- apiref
api_name:
- RtmDeregisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab1f56d3d65e13c083d8952f500cfba4638ab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369605"
---
# <a name="rtmderegisterclient-function"></a><span data-ttu-id="092dc-104">Função RtmDeregisterClient</span><span class="sxs-lookup"><span data-stu-id="092dc-104">RtmDeregisterClient function</span></span>

<span data-ttu-id="092dc-105">\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="092dc-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="092dc-106">Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]</span><span class="sxs-lookup"><span data-stu-id="092dc-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="092dc-107">A função **RtmDeregisterClient** cancela o registro do cliente e libera os recursos associados ao cliente.</span><span class="sxs-lookup"><span data-stu-id="092dc-107">The **RtmDeregisterClient** function deregisters the client, and frees resources associated with the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="092dc-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="092dc-108">Syntax</span></span>


```C++
DWORD RtmDeregisterClient(
  _In_ HANDLE ClientHandle
);
```



## <a name="parameters"></a><span data-ttu-id="092dc-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="092dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="092dc-110">*ClientHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="092dc-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="092dc-111">Identificador que identifica o cliente para cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="092dc-111">Handle that identifies the client to deregister.</span></span> <span data-ttu-id="092dc-112">Obtenha esse identificador chamando [**RtmRegisterClient**](rtmregisterclient.md).</span><span class="sxs-lookup"><span data-stu-id="092dc-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="092dc-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="092dc-113">Return value</span></span>

<span data-ttu-id="092dc-114">Se a função for realizada com sucesso, o valor de retorno não será um \_ erro.</span><span class="sxs-lookup"><span data-stu-id="092dc-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="092dc-115">Se a função falhar, o valor de retorno será um dos códigos de erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="092dc-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="092dc-116">Valor</span><span class="sxs-lookup"><span data-stu-id="092dc-116">Value</span></span>                                                                                                       | <span data-ttu-id="092dc-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="092dc-117">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="092dc-118"><dt>**\_identificador inválido do erro \_**</dt></span><span class="sxs-lookup"><span data-stu-id="092dc-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="092dc-119">O parâmetro *ClientHandle* não é um identificador válido.</span><span class="sxs-lookup"><span data-stu-id="092dc-119">The *ClientHandle* parameter is not a valid handle.</span></span><br/> |
| <dl> <span data-ttu-id="092dc-120"><dt>**ERRO \_ sem \_ recursos do sistema \_**</dt></span><span class="sxs-lookup"><span data-stu-id="092dc-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="092dc-121">Recursos insuficientes para realizar a operação.</span><span class="sxs-lookup"><span data-stu-id="092dc-121">Insufficient resources to carry out the operation.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="092dc-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="092dc-122">Remarks</span></span>

<span data-ttu-id="092dc-123">Essa função remove todas as rotas que foram adicionadas pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="092dc-123">This function removes all routes that were added by the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="092dc-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="092dc-124">Requirements</span></span>



| <span data-ttu-id="092dc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="092dc-125">Requirement</span></span> | <span data-ttu-id="092dc-126">Valor</span><span class="sxs-lookup"><span data-stu-id="092dc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="092dc-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="092dc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="092dc-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="092dc-128">None supported</span></span><br/>                                                          |
| <span data-ttu-id="092dc-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="092dc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="092dc-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="092dc-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="092dc-131">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="092dc-131">End of server support</span></span><br/>    | <span data-ttu-id="092dc-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="092dc-132">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="092dc-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="092dc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="092dc-134"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="092dc-134"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="092dc-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="092dc-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="092dc-136"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="092dc-136"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="092dc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="092dc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="092dc-138"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="092dc-138"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="092dc-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="092dc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="092dc-140">Referência da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="092dc-140">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="092dc-141">Funções da versão 1 do Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="092dc-141">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="092dc-142">**RtmRegisterClient**</span><span class="sxs-lookup"><span data-stu-id="092dc-142">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





