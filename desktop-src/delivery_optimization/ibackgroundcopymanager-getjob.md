---
title: Método IBackgroundCopyManager GetJob (Deliveryoptimization. h)
description: Recupera um trabalho especificado da fila de transferência. Normalmente, seu aplicativo persiste o identificador de trabalho, para que você possa recuperar posteriormente o trabalho da fila.
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- Método GetJob
- Método GetJob, interface IBackgroundCopyManager
- Interface IBackgroundCopyManager, método GetJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a59956e68b5b656e7182e62969b3212c2ef6732c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812025"
---
# <a name="ibackgroundcopymanagergetjob-method"></a><span data-ttu-id="b20cf-107">Método IBackgroundCopyManager:: GetJob</span><span class="sxs-lookup"><span data-stu-id="b20cf-107">IBackgroundCopyManager::GetJob method</span></span>

<span data-ttu-id="b20cf-108">Recupera um trabalho especificado da fila de transferência.</span><span class="sxs-lookup"><span data-stu-id="b20cf-108">Retrieves a specified job from the transfer queue.</span></span> <span data-ttu-id="b20cf-109">Normalmente, seu aplicativo persiste o identificador de trabalho, para que você possa recuperar posteriormente o trabalho da fila.</span><span class="sxs-lookup"><span data-stu-id="b20cf-109">Typically, your application persists the job identifier, so you can later retrieve the job from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="b20cf-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b20cf-110">Syntax</span></span>


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="b20cf-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b20cf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b20cf-112">*JobID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b20cf-112">*JobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b20cf-113">Identifica o trabalho a ser recuperado da fila de transferência.</span><span class="sxs-lookup"><span data-stu-id="b20cf-113">Identifies the job to retrieve from the transfer queue.</span></span> <span data-ttu-id="b20cf-114">O método [**CreateJob**](ibackgroundcopymanager-createjob.md) retorna o identificador do trabalho.</span><span class="sxs-lookup"><span data-stu-id="b20cf-114">The [**CreateJob**](ibackgroundcopymanager-createjob.md) method returns the job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="b20cf-115">*ppJob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b20cf-115">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b20cf-116">Um ponteiro de interface [**método ibackgroundcopyjob**](ibackgroundcopyjob-.md) para o trabalho especificado por *JobID*.</span><span class="sxs-lookup"><span data-stu-id="b20cf-116">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer to the job specified by *JobID*.</span></span> <span data-ttu-id="b20cf-117">Quando terminar, libere *ppJob*.</span><span class="sxs-lookup"><span data-stu-id="b20cf-117">When done, release *ppJob*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b20cf-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b20cf-118">Return value</span></span>

<span data-ttu-id="b20cf-119">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="b20cf-119">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="b20cf-120">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b20cf-120">Return code</span></span>                                                                                      | <span data-ttu-id="b20cf-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="b20cf-121">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b20cf-122"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b20cf-122"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>         | <span data-ttu-id="b20cf-123">O trabalho foi recuperado com êxito da fila de transferência.</span><span class="sxs-lookup"><span data-stu-id="b20cf-123">Job was successfully retrieved from the transfer queue.</span></span><br/> |
| <dl> <span data-ttu-id="b20cf-124"><dt>**DO_E_NOT_FOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="b20cf-124"><dt>**DO_E_NOT_FOUND**</dt></span></span> </dl> | <span data-ttu-id="b20cf-125">O trabalho não foi encontrado na fila.</span><span class="sxs-lookup"><span data-stu-id="b20cf-125">The job was not found in the queue.</span></span><br/>                     |
| <dl> <span data-ttu-id="b20cf-126"><dt>**E_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b20cf-126"><dt>**E_ACCESSDENIED**</dt></span></span> </dl>   | <span data-ttu-id="b20cf-127">O usuário não tem permissão para recuperar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="b20cf-127">User does not have permission to retrieve the job.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="b20cf-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b20cf-128">Requirements</span></span>



| <span data-ttu-id="b20cf-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b20cf-129">Requirement</span></span> | <span data-ttu-id="b20cf-130">Valor</span><span class="sxs-lookup"><span data-stu-id="b20cf-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b20cf-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b20cf-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b20cf-132">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="b20cf-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b20cf-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b20cf-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b20cf-134">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="b20cf-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b20cf-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b20cf-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b20cf-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b20cf-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b20cf-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="b20cf-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b20cf-138"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b20cf-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b20cf-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b20cf-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="b20cf-140"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b20cf-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b20cf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b20cf-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b20cf-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b20cf-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b20cf-143">IID</span><span class="sxs-lookup"><span data-stu-id="b20cf-143">IID</span></span><br/>                      | <span data-ttu-id="b20cf-144">IID_IBackgroundCopyManager é definido como 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="b20cf-144">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="b20cf-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="b20cf-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b20cf-146">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="b20cf-146">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="b20cf-147">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="b20cf-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="b20cf-148">**Método ibackgroundcopyjob:: GetId**</span><span class="sxs-lookup"><span data-stu-id="b20cf-148">**IBackgroundCopyJob::GetId**</span></span>](ibackgroundcopyjob-getid.md)
</dt> <dt>

[<span data-ttu-id="b20cf-149">**IBackgroundCopyManager:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="b20cf-149">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





