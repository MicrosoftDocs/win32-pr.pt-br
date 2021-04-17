---
title: Método de suspensão de método ibackgroundcopyjob (Deliveryoptimization. h)
description: Suspende um trabalho. Novos trabalhos, trabalhos que estão em erro e trabalhos que concluíram a transferência de arquivos são suspensos automaticamente.
ms.assetid: 23EED354-A3AC-4865-8C06-ADA097851F96
keywords:
- Método Suspend
- Método Suspend, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método Suspend
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Suspend
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd4464a04f87a7759e9b51974eef2188ba1d0c2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369614"
---
# <a name="ibackgroundcopyjobsuspend-method"></a><span data-ttu-id="7639b-107">Método método ibackgroundcopyjob:: Suspend</span><span class="sxs-lookup"><span data-stu-id="7639b-107">IBackgroundCopyJob::Suspend method</span></span>

<span data-ttu-id="7639b-108">Suspende um trabalho.</span><span class="sxs-lookup"><span data-stu-id="7639b-108">Suspends a job.</span></span> <span data-ttu-id="7639b-109">Novos trabalhos, trabalhos que estão em erro e trabalhos que concluíram a transferência de arquivos são suspensos automaticamente.</span><span class="sxs-lookup"><span data-stu-id="7639b-109">New jobs, jobs that are in error, and jobs that have finished transferring files are automatically suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="7639b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7639b-110">Syntax</span></span>


```C++
HRESULT Suspend();
```



## <a name="parameters"></a><span data-ttu-id="7639b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7639b-111">Parameters</span></span>

<span data-ttu-id="7639b-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7639b-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7639b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7639b-113">Return value</span></span>

<span data-ttu-id="7639b-114">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="7639b-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="7639b-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7639b-115">Return code</span></span>                                                                                          | <span data-ttu-id="7639b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="7639b-116">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7639b-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="7639b-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="7639b-118">Trabalho suspenso com êxito.</span><span class="sxs-lookup"><span data-stu-id="7639b-118">Successfully suspended the job.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="7639b-119"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="7639b-119"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="7639b-120">O estado do trabalho não pode ser BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="7639b-120">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7639b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7639b-121">Requirements</span></span>



| <span data-ttu-id="7639b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7639b-122">Requirement</span></span> | <span data-ttu-id="7639b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7639b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7639b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7639b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7639b-125">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="7639b-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7639b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7639b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7639b-127">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="7639b-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7639b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7639b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7639b-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="7639b-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="7639b-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="7639b-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7639b-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7639b-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="7639b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7639b-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="7639b-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7639b-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="7639b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7639b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7639b-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7639b-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="7639b-136">IID</span><span class="sxs-lookup"><span data-stu-id="7639b-136">IID</span></span><br/>                      | <span data-ttu-id="7639b-137">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="7639b-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7639b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="7639b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7639b-139">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="7639b-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="7639b-140">**Método ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="7639b-140">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="7639b-141">**Método ibackgroundcopyjob:: retomar**</span><span class="sxs-lookup"><span data-stu-id="7639b-141">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





