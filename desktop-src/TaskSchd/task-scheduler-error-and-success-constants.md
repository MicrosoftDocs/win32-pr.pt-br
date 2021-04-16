---
title: Agendador de Tarefas constantes de erro e êxito (WinError. h)
description: Se ocorrer um erro, as APIs de Agendador de Tarefas poderão retornar um dos códigos de erro a seguir como um valor HRESULT.
ms.assetid: 54278bbd-7dca-438e-a771-5fcb08c4aa68
keywords:
- Agendador de Tarefas Agendador de Tarefas, referência, erro e constantes de sucesso
topic_type:
- apiref
api_name:
- SCHED_S_TASK_READY
- SCHED_S_TASK_RUNNING
- SCHED_S_TASK_DISABLED
- SCHED_S_TASK_HAS_NOT_RUN
- SCHED_S_TASK_NO_MORE_RUNS
- SCHED_S_TASK_NOT_SCHEDULED
- SCHED_S_TASK_TERMINATED
- SCHED_S_TASK_NO_VALID_TRIGGERS
- SCHED_S_EVENT_TRIGGER
- SCHED_E_TRIGGER_NOT_FOUND
- SCHED_E_TASK_NOT_READY
- SCHED_E_TASK_NOT_RUNNING
- SCHED_E_SERVICE_NOT_INSTALLED
- SCHED_E_CANNOT_OPEN_TASK
- SCHED_E_INVALID_TASK
- SCHED_E_ACCOUNT_INFORMATION_NOT_SET
- SCHED_E_ACCOUNT_NAME_NOT_FOUND
- SCHED_E_ACCOUNT_DBASE_CORRUPT
- SCHED_E_NO_SECURITY_SERVICES
- SCHED_E_UNKNOWN_OBJECT_VERSION
- SCHED_E_UNSUPPORTED_ACCOUNT_OPTION
- SCHED_E_SERVICE_NOT_RUNNING
- SCHED_E_UNEXPECTEDNODE
- SCHED_E_NAMESPACE
- SCHED_E_INVALIDVALUE
- SCHED_E_MISSINGNODE
- SCHED_E_MALFORMEDXML
- SCHED_S_SOME_TRIGGERS_FAILED
- SCHED_S_BATCH_LOGON_PROBLEM
- SCHED_E_TOO_MANY_NODES
- SCHED_E_PAST_END_BOUNDARY
- SCHED_E_ALREADY_RUNNING
- SCHED_E_USER_NOT_LOGGED_ON
- SCHED_E_INVALID_TASK_HASH
- SCHED_E_SERVICE_NOT_AVAILABLE
- SCHED_E_SERVICE_TOO_BUSY
- SCHED_E_TASK_ATTEMPTED
- SCHED_S_TASK_QUEUED
- SCHED_E_TASK_DISABLED
- SCHED_E_TASK_NOT_V1_COMPAT
- SCHED_E_START_ON_DEMAND
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: a1d0347938020ca8937f2764e3b2c62a38fc9273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757608"
---
# <a name="task-scheduler-error-and-success-constants"></a><span data-ttu-id="0de27-104">Agendador de Tarefas constantes de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="0de27-104">Task Scheduler Error and Success Constants</span></span>

<span data-ttu-id="0de27-105">Se ocorrer um erro, as APIs de Agendador de Tarefas poderão retornar um dos códigos de erro a seguir como um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0de27-105">If an error occurs, the Task Scheduler APIs can return one of the following error codes as an **HRESULT** value.</span></span>

<span data-ttu-id="0de27-106">As constantes que começam com os \_ S sched \_ são constantes de sucesso e as constantes que começam com sched \_ E \_ são constantes de erro.</span><span class="sxs-lookup"><span data-stu-id="0de27-106">The constants that begin with SCHED\_S\_ are success constants, and the constants that begin with SCHED\_E\_ are error constants.</span></span>

```cpp
  HRESULT phrStatus;
  hr = pITask->GetStatus(&phrStatus);
  
  // Release the ITask interface.
  pITask->Release();
    
  switch(phrStatus)
  {
  case SCHED_S_TASK_READY:
       wprintf(L"  SCHED_S_TASK_READY\n");
       break;
  case SCHED_S_TASK_RUNNING:
       wprintf(L"  SCHED_S_TASK_RUNNING\n");
       break;

  //...
  }
```

<span data-ttu-id="0de27-107">Exemplo do [exemplo de código C/C++: Recuperando o status da tarefa](c-c-code-example-retrieving-task-status.md).</span><span class="sxs-lookup"><span data-stu-id="0de27-107">Example from [C/C++ Code Example: Retrieving Task Status](c-c-code-example-retrieving-task-status.md).</span></span>

> [!Note]  
> <span data-ttu-id="0de27-108">Algumas APIs Agendador de Tarefas podem retornar códigos de erro do sistema e da rede (64, por exemplo).</span><span class="sxs-lookup"><span data-stu-id="0de27-108">Some Task Scheduler APIs can return system and network error codes (64 for example).</span></span> <span data-ttu-id="0de27-109">Você pode verificar a definição desses tipos de códigos de erro usando o comando **net helpmsg** na janela do prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="0de27-109">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="0de27-110">Por exemplo, o comando **net helpmsg 64** retorna a mensagem: o nome de rede especificado não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="0de27-110">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="0de27-111">Para obter mais informações sobre eventos e mensagens de erro, consulte [central de mensagens de eventos e erros](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).</span><span class="sxs-lookup"><span data-stu-id="0de27-111">For more information about events and error messages, see [Events and Errors Message Center](https://www.microsoft.com/technet/support/ee/ee_advanced.aspx).</span></span>

<dl> <dt>

<span data-ttu-id="0de27-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**tarefa do SCHED \_ S \_ \_ pronta**</span><span class="sxs-lookup"><span data-stu-id="0de27-112"><span id="SCHED_S_TASK_READY"></span><span id="sched_s_task_ready"></span>**SCHED\_S\_TASK\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-113">0x00041300</span><span class="sxs-lookup"><span data-stu-id="0de27-113">0x00041300</span></span>
</dt> <dt>



<span data-ttu-id="0de27-114">A tarefa está pronta para ser executada no próximo horário agendado.</span><span class="sxs-lookup"><span data-stu-id="0de27-114">The task is ready to run at its next scheduled time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**tarefa do SCHED \_ S \_ \_ em execução**</span><span class="sxs-lookup"><span data-stu-id="0de27-115"><span id="SCHED_S_TASK_RUNNING"></span><span id="sched_s_task_running"></span>**SCHED\_S\_TASK\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-116">0x00041301</span><span class="sxs-lookup"><span data-stu-id="0de27-116">0x00041301</span></span>
</dt> <dt>



<span data-ttu-id="0de27-117">A tarefa está em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="0de27-117">The task is currently running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**tarefa do SCHED \_ S \_ \_ desabilitada**</span><span class="sxs-lookup"><span data-stu-id="0de27-118"><span id="SCHED_S_TASK_DISABLED"></span><span id="sched_s_task_disabled"></span>**SCHED\_S\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-119">0x00041302</span><span class="sxs-lookup"><span data-stu-id="0de27-119">0x00041302</span></span>
</dt> <dt>



<span data-ttu-id="0de27-120">A tarefa não será executada nos horários agendados porque foi desabilitada.</span><span class="sxs-lookup"><span data-stu-id="0de27-120">The task will not run at the scheduled times because it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**a \_ tarefa do sched S \_ \_ \_ não foi \_ executada**</span><span class="sxs-lookup"><span data-stu-id="0de27-121"><span id="SCHED_S_TASK_HAS_NOT_RUN"></span><span id="sched_s_task_has_not_run"></span>**SCHED\_S\_TASK\_HAS\_NOT\_RUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-122">0x00041303</span><span class="sxs-lookup"><span data-stu-id="0de27-122">0x00041303</span></span>
</dt> <dt>



<span data-ttu-id="0de27-123">A tarefa ainda não foi executada.</span><span class="sxs-lookup"><span data-stu-id="0de27-123">The task has not yet run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**a \_ tarefa sched S \_ \_ não \_ \_ executa mais**</span><span class="sxs-lookup"><span data-stu-id="0de27-124"><span id="SCHED_S_TASK_NO_MORE_RUNS"></span><span id="sched_s_task_no_more_runs"></span>**SCHED\_S\_TASK\_NO\_MORE\_RUNS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-125">0x00041304</span><span class="sxs-lookup"><span data-stu-id="0de27-125">0x00041304</span></span>
</dt> <dt>



<span data-ttu-id="0de27-126">Não há mais execuções agendadas para esta tarefa.</span><span class="sxs-lookup"><span data-stu-id="0de27-126">There are no more runs scheduled for this task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**\_tarefa S \_ sched \_ não \_ agendada**</span><span class="sxs-lookup"><span data-stu-id="0de27-127"><span id="SCHED_S_TASK_NOT_SCHEDULED"></span><span id="sched_s_task_not_scheduled"></span>**SCHED\_S\_TASK\_NOT\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-128">0x00041305</span><span class="sxs-lookup"><span data-stu-id="0de27-128">0x00041305</span></span>
</dt> <dt>



<span data-ttu-id="0de27-129">Uma ou mais das propriedades necessárias para executar essa tarefa em um agendamento não foram definidas.</span><span class="sxs-lookup"><span data-stu-id="0de27-129">One or more of the properties that are needed to run this task on a schedule have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**tarefa de SCHED \_ S \_ \_ encerrada**</span><span class="sxs-lookup"><span data-stu-id="0de27-130"><span id="SCHED_S_TASK_TERMINATED"></span><span id="sched_s_task_terminated"></span>**SCHED\_S\_TASK\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-131">0x00041306</span><span class="sxs-lookup"><span data-stu-id="0de27-131">0x00041306</span></span>
</dt> <dt>



<span data-ttu-id="0de27-132">A última execução da tarefa foi encerrada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="0de27-132">The last run of the task was terminated by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**tarefa do SCHED \_ S \_ \_ nenhum \_ \_ gatilho válido**</span><span class="sxs-lookup"><span data-stu-id="0de27-133"><span id="SCHED_S_TASK_NO_VALID_TRIGGERS"></span><span id="sched_s_task_no_valid_triggers"></span>**SCHED\_S\_TASK\_NO\_VALID\_TRIGGERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-134">0x00041307</span><span class="sxs-lookup"><span data-stu-id="0de27-134">0x00041307</span></span>
</dt> <dt>



<span data-ttu-id="0de27-135">A tarefa não tem gatilhos ou os gatilhos existentes estão desabilitados ou não foram definidos.</span><span class="sxs-lookup"><span data-stu-id="0de27-135">Either the task has no triggers or the existing triggers are disabled or not set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**\_gatilho de \_ evento sched S \_**</span><span class="sxs-lookup"><span data-stu-id="0de27-136"><span id="SCHED_S_EVENT_TRIGGER"></span><span id="sched_s_event_trigger"></span>**SCHED\_S\_EVENT\_TRIGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-137">0x00041308</span><span class="sxs-lookup"><span data-stu-id="0de27-137">0x00041308</span></span>
</dt> <dt>



<span data-ttu-id="0de27-138">Os gatilhos de evento não têm tempos de execução definidos.</span><span class="sxs-lookup"><span data-stu-id="0de27-138">Event triggers do not have set run times.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**\_gatilho sched \_ E \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="0de27-139"><span id="SCHED_E_TRIGGER_NOT_FOUND"></span><span id="sched_e_trigger_not_found"></span>**SCHED\_E\_TRIGGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-140">0x80041309</span><span class="sxs-lookup"><span data-stu-id="0de27-140">0x80041309</span></span>
</dt> <dt>



<span data-ttu-id="0de27-141">O gatilho de uma tarefa não foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="0de27-141">A task's trigger is not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**a \_ tarefa sched E \_ \_ não \_ está pronta**</span><span class="sxs-lookup"><span data-stu-id="0de27-142"><span id="SCHED_E_TASK_NOT_READY"></span><span id="sched_e_task_not_ready"></span>**SCHED\_E\_TASK\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-143">0x8004130A</span><span class="sxs-lookup"><span data-stu-id="0de27-143">0x8004130A</span></span>
</dt> <dt>



<span data-ttu-id="0de27-144">Uma ou mais das propriedades necessárias para executar esta tarefa não foram definidas.</span><span class="sxs-lookup"><span data-stu-id="0de27-144">One or more of the properties required to run this task have not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**\_tarefa sched \_ E \_ não \_ em execução**</span><span class="sxs-lookup"><span data-stu-id="0de27-145"><span id="SCHED_E_TASK_NOT_RUNNING"></span><span id="sched_e_task_not_running"></span>**SCHED\_E\_TASK\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-146">0x8004130B</span><span class="sxs-lookup"><span data-stu-id="0de27-146">0x8004130B</span></span>
</dt> <dt>



<span data-ttu-id="0de27-147">Não há nenhuma instância em execução da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0de27-147">There is no running instance of the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**o \_ serviço sched E \_ \_ não está \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="0de27-148"><span id="SCHED_E_SERVICE_NOT_INSTALLED"></span><span id="sched_e_service_not_installed"></span>**SCHED\_E\_SERVICE\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-149">0x8004130C</span><span class="sxs-lookup"><span data-stu-id="0de27-149">0x8004130C</span></span>
</dt> <dt>



<span data-ttu-id="0de27-150">O serviço de Agendador de Tarefas não está instalado neste computador.</span><span class="sxs-lookup"><span data-stu-id="0de27-150">The Task Scheduler service is not installed on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**SCHED \_ E \_ não é possível \_ abrir a \_ tarefa**</span><span class="sxs-lookup"><span data-stu-id="0de27-151"><span id="SCHED_E_CANNOT_OPEN_TASK"></span><span id="sched_e_cannot_open_task"></span>**SCHED\_E\_CANNOT\_OPEN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-152">0x8004130D</span><span class="sxs-lookup"><span data-stu-id="0de27-152">0x8004130D</span></span>
</dt> <dt>



<span data-ttu-id="0de27-153">Não foi possível abrir o objeto de tarefa.</span><span class="sxs-lookup"><span data-stu-id="0de27-153">The task object could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**\_tarefa sched E \_ inválida \_**</span><span class="sxs-lookup"><span data-stu-id="0de27-154"><span id="SCHED_E_INVALID_TASK"></span><span id="sched_e_invalid_task"></span>**SCHED\_E\_INVALID\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-155">0x8004130E</span><span class="sxs-lookup"><span data-stu-id="0de27-155">0x8004130E</span></span>
</dt> <dt>



<span data-ttu-id="0de27-156">O objeto é um objeto de tarefa inválido ou não é um objeto de tarefa.</span><span class="sxs-lookup"><span data-stu-id="0de27-156">The object is either an invalid task object or is not a task object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**\_informações da conta sched E \_ \_ \_ não \_ definidas**</span><span class="sxs-lookup"><span data-stu-id="0de27-157"><span id="SCHED_E_ACCOUNT_INFORMATION_NOT_SET"></span><span id="sched_e_account_information_not_set"></span>**SCHED\_E\_ACCOUNT\_INFORMATION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-158">0x8004130F</span><span class="sxs-lookup"><span data-stu-id="0de27-158">0x8004130F</span></span>
</dt> <dt>



<span data-ttu-id="0de27-159">Nenhuma informação de conta foi encontrada no banco de dados de segurança Agendador de Tarefas para a tarefa indicada.</span><span class="sxs-lookup"><span data-stu-id="0de27-159">No account information could be found in the Task Scheduler security database for the task indicated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**\_nome da conta sched E \_ \_ \_ não \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="0de27-160"><span id="SCHED_E_ACCOUNT_NAME_NOT_FOUND"></span><span id="sched_e_account_name_not_found"></span>**SCHED\_E\_ACCOUNT\_NAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-161">0x80041310</span><span class="sxs-lookup"><span data-stu-id="0de27-161">0x80041310</span></span>
</dt> <dt>



<span data-ttu-id="0de27-162">Não é possível estabelecer a existência da conta especificada.</span><span class="sxs-lookup"><span data-stu-id="0de27-162">Unable to establish existence of the account specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**\_dBASE E \_ conta do sched \_ \_ corrompida**</span><span class="sxs-lookup"><span data-stu-id="0de27-163"><span id="SCHED_E_ACCOUNT_DBASE_CORRUPT"></span><span id="sched_e_account_dbase_corrupt"></span>**SCHED\_E\_ACCOUNT\_DBASE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-164">0x80041311</span><span class="sxs-lookup"><span data-stu-id="0de27-164">0x80041311</span></span>
</dt> <dt>



<span data-ttu-id="0de27-165">Foi detectado um dano no banco de dados de segurança do Agendador de Tarefas; o banco de dados foi redefinido.</span><span class="sxs-lookup"><span data-stu-id="0de27-165">Corruption was detected in the Task Scheduler security database; the database has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED \_ E \_ nenhum \_ serviço de segurança \_**</span><span class="sxs-lookup"><span data-stu-id="0de27-166"><span id="SCHED_E_NO_SECURITY_SERVICES"></span><span id="sched_e_no_security_services"></span>**SCHED\_E\_NO\_SECURITY\_SERVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-167">0x80041312</span><span class="sxs-lookup"><span data-stu-id="0de27-167">0x80041312</span></span>
</dt> <dt>



<span data-ttu-id="0de27-168">Agendador de Tarefas serviços de segurança estão disponíveis apenas no Windows NT.</span><span class="sxs-lookup"><span data-stu-id="0de27-168">Task Scheduler security services are available only on Windows NT.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**\_versão do objeto sched E \_ desconhecido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0de27-169"><span id="SCHED_E_UNKNOWN_OBJECT_VERSION"></span><span id="sched_e_unknown_object_version"></span>**SCHED\_E\_UNKNOWN\_OBJECT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-170">0x80041313</span><span class="sxs-lookup"><span data-stu-id="0de27-170">0x80041313</span></span>
</dt> <dt>



<span data-ttu-id="0de27-171">A versão do objeto da tarefa não é suportada ou é inválida.</span><span class="sxs-lookup"><span data-stu-id="0de27-171">The task object version is either unsupported or invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**\_opção de conta sched E \_ sem suporte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0de27-172"><span id="SCHED_E_UNSUPPORTED_ACCOUNT_OPTION"></span><span id="sched_e_unsupported_account_option"></span>**SCHED\_E\_UNSUPPORTED\_ACCOUNT\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-173">0x80041314</span><span class="sxs-lookup"><span data-stu-id="0de27-173">0x80041314</span></span>
</dt> <dt>



<span data-ttu-id="0de27-174">A tarefa foi configurada com uma combinação sem suporte de configurações de conta e opções de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="0de27-174">The task has been configured with an unsupported combination of account settings and run time options.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**o \_ serviço sched E \_ \_ não \_ está em execução**</span><span class="sxs-lookup"><span data-stu-id="0de27-175"><span id="SCHED_E_SERVICE_NOT_RUNNING"></span><span id="sched_e_service_not_running"></span>**SCHED\_E\_SERVICE\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-176">0x80041315</span><span class="sxs-lookup"><span data-stu-id="0de27-176">0x80041315</span></span>
</dt> <dt>



<span data-ttu-id="0de27-177">O serviço de Agendador de Tarefas não está em execução.</span><span class="sxs-lookup"><span data-stu-id="0de27-177">The Task Scheduler Service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHED \_ E \_ UNEXPECTEDNODE**</span><span class="sxs-lookup"><span data-stu-id="0de27-178"><span id="SCHED_E_UNEXPECTEDNODE"></span><span id="sched_e_unexpectednode"></span>**SCHED\_E\_UNEXPECTEDNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-179">0x80041316</span><span class="sxs-lookup"><span data-stu-id="0de27-179">0x80041316</span></span>
</dt> <dt>



<span data-ttu-id="0de27-180">O XML da tarefa contém um nó inesperado.</span><span class="sxs-lookup"><span data-stu-id="0de27-180">The task XML contains an unexpected node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**\_namespace sched E \_**</span><span class="sxs-lookup"><span data-stu-id="0de27-181"><span id="SCHED_E_NAMESPACE"></span><span id="sched_e_namespace"></span>**SCHED\_E\_NAMESPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-182">0x80041317</span><span class="sxs-lookup"><span data-stu-id="0de27-182">0x80041317</span></span>
</dt> <dt>



<span data-ttu-id="0de27-183">O XML da tarefa contém um elemento ou atributo de um namespace inesperado.</span><span class="sxs-lookup"><span data-stu-id="0de27-183">The task XML contains an element or attribute from an unexpected namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHED \_ E \_ inválidovalue**</span><span class="sxs-lookup"><span data-stu-id="0de27-184"><span id="SCHED_E_INVALIDVALUE"></span><span id="sched_e_invalidvalue"></span>**SCHED\_E\_INVALIDVALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-185">0x80041318</span><span class="sxs-lookup"><span data-stu-id="0de27-185">0x80041318</span></span>
</dt> <dt>



<span data-ttu-id="0de27-186">O XML da tarefa contém um valor formatado incorretamente ou fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="0de27-186">The task XML contains a value which is incorrectly formatted or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHED \_ E \_ MISSINGNODE**</span><span class="sxs-lookup"><span data-stu-id="0de27-187"><span id="SCHED_E_MISSINGNODE"></span><span id="sched_e_missingnode"></span>**SCHED\_E\_MISSINGNODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-188">0x80041319</span><span class="sxs-lookup"><span data-stu-id="0de27-188">0x80041319</span></span>
</dt> <dt>



<span data-ttu-id="0de27-189">Falta um elemento ou atributo necessário no XML da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0de27-189">The task XML is missing a required element or attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHED \_ E \_ MALFORMEDXML**</span><span class="sxs-lookup"><span data-stu-id="0de27-190"><span id="SCHED_E_MALFORMEDXML"></span><span id="sched_e_malformedxml"></span>**SCHED\_E\_MALFORMEDXML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-191">0x8004131A</span><span class="sxs-lookup"><span data-stu-id="0de27-191">0x8004131A</span></span>
</dt> <dt>



<span data-ttu-id="0de27-192">O XML da tarefa está malformado.</span><span class="sxs-lookup"><span data-stu-id="0de27-192">The task XML is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**\_falha em \_ alguns \_ GATILHOs de sched \_**</span><span class="sxs-lookup"><span data-stu-id="0de27-193"><span id="SCHED_S_SOME_TRIGGERS_FAILED"></span><span id="sched_s_some_triggers_failed"></span>**SCHED\_S\_SOME\_TRIGGERS\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-194">0x0004131B</span><span class="sxs-lookup"><span data-stu-id="0de27-194">0x0004131B</span></span>
</dt> <dt>



<span data-ttu-id="0de27-195">A tarefa está registrada, mas nem todos os gatilhos especificados iniciarão a tarefa.</span><span class="sxs-lookup"><span data-stu-id="0de27-195">The task is registered, but not all specified triggers will start the task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**\_problema de \_ logon em lote do sched S \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0de27-196"><span id="SCHED_S_BATCH_LOGON_PROBLEM"></span><span id="sched_s_batch_logon_problem"></span>**SCHED\_S\_BATCH\_LOGON\_PROBLEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-197">0x0004131C</span><span class="sxs-lookup"><span data-stu-id="0de27-197">0x0004131C</span></span>
</dt> <dt>



<span data-ttu-id="0de27-198">A tarefa está registrada, mas pode falhar ao iniciar.</span><span class="sxs-lookup"><span data-stu-id="0de27-198">The task is registered, but may fail to start.</span></span> <span data-ttu-id="0de27-199">O privilégio de logon em lotes precisa ser habilitado para a entidade de segurança da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0de27-199">Batch logon privilege needs to be enabled for the task principal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHED \_ E \_ \_ muitos \_ nós**</span><span class="sxs-lookup"><span data-stu-id="0de27-200"><span id="SCHED_E_TOO_MANY_NODES"></span><span id="sched_e_too_many_nodes"></span>**SCHED\_E\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-201">0x8004131D</span><span class="sxs-lookup"><span data-stu-id="0de27-201">0x8004131D</span></span>
</dt> <dt>



<span data-ttu-id="0de27-202">O XML da tarefa contém muitos nós do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="0de27-202">The task XML contains too many nodes of the same type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**\_& \_ \_ eslimite de extremidade posterior \_ do sched**</span><span class="sxs-lookup"><span data-stu-id="0de27-203"><span id="SCHED_E_PAST_END_BOUNDARY"></span><span id="sched_e_past_end_boundary"></span>**SCHED\_E\_PAST\_END\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-204">0x8004131E</span><span class="sxs-lookup"><span data-stu-id="0de27-204">0x8004131E</span></span>
</dt> <dt>



<span data-ttu-id="0de27-205">A tarefa não pode ser iniciada após o limite de término do gatilho.</span><span class="sxs-lookup"><span data-stu-id="0de27-205">The task cannot be started after the trigger end boundary.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED \_ E \_ já \_ em execução**</span><span class="sxs-lookup"><span data-stu-id="0de27-206"><span id="SCHED_E_ALREADY_RUNNING"></span><span id="sched_e_already_running"></span>**SCHED\_E\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-207">0x8004131F</span><span class="sxs-lookup"><span data-stu-id="0de27-207">0x8004131F</span></span>
</dt> <dt>



<span data-ttu-id="0de27-208">Uma instância desta tarefa já está em execução.</span><span class="sxs-lookup"><span data-stu-id="0de27-208">An instance of this task is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**o \_ \_ usuário do sched E \_ não \_ fez logon \_**</span><span class="sxs-lookup"><span data-stu-id="0de27-209"><span id="SCHED_E_USER_NOT_LOGGED_ON"></span><span id="sched_e_user_not_logged_on"></span>**SCHED\_E\_USER\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-210">0x80041320</span><span class="sxs-lookup"><span data-stu-id="0de27-210">0x80041320</span></span>
</dt> <dt>



<span data-ttu-id="0de27-211">A tarefa não será executada porque o usuário não está conectado.</span><span class="sxs-lookup"><span data-stu-id="0de27-211">The task will not run because the user is not logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**\_hash de tarefa sched E \_ inválido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0de27-212"><span id="SCHED_E_INVALID_TASK_HASH"></span><span id="sched_e_invalid_task_hash"></span>**SCHED\_E\_INVALID\_TASK\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-213">0x80041321</span><span class="sxs-lookup"><span data-stu-id="0de27-213">0x80041321</span></span>
</dt> <dt>



<span data-ttu-id="0de27-214">A imagem da tarefa está corrompida ou foi violada.</span><span class="sxs-lookup"><span data-stu-id="0de27-214">The task image is corrupt or has been tampered with.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**o \_ serviço sched E \_ \_ não \_ está disponível**</span><span class="sxs-lookup"><span data-stu-id="0de27-215"><span id="SCHED_E_SERVICE_NOT_AVAILABLE"></span><span id="sched_e_service_not_available"></span>**SCHED\_E\_SERVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-216">0x80041322</span><span class="sxs-lookup"><span data-stu-id="0de27-216">0x80041322</span></span>
</dt> <dt>



<span data-ttu-id="0de27-217">O serviço de Agendador de Tarefas não está disponível.</span><span class="sxs-lookup"><span data-stu-id="0de27-217">The Task Scheduler service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**o \_ serviço sched E está \_ \_ muito \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="0de27-218"><span id="SCHED_E_SERVICE_TOO_BUSY"></span><span id="sched_e_service_too_busy"></span>**SCHED\_E\_SERVICE\_TOO\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-219">0x80041323</span><span class="sxs-lookup"><span data-stu-id="0de27-219">0x80041323</span></span>
</dt> <dt>



<span data-ttu-id="0de27-220">O serviço de Agendador de Tarefas está muito ocupado para lidar com sua solicitação.</span><span class="sxs-lookup"><span data-stu-id="0de27-220">The Task Scheduler service is too busy to handle your request.</span></span> <span data-ttu-id="0de27-221">Tente novamente mais tarde.</span><span class="sxs-lookup"><span data-stu-id="0de27-221">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**\_tarefa sched \_ E \_ tentada**</span><span class="sxs-lookup"><span data-stu-id="0de27-222"><span id="SCHED_E_TASK_ATTEMPTED"></span><span id="sched_e_task_attempted"></span>**SCHED\_E\_TASK\_ATTEMPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-223">0x80041324</span><span class="sxs-lookup"><span data-stu-id="0de27-223">0x80041324</span></span>
</dt> <dt>



<span data-ttu-id="0de27-224">O serviço de Agendador de Tarefas tentou executar a tarefa, mas a tarefa não foi executada devido a uma das restrições na definição da tarefa.</span><span class="sxs-lookup"><span data-stu-id="0de27-224">The Task Scheduler service attempted to run the task, but the task did not run due to one of the constraints in the task definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**tarefa de SCHED \_ S \_ \_ enfileirada**</span><span class="sxs-lookup"><span data-stu-id="0de27-225"><span id="SCHED_S_TASK_QUEUED"></span><span id="sched_s_task_queued"></span>**SCHED\_S\_TASK\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-226">0x00041325</span><span class="sxs-lookup"><span data-stu-id="0de27-226">0x00041325</span></span>
</dt> <dt>



<span data-ttu-id="0de27-227">O serviço Agendador de Tarefas fez com que a tarefa fosse executada.</span><span class="sxs-lookup"><span data-stu-id="0de27-227">The Task Scheduler service has asked the task to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**\_tarefa sched \_ E \_ desabilitada**</span><span class="sxs-lookup"><span data-stu-id="0de27-228"><span id="SCHED_E_TASK_DISABLED"></span><span id="sched_e_task_disabled"></span>**SCHED\_E\_TASK\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-229">0x80041326</span><span class="sxs-lookup"><span data-stu-id="0de27-229">0x80041326</span></span>
</dt> <dt>



<span data-ttu-id="0de27-230">A tarefa está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="0de27-230">The task is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**\_Tarefa sched \_ E \_ não \_ v1 \_ compatível**</span><span class="sxs-lookup"><span data-stu-id="0de27-231"><span id="SCHED_E_TASK_NOT_V1_COMPAT"></span><span id="sched_e_task_not_v1_compat"></span>**SCHED\_E\_TASK\_NOT\_V1\_COMPAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-232">0x80041327</span><span class="sxs-lookup"><span data-stu-id="0de27-232">0x80041327</span></span>
</dt> <dt>



<span data-ttu-id="0de27-233">A tarefa tem propriedades que não são compatíveis com as versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="0de27-233">The task has properties that are not compatible with earlier versions of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0de27-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**\_ \_ Iniciar \_ na demanda do sched E \_**</span><span class="sxs-lookup"><span data-stu-id="0de27-234"><span id="SCHED_E_START_ON_DEMAND"></span><span id="sched_e_start_on_demand"></span>**SCHED\_E\_START\_ON\_DEMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0de27-235">0x80041328</span><span class="sxs-lookup"><span data-stu-id="0de27-235">0x80041328</span></span>
</dt> <dt>



<span data-ttu-id="0de27-236">As configurações de tarefa não permitem que a tarefa seja iniciada sob demanda.</span><span class="sxs-lookup"><span data-stu-id="0de27-236">The task settings do not allow the task to start on demand.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0de27-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0de27-237">Requirements</span></span>



| <span data-ttu-id="0de27-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="0de27-238">Requirement</span></span> | <span data-ttu-id="0de27-239">Valor</span><span class="sxs-lookup"><span data-stu-id="0de27-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0de27-240">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0de27-240">Minimum supported client</span></span><br/> | <span data-ttu-id="0de27-241">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0de27-241">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0de27-242">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0de27-242">Minimum supported server</span></span><br/> | <span data-ttu-id="0de27-243">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0de27-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0de27-244">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0de27-244">Header</span></span><br/>                   | <dl> <span data-ttu-id="0de27-245"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="0de27-245"><dt>WinError.h</dt></span></span> </dl> |



 

 





