---
title: Método GetError método ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera a interface de erro após ocorrer um erro.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- Método GetError
- Método GetError, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f2da994da83a786b89adb5ae63104dbaa6e2ef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369616"
---
# <a name="ibackgroundcopyjobgeterror-method"></a><span data-ttu-id="c4b69-106">Método método ibackgroundcopyjob:: GetError</span><span class="sxs-lookup"><span data-stu-id="c4b69-106">IBackgroundCopyJob::GetError method</span></span>

<span data-ttu-id="c4b69-107">Recupera a interface de erro após ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="c4b69-107">Retrieves the error interface after an error occurs.</span></span>

<span data-ttu-id="c4b69-108">A otimização de entrega (DO) gera um objeto de erro quando o estado do trabalho é BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="c4b69-108">Delivery Optimization (DO) generates an error object when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="c4b69-109">O serviço não cria um objeto de erro quando uma chamada para um método de interface **IBackgroundCopyXXXX** falha.</span><span class="sxs-lookup"><span data-stu-id="c4b69-109">The service does not create an error object when a call to an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="c4b69-110">O objeto de erro está disponível até que o comece a transferir dados (o estado do trabalho é alterado para BG_JOB_STATE_TRANSFERRING) para o trabalho ou até que o aplicativo saia.</span><span class="sxs-lookup"><span data-stu-id="c4b69-110">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job or until your application exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4b69-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4b69-111">Syntax</span></span>


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a><span data-ttu-id="c4b69-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4b69-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4b69-113">*ppError* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c4b69-113">*ppError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4b69-114">Interface de erro que fornece o código de erro, uma descrição do erro e o contexto no qual ocorreu o erro.</span><span class="sxs-lookup"><span data-stu-id="c4b69-114">Error interface that provides the error code, a description of the error, and the context in which the error occurred.</span></span> <span data-ttu-id="c4b69-115">Esse parâmetro também identifica o arquivo que está sendo transferido no momento em que o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="c4b69-115">This parameter also identifies the file being transferred at the time the error occurred.</span></span> <span data-ttu-id="c4b69-116">Libere *ppError* quando terminar.</span><span class="sxs-lookup"><span data-stu-id="c4b69-116">Release *ppError* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4b69-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4b69-117">Return value</span></span>

<span data-ttu-id="c4b69-118">Esse método retorna os valores **HRESULT** a seguir, bem como outros.</span><span class="sxs-lookup"><span data-stu-id="c4b69-118">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="c4b69-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c4b69-119">Return code</span></span>                                                                                                           | <span data-ttu-id="c4b69-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4b69-120">Description</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c4b69-121"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="c4b69-121"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                              | <span data-ttu-id="c4b69-122">Objeto de erro gerado com êxito.</span><span class="sxs-lookup"><span data-stu-id="c4b69-122">Successfully generated the error object.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="c4b69-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="c4b69-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="c4b69-124">A interface de erro está disponível somente após ocorrer um erro (BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR) e antes de começar a transferir dados (BG_JOB_STATE_TRANSFERRING).</span><span class="sxs-lookup"><span data-stu-id="c4b69-124">The error interface is available only after an error occurs (BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR) and before DO begins transferring data (BG_JOB_STATE_TRANSFERRING).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c4b69-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4b69-125">Remarks</span></span>

<span data-ttu-id="c4b69-126">O trabalho é colocado em um estado de erro em erros fatais.</span><span class="sxs-lookup"><span data-stu-id="c4b69-126">The job is placed in an error state on fatal errors.</span></span> <span data-ttu-id="c4b69-127">Use uma das opções a seguir para determinar se o trabalho está em erro:</span><span class="sxs-lookup"><span data-stu-id="c4b69-127">Use one of the following options to determine if the job is in error:</span></span>

-   <span data-ttu-id="c4b69-128">Para sondar o estado do trabalho, chame o método [**método ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="c4b69-128">To poll for the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="c4b69-129">O trabalho estará em erro se o estado for BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="c4b69-129">The job is in error if the state is BG_JOB_STATE_ERROR.</span></span>
-   <span data-ttu-id="c4b69-130">Para receber uma notificação quando ocorrer um erro, implemente a interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (especificamente, o método [**JobError**](https://www.bing.com/search?q=**JobError**) ).</span><span class="sxs-lookup"><span data-stu-id="c4b69-130">To receive notification when an error occurs, implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface (specifically, the [**JobError**](https://www.bing.com/search?q=**JobError**) method).</span></span> <span data-ttu-id="c4b69-131">Em seguida, chame o método [**método ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) para registrar o retorno de chamada e o método [**método ibackgroundcopyjob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) para definir o sinalizador de BG_NOTIFY_JOB_ERROR.</span><span class="sxs-lookup"><span data-stu-id="c4b69-131">Then, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to register the callback and the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to set the BG_NOTIFY_JOB_ERROR flag.</span></span>

<span data-ttu-id="c4b69-132">A interface [**IBackgroundCopyError**](ibackgroundcopyerror.md) contém informações que você usa para determinar a causa do erro e se o processo de transferência pode continuar.</span><span class="sxs-lookup"><span data-stu-id="c4b69-132">The [**IBackgroundCopyError**](ibackgroundcopyerror.md) interface contains information that you use to determine the cause of the error and if the transfer process can proceed.</span></span> <span data-ttu-id="c4b69-133">Depois de determinar a causa do erro, execute uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="c4b69-133">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="c4b69-134">Para cancelar o trabalho, chame o método [**método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="c4b69-134">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="c4b69-135">Para salvar os arquivos transferidos com êxito antes da ocorrência do erro, chame o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="c4b69-135">To save those files that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span>
-   <span data-ttu-id="c4b69-136">Para concluir o processamento do trabalho, corrija o problema e, em seguida, chame o método [**método ibackgroundcopyjob:: resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="c4b69-136">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4b69-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4b69-137">Requirements</span></span>



| <span data-ttu-id="c4b69-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4b69-138">Requirement</span></span> | <span data-ttu-id="c4b69-139">Valor</span><span class="sxs-lookup"><span data-stu-id="c4b69-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4b69-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4b69-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c4b69-141">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="c4b69-141">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c4b69-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4b69-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c4b69-143">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="c4b69-143">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c4b69-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4b69-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4b69-145"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4b69-145"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4b69-146">INSERI</span><span class="sxs-lookup"><span data-stu-id="c4b69-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4b69-147"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4b69-147"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c4b69-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4b69-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4b69-149"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4b69-149"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c4b69-150">DLL</span><span class="sxs-lookup"><span data-stu-id="c4b69-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4b69-151"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4b69-151"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c4b69-152">IID</span><span class="sxs-lookup"><span data-stu-id="c4b69-152">IID</span></span><br/>                      | <span data-ttu-id="c4b69-153">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="c4b69-153">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="c4b69-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4b69-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4b69-155">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="c4b69-155">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="c4b69-156">**IBackgroundCopyCallback::JobError**</span><span class="sxs-lookup"><span data-stu-id="c4b69-156">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[<span data-ttu-id="c4b69-157">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="c4b69-157">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="c4b69-158">**Método ibackgroundcopyjob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="c4b69-158">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





