---
title: Método método ibackgroundcopyjob GetType (Deliveryoptimization. h)
description: Recupera o tipo de transferência que está sendo executada, como um download de arquivo ou upload.
ms.assetid: F543A601-9385-4A73-A4E2-DE61433E84D3
keywords:
- Método GetType
- Método GetType, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetType
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetType
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b0a09a3c7387b5b911bf6731921e7ed4e9b9163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009013"
---
# <a name="ibackgroundcopyjobgettype-method"></a><span data-ttu-id="783f4-106">Método método ibackgroundcopyjob:: GetType</span><span class="sxs-lookup"><span data-stu-id="783f4-106">IBackgroundCopyJob::GetType method</span></span>

<span data-ttu-id="783f4-107">Recupera o tipo de transferência que está sendo executada, como um download de arquivo ou upload.</span><span class="sxs-lookup"><span data-stu-id="783f4-107">Retrieves the type of transfer being performed, such as a file download or upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="783f4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="783f4-108">Syntax</span></span>


```C++
HRESULT GetType(
  [out] BG_JOB_TYPE *pJobType
);
```



## <a name="parameters"></a><span data-ttu-id="783f4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="783f4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="783f4-110">*pJobType* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="783f4-110">*pJobType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="783f4-111">Tipo de transferência sendo executada.</span><span class="sxs-lookup"><span data-stu-id="783f4-111">Type of transfer being performed.</span></span> <span data-ttu-id="783f4-112">Para obter uma lista de tipos de transferência, consulte a enumeração [**BG_JOB_TYPE**](bg-job-type.md) .</span><span class="sxs-lookup"><span data-stu-id="783f4-112">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="783f4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="783f4-113">Return value</span></span>

<span data-ttu-id="783f4-114">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="783f4-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="783f4-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="783f4-115">Return code</span></span>                                                                              | <span data-ttu-id="783f4-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="783f4-116">Description</span></span>                                          |
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="783f4-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="783f4-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="783f4-118">O tipo de transferência foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="783f4-118">Transfer type was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="783f4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="783f4-119">Remarks</span></span>

<span data-ttu-id="783f4-120">Especifique o tipo de transferência ao criar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="783f4-120">Specify the type of transfer when you create the job.</span></span>

## <a name="requirements"></a><span data-ttu-id="783f4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="783f4-121">Requirements</span></span>



| <span data-ttu-id="783f4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="783f4-122">Requirement</span></span> | <span data-ttu-id="783f4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="783f4-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="783f4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="783f4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="783f4-125">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="783f4-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="783f4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="783f4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="783f4-127">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="783f4-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="783f4-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="783f4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="783f4-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="783f4-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="783f4-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="783f4-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="783f4-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="783f4-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="783f4-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="783f4-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="783f4-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="783f4-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="783f4-134">DLL</span><span class="sxs-lookup"><span data-stu-id="783f4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="783f4-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="783f4-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="783f4-136">IID</span><span class="sxs-lookup"><span data-stu-id="783f4-136">IID</span></span><br/>                      | <span data-ttu-id="783f4-137">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="783f4-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="783f4-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="783f4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="783f4-139">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="783f4-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="783f4-140">**BG_JOB_TYPE**</span><span class="sxs-lookup"><span data-stu-id="783f4-140">**BG_JOB_TYPE**</span></span>](bg-job-type.md)
</dt> <dt>

[<span data-ttu-id="783f4-141">**IBackgroundCopyManager:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="783f4-141">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





