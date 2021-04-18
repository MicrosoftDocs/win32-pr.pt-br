---
title: Interface IBackgroundCopyCallback (Deliveryoptimization. h)
description: Implemente a interface IBackgroundCopyCallback para receber a notificação de que um trabalho foi concluído, foi modificado ou está com erro. Os clientes usam essa interface em vez de sondar o status do trabalho.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- Interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4169acec87e4d1e8a31eecaa4f93b9404aafb714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105798273"
---
# <a name="ibackgroundcopycallback-interface"></a><span data-ttu-id="f978d-106">Interface IBackgroundCopyCallback</span><span class="sxs-lookup"><span data-stu-id="f978d-106">IBackgroundCopyCallback interface</span></span>

<span data-ttu-id="f978d-107">Implemente a interface **IBackgroundCopyCallback** para receber a notificação de que um trabalho foi concluído, foi modificado ou está com erro.</span><span class="sxs-lookup"><span data-stu-id="f978d-107">Implement the **IBackgroundCopyCallback** interface to receive notification that a job is complete, has been modified, or is in error.</span></span> <span data-ttu-id="f978d-108">Os clientes usam essa interface em vez de sondar o status do trabalho.</span><span class="sxs-lookup"><span data-stu-id="f978d-108">Clients use this interface instead of polling for the status of the job.</span></span>

## <a name="members"></a><span data-ttu-id="f978d-109">Membros</span><span class="sxs-lookup"><span data-stu-id="f978d-109">Members</span></span>

<span data-ttu-id="f978d-110">A interface **IBackgroundCopyCallback** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f978d-110">The **IBackgroundCopyCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f978d-111">**IBackgroundCopyCallback** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f978d-111">**IBackgroundCopyCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="f978d-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="f978d-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f978d-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="f978d-113">Methods</span></span>

<span data-ttu-id="f978d-114">A interface **IBackgroundCopyCallback** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f978d-114">The **IBackgroundCopyCallback** interface has these methods.</span></span>



| <span data-ttu-id="f978d-115">Método</span><span class="sxs-lookup"><span data-stu-id="f978d-115">Method</span></span>                                                                    | <span data-ttu-id="f978d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="f978d-116">Description</span></span>                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="f978d-117">**JobError**</span><span class="sxs-lookup"><span data-stu-id="f978d-117">**JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)               | <span data-ttu-id="f978d-118">Chamado quando ocorre um erro.</span><span class="sxs-lookup"><span data-stu-id="f978d-118">Called when an error occurs.</span></span><br/>                                           |
| [<span data-ttu-id="f978d-119">**JobModification**</span><span class="sxs-lookup"><span data-stu-id="f978d-119">**JobModification**</span></span>](ibackgroundcopycallback-jobmodification-method.md) | <span data-ttu-id="f978d-120">Chamado quando um trabalho é modificado.</span><span class="sxs-lookup"><span data-stu-id="f978d-120">Called when a job is modified.</span></span><br/>                                         |
| [<span data-ttu-id="f978d-121">**JobTransferred**</span><span class="sxs-lookup"><span data-stu-id="f978d-121">**JobTransferred**</span></span>](ibackgroundcopycallback-jobtransferred.md)          | <span data-ttu-id="f978d-122">Chamado quando todos os arquivos no trabalho foram transferidos com êxito.</span><span class="sxs-lookup"><span data-stu-id="f978d-122">Called when all of the files in the job have successfully transferred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f978d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f978d-123">Remarks</span></span>

<span data-ttu-id="f978d-124">Para receber notificações, chame o método [**método ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) para especificar o ponteiro de interface para sua implementação de **IBackgroundCopyCallback** .</span><span class="sxs-lookup"><span data-stu-id="f978d-124">To receive notifications, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to specify the interface pointer to your **IBackgroundCopyCallback** implementation.</span></span> <span data-ttu-id="f978d-125">Para especificar quais notificações você deseja receber, chame o método [**método ibackgroundcopyjob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) .</span><span class="sxs-lookup"><span data-stu-id="f978d-125">To specify which notifications you want to receive, call the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method.</span></span>

<span data-ttu-id="f978d-126">Chamará seus retornos de chamada, desde que o ponteiro de interface seja válido.</span><span class="sxs-lookup"><span data-stu-id="f978d-126">DO will call your callbacks as long as the interface pointer is valid.</span></span> <span data-ttu-id="f978d-127">A interface de notificação não é mais válida quando o aplicativo é encerrado; Não mantém a interface de notificação.</span><span class="sxs-lookup"><span data-stu-id="f978d-127">The notification interface is no longer valid when your application terminates; DO does not persist the notify interface.</span></span> <span data-ttu-id="f978d-128">Como resultado, o processo de inicialização do aplicativo deve chamar o método [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) nesses trabalhos existentes para os quais você deseja receber a notificação.</span><span class="sxs-lookup"><span data-stu-id="f978d-128">As a result, your application's initialization process should call the [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method on those existing jobs for which you want to receive notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="f978d-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f978d-129">Requirements</span></span>



| <span data-ttu-id="f978d-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f978d-130">Requirement</span></span> | <span data-ttu-id="f978d-131">Valor</span><span class="sxs-lookup"><span data-stu-id="f978d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f978d-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f978d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f978d-133">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="f978d-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f978d-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f978d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f978d-135">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="f978d-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f978d-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f978d-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f978d-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="f978d-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="f978d-138">INSERI</span><span class="sxs-lookup"><span data-stu-id="f978d-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f978d-139"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f978d-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="f978d-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f978d-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="f978d-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f978d-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="f978d-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f978d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f978d-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f978d-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="f978d-144">IID</span><span class="sxs-lookup"><span data-stu-id="f978d-144">IID</span></span><br/>                      | <span data-ttu-id="f978d-145">IID_IBackgroundCopyCallback é definido como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="f978d-145">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="f978d-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="f978d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f978d-147">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="f978d-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="f978d-148">**Método ibackgroundcopyjob:: SetNotifyFlags**</span><span class="sxs-lookup"><span data-stu-id="f978d-148">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="f978d-149">**Método ibackgroundcopyjob:: SetNotifyInterface**</span><span class="sxs-lookup"><span data-stu-id="f978d-149">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

