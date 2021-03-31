---
title: Método GetProgress do método ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera informações de progresso relacionadas ao trabalho, como o número de bytes e arquivos transferidos.
ms.assetid: E23C82E1-3805-4C5D-9F18-0DA17F7C473E
keywords:
- Método GetProgress
- Método GetProgress, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d49a040bb5656ae6ef6d926a45b31808623e399b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085647"
---
# <a name="ibackgroundcopyjobgetprogress-method"></a><span data-ttu-id="a8828-106">Método método ibackgroundcopyjob:: GetProgress</span><span class="sxs-lookup"><span data-stu-id="a8828-106">IBackgroundCopyJob::GetProgress method</span></span>

<span data-ttu-id="a8828-107">Recupera informações de progresso relacionadas ao trabalho, como o número de bytes e arquivos transferidos.</span><span class="sxs-lookup"><span data-stu-id="a8828-107">Retrieves job-related progress information, such as the number of bytes and files transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8828-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8828-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_JOB_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="a8828-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8828-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8828-110">*pProgress* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a8828-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8828-111">Contém dados que você pode usar para calcular a porcentagem do trabalho que está concluído.</span><span class="sxs-lookup"><span data-stu-id="a8828-111">Contains data that you can use to calculate the percentage of the job that is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8828-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8828-112">Return value</span></span>

<span data-ttu-id="a8828-113">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="a8828-113">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="a8828-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a8828-114">Return code</span></span>                                                                              | <span data-ttu-id="a8828-115">Description</span><span class="sxs-lookup"><span data-stu-id="a8828-115">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="a8828-116"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="a8828-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="a8828-117">As informações de progresso foram recuperadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="a8828-117">Progress information was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a8828-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8828-118">Requirements</span></span>



| <span data-ttu-id="a8828-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8828-119">Requirement</span></span> | <span data-ttu-id="a8828-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a8828-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8828-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8828-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a8828-122">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="a8828-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a8828-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8828-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a8828-124">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="a8828-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a8828-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8828-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8828-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8828-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8828-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="a8828-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a8828-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a8828-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a8828-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8828-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="a8828-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8828-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a8828-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a8828-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8828-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8828-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a8828-133">IID</span><span class="sxs-lookup"><span data-stu-id="a8828-133">IID</span></span><br/>                      | <span data-ttu-id="a8828-134">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="a8828-134">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a8828-135">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a8828-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8828-136">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="a8828-136">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





