---
title: Método IMsTscAxEvents OnFatalError
description: Chamado quando o controle de cliente encontra um erro fatal.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnFatalError
- Método OnFatalError Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnFatalError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73402ac178bcb2ac3dc03c0adda092d3b49f6ba3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824546"
---
# <a name="imstscaxeventsonfatalerror-method"></a><span data-ttu-id="c894b-106">Método IMsTscAxEvents:: OnFatalError</span><span class="sxs-lookup"><span data-stu-id="c894b-106">IMsTscAxEvents::OnFatalError method</span></span>

<span data-ttu-id="c894b-107">Chamado quando o controle de cliente encontra um erro fatal.</span><span class="sxs-lookup"><span data-stu-id="c894b-107">Called when the client control encounters a fatal error.</span></span>

## <a name="syntax"></a><span data-ttu-id="c894b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c894b-108">Syntax</span></span>


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="c894b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c894b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c894b-110">*ErrorCode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c894b-110">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c894b-111">Indica o código de erro.</span><span class="sxs-lookup"><span data-stu-id="c894b-111">Indicates the error code.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="c894b-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="c894b-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="c894b-113">Ocorreu um erro desconhecido.</span><span class="sxs-lookup"><span data-stu-id="c894b-113">An unknown error has occurred.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="c894b-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="c894b-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="c894b-115">Código de erro interno 1.</span><span class="sxs-lookup"><span data-stu-id="c894b-115">Internal error code 1.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="c894b-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="c894b-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="c894b-117">Ocorreu um erro de memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="c894b-117">An out-of-memory error has occurred.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="c894b-118"><span id="3"></span>**Beta**</span><span class="sxs-lookup"><span data-stu-id="c894b-118"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="c894b-119">Ocorreu um erro de criação de janela.</span><span class="sxs-lookup"><span data-stu-id="c894b-119">A window-creation error has occurred.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="c894b-120"><span id="4"></span>**quatro**</span><span class="sxs-lookup"><span data-stu-id="c894b-120"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="c894b-121">Código de erro interno 2.</span><span class="sxs-lookup"><span data-stu-id="c894b-121">Internal error code 2.</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="c894b-122"><span id="5"></span>**05**</span><span class="sxs-lookup"><span data-stu-id="c894b-122"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="c894b-123">Código de erro interno 3.</span><span class="sxs-lookup"><span data-stu-id="c894b-123">Internal error code 3.</span></span> <span data-ttu-id="c894b-124">Este não é um estado válido.</span><span class="sxs-lookup"><span data-stu-id="c894b-124">This is not a valid state.</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="c894b-125"><span id="6"></span>**152**</span><span class="sxs-lookup"><span data-stu-id="c894b-125"><span id="6"></span>**6**</span></span>


</dt> <dd>

<span data-ttu-id="c894b-126">Código de erro interno 4.</span><span class="sxs-lookup"><span data-stu-id="c894b-126">Internal error code 4.</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="c894b-127"><span id="7"></span>**7**</span><span class="sxs-lookup"><span data-stu-id="c894b-127"><span id="7"></span>**7**</span></span>


</dt> <dd>

<span data-ttu-id="c894b-128">Ocorreu um erro irrecuperável durante a conexão do cliente.</span><span class="sxs-lookup"><span data-stu-id="c894b-128">An unrecoverable error has occurred during client connection.</span></span>

</dd> <dt>

<span id="100"></span>

<span data-ttu-id="c894b-129"><span id="100"></span>**100**</span><span class="sxs-lookup"><span data-stu-id="c894b-129"><span id="100"></span>**100**</span></span>


</dt> <dd>

<span data-ttu-id="c894b-130">Erro de inicialização do Winsock.</span><span class="sxs-lookup"><span data-stu-id="c894b-130">Winsock initialization error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c894b-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c894b-131">Return value</span></span>

<span data-ttu-id="c894b-132">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c894b-132">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c894b-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="c894b-133">Remarks</span></span>

<span data-ttu-id="c894b-134">Em resposta a esse evento, o contêiner exibe uma mensagem de erro e é desligado.</span><span class="sxs-lookup"><span data-stu-id="c894b-134">In response to this event, the container displays an error message and shuts down.</span></span>

<span data-ttu-id="c894b-135">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c894b-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c894b-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c894b-136">Requirements</span></span>



| <span data-ttu-id="c894b-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="c894b-137">Requirement</span></span> | <span data-ttu-id="c894b-138">Valor</span><span class="sxs-lookup"><span data-stu-id="c894b-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c894b-139">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c894b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="c894b-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c894b-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c894b-141">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c894b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="c894b-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c894b-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c894b-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c894b-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="c894b-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c894b-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c894b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="c894b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c894b-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c894b-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c894b-147">IID</span><span class="sxs-lookup"><span data-stu-id="c894b-147">IID</span></span><br/>                      | <span data-ttu-id="c894b-148">IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="c894b-148">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="c894b-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="c894b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c894b-150">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="c894b-150">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





