---
title: Método método ibackgroundcopyjob Cancel (Deliveryoptimization. h)
description: Exclui o trabalho da fila de transferência e remove arquivos temporários relacionados do cliente (downloads) e do servidor (uploads).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Método Cancel
- Método Cancel, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método Cancel
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824350"
---
# <a name="ibackgroundcopyjobcancel-method"></a><span data-ttu-id="aa0d8-106">Método método ibackgroundcopyjob:: Cancel</span><span class="sxs-lookup"><span data-stu-id="aa0d8-106">IBackgroundCopyJob::Cancel method</span></span>

<span data-ttu-id="aa0d8-107">Exclui o trabalho da fila de transferência e remove arquivos temporários relacionados do cliente (downloads) e do servidor (uploads).</span><span class="sxs-lookup"><span data-stu-id="aa0d8-107">Deletes the job from the transfer queue and removes related temporary files from the client (downloads) and server (uploads).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa0d8-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa0d8-108">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="aa0d8-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa0d8-109">Parameters</span></span>

<span data-ttu-id="aa0d8-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="aa0d8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa0d8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa0d8-111">Return value</span></span>

<span data-ttu-id="aa0d8-112">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="aa0d8-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="aa0d8-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="aa0d8-113">Return code</span></span>                                                                                          | <span data-ttu-id="aa0d8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="aa0d8-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa0d8-115"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="aa0d8-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="aa0d8-116">O trabalho foi cancelado com êxito.</span><span class="sxs-lookup"><span data-stu-id="aa0d8-116">Job was successfully canceled.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="aa0d8-117"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="aa0d8-117"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="aa0d8-118">Não é possível cancelar um trabalho cujo estado é BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="aa0d8-118">Cannot cancel a job whose state is BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aa0d8-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa0d8-119">Remarks</span></span>

<span data-ttu-id="aa0d8-120">Você pode cancelar um trabalho a qualquer momento; no entanto, o trabalho não pode ser recuperado após ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="aa0d8-120">You can cancel a job at any time; however, the job cannot be recovered after it is canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa0d8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa0d8-121">Requirements</span></span>



| <span data-ttu-id="aa0d8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa0d8-122">Requirement</span></span> | <span data-ttu-id="aa0d8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="aa0d8-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa0d8-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa0d8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="aa0d8-125">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="aa0d8-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aa0d8-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa0d8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="aa0d8-127">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="aa0d8-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="aa0d8-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa0d8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa0d8-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa0d8-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="aa0d8-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="aa0d8-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aa0d8-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aa0d8-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="aa0d8-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa0d8-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="aa0d8-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aa0d8-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="aa0d8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="aa0d8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa0d8-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa0d8-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="aa0d8-136">IID</span><span class="sxs-lookup"><span data-stu-id="aa0d8-136">IID</span></span><br/>                      | <span data-ttu-id="aa0d8-137">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="aa0d8-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="aa0d8-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa0d8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa0d8-139">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="aa0d8-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="aa0d8-140">**Método ibackgroundcopyjob:: concluir**</span><span class="sxs-lookup"><span data-stu-id="aa0d8-140">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="aa0d8-141">**Método ibackgroundcopyjob:: retomar**</span><span class="sxs-lookup"><span data-stu-id="aa0d8-141">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> <dt>

[<span data-ttu-id="aa0d8-142">**Método ibackgroundcopyjob:: suspender**</span><span class="sxs-lookup"><span data-stu-id="aa0d8-142">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





