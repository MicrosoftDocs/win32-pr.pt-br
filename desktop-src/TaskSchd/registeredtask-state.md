---
title: Propriedade RegisteredTask. State
description: Para scripts, obtém o estado operacional da tarefa registrada.
ms.assetid: 1acd4946-322f-4f24-b317-92be80e19de5
keywords:
- Agendador de Tarefas de propriedade de estado
- Agendador de Tarefas de propriedade de estado, objeto RegisteredTask
- Agendador de Tarefas de objeto RegisteredTask, propriedade State
topic_type:
- apiref
api_name:
- RegisteredTask.State
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47af082174bc6927a16760e87566f311ec9f4a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455877"
---
# <a name="registeredtaskstate-property"></a><span data-ttu-id="f1c3e-106">Propriedade RegisteredTask. State</span><span class="sxs-lookup"><span data-stu-id="f1c3e-106">RegisteredTask.State property</span></span>

<span data-ttu-id="f1c3e-107">Para scripts, obtém o estado operacional da tarefa registrada.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-107">For scripting, gets the operational state of the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1c3e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1c3e-108">Syntax</span></span>


```VB
RegisteredTask.State As Integer
```



## <a name="property-value"></a><span data-ttu-id="f1c3e-109">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="f1c3e-109">Property value</span></span>

<span data-ttu-id="f1c3e-110">Uma constante de [**\_ estado de tarefa**](/windows/desktop/api/taskschd/ne-taskschd-task_state) que define o estado operacional da tarefa.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-110">A [**TASK\_STATE**](/windows/desktop/api/taskschd/ne-taskschd-task_state) constant that defines the operational state of the task.</span></span>



| <span data-ttu-id="f1c3e-111">Valor</span><span class="sxs-lookup"><span data-stu-id="f1c3e-111">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="f1c3e-112">Significado</span><span class="sxs-lookup"><span data-stu-id="f1c3e-112">Meaning</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_STATE_UNKNOWN"></span><span id="task_state_unknown"></span><dl> <span data-ttu-id="f1c3e-113"><dt>**Tarefa \_ do ESTADO \_ desconhecido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f1c3e-113"><dt>**TASK\_STATE\_UNKNOWN**</dt> <dt>0</dt></span></span> </dl>    | <span data-ttu-id="f1c3e-114">O estado da tarefa é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-114">The state of the task is unknown.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_DISABLED"></span><span id="task_state_disabled"></span><dl> <span data-ttu-id="f1c3e-115"><dt>**Tarefa \_ do ESTADO \_ desabilitado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f1c3e-115"><dt>**TASK\_STATE\_DISABLED**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="f1c3e-116">A tarefa está registrada, mas está desabilitada e nenhuma instância da tarefa está em fila ou em execução.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-116">The task is registered but is disabled and no instances of the task are queued or running.</span></span> <span data-ttu-id="f1c3e-117">A tarefa não pode ser executada até que esteja habilitada.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-117">The task cannot be run until it is enabled.</span></span><br/> |
| <span id="TASK_STATE_QUEUED"></span><span id="task_state_queued"></span><dl> <span data-ttu-id="f1c3e-118"><dt>**Tarefa \_ do ESTADO \_ na fila**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f1c3e-118"><dt>**TASK\_STATE\_QUEUED**</dt> <dt>2</dt></span></span> </dl>       | <span data-ttu-id="f1c3e-119">As instâncias da tarefa são enfileiradas.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-119">Instances of the task are queued.</span></span><br/>                                                                                                      |
| <span id="TASK_STATE_READY"></span><span id="task_state_ready"></span><dl> <span data-ttu-id="f1c3e-120"><dt>**Tarefa \_ do ESTADO \_ pronto**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f1c3e-120"><dt>**TASK\_STATE\_READY**</dt> <dt>3</dt></span></span> </dl>          | <span data-ttu-id="f1c3e-121">A tarefa está pronta para ser executada, mas nenhuma instância está enfileirada ou em execução.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-121">The task is ready to be executed, but no instances are queued or running.</span></span><br/>                                                              |
| <span id="TASK_STATE_RUNNING"></span><span id="task_state_running"></span><dl> <span data-ttu-id="f1c3e-122"><dt>**Tarefa \_ do ESTADO \_ em execução**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="f1c3e-122"><dt>**TASK\_STATE\_RUNNING**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="f1c3e-123">Uma ou mais instâncias da tarefa estão em execução.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-123">One or more instances of the task are running.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="f1c3e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1c3e-124">Requirements</span></span>



| <span data-ttu-id="f1c3e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1c3e-125">Requirement</span></span> | <span data-ttu-id="f1c3e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f1c3e-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c3e-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1c3e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f1c3e-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f1c3e-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f1c3e-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1c3e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f1c3e-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f1c3e-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f1c3e-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f1c3e-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="f1c3e-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f1c3e-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f1c3e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f1c3e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1c3e-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1c3e-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1c3e-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1c3e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c3e-136">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="f1c3e-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="f1c3e-137">**RegisteredTask**</span><span class="sxs-lookup"><span data-stu-id="f1c3e-137">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





