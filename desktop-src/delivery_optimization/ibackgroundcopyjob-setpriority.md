---
title: Método de método ibackgroundcopyjob prepriorion (Deliveryoptimization. h)
description: Especifica o nível de prioridade do seu trabalho. O nível de prioridade determina quando seu trabalho é processado em relação a outros trabalhos na fila de transferência.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- Método setanteriority
- Método setanteriority, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método setanteriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fb6407c5d693a2c6e75f8aaf8f7a0544d08cdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644703"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a><span data-ttu-id="ba5a1-107">Método método ibackgroundcopyjob:: prepriorion</span><span class="sxs-lookup"><span data-stu-id="ba5a1-107">IBackgroundCopyJob::SetPriority method</span></span>

<span data-ttu-id="ba5a1-108">Especifica o nível de prioridade do seu trabalho.</span><span class="sxs-lookup"><span data-stu-id="ba5a1-108">Specifies the priority level of your job.</span></span> <span data-ttu-id="ba5a1-109">O nível de prioridade determina quando seu trabalho é processado em relação a outros trabalhos na fila de transferência.</span><span class="sxs-lookup"><span data-stu-id="ba5a1-109">The priority level determines when your job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba5a1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba5a1-110">Syntax</span></span>


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a><span data-ttu-id="ba5a1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba5a1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba5a1-112">*Prioridade* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="ba5a1-112">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba5a1-113">Especifica o nível de prioridade do seu trabalho em relação a outros trabalhos na fila de transferência.</span><span class="sxs-lookup"><span data-stu-id="ba5a1-113">Specifies the priority level of your job relative to other jobs in the transfer queue.</span></span> <span data-ttu-id="ba5a1-114">O padrão é BG_JOB_PRIORITY_NORMAL.</span><span class="sxs-lookup"><span data-stu-id="ba5a1-114">The default is BG_JOB_PRIORITY_NORMAL.</span></span> <span data-ttu-id="ba5a1-115">Para obter uma lista de níveis de prioridade, consulte a enumeração [**BG_JOB_PRIORITY**](bg-job-priority-.md) .</span><span class="sxs-lookup"><span data-stu-id="ba5a1-115">For a list of priority levels, see the [**BG_JOB_PRIORITY**](bg-job-priority-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba5a1-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba5a1-116">Return value</span></span>

<span data-ttu-id="ba5a1-117">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="ba5a1-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="ba5a1-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ba5a1-118">Return code</span></span>                                                                              | <span data-ttu-id="ba5a1-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba5a1-119">Description</span></span>                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="ba5a1-120"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="ba5a1-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="ba5a1-121">A prioridade do trabalho foi definida com êxito.</span><span class="sxs-lookup"><span data-stu-id="ba5a1-121">Job priority was successfully set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ba5a1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba5a1-122">Requirements</span></span>



| <span data-ttu-id="ba5a1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba5a1-123">Requirement</span></span> | <span data-ttu-id="ba5a1-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ba5a1-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba5a1-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba5a1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ba5a1-126">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="ba5a1-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ba5a1-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba5a1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ba5a1-128">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="ba5a1-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ba5a1-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba5a1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba5a1-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba5a1-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba5a1-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="ba5a1-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ba5a1-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ba5a1-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="ba5a1-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba5a1-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba5a1-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba5a1-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="ba5a1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="ba5a1-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba5a1-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba5a1-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="ba5a1-137">IID</span><span class="sxs-lookup"><span data-stu-id="ba5a1-137">IID</span></span><br/>                      | <span data-ttu-id="ba5a1-138">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="ba5a1-138">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ba5a1-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba5a1-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba5a1-140">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="ba5a1-140">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="ba5a1-141">**BG_JOB_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="ba5a1-141">**BG_JOB_PRIORITY**</span></span>](bg-job-priority-.md)
</dt> <dt>

[<span data-ttu-id="ba5a1-142">**Método ibackgroundcopyjob:: getanteriority**</span><span class="sxs-lookup"><span data-stu-id="ba5a1-142">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





