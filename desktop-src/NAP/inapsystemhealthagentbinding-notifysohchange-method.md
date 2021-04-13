---
title: Método INapSystemHealthAgentBinding NotifySoHChange (NapSystemHealthAgent. h)
description: É usado por SHAs quando seu SoH é alterado.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- Método NotifySoHChange NAP
- Método NotifySoHChange NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, método NotifySoHChange
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b18c03be03c4bc5282e9ea62ec10d5356871cf5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499764"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a><span data-ttu-id="8bf02-106">Método INapSystemHealthAgentBinding:: NotifySoHChange</span><span class="sxs-lookup"><span data-stu-id="8bf02-106">INapSystemHealthAgentBinding::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="8bf02-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="8bf02-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8bf02-108">O método **INapSystemHealthAgentBinding:: NotifySoHChange** é usado por SHAs quando seu soh é alterado.</span><span class="sxs-lookup"><span data-stu-id="8bf02-108">The **INapSystemHealthAgentBinding::NotifySoHChange** method is used by SHAs when their SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf02-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8bf02-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="8bf02-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8bf02-110">Parameters</span></span>

<span data-ttu-id="8bf02-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8bf02-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8bf02-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8bf02-112">Return value</span></span>

<span data-ttu-id="8bf02-113">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="8bf02-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="8bf02-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8bf02-114">Return code</span></span>                                                                                             | <span data-ttu-id="8bf02-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="8bf02-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8bf02-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf02-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="8bf02-117">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8bf02-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="8bf02-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf02-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="8bf02-119">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="8bf02-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="8bf02-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf02-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="8bf02-121">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="8bf02-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="8bf02-122"><dt>**NAP \_ E \_ não \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf02-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="8bf02-123">O SHA não foi inicializado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8bf02-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="8bf02-124"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="8bf02-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="8bf02-125">O NapAgent foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="8bf02-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="8bf02-126">Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="8bf02-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8bf02-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bf02-127">Remarks</span></span>

<span data-ttu-id="8bf02-128">Os SHAs não devem chamar essa API especulativamente, pois resulta em uma troca de SoH na conexão.</span><span class="sxs-lookup"><span data-stu-id="8bf02-128">SHAs must not call this API speculatively since it results in an SoH exchange on the wire.</span></span> <span data-ttu-id="8bf02-129">As chamadas para essa API só devem ser feitas quando necessário.</span><span class="sxs-lookup"><span data-stu-id="8bf02-129">Calls to this API should only be made when necessary.</span></span>

<span data-ttu-id="8bf02-130">O NapAgent não mantém esse thread para processar a alteração SoH.</span><span class="sxs-lookup"><span data-stu-id="8bf02-130">The NapAgent does not hold this thread to process the SoH change.</span></span> <span data-ttu-id="8bf02-131">Em vez disso, ele retorna imediatamente e processa a alteração de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8bf02-131">Instead, it returns immediately and processes the change asynchronously.</span></span>

<span data-ttu-id="8bf02-132">O SHA deve chamar [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de chamar este método ou qualquer outro método da interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="8bf02-132">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf02-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bf02-133">Requirements</span></span>



| <span data-ttu-id="8bf02-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bf02-134">Requirement</span></span> | <span data-ttu-id="8bf02-135">Valor</span><span class="sxs-lookup"><span data-stu-id="8bf02-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf02-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bf02-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf02-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8bf02-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8bf02-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bf02-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf02-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8bf02-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8bf02-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8bf02-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="8bf02-141"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="8bf02-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="8bf02-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="8bf02-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8bf02-143"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8bf02-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="8bf02-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8bf02-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bf02-145"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bf02-145"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="8bf02-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bf02-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf02-147">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="8bf02-147">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





