---
title: Método método ibackgroundcopyjob GetNotifyInterface (Deliveryoptimization. h)
description: Recupera o ponteiro de interface para sua implementação da interface IBackgroundCopyCallback.
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- Método GetNotifyInterface
- Método GetNotifyInterface, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6586a90de5783ceb24e5a7677f699a9cf6dfa60c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763801"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a><span data-ttu-id="57045-106">Método método ibackgroundcopyjob:: GetNotifyInterface</span><span class="sxs-lookup"><span data-stu-id="57045-106">IBackgroundCopyJob::GetNotifyInterface method</span></span>

<span data-ttu-id="57045-107">Recupera o ponteiro de interface para sua implementação da interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="57045-107">Retrieves the interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="57045-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57045-108">Syntax</span></span>


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="57045-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57045-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57045-110">*ppNotifyInterface* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="57045-110">*ppNotifyInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="57045-111">Ponteiro de interface para sua implementação da interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="57045-111">Interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="57045-112">Quando terminar, libere *ppNotifyInterface*.</span><span class="sxs-lookup"><span data-stu-id="57045-112">When done, release *ppNotifyInterface*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57045-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57045-113">Return value</span></span>

<span data-ttu-id="57045-114">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="57045-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="57045-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="57045-115">Return code</span></span>                                                                              | <span data-ttu-id="57045-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="57045-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="57045-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="57045-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="57045-118">O ponteiro da interface de notificação foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="57045-118">Notification interface pointer was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="57045-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57045-119">Requirements</span></span>



| <span data-ttu-id="57045-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="57045-120">Requirement</span></span> | <span data-ttu-id="57045-121">Valor</span><span class="sxs-lookup"><span data-stu-id="57045-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57045-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57045-122">Minimum supported client</span></span><br/> | <span data-ttu-id="57045-123">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="57045-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="57045-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="57045-124">Minimum supported server</span></span><br/> | <span data-ttu-id="57045-125">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="57045-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="57045-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57045-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="57045-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="57045-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="57045-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="57045-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="57045-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="57045-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="57045-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57045-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="57045-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57045-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="57045-132">DLL</span><span class="sxs-lookup"><span data-stu-id="57045-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57045-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57045-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="57045-134">IID</span><span class="sxs-lookup"><span data-stu-id="57045-134">IID</span></span><br/>                      | <span data-ttu-id="57045-135">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="57045-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="57045-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="57045-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57045-137">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="57045-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="57045-138">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="57045-138">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="57045-139">**Método ibackgroundcopyjob:: GetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="57045-139">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="57045-140">**Método ibackgroundcopyjob:: SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="57045-140">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





