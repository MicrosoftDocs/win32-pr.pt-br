---
title: Método IBackgroundCopyCallback JobError (Deliveryoptimization. h)
description: A otimização de entrega (DO) chama a implementação do método JobError quando o estado do trabalho é alterado para BG_JOB_STATE_ERROR.
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- Método JobError
- Método JobError, interface IBackgroundCopyCallback
- Interface IBackgroundCopyCallback, método JobError
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0122f5777303506be5fd81d0966b00f828bf2073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369545"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a><span data-ttu-id="be5d2-106">Método IBackgroundCopyCallback:: JobError</span><span class="sxs-lookup"><span data-stu-id="be5d2-106">IBackgroundCopyCallback::JobError method</span></span>

<span data-ttu-id="be5d2-107">A otimização de entrega (DO) chama a implementação do método [**JobError**](https://www.bing.com/search?q=**JobError**) quando o estado do trabalho é alterado para BG_JOB_STATE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="be5d2-107">Delivery Optimization (DO) calls your implementation of the [**JobError**](https://www.bing.com/search?q=**JobError**) method when the state of the job changes to BG_JOB_STATE_ERROR.</span></span>

## <a name="syntax"></a><span data-ttu-id="be5d2-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="be5d2-108">Syntax</span></span>


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a><span data-ttu-id="be5d2-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be5d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be5d2-110">*pJob* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be5d2-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be5d2-111">Contém informações relacionadas ao trabalho, como o número de bytes e arquivos transferidos antes de o erro ter ocorrido.</span><span class="sxs-lookup"><span data-stu-id="be5d2-111">Contains job-related information, such as the number of bytes and files transferred before the error occurred.</span></span> <span data-ttu-id="be5d2-112">Ele também contém os métodos para retomar e cancelar o trabalho.</span><span class="sxs-lookup"><span data-stu-id="be5d2-112">It also contains the methods to resume and cancel the job.</span></span> <span data-ttu-id="be5d2-113">Não liberar *pJob*; Libera a interface quando o método [**JobError**](https://www.bing.com/search?q=**JobError**) retorna.</span><span class="sxs-lookup"><span data-stu-id="be5d2-113">Do not release *pJob*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="be5d2-114">*perror* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="be5d2-114">*pError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be5d2-115">Contém informações de erro, como o arquivo que está sendo processado no momento em que ocorreu o erro fatal e uma descrição do erro.</span><span class="sxs-lookup"><span data-stu-id="be5d2-115">Contains error information, such as the file being processed at the time the fatal error occurred and a description of the error.</span></span> <span data-ttu-id="be5d2-116">Não liberar *perror*; Libera a interface quando o método [**JobError**](https://www.bing.com/search?q=**JobError**) retorna.</span><span class="sxs-lookup"><span data-stu-id="be5d2-116">Do not release *pError*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be5d2-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be5d2-117">Return value</span></span>

<span data-ttu-id="be5d2-118">Este método deve retornar **S_OK**; caso contrário, o continuará a chamar esse método até que **S_OK** seja retornado.</span><span class="sxs-lookup"><span data-stu-id="be5d2-118">This method should return **S_OK**; otherwise, DO continues to call this method until **S_OK** is returned.</span></span> <span data-ttu-id="be5d2-119">Por motivos de desempenho, você deve limitar o número de vezes que retorna um valor diferente de **S_OK** a algumas vezes.</span><span class="sxs-lookup"><span data-stu-id="be5d2-119">For performance reasons, you should limit the number of times you return a value other than **S_OK** to a few times.</span></span> <span data-ttu-id="be5d2-120">Como alternativa para retornar um código de erro, considere sempre retornar **S_OK** e manipular o erro internamente.</span><span class="sxs-lookup"><span data-stu-id="be5d2-120">As an alternative to returning an error code, consider always returning **S_OK** and handling the error internally.</span></span> <span data-ttu-id="be5d2-121">O intervalo no qual esse método é chamado é arbitrário.</span><span class="sxs-lookup"><span data-stu-id="be5d2-121">The interval at which this method is called is arbitrary.</span></span>

## <a name="remarks"></a><span data-ttu-id="be5d2-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="be5d2-122">Remarks</span></span>

<span data-ttu-id="be5d2-123">Depois de determinar a causa do erro, execute uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="be5d2-123">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="be5d2-124">Para cancelar o trabalho, chame o método [**método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="be5d2-124">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="be5d2-125">Para aceitar a parte do trabalho que foi transferida com êxito antes da ocorrência do erro, chame o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="be5d2-125">To accept the portion of the job that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="be5d2-126">Esta opção não se aplica aos trabalhos de carregamento; Não é possível concluir uma parte de um trabalho de carregamento.</span><span class="sxs-lookup"><span data-stu-id="be5d2-126">This option does not apply to upload jobs; you cannot complete a portion of an upload job.</span></span>
-   <span data-ttu-id="be5d2-127">Para concluir o processamento do trabalho, corrija o problema e, em seguida, chame o método [**método ibackgroundcopyjob:: resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="be5d2-127">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

<span data-ttu-id="be5d2-128">Os erros transitórios não geram chamadas para o método [**JobError**](https://www.bing.com/search?q=**JobError**) .</span><span class="sxs-lookup"><span data-stu-id="be5d2-128">Transient errors do not generate calls to the [**JobError**](https://www.bing.com/search?q=**JobError**) method.</span></span>

<span data-ttu-id="be5d2-129">O retorna BG_ERROR_CONTEXT_REMOTE_FILE se o trabalho atingir um erro HTTP 403, BG_ERROR_CONTEXT_NONE caso contrário.</span><span class="sxs-lookup"><span data-stu-id="be5d2-129">DO returns BG_ERROR_CONTEXT_REMOTE_FILE if the job hit a HTTP 403 error, BG_ERROR_CONTEXT_NONE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="be5d2-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be5d2-130">Requirements</span></span>



| <span data-ttu-id="be5d2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="be5d2-131">Requirement</span></span> | <span data-ttu-id="be5d2-132">Valor</span><span class="sxs-lookup"><span data-stu-id="be5d2-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be5d2-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be5d2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="be5d2-134">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="be5d2-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="be5d2-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be5d2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="be5d2-136">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="be5d2-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="be5d2-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be5d2-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="be5d2-138"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="be5d2-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="be5d2-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="be5d2-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be5d2-140"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be5d2-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="be5d2-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="be5d2-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="be5d2-142"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="be5d2-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="be5d2-143">DLL</span><span class="sxs-lookup"><span data-stu-id="be5d2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be5d2-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be5d2-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="be5d2-145">IID</span><span class="sxs-lookup"><span data-stu-id="be5d2-145">IID</span></span><br/>                      | <span data-ttu-id="be5d2-146">IID_IBackgroundCopyCallback é definido como 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span><span class="sxs-lookup"><span data-stu-id="be5d2-146">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="be5d2-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="be5d2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be5d2-148">**IBackgroundCopyCallback**</span><span class="sxs-lookup"><span data-stu-id="be5d2-148">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="be5d2-149">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="be5d2-149">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="be5d2-150">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="be5d2-150">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="be5d2-151">**Método ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="be5d2-151">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="be5d2-152">**Método ibackgroundcopyjob:: retomar**</span><span class="sxs-lookup"><span data-stu-id="be5d2-152">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





