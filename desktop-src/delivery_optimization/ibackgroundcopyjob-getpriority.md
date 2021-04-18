---
title: Método Getmétodo ibackgroundcopyjobname (Deliveryoptimization. h)
description: Recupera o nível de prioridade para o trabalho. O nível de prioridade determina quando o trabalho é processado em relação a outros trabalhos na fila de transferência.
ms.assetid: 2F778B35-8DBB-4540-88C2-A2E18EBB0D89
keywords:
- Método getanteriority
- Método getanteriority, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método getanteriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae9a865045ee1264a0598a3d3c1db8cc3c3b8bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105784976"
---
# <a name="ibackgroundcopyjobgetpriority-method"></a><span data-ttu-id="be6c3-107">Método método ibackgroundcopyjob:: getanteriority</span><span class="sxs-lookup"><span data-stu-id="be6c3-107">IBackgroundCopyJob::GetPriority method</span></span>

<span data-ttu-id="be6c3-108">Recupera o nível de prioridade para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="be6c3-108">Retrieves the priority level for the job.</span></span> <span data-ttu-id="be6c3-109">O nível de prioridade determina quando o trabalho é processado em relação a outros trabalhos na fila de transferência.</span><span class="sxs-lookup"><span data-stu-id="be6c3-109">The priority level determines when the job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="be6c3-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be6c3-110">Syntax</span></span>


```C++
HRESULT GetPriority(
  [out] BG_JOB_PRIORITY *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="be6c3-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be6c3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be6c3-112">*pPriority* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="be6c3-112">*pPriority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="be6c3-113">Prioridade do trabalho em relação a outros trabalhos na fila de transferência.</span><span class="sxs-lookup"><span data-stu-id="be6c3-113">Priority of the job relative to other jobs in the transfer queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be6c3-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be6c3-114">Return value</span></span>

<span data-ttu-id="be6c3-115">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="be6c3-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="be6c3-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="be6c3-116">Return code</span></span>                                                                              | <span data-ttu-id="be6c3-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="be6c3-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="be6c3-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="be6c3-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="be6c3-119">O nível de prioridade foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="be6c3-119">Priority level was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="be6c3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be6c3-120">Requirements</span></span>



| <span data-ttu-id="be6c3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="be6c3-121">Requirement</span></span> | <span data-ttu-id="be6c3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="be6c3-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be6c3-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be6c3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="be6c3-124">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="be6c3-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="be6c3-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be6c3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="be6c3-126">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="be6c3-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="be6c3-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be6c3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="be6c3-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="be6c3-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="be6c3-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="be6c3-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be6c3-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be6c3-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="be6c3-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be6c3-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="be6c3-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be6c3-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="be6c3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="be6c3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be6c3-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be6c3-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="be6c3-135">IID</span><span class="sxs-lookup"><span data-stu-id="be6c3-135">IID</span></span><br/>                      | <span data-ttu-id="be6c3-136">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="be6c3-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="be6c3-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="be6c3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be6c3-138">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="be6c3-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="be6c3-139">**Método ibackgroundcopyjob:: setanteriority**</span><span class="sxs-lookup"><span data-stu-id="be6c3-139">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





