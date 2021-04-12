---
title: Método método ibackgroundcopyjob GetNotifyFlags (Deliveryoptimization. h)
description: Recupera os sinalizadores de notificação de eventos para o trabalho.
ms.assetid: 95ADC97F-63DC-4EB6-B85C-7BCC79238C12
keywords:
- Método GetNotifyFlags
- Método GetNotifyFlags, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e104857725849dfeb899b449ea055bc3cdb046bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295783"
---
# <a name="ibackgroundcopyjobgetnotifyflags-method"></a><span data-ttu-id="3b53e-106">Método método ibackgroundcopyjob:: GetNotifyFlags</span><span class="sxs-lookup"><span data-stu-id="3b53e-106">IBackgroundCopyJob::GetNotifyFlags method</span></span>

<span data-ttu-id="3b53e-107">Recupera os sinalizadores de notificação de eventos para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="3b53e-107">Retrieves the event notification flags for the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b53e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b53e-108">Syntax</span></span>


```C++
HRESULT GetNotifyFlags(
  [out] ULONG *pNotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3b53e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b53e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b53e-110">*pNotifyFlags* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3b53e-110">*pNotifyFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b53e-111">Identifica os eventos que seu aplicativo recebe.</span><span class="sxs-lookup"><span data-stu-id="3b53e-111">Identifies the events that your application receives.</span></span> <span data-ttu-id="3b53e-112">A tabela a seguir lista os valores de sinalizador de notificação de eventos.</span><span class="sxs-lookup"><span data-stu-id="3b53e-112">The following table lists the event notification flag values.</span></span>



| <span data-ttu-id="3b53e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3b53e-113">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="3b53e-114">Significado</span><span class="sxs-lookup"><span data-stu-id="3b53e-114">Meaning</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="3b53e-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span><span class="sxs-lookup"><span data-stu-id="3b53e-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span></span> </dl>    | <span data-ttu-id="3b53e-116">Todos os arquivos no trabalho foram transferidos.</span><span class="sxs-lookup"><span data-stu-id="3b53e-116">All of the files in the job have been transferred.</span></span><br/>                  |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="3b53e-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="3b53e-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span></span> </dl>                      | <span data-ttu-id="3b53e-118">Ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="3b53e-118">An error has occurred.</span></span><br/>                                              |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="3b53e-119"><dt>**BG_NOTIFY_DISABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="3b53e-119"><dt>**BG_NOTIFY_DISABLE**</dt></span></span> </dl>                             | <span data-ttu-id="3b53e-120">A notificação de eventos está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="3b53e-120">Event notification is disabled.</span></span> <span data-ttu-id="3b53e-121">Se definido, ignora os outros sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="3b53e-121">If set, DO ignores the other flags.</span></span><br/> |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="3b53e-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span><span class="sxs-lookup"><span data-stu-id="3b53e-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span></span> </dl> | <span data-ttu-id="3b53e-123">O trabalho foi modificado.</span><span class="sxs-lookup"><span data-stu-id="3b53e-123">The job has been modified.</span></span><br/>                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b53e-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b53e-124">Return value</span></span>

<span data-ttu-id="3b53e-125">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="3b53e-125">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="3b53e-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3b53e-126">Return code</span></span>                                                                              | <span data-ttu-id="3b53e-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b53e-127">Description</span></span>                                                |
|------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="3b53e-128"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="3b53e-128"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="3b53e-129">Os sinalizadores de notificação de eventos foram recuperados com êxito.</span><span class="sxs-lookup"><span data-stu-id="3b53e-129">Event notify flags were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3b53e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b53e-130">Requirements</span></span>



| <span data-ttu-id="3b53e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b53e-131">Requirement</span></span> | <span data-ttu-id="3b53e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="3b53e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b53e-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b53e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3b53e-134">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="3b53e-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3b53e-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b53e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3b53e-136">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="3b53e-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3b53e-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b53e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b53e-138"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b53e-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b53e-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="3b53e-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3b53e-140"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3b53e-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3b53e-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b53e-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="3b53e-142"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b53e-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3b53e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="3b53e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b53e-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b53e-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3b53e-145">IID</span><span class="sxs-lookup"><span data-stu-id="3b53e-145">IID</span></span><br/>                      | <span data-ttu-id="3b53e-146">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="3b53e-146">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="3b53e-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b53e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b53e-148">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="3b53e-148">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="3b53e-149">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="3b53e-149">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="3b53e-150">**Método ibackgroundcopyjob:: GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="3b53e-150">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="3b53e-151">**Método ibackgroundcopyjob:: SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="3b53e-151">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





