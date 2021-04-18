---
title: Método INapSystemHealthAgentBinding FlushCache (NapSystemHealthAgent. h)
description: É chamado por um SHA para liberar seu cache SoH.
ms.assetid: a771ce03-1922-4e2d-9490-7ee9f693857c
keywords:
- Método FlushCache NAP
- Método FlushCache NAP, interface INapSystemHealthAgentBinding
- INapSystemHealthAgentBinding interface NAP, método FlushCache
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.FlushCache
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ead6e496d220619439b80fdc5c7601675fdb7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105778419"
---
# <a name="inapsystemhealthagentbindingflushcache-method"></a><span data-ttu-id="4b4ee-106">Método INapSystemHealthAgentBinding:: FlushCache</span><span class="sxs-lookup"><span data-stu-id="4b4ee-106">INapSystemHealthAgentBinding::FlushCache method</span></span>

> [!Note]  
> <span data-ttu-id="4b4ee-107">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="4b4ee-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4b4ee-108">O método **INapSystemHealthAgentBinding:: FlushCache** é chamado por um SHA para liberar seu cache soh.</span><span class="sxs-lookup"><span data-stu-id="4b4ee-108">The **INapSystemHealthAgentBinding::FlushCache** method is called by an SHA to flush its SoH cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b4ee-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b4ee-109">Syntax</span></span>


```C++
HRESULT FlushCache();
```



## <a name="parameters"></a><span data-ttu-id="4b4ee-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b4ee-110">Parameters</span></span>

<span data-ttu-id="4b4ee-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b4ee-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b4ee-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b4ee-112">Return value</span></span>

<span data-ttu-id="4b4ee-113">Outros códigos de erro específicos de COM também podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="4b4ee-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4b4ee-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4b4ee-114">Return code</span></span>                                                                                         | <span data-ttu-id="4b4ee-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b4ee-115">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4b4ee-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4b4ee-116"><dt>**S\_OK** </dt></span></span> </dl>               | <span data-ttu-id="4b4ee-117">Operação bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4b4ee-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="4b4ee-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4b4ee-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>     | <span data-ttu-id="4b4ee-119">Erro de permissões, acesso negado.</span><span class="sxs-lookup"><span data-stu-id="4b4ee-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="4b4ee-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4b4ee-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>      | <span data-ttu-id="4b4ee-121">O limite de recursos do sistema não pôde executar a operação.</span><span class="sxs-lookup"><span data-stu-id="4b4ee-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="4b4ee-122"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="4b4ee-122"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="4b4ee-123">O NapAgent foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="4b4ee-123">The NapAgent has been stopped.</span></span> <span data-ttu-id="4b4ee-124">Este objeto será recuperado automaticamente e reassociado ao NapAgent, depois que ele for reiniciado.</span><span class="sxs-lookup"><span data-stu-id="4b4ee-124">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b4ee-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b4ee-125">Remarks</span></span>

<span data-ttu-id="4b4ee-126">O NapAgent mantém um cache de SoHs recentes fornecido por SHAs diferentes.</span><span class="sxs-lookup"><span data-stu-id="4b4ee-126">The NapAgent maintains a cache of recent SoHs provided by different SHAs.</span></span> <span data-ttu-id="4b4ee-127">Esse cache é útil para otimizar o desempenho do tempo de inicialização, quando os SHAs podem ou não estar associados ao sistema.</span><span class="sxs-lookup"><span data-stu-id="4b4ee-127">This cache is useful to optimize boot-time performance, when SHAs may or may not be bound to the system.</span></span>

<span data-ttu-id="4b4ee-128">O SHA deve chamar [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de chamar este método ou qualquer outro método da interface [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="4b4ee-128">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b4ee-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b4ee-129">Requirements</span></span>



| <span data-ttu-id="4b4ee-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b4ee-130">Requirement</span></span> | <span data-ttu-id="4b4ee-131">Valor</span><span class="sxs-lookup"><span data-stu-id="4b4ee-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b4ee-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b4ee-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4b4ee-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4b4ee-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4b4ee-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4b4ee-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4b4ee-135">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4b4ee-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4b4ee-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b4ee-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b4ee-137"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b4ee-137"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b4ee-138">INSERI</span><span class="sxs-lookup"><span data-stu-id="4b4ee-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4b4ee-139"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b4ee-139"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="4b4ee-140">DLL</span><span class="sxs-lookup"><span data-stu-id="4b4ee-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b4ee-141"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b4ee-141"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4b4ee-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b4ee-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b4ee-143">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="4b4ee-143">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





