---
title: Método gettimeies do método ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera carimbos de data/hora relacionados ao trabalho, como a hora em que o trabalho foi criado ou modificado pela última vez.
ms.assetid: 9002FB8D-08CB-4878-980F-15FE0DC952A6
keywords:
- Método gettimeies
- Método gettimers, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método gettimes
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetTimes
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04e779b59e0976e77b287bc575f3b08f8d39340a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455251"
---
# <a name="ibackgroundcopyjobgettimes-method"></a><span data-ttu-id="bb1b4-106">Método método ibackgroundcopyjob:: gettimeies</span><span class="sxs-lookup"><span data-stu-id="bb1b4-106">IBackgroundCopyJob::GetTimes method</span></span>

<span data-ttu-id="bb1b4-107">Recupera carimbos de data/hora relacionados ao trabalho, como a hora em que o trabalho foi criado ou modificado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="bb1b4-107">Retrieves job-related time stamps, such as the time that the job was created or last modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb1b4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb1b4-108">Syntax</span></span>


```C++
HRESULT GetTimes(
  [out] BG_JOB_TIMES *pTimes
);
```



## <a name="parameters"></a><span data-ttu-id="bb1b4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb1b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb1b4-110">*pTimes* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bb1b4-110">*pTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb1b4-111">Contém carimbos de data/hora relacionados ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="bb1b4-111">Contains job-related time stamps.</span></span> <span data-ttu-id="bb1b4-112">Para carimbos de data/hora disponíveis, consulte a estrutura de [**BG_JOB_TIMES**](bg-job-times.md) .</span><span class="sxs-lookup"><span data-stu-id="bb1b4-112">For available time stamps, see the [**BG_JOB_TIMES**](bg-job-times.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb1b4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bb1b4-113">Return value</span></span>

<span data-ttu-id="bb1b4-114">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="bb1b4-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="bb1b4-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bb1b4-115">Return code</span></span>                                                                              | <span data-ttu-id="bb1b4-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="bb1b4-116">Description</span></span>                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="bb1b4-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="bb1b4-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="bb1b4-118">Carimbos de data/hora recuperados com êxito.</span><span class="sxs-lookup"><span data-stu-id="bb1b4-118">Time stamps were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bb1b4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb1b4-119">Requirements</span></span>



| <span data-ttu-id="bb1b4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb1b4-120">Requirement</span></span> | <span data-ttu-id="bb1b4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bb1b4-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb1b4-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb1b4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bb1b4-123">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="bb1b4-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bb1b4-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb1b4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bb1b4-125">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="bb1b4-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bb1b4-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb1b4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb1b4-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb1b4-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb1b4-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="bb1b4-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bb1b4-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bb1b4-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="bb1b4-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb1b4-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb1b4-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb1b4-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="bb1b4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bb1b4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb1b4-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb1b4-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="bb1b4-134">IID</span><span class="sxs-lookup"><span data-stu-id="bb1b4-134">IID</span></span><br/>                      | <span data-ttu-id="bb1b4-135">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="bb1b4-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="bb1b4-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb1b4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb1b4-137">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="bb1b4-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="bb1b4-138">**BG_JOB_TIMES**</span><span class="sxs-lookup"><span data-stu-id="bb1b4-138">**BG_JOB_TIMES**</span></span>](bg-job-times.md)
</dt> </dl>

 

 





