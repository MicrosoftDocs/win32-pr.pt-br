---
title: Método ITsSbResourcePluginStoreEx AcquireTargetLock
description: Bloqueia um destino.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método AcquireTargetLock
- Método AcquireTargetLock Serviços de Área de Trabalho Remota, interface ITsSbResourcePluginStoreEx
- Serviços de Área de Trabalho Remota de interface ITsSbResourcePluginStoreEx, método AcquireTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c18be0a544ebcea2d2cecb40dcea3a08e4bd35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085301"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a><span data-ttu-id="1a02f-106">Método ITsSbResourcePluginStoreEx:: AcquireTargetLock</span><span class="sxs-lookup"><span data-stu-id="1a02f-106">ITsSbResourcePluginStoreEx::AcquireTargetLock method</span></span>

<span data-ttu-id="1a02f-107">Bloqueia um destino.</span><span class="sxs-lookup"><span data-stu-id="1a02f-107">Locks a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a02f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a02f-108">Syntax</span></span>


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a><span data-ttu-id="1a02f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a02f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a02f-110">*TargetName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a02f-110">*targetName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a02f-111">O nome do destino a ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="1a02f-111">The name of the target to lock.</span></span>

</dd> <dt>

<span data-ttu-id="1a02f-112">*dwTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1a02f-112">*dwTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a02f-113">O tempo limite para a operação, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="1a02f-113">The timeout for the operation, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="1a02f-114">*ppContext* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1a02f-114">*ppContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a02f-115">Retorna um ponteiro para o contexto do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="1a02f-115">Returns a pointer to the context of the lock.</span></span> <span data-ttu-id="1a02f-116">Para liberar o bloqueio, forneça esse ponteiro para o método [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) .</span><span class="sxs-lookup"><span data-stu-id="1a02f-116">To release the lock, supply this pointer to the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a02f-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a02f-117">Return value</span></span>

<span data-ttu-id="1a02f-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1a02f-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1a02f-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1a02f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a02f-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a02f-120">Remarks</span></span>

<span data-ttu-id="1a02f-121">Depois que o bloqueio é adquirido, supõe-se que o thread de chamada tenha acesso exclusivo ao objeto de destino e, portanto, nenhum outro thread (dentro do mesmo computador) possa atualizá-lo.</span><span class="sxs-lookup"><span data-stu-id="1a02f-121">After the lock is acquired, the calling thread is assumed to have exclusive access to the target object and therefore no other thread (within the same machine) can update it.</span></span> <span data-ttu-id="1a02f-122">Portanto, o thread de chamada deve chamar o método [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) assim que tiver feito as atualizações necessárias para o objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="1a02f-122">Therefore the calling thread must call the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method as soon as it has made the necessary updates to the target object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1a02f-123">Esse bloqueio não impede completamente que os objetos de destino sejam modificados externamente se houver mais de um agente de conexão na implantação.</span><span class="sxs-lookup"><span data-stu-id="1a02f-123">this lock does not completely prevent target objects from being modified externally if more than one Connection Broker exists in the deployment.</span></span> <span data-ttu-id="1a02f-124">O thread de chamada deve estar preparado para manipular uma falha normalmente e repetir a atualização de destino.</span><span class="sxs-lookup"><span data-stu-id="1a02f-124">The calling thread must be prepared to handle a failure gracefully and retry the target update.</span></span>

 

<span data-ttu-id="1a02f-125">Esse método está disponível no Windows Server 2012 R2 com [KB3091411](https://support.microsoft.com/kb/3091411) instalado na interface [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) .</span><span class="sxs-lookup"><span data-stu-id="1a02f-125">This method is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a02f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a02f-126">Requirements</span></span>



| <span data-ttu-id="1a02f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a02f-127">Requirement</span></span> | <span data-ttu-id="1a02f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="1a02f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a02f-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a02f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1a02f-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1a02f-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1a02f-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1a02f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1a02f-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1a02f-132">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="1a02f-133">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1a02f-133">End of server support</span></span><br/>    | <span data-ttu-id="1a02f-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1a02f-134">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="1a02f-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="1a02f-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1a02f-136"><dt>SbTsV. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1a02f-136"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="1a02f-137">IID</span><span class="sxs-lookup"><span data-stu-id="1a02f-137">IID</span></span><br/>                      | <span data-ttu-id="1a02f-138">IID \_ ITsSbResourcePluginStoreEx é definido como 80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="1a02f-138">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a02f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a02f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a02f-140">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="1a02f-140">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





