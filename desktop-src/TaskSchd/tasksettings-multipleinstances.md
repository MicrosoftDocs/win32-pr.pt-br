---
title: Propriedade TaskSettings. MultipleInstances
description: Para scripts, Obtém ou define a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa.
ms.assetid: a25be615-fbb9-47fe-805a-5b93eab95f47
keywords:
- Agendador de Tarefas da propriedade MultipleInstances
- Propriedade MultipleInstances Agendador de Tarefas, objeto TaskSettings
- Objeto TaskSettings Agendador de Tarefas, Propriedade MultipleInstances
topic_type:
- apiref
api_name:
- TaskSettings.MultipleInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794ea07f1c01dabe957181bd327f8787f873917b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499271"
---
# <a name="tasksettingsmultipleinstances-property"></a><span data-ttu-id="025e7-106">Propriedade TaskSettings. MultipleInstances</span><span class="sxs-lookup"><span data-stu-id="025e7-106">TaskSettings.MultipleInstances property</span></span>

<span data-ttu-id="025e7-107">Para scripts, Obtém ou define a política que define como o Agendador de Tarefas lida com várias instâncias da tarefa.</span><span class="sxs-lookup"><span data-stu-id="025e7-107">For scripting, gets or sets the policy that defines how the Task Scheduler deals with multiple instances of the task.</span></span>

<span data-ttu-id="025e7-108">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="025e7-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="025e7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="025e7-109">Syntax</span></span>


```VB
TaskSettings.MultipleInstances As Integer
```



## <a name="property-value"></a><span data-ttu-id="025e7-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="025e7-110">Property value</span></span>

<span data-ttu-id="025e7-111">[**Tarefa \_ do Constantes de \_ política de instâncias**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) .</span><span class="sxs-lookup"><span data-stu-id="025e7-111">[**TASK\_INSTANCES\_POLICY**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy) constants.</span></span>



| <span data-ttu-id="025e7-112">Valor</span><span class="sxs-lookup"><span data-stu-id="025e7-112">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="025e7-113">Significado</span><span class="sxs-lookup"><span data-stu-id="025e7-113">Meaning</span></span>                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="TASK_INSTANCES_PARALLEL"></span><span id="task_instances_parallel"></span><dl> <span data-ttu-id="025e7-114"><dt>**Tarefa \_ do INSTÂNCIAS \_ paralelas**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="025e7-114"><dt>**TASK\_INSTANCES\_PARALLEL**</dt> <dt>0</dt></span></span> </dl>                 | <span data-ttu-id="025e7-115">Inicia uma nova instância enquanto uma instância existente da tarefa está em execução.</span><span class="sxs-lookup"><span data-stu-id="025e7-115">Starts a new instance while an existing instance of the task is running.</span></span><br/>              |
| <span id="TASK_INSTANCES_QUEUE"></span><span id="task_instances_queue"></span><dl> <span data-ttu-id="025e7-116"><dt>**Tarefa \_ do INSTÂNCIAS da \_ fila**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="025e7-116"><dt>**TASK\_INSTANCES\_QUEUE**</dt> <dt>1</dt></span></span> </dl>                          | <span data-ttu-id="025e7-117">Inicia uma nova instância da tarefa depois que todas as outras instâncias da tarefa são concluídas.</span><span class="sxs-lookup"><span data-stu-id="025e7-117">Starts a new instance of the task after all other instances of the task are complete.</span></span><br/> |
| <span id="TASK_INSTANCES_IGNORE_NEW"></span><span id="task_instances_ignore_new"></span><dl> <span data-ttu-id="025e7-118"><dt>**Tarefa \_ do INSTÂNCIAS \_ ignoram \_ novas**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="025e7-118"><dt>**TASK\_INSTANCES\_IGNORE\_NEW**</dt> <dt>2</dt></span></span> </dl>          | <span data-ttu-id="025e7-119">Não iniciará uma nova instância se uma instância existente da tarefa estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="025e7-119">Does not start a new instance if an existing instance of the task is running.</span></span><br/>         |
| <span id="TASK_INSTANCES_STOP_EXISTING"></span><span id="task_instances_stop_existing"></span><dl> <span data-ttu-id="025e7-120"><dt>**Tarefa \_ do As \_ instâncias \_ param**</dt> <dt>3</dt> existentes</span><span class="sxs-lookup"><span data-stu-id="025e7-120"><dt>**TASK\_INSTANCES\_STOP\_EXISTING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="025e7-121">Interrompe uma instância existente da tarefa antes de iniciar nova instância.</span><span class="sxs-lookup"><span data-stu-id="025e7-121">Stops an existing instance of the task before it starts new instance.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="025e7-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="025e7-122">Remarks</span></span>

<span data-ttu-id="025e7-123">Ao ler ou gravar XML para uma tarefa, essa configuração é especificada no elemento [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) do esquema de Agendador de tarefas.</span><span class="sxs-lookup"><span data-stu-id="025e7-123">When reading or writing XML for a task, this setting is specified in the [**MultipleInstancesPolicy**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="025e7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="025e7-124">Requirements</span></span>



| <span data-ttu-id="025e7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="025e7-125">Requirement</span></span> | <span data-ttu-id="025e7-126">Valor</span><span class="sxs-lookup"><span data-stu-id="025e7-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="025e7-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="025e7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="025e7-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="025e7-128">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="025e7-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="025e7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="025e7-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="025e7-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="025e7-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="025e7-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="025e7-132"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="025e7-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="025e7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="025e7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="025e7-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="025e7-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="025e7-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="025e7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="025e7-136">**\_política de instâncias de tarefas \_**</span><span class="sxs-lookup"><span data-stu-id="025e7-136">**TASK\_INSTANCES\_POLICY**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)
</dt> <dt>

[<span data-ttu-id="025e7-137">Agendador de Tarefas</span><span class="sxs-lookup"><span data-stu-id="025e7-137">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





