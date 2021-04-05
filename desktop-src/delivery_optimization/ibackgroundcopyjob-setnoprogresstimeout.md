---
title: Método método ibackgroundcopyjob SetNoProgressTimeout (Deliveryoptimization. h)
description: Define o período de tempo que a otimização de entrega (DO) tenta transferir o arquivo depois que ocorre uma condição de erro transitória. Se houver um progresso, o temporizador será redefinido.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Método SetNoProgressTimeout
- Método SetNoProgressTimeout, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método SetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 276c8c44d2b2b034543aae25361c5f5c94046f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009434"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a><span data-ttu-id="100f5-107">Método método ibackgroundcopyjob:: SetNoProgressTimeout</span><span class="sxs-lookup"><span data-stu-id="100f5-107">IBackgroundCopyJob::SetNoProgressTimeout method</span></span>

<span data-ttu-id="100f5-108">Define o período de tempo que a otimização de entrega (DO) tenta transferir o arquivo depois que ocorre uma condição de erro transitória.</span><span class="sxs-lookup"><span data-stu-id="100f5-108">Sets the length of time that Delivery Optimization (DO) tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="100f5-109">Se houver um progresso, o temporizador será redefinido.</span><span class="sxs-lookup"><span data-stu-id="100f5-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="100f5-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="100f5-110">Syntax</span></span>


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="100f5-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="100f5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="100f5-112">*RetryPeriod* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="100f5-112">*RetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="100f5-113">Período de tempo, em segundos, que tenta transferir o arquivo após não ter sido feito nenhum progresso.</span><span class="sxs-lookup"><span data-stu-id="100f5-113">Length of time, in seconds, that DO tries to transfer the file after there has been no progress made.</span></span> <span data-ttu-id="100f5-114">O período de repetição padrão para trabalho de alta prioridade é de 3600 segundos (1 hora) e o trabalho de baixa prioridade é de 86400 segundos (24 horas).</span><span class="sxs-lookup"><span data-stu-id="100f5-114">The default retry period for high priority job is 3600 seconds (1 hour) and for low priority job is 86400 seconds (24 hours).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="100f5-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="100f5-115">Return value</span></span>

<span data-ttu-id="100f5-116">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="100f5-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="100f5-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="100f5-117">Return code</span></span>                                                                                          | <span data-ttu-id="100f5-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="100f5-118">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="100f5-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="100f5-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="100f5-120">Período de repetição definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="100f5-120">Retry period successfully set.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="100f5-121"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="100f5-121"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="100f5-122">O estado do trabalho não pode ser BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="100f5-122">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="100f5-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="100f5-123">Remarks</span></span>

<span data-ttu-id="100f5-124">Se o não fizer o andamento durante o período de repetição, ele moverá o estado do trabalho de BG_JOB_STATE_TRANSIENT_ERROR para BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="100f5-124">If DO does not make progress during the retry period, it moves the state of the job from BG_JOB_STATE_TRANSIENT_ERROR to BG_JOB_STATE_ERROR.</span></span> <span data-ttu-id="100f5-125">Se você solicitar uma notificação de erro, o chamará o retorno de chamada [**JobError**](https://www.bing.com/search?q=**JobError**) .</span><span class="sxs-lookup"><span data-stu-id="100f5-125">If you request error notification, DO then calls your [**JobError**](https://www.bing.com/search?q=**JobError**) callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="100f5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="100f5-126">Requirements</span></span>



| <span data-ttu-id="100f5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="100f5-127">Requirement</span></span> | <span data-ttu-id="100f5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="100f5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="100f5-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="100f5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="100f5-130">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="100f5-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="100f5-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="100f5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="100f5-132">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="100f5-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="100f5-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="100f5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="100f5-134"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="100f5-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="100f5-135">INSERI</span><span class="sxs-lookup"><span data-stu-id="100f5-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="100f5-136"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="100f5-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="100f5-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="100f5-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="100f5-138"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="100f5-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="100f5-139">DLL</span><span class="sxs-lookup"><span data-stu-id="100f5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="100f5-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="100f5-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="100f5-141">IID</span><span class="sxs-lookup"><span data-stu-id="100f5-141">IID</span></span><br/>                      | <span data-ttu-id="100f5-142">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="100f5-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="100f5-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="100f5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="100f5-144">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="100f5-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="100f5-145">**Método ibackgroundcopyjob:: GetNoProgressTimeout**</span><span class="sxs-lookup"><span data-stu-id="100f5-145">**IBackgroundCopyJob::GetNoProgressTimeout**</span></span>](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





