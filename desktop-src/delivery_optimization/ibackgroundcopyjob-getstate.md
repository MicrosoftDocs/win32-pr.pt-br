---
title: Método GetState método ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera o estado do trabalho.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- Método GetState
- Método GetState, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetState
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b195377a44cab8f336bae8090bacc5ca5624d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644704"
---
# <a name="ibackgroundcopyjobgetstate-method"></a><span data-ttu-id="380bf-106">Método método ibackgroundcopyjob:: GetState</span><span class="sxs-lookup"><span data-stu-id="380bf-106">IBackgroundCopyJob::GetState method</span></span>

<span data-ttu-id="380bf-107">Recupera o estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="380bf-107">Retrieves the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="380bf-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="380bf-108">Syntax</span></span>


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a><span data-ttu-id="380bf-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="380bf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="380bf-110">*pJobState* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="380bf-110">*pJobState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="380bf-111">O estado do trabalho.</span><span class="sxs-lookup"><span data-stu-id="380bf-111">The state of the job.</span></span> <span data-ttu-id="380bf-112">Por exemplo, o estado reflete se o trabalho está em erro, transferindo dados ou suspenso.</span><span class="sxs-lookup"><span data-stu-id="380bf-112">For example, the state reflects whether the job is in error, transferring data, or suspended.</span></span> <span data-ttu-id="380bf-113">Para obter uma lista de Estados de trabalho, consulte a enumeração [**BG_JOB_STATE**](bg-job-state-.md) .</span><span class="sxs-lookup"><span data-stu-id="380bf-113">For a list of job states, see the [**BG_JOB_STATE**](bg-job-state-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="380bf-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="380bf-114">Return value</span></span>

<span data-ttu-id="380bf-115">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="380bf-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="380bf-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="380bf-116">Return code</span></span>                                                                              | <span data-ttu-id="380bf-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="380bf-117">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="380bf-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="380bf-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="380bf-119">O estado do trabalho foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="380bf-119">The state of the job was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="380bf-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="380bf-120">Remarks</span></span>

<span data-ttu-id="380bf-121">Se você quiser saber quando um trabalho está com erro ou transferiu todos os arquivos do trabalho, você pode usar esse método para sondar o estado do trabalho ou pode se registrar para receber notificações quando ocorrerem eventos.</span><span class="sxs-lookup"><span data-stu-id="380bf-121">If you want to know when a job is in error or has transferred all the files in the job, you can use this method to poll for the state of the job or you can register to receive notification when events occur.</span></span> <span data-ttu-id="380bf-122">Para obter detalhes sobre como registrar-se para receber a notificação de eventos, consulte a interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="380bf-122">For details on registering to receive event notification, see the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="380bf-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="380bf-123">Requirements</span></span>



| <span data-ttu-id="380bf-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="380bf-124">Requirement</span></span> | <span data-ttu-id="380bf-125">Valor</span><span class="sxs-lookup"><span data-stu-id="380bf-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="380bf-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="380bf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="380bf-127">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="380bf-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="380bf-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="380bf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="380bf-129">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="380bf-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="380bf-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="380bf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="380bf-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="380bf-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="380bf-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="380bf-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="380bf-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="380bf-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="380bf-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="380bf-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="380bf-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="380bf-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="380bf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="380bf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="380bf-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="380bf-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="380bf-138">IID</span><span class="sxs-lookup"><span data-stu-id="380bf-138">IID</span></span><br/>                      | <span data-ttu-id="380bf-139">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="380bf-139">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="380bf-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="380bf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="380bf-141">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="380bf-141">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="380bf-142">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="380bf-142">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="380bf-143">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="380bf-143">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> </dl>

 

 





