---
title: Método método ibackgroundcopyjob SetNotifyInterface (Deliveryoptimization. h)
description: Identifica a implementação da interface IBackgroundCopyCallback a ser feita. Use a interface IBackgroundCopyCallback para receber a notificação de eventos relacionados ao trabalho.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- Método SetNotifyInterface
- Método SetNotifyInterface, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método SetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f3b6e8205eb60cbd2ca645cd484e41f8f242619d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295772"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a><span data-ttu-id="a7d99-107">Método método ibackgroundcopyjob:: SetNotifyInterface</span><span class="sxs-lookup"><span data-stu-id="a7d99-107">IBackgroundCopyJob::SetNotifyInterface method</span></span>

<span data-ttu-id="a7d99-108">Identifica a implementação da interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) a ser feita.</span><span class="sxs-lookup"><span data-stu-id="a7d99-108">Identifies your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to DO.</span></span> <span data-ttu-id="a7d99-109">Use a interface **IBackgroundCopyCallback** para receber a notificação de eventos relacionados ao trabalho.</span><span class="sxs-lookup"><span data-stu-id="a7d99-109">Use the **IBackgroundCopyCallback** interface to receive notification of job-related events.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d99-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7d99-110">Syntax</span></span>


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="a7d99-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7d99-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7d99-112">*pNotifyInterface*</span><span class="sxs-lookup"><span data-stu-id="a7d99-112">*pNotifyInterface*</span></span> 
</dt> <dd>

<span data-ttu-id="a7d99-113">Um ponteiro de interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="a7d99-113">An [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface pointer.</span></span> <span data-ttu-id="a7d99-114">Para remover o ponteiro de interface de retorno de chamada atual, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a7d99-114">To remove the current callback interface pointer, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7d99-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7d99-115">Return value</span></span>

<span data-ttu-id="a7d99-116">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="a7d99-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="a7d99-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a7d99-117">Return code</span></span>                                                                              | <span data-ttu-id="a7d99-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7d99-118">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a7d99-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="a7d99-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="a7d99-120">O ponteiro da interface de notificação foi definido com êxito.</span><span class="sxs-lookup"><span data-stu-id="a7d99-120">Notification interface pointer was successfully set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a7d99-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7d99-121">Remarks</span></span>

<span data-ttu-id="a7d99-122">Chame esse método somente se você implementar a interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .</span><span class="sxs-lookup"><span data-stu-id="a7d99-122">Call this method only if you implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="a7d99-123">Use o método **SetNotifyInterface** em conjunto com o método [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) para especificar o tipo de notificação que você deseja receber.</span><span class="sxs-lookup"><span data-stu-id="a7d99-123">Use the **SetNotifyInterface** method in conjunction with the [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to specify the type of notification that you want to receive.</span></span>

<span data-ttu-id="a7d99-124">A interface de notificação torna-se inválida quando o aplicativo é encerrado; Não mantém a interface de notificação.</span><span class="sxs-lookup"><span data-stu-id="a7d99-124">The notification interface becomes invalid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="a7d99-125">Como resultado, o processo de inicialização do aplicativo deve chamar o método **SetNotifyInterface** nesses trabalhos existentes para os quais você deseja receber a notificação.</span><span class="sxs-lookup"><span data-stu-id="a7d99-125">As a result, your application's initialization process should call the **SetNotifyInterface** method on those existing jobs for which you want to receive notification.</span></span> <span data-ttu-id="a7d99-126">Se você precisar capturar informações de estado e de progresso ocorridas desde a última vez em que seu aplicativo foi executado, pesquise informações de estado e progresso durante a inicialização do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a7d99-126">If you need to capture state and progress information that occurred since the last time your application was run, poll for state and progress information during application initialization.</span></span>

<span data-ttu-id="a7d99-127">Somente o proprietário/criador do trabalho ou um administrador pode se registrar para notificações.</span><span class="sxs-lookup"><span data-stu-id="a7d99-127">Only the job owner/creator or an administrator can register for notifications.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7d99-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7d99-128">Requirements</span></span>



| <span data-ttu-id="a7d99-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7d99-129">Requirement</span></span> | <span data-ttu-id="a7d99-130">Valor</span><span class="sxs-lookup"><span data-stu-id="a7d99-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d99-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7d99-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a7d99-132">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="a7d99-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a7d99-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7d99-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a7d99-134">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="a7d99-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a7d99-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7d99-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7d99-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7d99-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7d99-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="a7d99-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7d99-138"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7d99-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a7d99-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7d99-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="a7d99-140"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a7d99-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a7d99-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a7d99-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7d99-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7d99-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a7d99-143">IID</span><span class="sxs-lookup"><span data-stu-id="a7d99-143">IID</span></span><br/>                      | <span data-ttu-id="a7d99-144">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="a7d99-144">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a7d99-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7d99-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d99-146">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="a7d99-146">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="a7d99-147">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="a7d99-147">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="a7d99-148">**Método ibackgroundcopyjob:: GetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="a7d99-148">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="a7d99-149">**Método ibackgroundcopyjob:: SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="a7d99-149">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





