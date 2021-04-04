---
title: Método de retomada método ibackgroundcopyjob (Deliveryoptimization. h)
description: Ativa um novo trabalho ou reinicia um trabalho que foi suspenso.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Método Resume
- Método resume, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método resume
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f87f5b5347785810d84331ce56f240cd1f016383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085344"
---
# <a name="ibackgroundcopyjobresume-method"></a><span data-ttu-id="ff82a-106">Método método ibackgroundcopyjob:: resume</span><span class="sxs-lookup"><span data-stu-id="ff82a-106">IBackgroundCopyJob::Resume method</span></span>

<span data-ttu-id="ff82a-107">Ativa um novo trabalho ou reinicia um trabalho que foi suspenso.</span><span class="sxs-lookup"><span data-stu-id="ff82a-107">Activates a new job or restarts a job that has been suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff82a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff82a-108">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="ff82a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff82a-109">Parameters</span></span>

<span data-ttu-id="ff82a-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ff82a-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ff82a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff82a-111">Return value</span></span>

<span data-ttu-id="ff82a-112">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="ff82a-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="ff82a-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ff82a-113">Return code</span></span>                                                                                          | <span data-ttu-id="ff82a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff82a-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ff82a-115"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="ff82a-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="ff82a-116">O trabalho foi reiniciado com êxito.</span><span class="sxs-lookup"><span data-stu-id="ff82a-116">Job was successfully restarted.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="ff82a-117"><dt>**DO_E_EMPTY**</dt></span><span class="sxs-lookup"><span data-stu-id="ff82a-117"><dt>**DO_E_EMPTY**</dt></span></span> </dl>          | <span data-ttu-id="ff82a-118">Não existem arquivos a transferir.</span><span class="sxs-lookup"><span data-stu-id="ff82a-118">There are no files to transfer.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="ff82a-119"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="ff82a-119"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="ff82a-120">O estado do trabalho não pode ser BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="ff82a-120">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ff82a-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff82a-121">Remarks</span></span>

<span data-ttu-id="ff82a-122">Quando você cria um trabalho, o trabalho é suspenso inicialmente.</span><span class="sxs-lookup"><span data-stu-id="ff82a-122">When you create a job, the job is initially suspended.</span></span> <span data-ttu-id="ff82a-123">Chamar **resume** move o trabalho para o estado de transferência.</span><span class="sxs-lookup"><span data-stu-id="ff82a-123">Calling **Resume** moves the job to the Transferring state.</span></span> <span data-ttu-id="ff82a-124">Observe que o trabalho deve conter um ou mais arquivos antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="ff82a-124">Note that the job must contain one or more files before calling this method.</span></span>

<span data-ttu-id="ff82a-125">Se um trabalho que está no estado BG_JOB_STATE_TRANSIENT_ERROR ou BG_JOB_STATE_ERROR, chame o método **resume** para reiniciar o trabalho depois de corrigir o erro.</span><span class="sxs-lookup"><span data-stu-id="ff82a-125">If a job that is in the BG_JOB_STATE_TRANSIENT_ERROR or BG_JOB_STATE_ERROR state, call the **Resume** method to restart the job after you fix the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff82a-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff82a-126">Requirements</span></span>



| <span data-ttu-id="ff82a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff82a-127">Requirement</span></span> | <span data-ttu-id="ff82a-128">Valor</span><span class="sxs-lookup"><span data-stu-id="ff82a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff82a-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff82a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ff82a-130">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="ff82a-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ff82a-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff82a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ff82a-132">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="ff82a-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ff82a-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff82a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff82a-134"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff82a-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff82a-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="ff82a-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff82a-136"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff82a-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ff82a-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff82a-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff82a-138"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff82a-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ff82a-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ff82a-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff82a-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff82a-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ff82a-141">IID</span><span class="sxs-lookup"><span data-stu-id="ff82a-141">IID</span></span><br/>                      | <span data-ttu-id="ff82a-142">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="ff82a-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ff82a-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff82a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff82a-144">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="ff82a-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="ff82a-145">**Método ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="ff82a-145">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="ff82a-146">**Método ibackgroundcopyjob:: suspender**</span><span class="sxs-lookup"><span data-stu-id="ff82a-146">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





