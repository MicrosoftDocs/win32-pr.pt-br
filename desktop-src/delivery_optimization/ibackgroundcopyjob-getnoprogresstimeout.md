---
title: Método método ibackgroundcopyjob GetNoProgressTimeout (Deliveryoptimization. h)
description: Recupera o período de tempo que o serviço tenta transferir o arquivo depois que ocorre uma condição de erro transitória. Se houver um progresso, o temporizador será redefinido.
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- Método GetNoProgressTimeout
- Método GetNoProgressTimeout, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ccd236c17612aa03a28e07a08d087454f8db6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455252"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a><span data-ttu-id="9534a-107">Método método ibackgroundcopyjob:: GetNoProgressTimeout</span><span class="sxs-lookup"><span data-stu-id="9534a-107">IBackgroundCopyJob::GetNoProgressTimeout method</span></span>

<span data-ttu-id="9534a-108">Recupera o período de tempo que o serviço tenta transferir o arquivo depois que ocorre uma condição de erro transitória.</span><span class="sxs-lookup"><span data-stu-id="9534a-108">Retrieves the length of time that the service tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="9534a-109">Se houver um progresso, o temporizador será redefinido.</span><span class="sxs-lookup"><span data-stu-id="9534a-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="9534a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9534a-110">Syntax</span></span>


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="9534a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9534a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9534a-112">*pRetryPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9534a-112">*pRetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9534a-113">Período de tempo, em segundos, que o serviço tenta transferir o arquivo após ocorrer um erro transitório.</span><span class="sxs-lookup"><span data-stu-id="9534a-113">Length of time, in seconds, that the service tries to transfer the file after a transient error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9534a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9534a-114">Return value</span></span>

<span data-ttu-id="9534a-115">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="9534a-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="9534a-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9534a-116">Return code</span></span>                                                                              | <span data-ttu-id="9534a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="9534a-117">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="9534a-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="9534a-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="9534a-119">O tempo limite foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="9534a-119">Time-out was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9534a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9534a-120">Requirements</span></span>



| <span data-ttu-id="9534a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9534a-121">Requirement</span></span> | <span data-ttu-id="9534a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9534a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9534a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9534a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9534a-124">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="9534a-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9534a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9534a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9534a-126">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="9534a-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9534a-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9534a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9534a-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9534a-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9534a-129">INSERI</span><span class="sxs-lookup"><span data-stu-id="9534a-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9534a-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9534a-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9534a-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9534a-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="9534a-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9534a-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9534a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9534a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9534a-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9534a-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9534a-135">IID</span><span class="sxs-lookup"><span data-stu-id="9534a-135">IID</span></span><br/>                      | <span data-ttu-id="9534a-136">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="9534a-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9534a-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="9534a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9534a-138">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="9534a-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="9534a-139">**Método ibackgroundcopyjob:: SetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="9534a-139">**IBackgroundCopyJob::SetNoProgressTimeout**</span></span>](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





