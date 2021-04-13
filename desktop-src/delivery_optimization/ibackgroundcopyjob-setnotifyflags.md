---
title: Método método ibackgroundcopyjob SetNotifyFlags (Deliveryoptimization. h)
description: Especifica o tipo de notificação de evento que você deseja receber, como eventos de transferência de trabalho.
ms.assetid: 19E626A5-6B6E-44E0-BD6F-43F132F32890
keywords:
- Método SetNotifyFlags
- Método SetNotifyFlags, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método SetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ea754eeafca8f0efdcad5545cfc3a462c8b508cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499398"
---
# <a name="ibackgroundcopyjobsetnotifyflags-method"></a><span data-ttu-id="fafde-106">Método método ibackgroundcopyjob:: SetNotifyFlags</span><span class="sxs-lookup"><span data-stu-id="fafde-106">IBackgroundCopyJob::SetNotifyFlags method</span></span>

<span data-ttu-id="fafde-107">Especifica o tipo de notificação de evento que você deseja receber, como eventos de transferência de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fafde-107">Specifies the type of event notification you want to receive, such as job transferred events.</span></span>

## <a name="syntax"></a><span data-ttu-id="fafde-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fafde-108">Syntax</span></span>


```C++
HRESULT SetNotifyFlags(
  [in] ULONG NotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="fafde-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fafde-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fafde-110">*NotifyFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fafde-110">*NotifyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fafde-111">Defina um ou mais dos sinalizadores a seguir para identificar os eventos que você deseja receber.</span><span class="sxs-lookup"><span data-stu-id="fafde-111">Set one or more of the following flags to identify the events that you want to receive.</span></span>



| <span data-ttu-id="fafde-112">Valor</span><span class="sxs-lookup"><span data-stu-id="fafde-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="fafde-113">Significado</span><span class="sxs-lookup"><span data-stu-id="fafde-113">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="fafde-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="fafde-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="fafde-115">Todos os arquivos no trabalho foram transferidos.</span><span class="sxs-lookup"><span data-stu-id="fafde-115">All of the files in the job have been transferred.</span></span><br/>                                                                                                                                                          |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="fafde-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="fafde-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span></span> </dl>                                            | <span data-ttu-id="fafde-117">Ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="fafde-117">An error has occurred.</span></span><br/>                                                                                                                                                                                      |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="fafde-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="fafde-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span></span> </dl>                                                   | <span data-ttu-id="fafde-119">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="fafde-119">Not supported.</span></span><br/>                                                                                                                                                                                              |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="fafde-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="fafde-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span></span> </dl>                       | <span data-ttu-id="fafde-121">O trabalho foi modificado.</span><span class="sxs-lookup"><span data-stu-id="fafde-121">The job has been modified.</span></span> <span data-ttu-id="fafde-122">Por exemplo, um valor de propriedade alterado, o estado do trabalho foi alterado ou o progresso é feito transferindo os arquivos.</span><span class="sxs-lookup"><span data-stu-id="fafde-122">For example, a property value changed, the state of the job changed, or progress is made transferring the files.</span></span> <span data-ttu-id="fafde-123">Esse sinalizador será ignorado se a notificação de linha de comando for especificada.</span><span class="sxs-lookup"><span data-stu-id="fafde-123">This flag is ignored if command line notification is specified.</span></span><br/> |
| <span id="BG_NOTIFY_FILE_TRANSFERRED"></span><span id="bg_notify_file_transferred"></span><dl> <span data-ttu-id="fafde-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="fafde-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span></span> </dl>                       | <span data-ttu-id="fafde-125">Um arquivo no trabalho foi transferido.</span><span class="sxs-lookup"><span data-stu-id="fafde-125">A file in the job has been transferred.</span></span> <span data-ttu-id="fafde-126">Esse sinalizador será ignorado se a notificação de linha de comando for especificada.</span><span class="sxs-lookup"><span data-stu-id="fafde-126">This flag is ignored if command line notification is specified.</span></span><br/>                                                                                                     |
| <span id="BG_NOTIFY_FILE_RANGES_TRANSFERRED"></span><span id="bg_notify_file_ranges_transferred"></span><dl> <span data-ttu-id="fafde-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="fafde-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="fafde-128">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="fafde-128">Not supported.</span></span><br/>                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fafde-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fafde-129">Return value</span></span>

<span data-ttu-id="fafde-130">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="fafde-130">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="fafde-131">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fafde-131">Return code</span></span>                                                                                          | <span data-ttu-id="fafde-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="fafde-132">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fafde-133"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="fafde-133"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="fafde-134">O tipo de notificação de eventos foi definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="fafde-134">Type of event notification was successfully set.</span></span><br/>                                          |
| <dl> <span data-ttu-id="fafde-135"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="fafde-135"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="fafde-136">O estado do trabalho não pode ser BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="fafde-136">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fafde-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="fafde-137">Remarks</span></span>

<span data-ttu-id="fafde-138">Use o método **SetNotifyFlags** em conjunto com [**método ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).</span><span class="sxs-lookup"><span data-stu-id="fafde-138">Use the **SetNotifyFlags** method in conjunction with the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fafde-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fafde-139">Requirements</span></span>



| <span data-ttu-id="fafde-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="fafde-140">Requirement</span></span> | <span data-ttu-id="fafde-141">Valor</span><span class="sxs-lookup"><span data-stu-id="fafde-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fafde-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fafde-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fafde-143">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="fafde-143">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fafde-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fafde-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fafde-145">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="fafde-145">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="fafde-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fafde-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="fafde-147"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="fafde-147"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="fafde-148">INSERI</span><span class="sxs-lookup"><span data-stu-id="fafde-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fafde-149"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fafde-149"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="fafde-150">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fafde-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="fafde-151"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fafde-151"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="fafde-152">DLL</span><span class="sxs-lookup"><span data-stu-id="fafde-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fafde-153"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fafde-153"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="fafde-154">IID</span><span class="sxs-lookup"><span data-stu-id="fafde-154">IID</span></span><br/>                      | <span data-ttu-id="fafde-155">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="fafde-155">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="fafde-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="fafde-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fafde-157">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="fafde-157">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="fafde-158">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="fafde-158">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="fafde-159">**Método ibackgroundcopyjob:: GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="fafde-159">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="fafde-160">**Método ibackgroundcopyjob:: SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="fafde-160">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





