---
title: Enumeração de BG_JOB_STATE (Deliveryoptimization. h)
description: A enumeração BG_JOB_STATE define valores constantes para os diferentes Estados de um trabalho.
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- Enumeração de BG_JOB_STATE
- Enumeração de BG_JOB_STATE
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105764259"
---
# <a name="bg_job_state-enumeration"></a><span data-ttu-id="520ad-105">Enumeração de BG_JOB_STATE</span><span class="sxs-lookup"><span data-stu-id="520ad-105">BG_JOB_STATE enumeration</span></span>

<span data-ttu-id="520ad-106">A enumeração **BG_JOB_STATE** define valores constantes para os diferentes Estados de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="520ad-106">The **BG_JOB_STATE** enumeration defines constant values for the different states of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="520ad-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="520ad-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a><span data-ttu-id="520ad-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="520ad-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="520ad-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span><span class="sxs-lookup"><span data-stu-id="520ad-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span></span>
</dt> <dd>

<span data-ttu-id="520ad-110">Especifica que o trabalho está na fila e aguardando para ser executado.</span><span class="sxs-lookup"><span data-stu-id="520ad-110">Specifies that the job is in the queue and waiting to run.</span></span> <span data-ttu-id="520ad-111">Se um usuário fizer logoff enquanto seu trabalho estiver transferindo, o trabalho fará a transição para o estado enfileirado.</span><span class="sxs-lookup"><span data-stu-id="520ad-111">If a user logs off while their job is transferring, the job transitions to the queued state.</span></span>

</dd> <dt>

<span data-ttu-id="520ad-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span><span class="sxs-lookup"><span data-stu-id="520ad-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="520ad-113">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="520ad-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="520ad-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span><span class="sxs-lookup"><span data-stu-id="520ad-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span></span>
</dt> <dd>

<span data-ttu-id="520ad-115">Especifica que o faz a transferência de dados para o trabalho.</span><span class="sxs-lookup"><span data-stu-id="520ad-115">Specifies that DO is transferring data for the job.</span></span>

</dd> <dt>

<span data-ttu-id="520ad-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="520ad-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span></span>
</dt> <dd>

<span data-ttu-id="520ad-117">Especifica que o trabalho está suspenso (em pausa).</span><span class="sxs-lookup"><span data-stu-id="520ad-117">Specifies that the job is suspended (paused).</span></span> <span data-ttu-id="520ad-118">Para suspender um trabalho, chame o método [**método ibackgroundcopyjob:: Suspend**](ibackgroundcopyjob-suspend.md) .</span><span class="sxs-lookup"><span data-stu-id="520ad-118">To suspend a job, call the [**IBackgroundCopyJob::Suspend**](ibackgroundcopyjob-suspend.md) method.</span></span> <span data-ttu-id="520ad-119">O trabalho permanece suspenso até que você chame o método [**método ibackgroundcopyjob:: resume**](ibackgroundcopyjob-resume.md), [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md)ou [**método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .</span><span class="sxs-lookup"><span data-stu-id="520ad-119">The job remains suspended until you call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md), [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md), or [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="520ad-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span><span class="sxs-lookup"><span data-stu-id="520ad-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="520ad-121">Especifica que ocorreu um erro não recuperável (o serviço não pode transferir o arquivo).</span><span class="sxs-lookup"><span data-stu-id="520ad-121">Specifies that a nonrecoverable error occurred (the service is unable to transfer the file).</span></span> <span data-ttu-id="520ad-122">Se o erro, como um erro de acesso negado, puder ser corrigido, chame o método [**método ibackgroundcopyjob:: resume**](ibackgroundcopyjob-resume.md) depois que o erro for corrigido.</span><span class="sxs-lookup"><span data-stu-id="520ad-122">If the error, such as an access-denied error, can be corrected, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method after the error is fixed.</span></span> <span data-ttu-id="520ad-123">No entanto, se o erro não puder ser corrigido, chame o método [**método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) para cancelar o trabalho ou chame o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) para aceitar a parte de um trabalho de download que foi transferido com êxito.</span><span class="sxs-lookup"><span data-stu-id="520ad-123">However, if the error cannot be corrected, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job, or call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to accept the portion of a download job that transferred successfully.</span></span>

</dd> <dt>

<span data-ttu-id="520ad-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span><span class="sxs-lookup"><span data-stu-id="520ad-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="520ad-125">Especifica que ocorreu um erro recuperável.</span><span class="sxs-lookup"><span data-stu-id="520ad-125">Specifies that a recoverable error occurred.</span></span> <span data-ttu-id="520ad-126">O tentará novamente trabalhos no estado de erro transitório com base na configuração de repetição interna.</span><span class="sxs-lookup"><span data-stu-id="520ad-126">DO will retry jobs in the transient error state based on the internal retry configuration.</span></span> <span data-ttu-id="520ad-127">O estado do trabalho será alterado para **BG_JOB_STATE_ERROR** se o trabalho não conseguir fazer o andamento (consulte [**método ibackgroundcopyjob:: SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).</span><span class="sxs-lookup"><span data-stu-id="520ad-127">The state of the job changes to **BG_JOB_STATE_ERROR** if the job fails to make progress (see [**IBackgroundCopyJob::SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).</span></span>

</dd> <dt>

<span data-ttu-id="520ad-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span><span class="sxs-lookup"><span data-stu-id="520ad-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span></span>
</dt> <dd>

<span data-ttu-id="520ad-129">Especifica que o trabalho foi processado com êxito.</span><span class="sxs-lookup"><span data-stu-id="520ad-129">Specifies that your job was successfully processed.</span></span> <span data-ttu-id="520ad-130">Você deve chamar o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) para confirmar a conclusão do trabalho e tornar os arquivos disponíveis para o cliente.</span><span class="sxs-lookup"><span data-stu-id="520ad-130">You must call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge completion of the job and to make the files available to the client.</span></span>

</dd> <dt>

<span data-ttu-id="520ad-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span><span class="sxs-lookup"><span data-stu-id="520ad-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span></span>
</dt> <dd>

<span data-ttu-id="520ad-132">Especifica que você chamou o método [**método ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) para confirmar que seu trabalho foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="520ad-132">Specifies that you called the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that your job completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="520ad-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="520ad-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="520ad-134">Especifica que você chamou o método [**método ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) para cancelar o trabalho (remova o trabalho da fila de transferência).</span><span class="sxs-lookup"><span data-stu-id="520ad-134">Specifies that you called the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job (remove the job from the transfer queue).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="520ad-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="520ad-135">Requirements</span></span>



| <span data-ttu-id="520ad-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="520ad-136">Requirement</span></span> | <span data-ttu-id="520ad-137">Valor</span><span class="sxs-lookup"><span data-stu-id="520ad-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="520ad-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="520ad-138">Minimum supported client</span></span><br/> | <span data-ttu-id="520ad-139">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="520ad-139">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="520ad-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="520ad-140">Minimum supported server</span></span><br/> | <span data-ttu-id="520ad-141">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="520ad-141">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="520ad-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="520ad-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="520ad-143"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="520ad-143"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="520ad-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="520ad-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="520ad-145">**Método ibackgroundcopyjob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="520ad-145">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





