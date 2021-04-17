---
title: Método Uninitialize do INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: Faz com que o NapAgent libere todas as suas referências aos ponteiros COM do agente de integridade do sistema.
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- Método Uninitialize NAP
- Método Uninitialize NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, método Uninitialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a863e9d742610ab764a3b7a00966e8e112278317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754749"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a><span data-ttu-id="e36a8-106">Método INapSystemHealthAgentBinding:: Uninitialize</span><span class="sxs-lookup"><span data-stu-id="e36a8-106">INapSystemHealthAgentBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="e36a8-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="e36a8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e36a8-108">O método **INapSystemHealthAgentBinding:: Uninitialize** faz com que o NapAgent libere todas as suas referências aos ponteiros de com do agente de integridade do sistema.</span><span class="sxs-lookup"><span data-stu-id="e36a8-108">The **INapSystemHealthAgentBinding::Uninitialize** method causes the NapAgent to release all its references to system health agent COM pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e36a8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e36a8-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="e36a8-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e36a8-110">Parameters</span></span>

<span data-ttu-id="e36a8-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e36a8-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e36a8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e36a8-112">Return value</span></span>

<span data-ttu-id="e36a8-113">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="e36a8-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e36a8-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e36a8-114">Return code</span></span>                                                                                             | <span data-ttu-id="e36a8-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="e36a8-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e36a8-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e36a8-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="e36a8-117">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e36a8-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="e36a8-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e36a8-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="e36a8-119">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="e36a8-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="e36a8-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e36a8-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="e36a8-121">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="e36a8-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="e36a8-122"><dt>**NAP \_ E \_ não \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="e36a8-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="e36a8-123">O SHA não foi inicializado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e36a8-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="e36a8-124"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="e36a8-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="e36a8-125">O NapAgent foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="e36a8-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="e36a8-126">Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="e36a8-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e36a8-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="e36a8-127">Remarks</span></span>

<span data-ttu-id="e36a8-128">O NapAgent bloqueia a execução dessa chamada de método até que todas as chamadas existentes nas interfaces de ligação e retorno de chamada sejam concluídas.</span><span class="sxs-lookup"><span data-stu-id="e36a8-128">The NapAgent blocks execution of this method call until all existing calls on the Binding and Callback interfaces complete.</span></span>

<span data-ttu-id="e36a8-129">O SHA deve chamar [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de chamar este método ou qualquer outro método da interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="e36a8-129">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e36a8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e36a8-130">Requirements</span></span>



| <span data-ttu-id="e36a8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e36a8-131">Requirement</span></span> | <span data-ttu-id="e36a8-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e36a8-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e36a8-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e36a8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e36a8-134">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e36a8-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e36a8-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e36a8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e36a8-136">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e36a8-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e36a8-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e36a8-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e36a8-138"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="e36a8-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="e36a8-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="e36a8-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e36a8-140"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e36a8-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="e36a8-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e36a8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e36a8-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e36a8-142"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e36a8-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="e36a8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e36a8-144">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="e36a8-144">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





