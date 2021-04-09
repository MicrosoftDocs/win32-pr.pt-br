---
title: Método Complete método ibackgroundcopyjob (Deliveryoptimization. h)
description: Encerra o trabalho e salva os arquivos transferidos no cliente.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Método Complete
- Método Complete, interface método ibackgroundcopyjob
- Interface método ibackgroundcopyjob, método Complete
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72383bb235d31043f781998324891b6df134e6ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085548"
---
# <a name="ibackgroundcopyjobcomplete-method"></a><span data-ttu-id="c3c7e-106">Método método ibackgroundcopyjob:: Complete</span><span class="sxs-lookup"><span data-stu-id="c3c7e-106">IBackgroundCopyJob::Complete method</span></span>

<span data-ttu-id="c3c7e-107">Encerra o trabalho e salva os arquivos transferidos no cliente.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-107">Ends the job and saves the transferred files on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3c7e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3c7e-108">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="c3c7e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3c7e-109">Parameters</span></span>

<span data-ttu-id="c3c7e-110">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3c7e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3c7e-111">Return value</span></span>

<span data-ttu-id="c3c7e-112">Esse método retorna os valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-112">This method returns the following **HRESULT** values.</span></span> <span data-ttu-id="c3c7e-113">O método também pode retornar erros relacionados à renomeação das cópias temporárias dos arquivos transferidos para seus nomes especificados.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-113">The method can also return errors related to renaming the temporary copies of the transferred files to their given names.</span></span>



| <span data-ttu-id="c3c7e-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c3c7e-114">Return code</span></span>                                                                                          | <span data-ttu-id="c3c7e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3c7e-115">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c3c7e-116"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="c3c7e-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="c3c7e-117">Todos os arquivos foram transferidos com êxito.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-117">All files transferred successfully.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="c3c7e-118"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="c3c7e-118"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="c3c7e-119">Para downloads, o estado do trabalho não pode ser BG_JOB_STATE_CANCELLED ou BG_JOB_STATE_ACKNOWLEDGED.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-119">For downloads, the state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span> <br/> <span data-ttu-id="c3c7e-120">Para carregamentos, o estado do trabalho deve ser BG_JOB_STATE_TRANSFERRED.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-120">For uploads, the state of the job must be BG_JOB_STATE_TRANSFERRED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c3c7e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3c7e-121">Remarks</span></span>

<span data-ttu-id="c3c7e-122">Todos os arquivos foram transferidos com êxito se o estado do trabalho for **BG_JOB_STATE_TRANSFERRED**.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-122">All of the files have been successfully transferred if the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span> <span data-ttu-id="c3c7e-123">Para verificar o estado do trabalho, chame o método [**método ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md) .</span><span class="sxs-lookup"><span data-stu-id="c3c7e-123">To check the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="c3c7e-124">Você também pode implementar a interface [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) para receber notificações quando todos os arquivos tiverem sido transferidos para o cliente.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-124">You can also implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to receive notification when all of the files have been transferred to the client.</span></span>

<span data-ttu-id="c3c7e-125">O retém trabalhos com menos de 30 dias.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-125">DO retains jobs that are less than 30 days only.</span></span> <span data-ttu-id="c3c7e-126">Todos os trabalhos mais antigos serão removidos.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-126">All older jobs will be removed.</span></span> <span data-ttu-id="c3c7e-127">O não oferece suporte ao Política de Grupo [JobInactivityTimeout](https://www.bing.com/search?q=JobInactivityTimeout) .</span><span class="sxs-lookup"><span data-stu-id="c3c7e-127">DO does not support the [JobInactivityTimeout](https://www.bing.com/search?q=JobInactivityTimeout) Group Policy.</span></span>

<span data-ttu-id="c3c7e-128">Para baixar trabalhos, você pode chamar o método **Complete** a qualquer momento durante o processo de transferência; no entanto, somente os arquivos que foram transferidos com êxito para o cliente antes de chamar esse método são salvos.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-128">For download jobs, you can call the **Complete** method at anytime during the transfer process; however, only files that were successfully transferred to the client before calling this method are saved.</span></span> <span data-ttu-id="c3c7e-129">Por exemplo, se você chamar o método **Complete** enquanto o estiver processando o terceiro dos cinco arquivos, somente os dois primeiros arquivos serão salvos.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-129">For example, if you call the **Complete** method while DO is processing the third of five files, only the first two files are saved.</span></span> <span data-ttu-id="c3c7e-130">Para determinar quais arquivos foram transferidos, chame o método [**IBackgroundCopyFile:: GetProgress**](ibackgroundcopyfile-getprogress-method.md) e compare o membro **bytesTransferred** com o membro **bytesTotal** da estrutura [**BG_FILE_PROGRESS**](bg-file-progress.md) .</span><span class="sxs-lookup"><span data-stu-id="c3c7e-130">To determine which files have been transferred, call the [**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md) method and compare the **BytesTransferred** member to the **BytesTotal** member of the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

<span data-ttu-id="c3c7e-131">Para trabalhos de carregamento, você pode chamar o método **Complete** somente quando o estado do trabalho for **BG_JOB_STATE_TRANSFERRED**.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-131">For upload jobs, you can call the **Complete** method only when the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span>

<span data-ttu-id="c3c7e-132">O proprietário do arquivo é o usuário que fez a chamada.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-132">The owner of the file is the user who made the call.</span></span> <span data-ttu-id="c3c7e-133">Por exemplo, se um administrador concluir o trabalho de outra pessoa, o administrador não o proprietário do trabalho possui o arquivo.</span><span class="sxs-lookup"><span data-stu-id="c3c7e-133">For example, if an administrator completes someone else's job, the administrator not the owner of the job owns the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3c7e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3c7e-134">Requirements</span></span>



| <span data-ttu-id="c3c7e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3c7e-135">Requirement</span></span> | <span data-ttu-id="c3c7e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="c3c7e-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3c7e-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3c7e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c3c7e-138">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="c3c7e-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c3c7e-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c3c7e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c3c7e-140">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="c3c7e-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c3c7e-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3c7e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3c7e-142"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3c7e-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c3c7e-143">INSERI</span><span class="sxs-lookup"><span data-stu-id="c3c7e-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c3c7e-144"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c3c7e-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c3c7e-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3c7e-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="c3c7e-146"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3c7e-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c3c7e-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c3c7e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3c7e-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3c7e-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c3c7e-149">IID</span><span class="sxs-lookup"><span data-stu-id="c3c7e-149">IID</span></span><br/>                      | <span data-ttu-id="c3c7e-150">IID_IBackgroundCopyJob é definido como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="c3c7e-150">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="c3c7e-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3c7e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3c7e-152">**Método ibackgroundcopyjob**</span><span class="sxs-lookup"><span data-stu-id="c3c7e-152">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="c3c7e-153">**Método ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="c3c7e-153">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="c3c7e-154">**Método ibackgroundcopyjob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="c3c7e-154">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





